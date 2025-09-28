# Results vs. 3.12.6

- fork: python
- ref: 48d0d0dd9733eae4935f
- machine: darwin-arm64
- commit hash: 48d0d0d
- commit date: 2025-09-26
- overall geometric mean: 1.107x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 116 ms: 1.02x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                  |
| html5lib       | 23.0 ms                                                  | 24.0 ms: 1.04x slower                                                   |
| sphinx         | 434 ms                                                   | 404 ms: 1.07x faster                                                    |
| Geometric mean | (ref)                                                    | 1.00x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 251 ms: 1.98x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 250 ms: 1.92x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 251 ms: 1.83x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 251 ms: 1.78x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 104 ms: 1.65x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 112 ms: 1.59x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 147 ms: 1.57x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.49x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 261 ms: 1.30x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 264 ms: 1.27x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                    |
| async_generators                 | 206 ms                                                   | 182 ms: 1.13x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 41.9 ms: 1.09x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 191 ms: 1.00x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 248 ms: 1.16x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.0 ms: 2.71x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.25x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 31.0 ms: 1.22x faster                                                   |
| pidigits       | 161 ms                                                   | 160 ms: 1.01x faster                                                    |
| nbody          | 54.2 ms                                                  | 56.4 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.47 ms: 1.14x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 48.3 ms: 1.13x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 95.1 ms: 1.05x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.68 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 42.7 ms: 1.21x faster                                                   |
| tomli_loads          | 957 ms                                                   | 813 ms: 1.18x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 34.3 ms: 1.13x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.78 ms: 1.13x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 23.7 ms: 1.13x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 60.8 ms: 1.12x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 92.9 us: 1.11x faster                                                   |
| pickle_pure_python   | 139 us                                                   | 141 us: 1.01x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.1 us: 1.02x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.10x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.71 ms: 1.09x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.23 ms: 1.09x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.09x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.38 ms: 1.09x faster                                                   |
| genshi_text     | 10.5 ms                                                  | 9.90 ms: 1.06x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 21.9 ms: 1.01x slower                                                   |
| django_template | 13.6 ms                                                  | 15.4 ms: 1.13x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.00x faster                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.09 sec                                                 | 544 ms: 2.01x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 251 ms: 1.98x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 250 ms: 1.92x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 251 ms: 1.83x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 251 ms: 1.78x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 104 ms: 1.65x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 112 ms: 1.59x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 147 ms: 1.57x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.49x faster                                                    |
| deepcopy                         | 161 us                                                   | 110 us: 1.47x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.8 us: 1.42x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.34 us: 1.34x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 261 ms: 1.30x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.13 us: 1.29x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 264 ms: 1.27x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 43.9 ms: 1.24x faster                                                   |
| raytrace                         | 145 ms                                                   | 118 ms: 1.23x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 41.4 ns: 1.23x faster                                                   |
| float                            | 37.9 ms                                                  | 31.0 ms: 1.22x faster                                                   |
| go                               | 70.0 ms                                                  | 57.4 ms: 1.22x faster                                                   |
| generators                       | 21.9 ms                                                  | 18.0 ms: 1.22x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 50.5 ms: 1.21x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 42.7 ms: 1.21x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.4 ms: 1.19x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.0 ms: 1.18x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 813 ms: 1.18x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 122 ms: 1.16x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 17.9 ms: 1.16x faster                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 288 ms: 1.14x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 585 ms: 1.14x faster                                                    |
| pylint                           | 128 ms                                                   | 113 ms: 1.14x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.47 ms: 1.14x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 34.3 ms: 1.13x faster                                                   |
| async_generators                 | 206 ms                                                   | 182 ms: 1.13x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 48.3 ms: 1.13x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.98 sec: 1.13x faster                                                  |
| pyflate                          | 216 ms                                                   | 191 ms: 1.13x faster                                                    |
| k_core                           | 1.12 sec                                                 | 990 ms: 1.13x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.53 ms: 1.13x faster                                                   |
| json_dumps                       | 4.26 ms                                                  | 3.78 ms: 1.13x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 23.7 ms: 1.13x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 60.8 ms: 1.12x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 63.6 us: 1.12x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.32 us: 1.11x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 92.9 us: 1.11x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.55 us: 1.10x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 39.7 ms: 1.10x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.5 ms: 1.09x faster                                                   |
| mako                             | 4.77 ms                                                  | 4.38 ms: 1.09x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 41.9 ms: 1.09x faster                                                   |
| chaos                            | 28.9 ms                                                  | 26.6 ms: 1.09x faster                                                   |
| sphinx                           | 434 ms                                                   | 404 ms: 1.07x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.52 ms: 1.07x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 48.4 ms: 1.06x faster                                                   |
| genshi_text                      | 10.5 ms                                                  | 9.90 ms: 1.06x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 24.0 ms: 1.06x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.87 ms: 1.06x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 95.1 ms: 1.05x faster                                                   |
| richards                         | 22.4 ms                                                  | 21.4 ms: 1.05x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 927 ns: 1.04x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 55.5 ms: 1.04x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.03x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 37.6 ms: 1.03x faster                                                   |
| sympy_str                        | 104 ms                                                   | 101 ms: 1.03x faster                                                    |
| fannkuch                         | 176 ms                                                   | 171 ms: 1.03x faster                                                    |
| thrift                           | 322 us                                                   | 313 us: 1.03x faster                                                    |
| json                             | 1.93 ms                                                  | 1.91 ms: 1.01x faster                                                   |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                    |
| pidigits                         | 161 ms                                                   | 160 ms: 1.01x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 191 ms: 1.00x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 21.9 ms: 1.01x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 423 us: 1.01x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.68 ms: 1.01x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 141 us: 1.01x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.11 ms: 1.02x slower                                                   |
| 2to3                             | 114 ms                                                   | 116 ms: 1.02x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.05 ms: 1.02x slower                                                   |
| pycparser                        | 497 ms                                                   | 507 ms: 1.02x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.1 us: 1.02x slower                                                   |
| telco                            | 2.61 ms                                                  | 2.68 ms: 1.03x slower                                                   |
| docutils                         | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                  |
| sympy_expand                     | 167 ms                                                   | 172 ms: 1.03x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 49.5 ms: 1.04x slower                                                   |
| nbody                            | 54.2 ms                                                  | 56.4 ms: 1.04x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 24.0 ms: 1.04x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 42.3 ms: 1.07x slower                                                   |
| shortest_path                    | 219 ms                                                   | 235 ms: 1.07x slower                                                    |
| connected_components             | 201 ms                                                   | 218 ms: 1.09x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.71 ms: 1.09x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.23 ms: 1.09x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 914 us: 1.10x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.4 ms: 1.13x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 248 ms: 1.16x slower                                                    |
| coverage                         | 26.9 ms                                                  | 33.2 ms: 1.24x slower                                                   |
| many_optionals                   | 195 us                                                   | 330 us: 1.69x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.0 ms: 2.71x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.11x faster                                                            |
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250926-3.15.0a0-48d0d0d-JIT/bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.107x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.17x