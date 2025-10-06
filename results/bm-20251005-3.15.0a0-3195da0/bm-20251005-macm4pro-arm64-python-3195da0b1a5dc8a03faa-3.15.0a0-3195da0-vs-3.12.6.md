# Results vs. 3.12.6

- fork: python
- ref: 3195da0b1a5dc8a03faa
- machine: darwin-arm64
- commit hash: 3195da0
- commit date: 2025-10-05
- overall geometric mean: 1.088x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251005-macm4pro-arm64-python-3195da0b1a5dc8a03faa-3.15.0a0-3195da0 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| docutils       | 1.02 sec                                                 | 1.06 sec: 1.03x slower                                                  |
| html5lib       | 23.0 ms                                                  | 24.7 ms: 1.07x slower                                                   |
| sphinx         | 434 ms                                                   | 414 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                    | 1.01x slower                                                            |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251005-macm4pro-arm64-python-3195da0b1a5dc8a03faa-3.15.0a0-3195da0 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 254 ms: 1.96x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 256 ms: 1.87x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 256 ms: 1.79x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 257 ms: 1.74x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 107 ms: 1.61x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.56x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 150 ms: 1.54x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 151 ms: 1.48x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.97 ms: 1.36x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 264 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 267 ms: 1.25x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.19x faster                                                    |
| async_generators                 | 206 ms                                                   | 175 ms: 1.18x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 41.6 ms: 1.09x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 250 ms: 1.17x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 88.7 ms: 2.76x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.24x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251005-macm4pro-arm64-python-3195da0b1a5dc8a03faa-3.15.0a0-3195da0 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 31.6 ms: 1.20x faster                                                   |
| nbody          | 54.2 ms                                                  | 49.0 ms: 1.11x faster                                                   |
| pidigits       | 161 ms                                                   | 167 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251005-macm4pro-arm64-python-3195da0b1a5dc8a03faa-3.15.0a0-3195da0 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 49.8 ms: 1.10x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 98.5 ms: 1.01x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 10.0 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                    | 1.05x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251005-macm4pro-arm64-python-3195da0b1a5dc8a03faa-3.15.0a0-3195da0 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 45.1 ms: 1.14x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.93 ms: 1.08x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 63.2 ms: 1.07x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 36.2 ms: 1.07x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 25.8 ms: 1.04x faster                                                   |
| tomli_loads          | 957 ms                                                   | 926 ms: 1.03x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 102 us: 1.00x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 147 us: 1.06x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.04x faster                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251005-macm4pro-arm64-python-3195da0b1a5dc8a03faa-3.15.0a0-3195da0 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.73 ms: 1.09x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.24 ms: 1.09x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.09x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251005-macm4pro-arm64-python-3195da0b1a5dc8a03faa-3.15.0a0-3195da0 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 10.3 ms: 1.02x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 22.4 ms: 1.03x slower                                                   |
| mako            | 4.77 ms                                                  | 5.02 ms: 1.05x slower                                                   |
| django_template | 13.6 ms                                                  | 15.5 ms: 1.13x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.05x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251005-macm4pro-arm64-python-3195da0b1a5dc8a03faa-3.15.0a0-3195da0 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.09 sec                                                 | 550 ms: 1.99x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 254 ms: 1.96x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 256 ms: 1.87x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 256 ms: 1.79x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 257 ms: 1.74x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 107 ms: 1.61x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.56x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 150 ms: 1.54x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.3 us: 1.49x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 151 ms: 1.48x faster                                                    |
| deepcopy                         | 161 us                                                   | 111 us: 1.46x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.97 ms: 1.36x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.62 us: 1.29x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 264 ms: 1.28x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.17 us: 1.25x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 267 ms: 1.25x faster                                                    |
| generators                       | 21.9 ms                                                  | 17.9 ms: 1.23x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 41.9 ns: 1.22x faster                                                   |
| go                               | 70.0 ms                                                  | 57.7 ms: 1.21x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 45.3 ms: 1.20x faster                                                   |
| float                            | 37.9 ms                                                  | 31.6 ms: 1.20x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.19x faster                                                    |
| raytrace                         | 145 ms                                                   | 122 ms: 1.19x faster                                                    |
| async_generators                 | 206 ms                                                   | 175 ms: 1.18x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 52.2 ms: 1.17x faster                                                   |
| k_core                           | 1.12 sec                                                 | 960 ms: 1.16x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.6 ms: 1.16x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.4 ms: 1.16x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 45.1 ms: 1.14x faster                                                   |
| subparsers                       | 20.8 ms                                                  | 18.2 ms: 1.14x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 63.3 us: 1.12x faster                                                   |
| pylint                           | 128 ms                                                   | 115 ms: 1.12x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.00 sec: 1.12x faster                                                  |
| nqueens                          | 43.5 ms                                                  | 39.0 ms: 1.12x faster                                                   |
| nbody                            | 54.2 ms                                                  | 49.0 ms: 1.11x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.57 ms: 1.10x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.89 ms: 1.10x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 49.8 ms: 1.10x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 41.6 ms: 1.09x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 130 ms: 1.09x faster                                                    |
| pyflate                          | 216 ms                                                   | 199 ms: 1.09x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.93 ms: 1.08x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.59 us: 1.08x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.39 us: 1.08x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 63.2 ms: 1.07x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 36.2 ms: 1.07x faster                                                   |
| chaos                            | 28.9 ms                                                  | 27.0 ms: 1.07x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.51 ms: 1.07x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 30.4 ms: 1.06x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.87 ms: 1.06x faster                                                   |
| sphinx                           | 434 ms                                                   | 414 ms: 1.05x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 37.5 ms: 1.04x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 25.8 ms: 1.04x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 926 ms: 1.03x faster                                                    |
| sympy_str                        | 104 ms                                                   | 101 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| richards                         | 22.4 ms                                                  | 21.8 ms: 1.03x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 24.8 ms: 1.03x faster                                                   |
| genshi_text                      | 10.5 ms                                                  | 10.3 ms: 1.02x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 56.6 ms: 1.02x faster                                                   |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 98.5 ms: 1.01x faster                                                   |
| thrift                           | 322 us                                                   | 319 us: 1.01x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 102 us: 1.00x faster                                                    |
| shortest_path                    | 219 ms                                                   | 218 ms: 1.00x faster                                                    |
| connected_components             | 201 ms                                                   | 202 ms: 1.00x slower                                                    |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 670 ms: 1.01x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 332 ms: 1.01x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 22.4 ms: 1.03x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 171 ms: 1.03x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.07 ms: 1.03x slower                                                   |
| docutils                         | 1.02 sec                                                 | 1.06 sec: 1.03x slower                                                  |
| meteor_contest                   | 47.7 ms                                                  | 49.5 ms: 1.04x slower                                                   |
| pidigits                         | 161 ms                                                   | 167 ms: 1.04x slower                                                    |
| fannkuch                         | 176 ms                                                   | 183 ms: 1.04x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 10.0 ms: 1.05x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.02 ms: 1.05x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 147 us: 1.06x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 42.1 ms: 1.06x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 24.7 ms: 1.07x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 8.73 ms: 1.09x slower                                                   |
| telco                            | 2.61 ms                                                  | 2.85 ms: 1.09x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.24 ms: 1.09x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 933 us: 1.12x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.5 ms: 1.13x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 250 ms: 1.17x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.7 ms: 1.22x slower                                                   |
| many_optionals                   | 195 us                                                   | 331 us: 1.69x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 88.7 ms: 2.76x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.09x faster                                                            |

Benchmark hidden because not significant (7): sqlite_synth, json, 2to3, json_loads, bench_thread_pool, pycparser, scimark_lu
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251005-3.15.0a0-3195da0/bm-20251005-macm4pro-arm64-python-3195da0b1a5dc8a03faa-3.15.0a0-3195da0.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.088x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.14x