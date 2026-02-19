# Results vs. 3.12.6

- fork: python
- ref: 0bbdb4e897ae909af39c
- machine: darwin-arm64
- commit hash: 0bbdb4e
- commit date: 2026-02-18
- overall geometric mean: 1.128x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260218-macm4pro-arm64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 118 ms: 1.03x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                   |
| html5lib       | 23.0 ms                                                  | 22.7 ms: 1.01x faster                                                    |
| sphinx         | 434 ms                                                   | 402 ms: 1.08x faster                                                     |
| Geometric mean | (ref)                                                    | 1.01x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260218-macm4pro-arm64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 227 ms: 2.19x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 232 ms: 2.07x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 224 ms: 1.99x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 235 ms: 1.96x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.75x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 99.0 ms: 1.74x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 136 ms: 1.70x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 144 ms: 1.54x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 254 ms: 1.33x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 262 ms: 1.27x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 106 ms: 1.24x faster                                                     |
| async_generators                 | 206 ms                                                   | 181 ms: 1.14x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 41.9 ms: 1.09x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 121 ms: 1.07x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 239 ms: 1.12x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 82.2 ms: 2.56x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.30x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260218-macm4pro-arm64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.7 ms: 1.32x faster                                                    |
| nbody          | 54.2 ms                                                  | 47.4 ms: 1.14x faster                                                    |
| pidigits       | 161 ms                                                   | 166 ms: 1.03x slower                                                     |
| Geometric mean | (ref)                                                    | 1.14x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260218-macm4pro-arm64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 47.4 ms: 1.15x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.48 ms: 1.13x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 96.7 ms: 1.03x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.68 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260218-macm4pro-arm64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|---------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse | 51.6 ms                                                  | 41.5 ms: 1.24x faster                                                    |
| json_dumps          | 4.26 ms                                                  | 3.86 ms: 1.10x faster                                                    |
| tomli_loads         | 957 ms                                                   | 872 ms: 1.10x faster                                                     |
| xml_etree_generate  | 38.9 ms                                                  | 35.9 ms: 1.08x faster                                                    |
| xml_etree_parse     | 67.9 ms                                                  | 64.5 ms: 1.05x faster                                                    |
| xml_etree_process   | 26.7 ms                                                  | 25.6 ms: 1.04x faster                                                    |
| pickle_pure_python  | 139 us                                                   | 146 us: 1.05x slower                                                     |
| Geometric mean      | (ref)                                                    | 1.06x faster                                                             |

Benchmark hidden because not significant (2): unpickle_pure_python, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260218-macm4pro-arm64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.96 ms: 1.12x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.46 ms: 1.13x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.12x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260218-macm4pro-arm64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 10.2 ms: 1.03x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 21.9 ms: 1.01x slower                                                    |
| mako            | 4.77 ms                                                  | 4.83 ms: 1.01x slower                                                    |
| django_template | 13.6 ms                                                  | 15.2 ms: 1.12x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.02x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260218-macm4pro-arm64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.16 ms: 5.00x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 227 ms: 2.19x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 232 ms: 2.07x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 224 ms: 1.99x faster                                                     |
| mdp                              | 1.09 sec                                                 | 558 ms: 1.96x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 235 ms: 1.96x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.75x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 99.0 ms: 1.74x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 136 ms: 1.70x faster                                                     |
| deepcopy                         | 161 us                                                   | 101 us: 1.59x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 11.8 us: 1.55x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 144 ms: 1.54x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 254 ms: 1.33x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.11 us: 1.32x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.46 us: 1.32x faster                                                    |
| float                            | 37.9 ms                                                  | 28.7 ms: 1.32x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 262 ms: 1.27x faster                                                     |
| go                               | 70.0 ms                                                  | 55.9 ms: 1.25x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 41.5 ms: 1.24x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 106 ms: 1.24x faster                                                     |
| k_core                           | 1.12 sec                                                 | 910 ms: 1.23x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 119 ms: 1.19x faster                                                     |
| raytrace                         | 145 ms                                                   | 122 ms: 1.19x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 42.9 ns: 1.19x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 51.5 ms: 1.19x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 46.1 ms: 1.18x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 47.4 ms: 1.15x faster                                                    |
| nbody                            | 54.2 ms                                                  | 47.4 ms: 1.14x faster                                                    |
| async_generators                 | 206 ms                                                   | 181 ms: 1.14x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.48 ms: 1.13x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.0 ms: 1.12x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.51 us: 1.12x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 19.1 ms: 1.12x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.55 ms: 1.11x faster                                                    |
| pyflate                          | 216 ms                                                   | 194 ms: 1.11x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.32 us: 1.11x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.1 ms: 1.11x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.88 ms: 1.11x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.86 ms: 1.10x faster                                                    |
| chaos                            | 28.9 ms                                                  | 26.3 ms: 1.10x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.03 sec: 1.10x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 39.5 ms: 1.10x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 872 ms: 1.10x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 41.9 ms: 1.09x faster                                                    |
| pylint                           | 128 ms                                                   | 118 ms: 1.09x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 35.9 ms: 1.08x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 23.5 ms: 1.08x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 47.5 ms: 1.08x faster                                                    |
| sphinx                           | 434 ms                                                   | 402 ms: 1.08x faster                                                     |
| richards                         | 22.4 ms                                                  | 20.8 ms: 1.08x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 66.1 us: 1.07x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 64.5 ms: 1.05x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.91 ms: 1.05x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 25.6 ms: 1.04x faster                                                    |
| pycparser                        | 497 ms                                                   | 479 ms: 1.04x faster                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 7.72 ms: 1.04x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 10.2 ms: 1.03x faster                                                    |
| generators                       | 21.9 ms                                                  | 21.3 ms: 1.03x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 96.7 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 320 ms: 1.02x faster                                                     |
| pprint_pformat                   | 665 ms                                                   | 651 ms: 1.02x faster                                                     |
| thrift                           | 322 us                                                   | 317 us: 1.02x faster                                                     |
| fannkuch                         | 176 ms                                                   | 173 ms: 1.02x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 22.7 ms: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 521 ms: 1.01x faster                                                     |
| json                             | 1.93 ms                                                  | 1.91 ms: 1.01x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| sympy_str                        | 104 ms                                                   | 104 ms: 1.01x faster                                                     |
| sympy_sum                        | 57.6 ms                                                  | 57.3 ms: 1.01x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 21.9 ms: 1.01x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.68 ms: 1.01x slower                                                    |
| mako                             | 4.77 ms                                                  | 4.83 ms: 1.01x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 39.7 ms: 1.02x slower                                                    |
| pidigits                         | 161 ms                                                   | 166 ms: 1.03x slower                                                     |
| gc_traversal                     | 2.01 ms                                                  | 2.08 ms: 1.03x slower                                                    |
| 2to3                             | 114 ms                                                   | 118 ms: 1.03x slower                                                     |
| shortest_path                    | 219 ms                                                   | 227 ms: 1.04x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 436 us: 1.04x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 175 ms: 1.05x slower                                                     |
| connected_components             | 201 ms                                                   | 210 ms: 1.05x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 146 us: 1.05x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 50.8 ms: 1.06x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 121 ms: 1.07x slower                                                     |
| telco                            | 2.61 ms                                                  | 2.89 ms: 1.11x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.2 ms: 1.12x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.96 ms: 1.12x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 929 us: 1.12x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 239 ms: 1.12x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 6.46 ms: 1.13x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 46.1 ms: 1.16x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.3 ms: 1.20x slower                                                    |
| many_optionals                   | 195 us                                                   | 261 us: 1.33x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 82.2 ms: 2.56x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.12x faster                                                             |

Benchmark hidden because not significant (3): sqlite_synth, unpickle_pure_python, json_loads
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260218-3.15.0a6+-0bbdb4e/bm-20260218-macm4pro-arm64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.128x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.23x