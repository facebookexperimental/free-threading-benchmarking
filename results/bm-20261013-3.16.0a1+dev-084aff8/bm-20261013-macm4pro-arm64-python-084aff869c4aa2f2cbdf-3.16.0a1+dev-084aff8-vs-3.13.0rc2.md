# Results vs. 3.13.0rc2

- fork: python
- ref: 084aff869c4aa2f2cbdf
- machine: darwin-arm64
- commit hash: 084aff8
- commit date: 2026-10-13
- overall geometric mean: 1.094x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261013-macm4pro-arm64-python-084aff869c4aa2f2cbdf-3.16.0a1+dev-084aff8 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 116 ms: 1.04x slower                                                        |
| docutils       | 1.05 sec                                                       | 915 ms: 1.14x faster                                                        |
| html5lib       | 23.1 ms                                                        | 20.7 ms: 1.12x faster                                                       |
| sphinx         | 409 ms                                                         | 391 ms: 1.05x faster                                                        |
| Geometric mean | (ref)                                                          | 1.07x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261013-macm4pro-arm64-python-084aff869c4aa2f2cbdf-3.16.0a1+dev-084aff8 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 265 ms: 1.98x faster                                                        |
| async_tree_eager_io_tg           | 521 ms                                                         | 277 ms: 1.88x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 282 ms: 1.44x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 273 ms: 1.41x faster                                                        |
| async_generators                 | 193 ms                                                         | 143 ms: 1.35x faster                                                        |
| async_tree_none                  | 142 ms                                                         | 112 ms: 1.27x faster                                                        |
| async_tree_none_tg               | 133 ms                                                         | 112 ms: 1.18x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 158 ms: 1.18x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 162 ms: 1.14x faster                                                        |
| coroutines                       | 10.8 ms                                                        | 9.68 ms: 1.11x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 274 ms: 1.10x faster                                                        |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 269 ms: 1.09x faster                                                        |
| async_tree_eager_memoization     | 122 ms                                                         | 113 ms: 1.08x faster                                                        |
| async_tree_eager                 | 43.2 ms                                                        | 40.8 ms: 1.06x faster                                                       |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                        |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 252 ms: 1.21x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 142 ms: 1.38x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 94.4 ms: 3.26x slower                                                       |
| Geometric mean                   | (ref)                                                          | 1.10x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261013-macm4pro-arm64-python-084aff869c4aa2f2cbdf-3.16.0a1+dev-084aff8 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.4 ms: 1.15x faster                                                       |
| pidigits       | 166 ms                                                         | 165 ms: 1.01x faster                                                        |
| nbody          | 42.5 ms                                                        | 42.8 ms: 1.01x slower                                                       |
| Geometric mean | (ref)                                                          | 1.05x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261013-macm4pro-arm64-python-084aff869c4aa2f2cbdf-3.16.0a1+dev-084aff8 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.31 ms: 1.23x faster                                                       |
| regex_v8       | 10.7 ms                                                        | 9.09 ms: 1.18x faster                                                       |
| regex_dna      | 94.6 ms                                                        | 89.8 ms: 1.05x faster                                                       |
| regex_compile  | 47.9 ms                                                        | 54.7 ms: 1.14x slower                                                       |
| Geometric mean | (ref)                                                          | 1.08x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261013-macm4pro-arm64-python-084aff869c4aa2f2cbdf-3.16.0a1+dev-084aff8 |
|----------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.57 ms: 1.30x faster                                                       |
| tomli_loads          | 1000 ms                                                        | 836 ms: 1.20x faster                                                        |
| xml_etree_iterparse  | 46.1 ms                                                        | 42.2 ms: 1.09x faster                                                       |
| unpickle_pure_python | 99.5 us                                                        | 92.0 us: 1.08x faster                                                       |
| json_loads           | 10.8 us                                                        | 10.4 us: 1.04x faster                                                       |
| xml_etree_process    | 25.4 ms                                                        | 24.9 ms: 1.02x faster                                                       |
| xml_etree_generate   | 35.8 ms                                                        | 35.3 ms: 1.02x faster                                                       |
| xml_etree_parse      | 62.4 ms                                                        | 65.9 ms: 1.06x slower                                                       |
| pickle_pure_python   | 130 us                                                         | 139 us: 1.06x slower                                                        |
| Geometric mean       | (ref)                                                          | 1.07x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261013-macm4pro-arm64-python-084aff869c4aa2f2cbdf-3.16.0a1+dev-084aff8 |
|------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.88 ms: 1.03x slower                                                       |
| python_startup_no_site | 5.95 ms                                                        | 6.48 ms: 1.09x slower                                                       |
| Geometric mean         | (ref)                                                          | 1.06x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261013-macm4pro-arm64-python-084aff869c4aa2f2cbdf-3.16.0a1+dev-084aff8 |
|-----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.46 ms: 1.01x slower                                                       |
| django_template | 12.5 ms                                                        | 15.0 ms: 1.20x slower                                                       |
| Geometric mean  | (ref)                                                          | 1.10x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261013-macm4pro-arm64-python-084aff869c4aa2f2cbdf-3.16.0a1+dev-084aff8 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mdp                              | 1.06 sec                                                       | 504 ms: 2.10x faster                                                        |
| pylint                           | 106 ms                                                         | 52.5 ms: 2.01x faster                                                       |
| async_tree_eager_io              | 525 ms                                                         | 265 ms: 1.98x faster                                                        |
| async_tree_eager_io_tg           | 521 ms                                                         | 277 ms: 1.88x faster                                                        |
| create_gc_cycles                 | 993 us                                                         | 635 us: 1.56x faster                                                        |
| subparsers                       | 6.26 ms                                                        | 4.02 ms: 1.56x faster                                                       |
| deepcopy                         | 145 us                                                         | 96.2 us: 1.51x faster                                                       |
| k_core                           | 1.46 sec                                                       | 971 ms: 1.51x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 282 ms: 1.44x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 273 ms: 1.41x faster                                                        |
| deepcopy_memo                    | 16.5 us                                                        | 11.8 us: 1.40x faster                                                       |
| go                               | 72.6 ms                                                        | 52.2 ms: 1.39x faster                                                       |
| async_generators                 | 193 ms                                                         | 143 ms: 1.35x faster                                                        |
| typing_runtime_protocols         | 64.6 us                                                        | 48.7 us: 1.33x faster                                                       |
| json_dumps                       | 4.65 ms                                                        | 3.57 ms: 1.30x faster                                                       |
| scimark_sor                      | 64.0 ms                                                        | 49.5 ms: 1.29x faster                                                       |
| async_tree_none                  | 142 ms                                                         | 112 ms: 1.27x faster                                                        |
| regex_effbot                     | 1.61 ms                                                        | 1.31 ms: 1.23x faster                                                       |
| deepcopy_reduce                  | 1.30 us                                                        | 1.05 us: 1.23x faster                                                       |
| pyflate                          | 222 ms                                                         | 183 ms: 1.22x faster                                                        |
| tomli_loads                      | 1000 ms                                                        | 836 ms: 1.20x faster                                                        |
| async_tree_none_tg               | 133 ms                                                         | 112 ms: 1.18x faster                                                        |
| regex_v8                         | 10.7 ms                                                        | 9.09 ms: 1.18x faster                                                       |
| async_tree_memoization_tg        | 186 ms                                                         | 158 ms: 1.18x faster                                                        |
| gc_traversal                     | 2.04 ms                                                        | 1.78 ms: 1.15x faster                                                       |
| float                            | 31.4 ms                                                        | 27.4 ms: 1.15x faster                                                       |
| docutils                         | 1.05 sec                                                       | 915 ms: 1.14x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 162 ms: 1.14x faster                                                        |
| fannkuch                         | 179 ms                                                         | 160 ms: 1.12x faster                                                        |
| html5lib                         | 23.1 ms                                                        | 20.7 ms: 1.12x faster                                                       |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.91 sec: 1.12x faster                                                      |
| scimark_monte_carlo              | 29.9 ms                                                        | 26.9 ms: 1.11x faster                                                       |
| coroutines                       | 10.8 ms                                                        | 9.68 ms: 1.11x faster                                                       |
| scimark_fft                      | 124 ms                                                         | 112 ms: 1.11x faster                                                        |
| dulwich_log                      | 19.8 ms                                                        | 17.9 ms: 1.11x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 274 ms: 1.10x faster                                                        |
| richards                         | 22.1 ms                                                        | 20.2 ms: 1.09x faster                                                       |
| xml_etree_iterparse              | 46.1 ms                                                        | 42.2 ms: 1.09x faster                                                       |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 269 ms: 1.09x faster                                                        |
| async_tree_eager_memoization     | 122 ms                                                         | 113 ms: 1.08x faster                                                        |
| unpickle_pure_python             | 99.5 us                                                        | 92.0 us: 1.08x faster                                                       |
| hexiom                           | 2.85 ms                                                        | 2.64 ms: 1.08x faster                                                       |
| richards_super                   | 24.7 ms                                                        | 23.0 ms: 1.07x faster                                                       |
| nqueens                          | 37.2 ms                                                        | 34.9 ms: 1.07x faster                                                       |
| spectral_norm                    | 43.7 ms                                                        | 41.1 ms: 1.06x faster                                                       |
| telco                            | 3.07 ms                                                        | 2.89 ms: 1.06x faster                                                       |
| async_tree_eager                 | 43.2 ms                                                        | 40.8 ms: 1.06x faster                                                       |
| pathlib                          | 11.1 ms                                                        | 10.6 ms: 1.05x faster                                                       |
| regex_dna                        | 94.6 ms                                                        | 89.8 ms: 1.05x faster                                                       |
| logging_simple                   | 2.24 us                                                        | 2.14 us: 1.05x faster                                                       |
| sphinx                           | 409 ms                                                         | 391 ms: 1.05x faster                                                        |
| logging_format                   | 2.45 us                                                        | 2.34 us: 1.04x faster                                                       |
| json                             | 1.94 ms                                                        | 1.86 ms: 1.04x faster                                                       |
| json_loads                       | 10.8 us                                                        | 10.4 us: 1.04x faster                                                       |
| sqlite_synth                     | 948 ns                                                         | 920 ns: 1.03x faster                                                        |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.73 ms: 1.03x faster                                                       |
| pprint_safe_repr                 | 322 ms                                                         | 313 ms: 1.03x faster                                                        |
| deltablue                        | 1.45 ms                                                        | 1.42 ms: 1.02x faster                                                       |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                        |
| comprehensions                   | 6.80 us                                                        | 6.67 us: 1.02x faster                                                       |
| sympy_integrate                  | 7.53 ms                                                        | 7.38 ms: 1.02x faster                                                       |
| xml_etree_process                | 25.4 ms                                                        | 24.9 ms: 1.02x faster                                                       |
| pprint_pformat                   | 650 ms                                                         | 638 ms: 1.02x faster                                                        |
| xml_etree_generate               | 35.8 ms                                                        | 35.3 ms: 1.02x faster                                                       |
| thrift                           | 309 us                                                         | 305 us: 1.01x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                        |
| bench_thread_pool                | 412 us                                                         | 407 us: 1.01x faster                                                        |
| pidigits                         | 166 ms                                                         | 165 ms: 1.01x faster                                                        |
| shortest_path                    | 225 ms                                                         | 223 ms: 1.01x faster                                                        |
| connected_components             | 208 ms                                                         | 207 ms: 1.01x faster                                                        |
| nbody                            | 42.5 ms                                                        | 42.8 ms: 1.01x slower                                                       |
| mako                             | 4.41 ms                                                        | 4.46 ms: 1.01x slower                                                       |
| chaos                            | 24.3 ms                                                        | 24.8 ms: 1.02x slower                                                       |
| meteor_contest                   | 47.9 ms                                                        | 49.0 ms: 1.02x slower                                                       |
| python_startup                   | 8.63 ms                                                        | 8.88 ms: 1.03x slower                                                       |
| 2to3                             | 112 ms                                                         | 116 ms: 1.04x slower                                                        |
| sympy_str                        | 95.5 ms                                                        | 99.2 ms: 1.04x slower                                                       |
| logging_silent                   | 40.6 ns                                                        | 42.3 ns: 1.04x slower                                                       |
| raytrace                         | 109 ms                                                         | 113 ms: 1.04x slower                                                        |
| sympy_sum                        | 52.3 ms                                                        | 55.1 ms: 1.05x slower                                                       |
| sympy_expand                     | 159 ms                                                         | 168 ms: 1.05x slower                                                        |
| xml_etree_parse                  | 62.4 ms                                                        | 65.9 ms: 1.06x slower                                                       |
| pickle_pure_python               | 130 us                                                         | 139 us: 1.06x slower                                                        |
| scimark_lu                       | 42.8 ms                                                        | 45.7 ms: 1.07x slower                                                       |
| python_startup_no_site           | 5.95 ms                                                        | 6.48 ms: 1.09x slower                                                       |
| generators                       | 15.7 ms                                                        | 17.1 ms: 1.09x slower                                                       |
| crypto_pyaes                     | 33.6 ms                                                        | 37.0 ms: 1.10x slower                                                       |
| regex_compile                    | 47.9 ms                                                        | 54.7 ms: 1.14x slower                                                       |
| many_optionals                   | 200 us                                                         | 231 us: 1.15x slower                                                        |
| bench_mp_pool                    | 37.8 ms                                                        | 44.0 ms: 1.16x slower                                                       |
| django_template                  | 12.5 ms                                                        | 15.0 ms: 1.20x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 252 ms: 1.21x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 142 ms: 1.38x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 94.4 ms: 3.26x slower                                                       |
| Geometric mean                   | (ref)                                                          | 1.09x faster                                                                |

Benchmark hidden because not significant (1): pycparser
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261013-3.16.0a1+dev-084aff8/bm-20261013-macm4pro-arm64-python-084aff869c4aa2f2cbdf-3.16.0a1+dev-084aff8.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.094x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.13x