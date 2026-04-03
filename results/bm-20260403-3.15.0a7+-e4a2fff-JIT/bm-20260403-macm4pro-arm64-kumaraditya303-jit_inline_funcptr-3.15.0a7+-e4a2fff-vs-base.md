# Results vs. base

- fork: kumaraditya303
- ref: jit_inline_funcptr
- machine: darwin-arm64
- commit hash: e4a2fff
- commit date: 2026-04-03
- overall geometric mean: 1.005x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20260403-macm4pro-arm64-python-3908593039bde9d4b591-3.15.0a7+-3908593 | bm-20260403-macm4pro-arm64-kumaraditya303-jit_inline_funcptr-3.15.0a7+-e4a2fff |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                                   | 111 ms: 1.03x faster                                                           |
| docutils       | 993 ms                                                                   | 971 ms: 1.02x faster                                                           |
| html5lib       | 19.5 ms                                                                  | 19.3 ms: 1.01x faster                                                          |
| Geometric mean | (ref)                                                                    | 1.02x faster                                                                   |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                     | bm-20260403-macm4pro-arm64-python-3908593039bde9d4b591-3.15.0a7+-3908593 | bm-20260403-macm4pro-arm64-kumaraditya303-jit_inline_funcptr-3.15.0a7+-e4a2fff |
|-------------------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_generators              | 183 ms                                                                   | 178 ms: 1.03x faster                                                           |
| async_tree_eager_io           | 213 ms                                                                   | 207 ms: 1.03x faster                                                           |
| async_tree_eager_tg           | 79.0 ms                                                                  | 77.7 ms: 1.02x faster                                                          |
| async_tree_cpu_io_mixed_tg    | 246 ms                                                                   | 242 ms: 1.02x faster                                                           |
| async_tree_none               | 91.2 ms                                                                  | 89.9 ms: 1.02x faster                                                          |
| async_tree_cpu_io_mixed       | 245 ms                                                                   | 241 ms: 1.02x faster                                                           |
| asyncio_websockets            | 189 ms                                                                   | 186 ms: 1.01x faster                                                           |
| async_tree_eager_cpu_io_mixed | 219 ms                                                                   | 216 ms: 1.01x faster                                                           |
| async_tree_eager              | 36.7 ms                                                                  | 36.6 ms: 1.00x faster                                                          |
| async_tree_eager_memoization  | 103 ms                                                                   | 104 ms: 1.01x slower                                                           |
| Geometric mean                | (ref)                                                                    | 1.01x faster                                                                   |

Benchmark hidden because not significant (9): async_tree_io_tg, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_memoization_tg, async_tree_eager_io_tg, async_tree_none_tg, coroutines, async_tree_memoization_tg, async_tree_memoization, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20260403-macm4pro-arm64-python-3908593039bde9d4b591-3.15.0a7+-3908593 | bm-20260403-macm4pro-arm64-kumaraditya303-jit_inline_funcptr-3.15.0a7+-e4a2fff |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| float          | 23.5 ms                                                                  | 23.3 ms: 1.01x faster                                                          |
| pidigits       | 165 ms                                                                   | 164 ms: 1.01x faster                                                           |
| nbody          | 33.8 ms                                                                  | 34.0 ms: 1.01x slower                                                          |
| Geometric mean | (ref)                                                                    | 1.00x faster                                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20260403-macm4pro-arm64-python-3908593039bde9d4b591-3.15.0a7+-3908593 | bm-20260403-macm4pro-arm64-kumaraditya303-jit_inline_funcptr-3.15.0a7+-e4a2fff |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_v8       | 9.71 ms                                                                  | 9.62 ms: 1.01x faster                                                          |
| Geometric mean | (ref)                                                                    | 1.00x faster                                                                   |

Benchmark hidden because not significant (3): regex_effbot, regex_compile, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20260403-macm4pro-arm64-python-3908593039bde9d4b591-3.15.0a7+-3908593 | bm-20260403-macm4pro-arm64-kumaraditya303-jit_inline_funcptr-3.15.0a7+-e4a2fff |
|----------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| pickle_pure_python   | 125 us                                                                   | 125 us: 1.00x faster                                                           |
| xml_etree_generate   | 31.8 ms                                                                  | 31.8 ms: 1.00x faster                                                          |
| unpickle_pure_python | 84.3 us                                                                  | 84.5 us: 1.00x slower                                                          |
| tomli_loads          | 628 ms                                                                   | 633 ms: 1.01x slower                                                           |
| json_dumps           | 3.47 ms                                                                  | 3.52 ms: 1.01x slower                                                          |
| xml_etree_iterparse  | 38.4 ms                                                                  | 39.0 ms: 1.02x slower                                                          |
| xml_etree_parse      | 63.6 ms                                                                  | 64.6 ms: 1.02x slower                                                          |
| Geometric mean       | (ref)                                                                    | 1.01x slower                                                                   |

Benchmark hidden because not significant (2): xml_etree_process, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20260403-macm4pro-arm64-python-3908593039bde9d4b591-3.15.0a7+-3908593 | bm-20260403-macm4pro-arm64-kumaraditya303-jit_inline_funcptr-3.15.0a7+-e4a2fff |
|------------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| python_startup         | 8.91 ms                                                                  | 8.86 ms: 1.01x faster                                                          |
| python_startup_no_site | 6.39 ms                                                                  | 6.37 ms: 1.00x faster                                                          |
| Geometric mean         | (ref)                                                                    | 1.00x faster                                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20260403-macm4pro-arm64-python-3908593039bde9d4b591-3.15.0a7+-3908593 | bm-20260403-macm4pro-arm64-kumaraditya303-jit_inline_funcptr-3.15.0a7+-e4a2fff |
|-----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| mako            | 4.17 ms                                                                  | 4.10 ms: 1.02x faster                                                          |
| genshi_xml      | 20.5 ms                                                                  | 20.3 ms: 1.01x faster                                                          |
| django_template | 12.5 ms                                                                  | 12.4 ms: 1.01x faster                                                          |
| genshi_text     | 8.82 ms                                                                  | 8.93 ms: 1.01x slower                                                          |
| Geometric mean  | (ref)                                                                    | 1.01x faster                                                                   |

All benchmarks:
===============

| Benchmark                     | bm-20260403-macm4pro-arm64-python-3908593039bde9d4b591-3.15.0a7+-3908593 | bm-20260403-macm4pro-arm64-kumaraditya303-jit_inline_funcptr-3.15.0a7+-e4a2fff |
|-------------------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| gc_traversal                  | 2.51 ms                                                                  | 2.38 ms: 1.05x faster                                                          |
| many_optionals                | 233 us                                                                   | 225 us: 1.04x faster                                                           |
| async_generators              | 183 ms                                                                   | 178 ms: 1.03x faster                                                           |
| 2to3                          | 114 ms                                                                   | 111 ms: 1.03x faster                                                           |
| async_tree_eager_io           | 213 ms                                                                   | 207 ms: 1.03x faster                                                           |
| dulwich_log                   | 18.3 ms                                                                  | 17.8 ms: 1.03x faster                                                          |
| create_gc_cycles              | 968 us                                                                   | 943 us: 1.03x faster                                                           |
| bench_mp_pool                 | 46.0 ms                                                                  | 44.9 ms: 1.02x faster                                                          |
| logging_simple                | 1.78 us                                                                  | 1.74 us: 1.02x faster                                                          |
| docutils                      | 993 ms                                                                   | 971 ms: 1.02x faster                                                           |
| logging_format                | 1.94 us                                                                  | 1.90 us: 1.02x faster                                                          |
| deepcopy                      | 96.2 us                                                                  | 94.5 us: 1.02x faster                                                          |
| json                          | 1.85 ms                                                                  | 1.82 ms: 1.02x faster                                                          |
| async_tree_eager_tg           | 79.0 ms                                                                  | 77.7 ms: 1.02x faster                                                          |
| async_tree_cpu_io_mixed_tg    | 246 ms                                                                   | 242 ms: 1.02x faster                                                           |
| mako                          | 4.17 ms                                                                  | 4.10 ms: 1.02x faster                                                          |
| subparsers                    | 3.59 ms                                                                  | 3.54 ms: 1.02x faster                                                          |
| async_tree_none               | 91.2 ms                                                                  | 89.9 ms: 1.02x faster                                                          |
| async_tree_cpu_io_mixed       | 245 ms                                                                   | 241 ms: 1.02x faster                                                           |
| asyncio_websockets            | 189 ms                                                                   | 186 ms: 1.01x faster                                                           |
| html5lib                      | 19.5 ms                                                                  | 19.3 ms: 1.01x faster                                                          |
| async_tree_eager_cpu_io_mixed | 219 ms                                                                   | 216 ms: 1.01x faster                                                           |
| scimark_sor                   | 35.1 ms                                                                  | 34.7 ms: 1.01x faster                                                          |
| genshi_xml                    | 20.5 ms                                                                  | 20.3 ms: 1.01x faster                                                          |
| go                            | 47.2 ms                                                                  | 46.7 ms: 1.01x faster                                                          |
| meteor_contest                | 46.0 ms                                                                  | 45.5 ms: 1.01x faster                                                          |
| django_template               | 12.5 ms                                                                  | 12.4 ms: 1.01x faster                                                          |
| regex_v8                      | 9.71 ms                                                                  | 9.62 ms: 1.01x faster                                                          |
| float                         | 23.5 ms                                                                  | 23.3 ms: 1.01x faster                                                          |
| fannkuch                      | 152 ms                                                                   | 151 ms: 1.01x faster                                                           |
| raytrace                      | 110 ms                                                                   | 109 ms: 1.01x faster                                                           |
| sqlglot_v2_normalize          | 43.1 ms                                                                  | 42.8 ms: 1.01x faster                                                          |
| thrift                        | 303 us                                                                   | 300 us: 1.01x faster                                                           |
| deepcopy_memo                 | 11.0 us                                                                  | 10.9 us: 1.01x faster                                                          |
| pathlib                       | 10.7 ms                                                                  | 10.6 ms: 1.01x faster                                                          |
| pidigits                      | 165 ms                                                                   | 164 ms: 1.01x faster                                                           |
| python_startup                | 8.91 ms                                                                  | 8.86 ms: 1.01x faster                                                          |
| pickle_pure_python            | 125 us                                                                   | 125 us: 1.00x faster                                                           |
| deltablue                     | 1.11 ms                                                                  | 1.11 ms: 1.00x faster                                                          |
| comprehensions                | 5.89 us                                                                  | 5.87 us: 1.00x faster                                                          |
| crypto_pyaes                  | 31.7 ms                                                                  | 31.6 ms: 1.00x faster                                                          |
| hexiom                        | 2.42 ms                                                                  | 2.41 ms: 1.00x faster                                                          |
| python_startup_no_site        | 6.39 ms                                                                  | 6.37 ms: 1.00x faster                                                          |
| k_core                        | 861 ms                                                                   | 859 ms: 1.00x faster                                                           |
| async_tree_eager              | 36.7 ms                                                                  | 36.6 ms: 1.00x faster                                                          |
| xml_etree_generate            | 31.8 ms                                                                  | 31.8 ms: 1.00x faster                                                          |
| unpickle_pure_python          | 84.3 us                                                                  | 84.5 us: 1.00x slower                                                          |
| connected_components          | 196 ms                                                                   | 196 ms: 1.00x slower                                                           |
| scimark_fft                   | 94.2 ms                                                                  | 94.4 ms: 1.00x slower                                                          |
| nqueens                       | 31.8 ms                                                                  | 31.9 ms: 1.00x slower                                                          |
| sympy_str                     | 98.2 ms                                                                  | 98.5 ms: 1.00x slower                                                          |
| sympy_expand                  | 163 ms                                                                   | 164 ms: 1.00x slower                                                           |
| richards                      | 9.69 ms                                                                  | 9.74 ms: 1.01x slower                                                          |
| nbody                         | 33.8 ms                                                                  | 34.0 ms: 1.01x slower                                                          |
| pyflate                       | 147 ms                                                                   | 148 ms: 1.01x slower                                                           |
| bench_thread_pool             | 427 us                                                                   | 430 us: 1.01x slower                                                           |
| scimark_monte_carlo           | 22.7 ms                                                                  | 22.9 ms: 1.01x slower                                                          |
| tomli_loads                   | 628 ms                                                                   | 633 ms: 1.01x slower                                                           |
| async_tree_eager_memoization  | 103 ms                                                                   | 104 ms: 1.01x slower                                                           |
| scimark_lu                    | 27.6 ms                                                                  | 27.8 ms: 1.01x slower                                                          |
| genshi_text                   | 8.82 ms                                                                  | 8.93 ms: 1.01x slower                                                          |
| json_dumps                    | 3.47 ms                                                                  | 3.52 ms: 1.01x slower                                                          |
| xml_etree_iterparse           | 38.4 ms                                                                  | 39.0 ms: 1.02x slower                                                          |
| xml_etree_parse               | 63.6 ms                                                                  | 64.6 ms: 1.02x slower                                                          |
| spectral_norm                 | 35.7 ms                                                                  | 36.5 ms: 1.02x slower                                                          |
| logging_silent                | 32.8 ns                                                                  | 33.6 ns: 1.02x slower                                                          |
| Geometric mean                | (ref)                                                                    | 1.01x faster                                                                   |

Benchmark hidden because not significant (37): async_tree_io_tg, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_memoization_tg, async_tree_eager_io_tg, async_tree_none_tg, coroutines, pycparser, async_tree_memoization_tg, sympy_sum, async_tree_memoization, deepcopy_reduce, generators, pprint_safe_repr, async_tree_io, sphinx, regex_effbot, typing_runtime_protocols, richards_super, sqlglot_v2_parse, coverage, pprint_pformat, pylint, chaos, regex_compile, xml_etree_process, sqlglot_v2_transpile, dask, shortest_path, regex_dna, mdp, scimark_sparse_mat_mult, sympy_integrate, sqlite_synth, bpe_tokeniser, json_loads, telco, sqlglot_v2_optimize

- Geometric mean (including insignificant results): 1.005x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.99x