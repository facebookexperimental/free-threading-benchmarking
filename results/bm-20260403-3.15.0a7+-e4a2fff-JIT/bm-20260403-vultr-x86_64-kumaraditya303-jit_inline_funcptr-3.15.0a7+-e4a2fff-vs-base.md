# Results vs. base

- fork: kumaraditya303
- ref: jit_inline_funcptr
- machine: linux-x86_64
- commit hash: e4a2fff
- commit date: 2026-04-03
- overall geometric mean: 1.004x slower
- HPT reliability: 98.47%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20260403-vultr-x86_64-python-3908593039bde9d4b591-3.15.0a7+-3908593 | bm-20260403-vultr-x86_64-kumaraditya303-jit_inline_funcptr-3.15.0a7+-e4a2fff |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| docutils       | 2.63 sec                                                               | 2.65 sec: 1.01x slower                                                       |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                                 |

Benchmark hidden because not significant (3): 2to3, html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20260403-vultr-x86_64-python-3908593039bde9d4b591-3.15.0a7+-3908593 | bm-20260403-vultr-x86_64-kumaraditya303-jit_inline_funcptr-3.15.0a7+-e4a2fff |
|---------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_generators          | 355 ms                                                                 | 349 ms: 1.02x faster                                                         |
| async_tree_memoization_tg | 290 ms                                                                 | 295 ms: 1.02x slower                                                         |
| async_tree_none_tg        | 232 ms                                                                 | 236 ms: 1.02x slower                                                         |
| async_tree_memoization    | 280 ms                                                                 | 288 ms: 1.03x slower                                                         |
| Geometric mean            | (ref)                                                                  | 1.01x slower                                                                 |

Benchmark hidden because not significant (7): async_tree_cpu_io_mixed_tg, coroutines, asyncio_websockets, async_tree_cpu_io_mixed, async_tree_io, async_tree_none, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20260403-vultr-x86_64-python-3908593039bde9d4b591-3.15.0a7+-3908593 | bm-20260403-vultr-x86_64-kumaraditya303-jit_inline_funcptr-3.15.0a7+-e4a2fff |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| nbody          | 65.6 ms                                                                | 64.0 ms: 1.03x faster                                                        |
| pidigits       | 191 ms                                                                 | 187 ms: 1.02x faster                                                         |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                                 |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20260403-vultr-x86_64-python-3908593039bde9d4b591-3.15.0a7+-3908593 | bm-20260403-vultr-x86_64-kumaraditya303-jit_inline_funcptr-3.15.0a7+-e4a2fff |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 128 ms                                                                 | 126 ms: 1.01x faster                                                         |
| regex_v8       | 21.4 ms                                                                | 22.2 ms: 1.03x slower                                                        |
| regex_dna      | 165 ms                                                                 | 171 ms: 1.03x slower                                                         |
| regex_effbot   | 2.60 ms                                                                | 2.72 ms: 1.04x slower                                                        |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20260403-vultr-x86_64-python-3908593039bde9d4b591-3.15.0a7+-3908593 | bm-20260403-vultr-x86_64-kumaraditya303-jit_inline_funcptr-3.15.0a7+-e4a2fff |
|---------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_dumps          | 8.96 ms                                                                | 8.73 ms: 1.03x faster                                                        |
| json_loads          | 27.0 us                                                                | 26.9 us: 1.00x faster                                                        |
| xml_etree_iterparse | 82.6 ms                                                                | 83.0 ms: 1.00x slower                                                        |
| pickle_pure_python  | 314 us                                                                 | 319 us: 1.02x slower                                                         |
| Geometric mean      | (ref)                                                                  | 1.00x faster                                                                 |

Benchmark hidden because not significant (5): unpickle_pure_python, tomli_loads, xml_etree_process, xml_etree_parse, xml_etree_generate

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup_no_site, python_startup

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20260403-vultr-x86_64-python-3908593039bde9d4b591-3.15.0a7+-3908593 | bm-20260403-vultr-x86_64-kumaraditya303-jit_inline_funcptr-3.15.0a7+-e4a2fff |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako           | 10.8 ms                                                                | 10.9 ms: 1.01x slower                                                        |
| genshi_xml     | 49.8 ms                                                                | 51.6 ms: 1.04x slower                                                        |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                                 |

Benchmark hidden because not significant (2): genshi_text, django_template

All benchmarks:
===============

| Benchmark                 | bm-20260403-vultr-x86_64-python-3908593039bde9d4b591-3.15.0a7+-3908593 | bm-20260403-vultr-x86_64-kumaraditya303-jit_inline_funcptr-3.15.0a7+-e4a2fff |
|---------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_dumps                | 8.96 ms                                                                | 8.73 ms: 1.03x faster                                                        |
| nbody                     | 65.6 ms                                                                | 64.0 ms: 1.03x faster                                                        |
| deepcopy                  | 227 us                                                                 | 222 us: 1.02x faster                                                         |
| pidigits                  | 191 ms                                                                 | 187 ms: 1.02x faster                                                         |
| crypto_pyaes              | 65.3 ms                                                                | 64.2 ms: 1.02x faster                                                        |
| raytrace                  | 291 ms                                                                 | 286 ms: 1.02x faster                                                         |
| pyflate                   | 358 ms                                                                 | 351 ms: 1.02x faster                                                         |
| async_generators          | 355 ms                                                                 | 349 ms: 1.02x faster                                                         |
| sqlglot_v2_parse          | 1.21 ms                                                                | 1.19 ms: 1.01x faster                                                        |
| create_gc_cycles          | 1.88 ms                                                                | 1.85 ms: 1.01x faster                                                        |
| logging_silent            | 74.7 ns                                                                | 73.7 ns: 1.01x faster                                                        |
| many_optionals            | 973 us                                                                 | 963 us: 1.01x faster                                                         |
| sqlite_synth              | 2.16 us                                                                | 2.14 us: 1.01x faster                                                        |
| regex_compile             | 128 ms                                                                 | 126 ms: 1.01x faster                                                         |
| sqlglot_v2_optimize       | 51.2 ms                                                                | 50.8 ms: 1.01x faster                                                        |
| k_core                    | 1.84 sec                                                               | 1.82 sec: 1.01x faster                                                       |
| deepcopy_memo             | 22.6 us                                                                | 22.5 us: 1.01x faster                                                        |
| hexiom                    | 5.72 ms                                                                | 5.69 ms: 1.00x faster                                                        |
| json_loads                | 27.0 us                                                                | 26.9 us: 1.00x faster                                                        |
| bpe_tokeniser             | 3.88 sec                                                               | 3.87 sec: 1.00x faster                                                       |
| xml_etree_iterparse       | 82.6 ms                                                                | 83.0 ms: 1.00x slower                                                        |
| sympy_integrate           | 20.0 ms                                                                | 20.1 ms: 1.00x slower                                                        |
| mdp                       | 1.18 sec                                                               | 1.19 sec: 1.01x slower                                                       |
| sympy_str                 | 295 ms                                                                 | 296 ms: 1.01x slower                                                         |
| connected_components      | 369 ms                                                                 | 372 ms: 1.01x slower                                                         |
| go                        | 100 ms                                                                 | 101 ms: 1.01x slower                                                         |
| shortest_path             | 417 ms                                                                 | 420 ms: 1.01x slower                                                         |
| dulwich_log               | 70.2 ms                                                                | 70.8 ms: 1.01x slower                                                        |
| docutils                  | 2.63 sec                                                               | 2.65 sec: 1.01x slower                                                       |
| sympy_sum                 | 168 ms                                                                 | 169 ms: 1.01x slower                                                         |
| json                      | 4.89 ms                                                                | 4.94 ms: 1.01x slower                                                        |
| mako                      | 10.8 ms                                                                | 10.9 ms: 1.01x slower                                                        |
| scimark_fft               | 250 ms                                                                 | 253 ms: 1.01x slower                                                         |
| sqlglot_v2_transpile      | 1.50 ms                                                                | 1.52 ms: 1.01x slower                                                        |
| generators                | 28.6 ms                                                                | 29.1 ms: 1.01x slower                                                        |
| async_tree_memoization_tg | 290 ms                                                                 | 295 ms: 1.02x slower                                                         |
| spectral_norm             | 71.9 ms                                                                | 73.0 ms: 1.02x slower                                                        |
| async_tree_none_tg        | 232 ms                                                                 | 236 ms: 1.02x slower                                                         |
| scimark_lu                | 77.5 ms                                                                | 78.8 ms: 1.02x slower                                                        |
| pickle_pure_python        | 314 us                                                                 | 319 us: 1.02x slower                                                         |
| telco                     | 149 ms                                                                 | 152 ms: 1.02x slower                                                         |
| coverage                  | 81.0 ms                                                                | 82.7 ms: 1.02x slower                                                        |
| meteor_contest            | 98.5 ms                                                                | 101 ms: 1.02x slower                                                         |
| pprint_pformat            | 1.25 sec                                                               | 1.29 sec: 1.03x slower                                                       |
| async_tree_memoization    | 280 ms                                                                 | 288 ms: 1.03x slower                                                         |
| pathlib                   | 17.2 ms                                                                | 17.7 ms: 1.03x slower                                                        |
| richards                  | 17.9 ms                                                                | 18.5 ms: 1.03x slower                                                        |
| regex_v8                  | 21.4 ms                                                                | 22.2 ms: 1.03x slower                                                        |
| logging_simple            | 5.28 us                                                                | 5.46 us: 1.03x slower                                                        |
| regex_dna                 | 165 ms                                                                 | 171 ms: 1.03x slower                                                         |
| genshi_xml                | 49.8 ms                                                                | 51.6 ms: 1.04x slower                                                        |
| deepcopy_reduce           | 2.38 us                                                                | 2.48 us: 1.04x slower                                                        |
| regex_effbot              | 2.60 ms                                                                | 2.72 ms: 1.04x slower                                                        |
| gc_traversal              | 3.88 ms                                                                | 4.20 ms: 1.08x slower                                                        |
| Geometric mean            | (ref)                                                                  | 1.00x slower                                                                 |

Benchmark hidden because not significant (40): bench_mp_pool, pylint, richards_super, scimark_monte_carlo, comprehensions, bench_thread_pool, float, pprint_safe_repr, async_tree_cpu_io_mixed_tg, unpickle_pure_python, 2to3, scimark_sor, coroutines, python_startup_no_site, python_startup, nqueens, asyncio_websockets, sphinx, genshi_text, async_tree_cpu_io_mixed, async_tree_io, pycparser, tomli_loads, scimark_sparse_mat_mult, xml_etree_process, fannkuch, sympy_expand, deltablue, xml_etree_parse, sqlglot_v2_normalize, xml_etree_generate, chaos, subparsers, thrift, async_tree_none, html5lib, django_template, typing_runtime_protocols, logging_format, async_tree_io_tg

- Geometric mean (including insignificant results): 1.004x slower

# HPT report

- Reliability score: 98.47% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x