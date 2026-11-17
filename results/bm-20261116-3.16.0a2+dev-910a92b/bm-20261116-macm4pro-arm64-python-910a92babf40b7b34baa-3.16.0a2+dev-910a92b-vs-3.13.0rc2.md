# Results vs. 3.13.0rc2

- fork: python
- ref: 910a92babf40b7b34baa
- machine: darwin-arm64
- commit hash: 910a92b
- commit date: 2026-11-16
- overall geometric mean: 1.110x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261116-macm4pro-arm64-python-910a92babf40b7b34baa-3.16.0a2+dev-910a92b |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| docutils       | 1.05 sec                                                       | 897 ms: 1.17x faster                                                        |
| html5lib       | 23.1 ms                                                        | 20.7 ms: 1.12x faster                                                       |
| sphinx         | 409 ms                                                         | 388 ms: 1.05x faster                                                        |
| Geometric mean | (ref)                                                          | 1.08x faster                                                                |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261116-macm4pro-arm64-python-910a92babf40b7b34baa-3.16.0a2+dev-910a92b |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 263 ms: 2.00x faster                                                        |
| async_generators                 | 193 ms                                                         | 97.7 ms: 1.98x faster                                                       |
| async_tree_eager_io_tg           | 521 ms                                                         | 275 ms: 1.89x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 276 ms: 1.47x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 269 ms: 1.44x faster                                                        |
| async_tree_none                  | 142 ms                                                         | 110 ms: 1.29x faster                                                        |
| async_tree_none_tg               | 133 ms                                                         | 111 ms: 1.19x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 157 ms: 1.18x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 161 ms: 1.14x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 269 ms: 1.12x faster                                                        |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 264 ms: 1.11x faster                                                        |
| coroutines                       | 10.8 ms                                                        | 9.69 ms: 1.11x faster                                                       |
| async_tree_eager_memoization     | 122 ms                                                         | 113 ms: 1.08x faster                                                        |
| async_tree_eager                 | 43.2 ms                                                        | 40.3 ms: 1.07x faster                                                       |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.03x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 218 ms: 1.03x faster                                                        |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 246 ms: 1.18x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 141 ms: 1.37x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 92.6 ms: 3.20x slower                                                       |
| Geometric mean                   | (ref)                                                          | 1.13x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261116-macm4pro-arm64-python-910a92babf40b7b34baa-3.16.0a2+dev-910a92b |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.4 ms: 1.14x faster                                                       |
| pidigits       | 166 ms                                                         | 147 ms: 1.13x faster                                                        |
| nbody          | 42.5 ms                                                        | 43.5 ms: 1.02x slower                                                       |
| Geometric mean | (ref)                                                          | 1.08x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261116-macm4pro-arm64-python-910a92babf40b7b34baa-3.16.0a2+dev-910a92b |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.31 ms: 1.23x faster                                                       |
| regex_v8       | 10.7 ms                                                        | 9.21 ms: 1.16x faster                                                       |
| regex_dna      | 94.6 ms                                                        | 91.2 ms: 1.04x faster                                                       |
| regex_compile  | 47.9 ms                                                        | 53.9 ms: 1.12x slower                                                       |
| Geometric mean | (ref)                                                          | 1.07x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261116-macm4pro-arm64-python-910a92babf40b7b34baa-3.16.0a2+dev-910a92b |
|----------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.54 ms: 1.31x faster                                                       |
| tomli_loads          | 1000 ms                                                        | 823 ms: 1.21x faster                                                        |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.7 ms: 1.13x faster                                                       |
| unpickle_pure_python | 99.5 us                                                        | 91.9 us: 1.08x faster                                                       |
| xml_etree_generate   | 35.8 ms                                                        | 34.7 ms: 1.03x faster                                                       |
| json_loads           | 10.8 us                                                        | 10.5 us: 1.03x faster                                                       |
| xml_etree_process    | 25.4 ms                                                        | 24.8 ms: 1.02x faster                                                       |
| xml_etree_parse      | 62.4 ms                                                        | 63.6 ms: 1.02x slower                                                       |
| pickle_pure_python   | 130 us                                                         | 138 us: 1.06x slower                                                        |
| Geometric mean       | (ref)                                                          | 1.08x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261116-macm4pro-arm64-python-910a92babf40b7b34baa-3.16.0a2+dev-910a92b |
|------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.35 ms: 1.03x faster                                                       |
| python_startup_no_site | 5.95 ms                                                        | 6.45 ms: 1.08x slower                                                       |
| Geometric mean         | (ref)                                                          | 1.02x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261116-macm4pro-arm64-python-910a92babf40b7b34baa-3.16.0a2+dev-910a92b |
|-----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.33 ms: 1.02x faster                                                       |
| django_template | 12.5 ms                                                        | 14.6 ms: 1.17x slower                                                       |
| Geometric mean  | (ref)                                                          | 1.07x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261116-macm4pro-arm64-python-910a92babf40b7b34baa-3.16.0a2+dev-910a92b |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mdp                              | 1.06 sec                                                       | 503 ms: 2.10x faster                                                        |
| pylint                           | 106 ms                                                         | 51.4 ms: 2.05x faster                                                       |
| async_tree_eager_io              | 525 ms                                                         | 263 ms: 2.00x faster                                                        |
| async_generators                 | 193 ms                                                         | 97.7 ms: 1.98x faster                                                       |
| async_tree_eager_io_tg           | 521 ms                                                         | 275 ms: 1.89x faster                                                        |
| subparsers                       | 6.26 ms                                                        | 3.89 ms: 1.61x faster                                                       |
| create_gc_cycles                 | 993 us                                                         | 635 us: 1.56x faster                                                        |
| deepcopy                         | 145 us                                                         | 95.7 us: 1.52x faster                                                       |
| k_core                           | 1.46 sec                                                       | 977 ms: 1.50x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 276 ms: 1.47x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 269 ms: 1.44x faster                                                        |
| typing_runtime_protocols         | 64.6 us                                                        | 45.0 us: 1.44x faster                                                       |
| go                               | 72.6 ms                                                        | 52.1 ms: 1.39x faster                                                       |
| deepcopy_memo                    | 16.5 us                                                        | 11.8 us: 1.39x faster                                                       |
| json_dumps                       | 4.65 ms                                                        | 3.54 ms: 1.31x faster                                                       |
| scimark_sor                      | 64.0 ms                                                        | 49.0 ms: 1.31x faster                                                       |
| async_tree_none                  | 142 ms                                                         | 110 ms: 1.29x faster                                                        |
| deepcopy_reduce                  | 1.30 us                                                        | 1.04 us: 1.25x faster                                                       |
| regex_effbot                     | 1.61 ms                                                        | 1.31 ms: 1.23x faster                                                       |
| pyflate                          | 222 ms                                                         | 182 ms: 1.22x faster                                                        |
| tomli_loads                      | 1000 ms                                                        | 823 ms: 1.21x faster                                                        |
| async_tree_none_tg               | 133 ms                                                         | 111 ms: 1.19x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 157 ms: 1.18x faster                                                        |
| docutils                         | 1.05 sec                                                       | 897 ms: 1.17x faster                                                        |
| regex_v8                         | 10.7 ms                                                        | 9.21 ms: 1.16x faster                                                       |
| scimark_monte_carlo              | 29.9 ms                                                        | 26.1 ms: 1.15x faster                                                       |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.86 sec: 1.15x faster                                                      |
| float                            | 31.4 ms                                                        | 27.4 ms: 1.14x faster                                                       |
| gc_traversal                     | 2.04 ms                                                        | 1.78 ms: 1.14x faster                                                       |
| async_tree_memoization           | 184 ms                                                         | 161 ms: 1.14x faster                                                        |
| scimark_fft                      | 124 ms                                                         | 108 ms: 1.14x faster                                                        |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.7 ms: 1.13x faster                                                       |
| pidigits                         | 166 ms                                                         | 147 ms: 1.13x faster                                                        |
| fannkuch                         | 179 ms                                                         | 158 ms: 1.13x faster                                                        |
| dulwich_log                      | 19.8 ms                                                        | 17.7 ms: 1.12x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 269 ms: 1.12x faster                                                        |
| html5lib                         | 23.1 ms                                                        | 20.7 ms: 1.12x faster                                                       |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 264 ms: 1.11x faster                                                        |
| coroutines                       | 10.8 ms                                                        | 9.69 ms: 1.11x faster                                                       |
| richards                         | 22.1 ms                                                        | 20.1 ms: 1.10x faster                                                       |
| telco                            | 3.07 ms                                                        | 2.81 ms: 1.09x faster                                                       |
| nqueens                          | 37.2 ms                                                        | 34.4 ms: 1.08x faster                                                       |
| hexiom                           | 2.85 ms                                                        | 2.63 ms: 1.08x faster                                                       |
| unpickle_pure_python             | 99.5 us                                                        | 91.9 us: 1.08x faster                                                       |
| async_tree_eager_memoization     | 122 ms                                                         | 113 ms: 1.08x faster                                                        |
| richards_super                   | 24.7 ms                                                        | 22.9 ms: 1.08x faster                                                       |
| async_tree_eager                 | 43.2 ms                                                        | 40.3 ms: 1.07x faster                                                       |
| spectral_norm                    | 43.7 ms                                                        | 41.0 ms: 1.07x faster                                                       |
| sphinx                           | 409 ms                                                         | 388 ms: 1.05x faster                                                        |
| pathlib                          | 11.1 ms                                                        | 10.6 ms: 1.05x faster                                                       |
| json                             | 1.94 ms                                                        | 1.85 ms: 1.05x faster                                                       |
| logging_simple                   | 2.24 us                                                        | 2.15 us: 1.04x faster                                                       |
| regex_dna                        | 94.6 ms                                                        | 91.2 ms: 1.04x faster                                                       |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.72 ms: 1.03x faster                                                       |
| python_startup                   | 8.63 ms                                                        | 8.35 ms: 1.03x faster                                                       |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.03x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 218 ms: 1.03x faster                                                        |
| xml_etree_generate               | 35.8 ms                                                        | 34.7 ms: 1.03x faster                                                       |
| pprint_safe_repr                 | 322 ms                                                         | 312 ms: 1.03x faster                                                        |
| sqlite_synth                     | 948 ns                                                         | 921 ns: 1.03x faster                                                        |
| json_loads                       | 10.8 us                                                        | 10.5 us: 1.03x faster                                                       |
| thrift                           | 309 us                                                         | 300 us: 1.03x faster                                                        |
| sympy_integrate                  | 7.53 ms                                                        | 7.36 ms: 1.02x faster                                                       |
| xml_etree_process                | 25.4 ms                                                        | 24.8 ms: 1.02x faster                                                       |
| logging_format                   | 2.45 us                                                        | 2.40 us: 1.02x faster                                                       |
| pprint_pformat                   | 650 ms                                                         | 638 ms: 1.02x faster                                                        |
| mako                             | 4.41 ms                                                        | 4.33 ms: 1.02x faster                                                       |
| deltablue                        | 1.45 ms                                                        | 1.43 ms: 1.02x faster                                                       |
| comprehensions                   | 6.80 us                                                        | 6.69 us: 1.02x faster                                                       |
| connected_components             | 208 ms                                                         | 205 ms: 1.01x faster                                                        |
| bench_thread_pool                | 412 us                                                         | 407 us: 1.01x faster                                                        |
| shortest_path                    | 225 ms                                                         | 222 ms: 1.01x faster                                                        |
| meteor_contest                   | 47.9 ms                                                        | 48.6 ms: 1.01x slower                                                       |
| xml_etree_parse                  | 62.4 ms                                                        | 63.6 ms: 1.02x slower                                                       |
| nbody                            | 42.5 ms                                                        | 43.5 ms: 1.02x slower                                                       |
| raytrace                         | 109 ms                                                         | 113 ms: 1.03x slower                                                        |
| sympy_str                        | 95.5 ms                                                        | 98.7 ms: 1.03x slower                                                       |
| sympy_sum                        | 52.3 ms                                                        | 55.0 ms: 1.05x slower                                                       |
| sympy_expand                     | 159 ms                                                         | 168 ms: 1.05x slower                                                        |
| logging_silent                   | 40.6 ns                                                        | 42.8 ns: 1.05x slower                                                       |
| pickle_pure_python               | 130 us                                                         | 138 us: 1.06x slower                                                        |
| generators                       | 15.7 ms                                                        | 16.9 ms: 1.08x slower                                                       |
| scimark_lu                       | 42.8 ms                                                        | 46.2 ms: 1.08x slower                                                       |
| python_startup_no_site           | 5.95 ms                                                        | 6.45 ms: 1.08x slower                                                       |
| crypto_pyaes                     | 33.6 ms                                                        | 36.9 ms: 1.10x slower                                                       |
| bench_mp_pool                    | 37.8 ms                                                        | 41.6 ms: 1.10x slower                                                       |
| many_optionals                   | 200 us                                                         | 224 us: 1.12x slower                                                        |
| regex_compile                    | 47.9 ms                                                        | 53.9 ms: 1.12x slower                                                       |
| django_template                  | 12.5 ms                                                        | 14.6 ms: 1.17x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 246 ms: 1.18x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 141 ms: 1.37x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 92.6 ms: 3.20x slower                                                       |
| Geometric mean                   | (ref)                                                          | 1.11x faster                                                                |

Benchmark hidden because not significant (3): 2to3, pycparser, chaos
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261116-3.16.0a2+dev-910a92b/bm-20261116-macm4pro-arm64-python-910a92babf40b7b34baa-3.16.0a2+dev-910a92b.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.110x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.10x