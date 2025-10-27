# Results vs. 3.12.6

- fork: python
- ref: 3dab11f888fda34c0273
- machine: darwin-arm64
- commit hash: 3dab11f
- commit date: 2025-10-26
- overall geometric mean: 1.105x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251026-macm4pro-arm64-python-3dab11f888fda34c0273-3.15.0a1+-3dab11f |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 116 ms: 1.02x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                   |
| sphinx         | 434 ms                                                   | 405 ms: 1.07x faster                                                     |
| Geometric mean | (ref)                                                    | 1.00x faster                                                             |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251026-macm4pro-arm64-python-3dab11f888fda34c0273-3.15.0a1+-3dab11f |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 229 ms: 2.16x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 226 ms: 2.12x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 232 ms: 1.98x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 231 ms: 1.93x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 103 ms: 1.73x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 101 ms: 1.70x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 141 ms: 1.64x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 142 ms: 1.56x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 256 ms: 1.32x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.31x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 256 ms: 1.30x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                     |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 42.8 ms: 1.06x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 127 ms: 1.13x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 243 ms: 1.14x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 83.2 ms: 2.59x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.30x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251026-macm4pro-arm64-python-3dab11f888fda34c0273-3.15.0a1+-3dab11f |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.8 ms: 1.32x faster                                                    |
| nbody          | 54.2 ms                                                  | 50.0 ms: 1.09x faster                                                    |
| pidigits       | 161 ms                                                   | 164 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                    | 1.12x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251026-macm4pro-arm64-python-3dab11f888fda34c0273-3.15.0a1+-3dab11f |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 49.3 ms: 1.11x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 96.2 ms: 1.04x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.86 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251026-macm4pro-arm64-python-3dab11f888fda34c0273-3.15.0a1+-3dab11f |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.0 ms: 1.32x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 60.3 ms: 1.13x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 35.4 ms: 1.10x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 24.9 ms: 1.07x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.99 ms: 1.07x faster                                                    |
| tomli_loads          | 957 ms                                                   | 900 ms: 1.06x faster                                                     |
| unpickle_pure_python | 103 us                                                   | 101 us: 1.02x faster                                                     |
| pickle_pure_python   | 139 us                                                   | 146 us: 1.05x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.08x faster                                                             |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251026-macm4pro-arm64-python-3dab11f888fda34c0273-3.15.0a1+-3dab11f |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 5.71 ms                                                  | 6.24 ms: 1.09x slower                                                    |
| python_startup         | 8.01 ms                                                  | 8.81 ms: 1.10x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.10x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251026-macm4pro-arm64-python-3dab11f888fda34c0273-3.15.0a1+-3dab11f |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 10.00 ms: 1.05x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 21.9 ms: 1.01x slower                                                    |
| mako            | 4.77 ms                                                  | 4.88 ms: 1.02x slower                                                    |
| django_template | 13.6 ms                                                  | 15.6 ms: 1.15x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.03x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251026-macm4pro-arm64-python-3dab11f888fda34c0273-3.15.0a1+-3dab11f |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 229 ms: 2.16x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 226 ms: 2.12x faster                                                     |
| mdp                              | 1.09 sec                                                 | 541 ms: 2.02x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 232 ms: 1.98x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 231 ms: 1.93x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 103 ms: 1.73x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 101 ms: 1.70x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 141 ms: 1.64x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 142 ms: 1.56x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.2 us: 1.50x faster                                                    |
| deepcopy                         | 161 us                                                   | 111 us: 1.45x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.0 ms: 1.32x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 256 ms: 1.32x faster                                                     |
| float                            | 37.9 ms                                                  | 28.8 ms: 1.32x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.31x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.55 us: 1.30x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 256 ms: 1.30x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.16 us: 1.25x faster                                                    |
| go                               | 70.0 ms                                                  | 56.1 ms: 1.25x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 43.7 ms: 1.25x faster                                                    |
| k_core                           | 1.12 sec                                                 | 902 ms: 1.24x faster                                                     |
| raytrace                         | 145 ms                                                   | 118 ms: 1.23x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 49.6 ms: 1.23x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 42.0 ns: 1.21x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.2 ms: 1.20x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                     |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.49 ms: 1.16x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 18.2 ms: 1.14x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 125 ms: 1.14x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.13x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 60.3 ms: 1.13x faster                                                    |
| pyflate                          | 216 ms                                                   | 194 ms: 1.11x faster                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.87 ms: 1.11x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.02 sec: 1.11x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 49.3 ms: 1.11x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.2 ms: 1.10x faster                                                    |
| chaos                            | 28.9 ms                                                  | 26.3 ms: 1.10x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 35.4 ms: 1.10x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 39.7 ms: 1.10x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.35 us: 1.10x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 19.5 ms: 1.09x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.58 us: 1.09x faster                                                    |
| nbody                            | 54.2 ms                                                  | 50.0 ms: 1.09x faster                                                    |
| pylint                           | 128 ms                                                   | 118 ms: 1.09x faster                                                     |
| typing_runtime_protocols         | 71.0 us                                                  | 66.1 us: 1.07x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 24.9 ms: 1.07x faster                                                    |
| sphinx                           | 434 ms                                                   | 405 ms: 1.07x faster                                                     |
| hexiom                           | 3.04 ms                                                  | 2.84 ms: 1.07x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.99 ms: 1.07x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 42.8 ms: 1.06x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 48.2 ms: 1.06x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 900 ms: 1.06x faster                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 7.54 ms: 1.06x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 24.2 ms: 1.05x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 10.00 ms: 1.05x faster                                                   |
| richards                         | 22.4 ms                                                  | 21.5 ms: 1.04x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 96.2 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 38.0 ms: 1.02x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 101 us: 1.02x faster                                                     |
| sympy_str                        | 104 ms                                                   | 102 ms: 1.02x faster                                                     |
| thrift                           | 322 us                                                   | 317 us: 1.02x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                     |
| bench_thread_pool                | 419 us                                                   | 417 us: 1.00x faster                                                     |
| pprint_pformat                   | 665 ms                                                   | 667 ms: 1.00x slower                                                     |
| genshi_xml                       | 21.8 ms                                                  | 21.9 ms: 1.01x slower                                                    |
| sqlite_synth                     | 967 ns                                                   | 977 ns: 1.01x slower                                                     |
| shortest_path                    | 219 ms                                                   | 221 ms: 1.01x slower                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 332 ms: 1.01x slower                                                     |
| pidigits                         | 161 ms                                                   | 164 ms: 1.01x slower                                                     |
| 2to3                             | 114 ms                                                   | 116 ms: 1.02x slower                                                     |
| connected_components             | 201 ms                                                   | 205 ms: 1.02x slower                                                     |
| mako                             | 4.77 ms                                                  | 4.88 ms: 1.02x slower                                                    |
| pycparser                        | 497 ms                                                   | 509 ms: 1.02x slower                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.86 ms: 1.03x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                   |
| gc_traversal                     | 2.01 ms                                                  | 2.08 ms: 1.03x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 41.2 ms: 1.04x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 174 ms: 1.04x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 146 us: 1.05x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 50.2 ms: 1.05x slower                                                    |
| fannkuch                         | 176 ms                                                   | 185 ms: 1.05x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 6.24 ms: 1.09x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.81 ms: 1.10x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.91 ms: 1.11x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 127 ms: 1.13x slower                                                     |
| create_gc_cycles                 | 830 us                                                   | 945 us: 1.14x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 243 ms: 1.14x slower                                                     |
| django_template                  | 13.6 ms                                                  | 15.6 ms: 1.15x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.3 ms: 1.20x slower                                                    |
| many_optionals                   | 195 us                                                   | 376 us: 1.93x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 83.2 ms: 2.59x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                             |

Benchmark hidden because not significant (4): sympy_sum, json, json_loads, html5lib
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251026-3.15.0a1+-3dab11f/bm-20251026-macm4pro-arm64-python-3dab11f888fda34c0273-3.15.0a1+-3dab11f.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.105x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.19x