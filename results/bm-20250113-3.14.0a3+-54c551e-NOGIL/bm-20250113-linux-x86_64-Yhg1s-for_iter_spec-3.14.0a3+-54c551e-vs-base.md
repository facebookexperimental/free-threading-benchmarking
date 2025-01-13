# Results vs. base

- fork: Yhg1s
- ref: for_iter_spec
- machine: linux-x86_64
- commit hash: 54c551e
- commit date: 2025-01-13
- overall geometric mean: 1.012x slower
- HPT reliability: 99.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250109-linux-x86_64-python-7dc41ad6a7826ffc675f-3.14.0a3+-7dc41ad | bm-20250113-linux-x86_64-Yhg1s-for_iter_spec-3.14.0a3+-54c551e |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| docutils       | 4.55 sec                                                               | 4.96 sec: 1.09x slower                                         |
| html5lib       | 117 ms                                                                 | 130 ms: 1.11x slower                                           |
| sphinx         | 1.69 sec                                                               | 1.82 sec: 1.08x slower                                         |
| Geometric mean | (ref)                                                                  | 1.07x slower                                                   |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250109-linux-x86_64-python-7dc41ad6a7826ffc675f-3.14.0a3+-7dc41ad | bm-20250113-linux-x86_64-Yhg1s-for_iter_spec-3.14.0a3+-54c551e |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 833 ms                                                                 | 741 ms: 1.12x faster                                           |
| asyncio_websockets         | 810 ms                                                                 | 734 ms: 1.10x faster                                           |
| async_tree_none_tg         | 452 ms                                                                 | 428 ms: 1.06x faster                                           |
| async_generators           | 647 ms                                                                 | 715 ms: 1.10x slower                                           |
| async_tree_memoization     | 584 ms                                                                 | 651 ms: 1.11x slower                                           |
| async_tree_none            | 511 ms                                                                 | 610 ms: 1.19x slower                                           |
| Geometric mean             | (ref)                                                                  | 1.02x slower                                                   |

Benchmark hidden because not significant (5): coroutines, async_tree_io_tg, async_tree_cpu_io_mixed, async_tree_memoization_tg, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250109-linux-x86_64-python-7dc41ad6a7826ffc675f-3.14.0a3+-7dc41ad | bm-20250113-linux-x86_64-Yhg1s-for_iter_spec-3.14.0a3+-54c551e |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| nbody          | 186 ms                                                                 | 168 ms: 1.11x faster                                           |
| pidigits       | 249 ms                                                                 | 238 ms: 1.05x faster                                           |
| Geometric mean | (ref)                                                                  | 1.07x faster                                                   |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250109-linux-x86_64-python-7dc41ad6a7826ffc675f-3.14.0a3+-7dc41ad | bm-20250113-linux-x86_64-Yhg1s-for_iter_spec-3.14.0a3+-54c551e |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| regex_dna      | 317 ms                                                                 | 335 ms: 1.06x slower                                           |
| regex_v8       | 37.7 ms                                                                | 40.7 ms: 1.08x slower                                          |
| regex_effbot   | 4.17 ms                                                                | 4.83 ms: 1.16x slower                                          |
| Geometric mean | (ref)                                                                  | 1.08x slower                                                   |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20250109-linux-x86_64-python-7dc41ad6a7826ffc675f-3.14.0a3+-7dc41ad | bm-20250113-linux-x86_64-Yhg1s-for_iter_spec-3.14.0a3+-54c551e |
|---------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| xml_etree_iterparse | 135 ms                                                                 | 141 ms: 1.04x slower                                           |
| xml_etree_process   | 108 ms                                                                 | 116 ms: 1.07x slower                                           |
| Geometric mean      | (ref)                                                                  | 1.00x faster                                                   |

Benchmark hidden because not significant (7): pickle_pure_python, xml_etree_parse, json_loads, json_dumps, unpickle_pure_python, tomli_loads, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250109-linux-x86_64-python-7dc41ad6a7826ffc675f-3.14.0a3+-7dc41ad | bm-20250113-linux-x86_64-Yhg1s-for_iter_spec-3.14.0a3+-54c551e |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| python_startup_no_site | 23.3 ms                                                                | 22.3 ms: 1.05x faster                                          |
| python_startup         | 36.0 ms                                                                | 34.5 ms: 1.04x faster                                          |
| Geometric mean         | (ref)                                                                  | 1.05x faster                                                   |

Benchmarks with tag 'template':
===============================

Benchmark hidden because not significant (4): django_template, genshi_xml, mako, genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20250109-linux-x86_64-python-7dc41ad6a7826ffc675f-3.14.0a3+-7dc41ad | bm-20250113-linux-x86_64-Yhg1s-for_iter_spec-3.14.0a3+-54c551e |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| create_gc_cycles           | 4.77 ms                                                                | 3.73 ms: 1.28x faster                                          |
| sqlglot_optimize           | 102 ms                                                                 | 82.5 ms: 1.24x faster                                          |
| meteor_contest             | 200 ms                                                                 | 176 ms: 1.13x faster                                           |
| async_tree_cpu_io_mixed_tg | 833 ms                                                                 | 741 ms: 1.12x faster                                           |
| pathlib                    | 36.7 ms                                                                | 32.7 ms: 1.12x faster                                          |
| nbody                      | 186 ms                                                                 | 168 ms: 1.11x faster                                           |
| asyncio_websockets         | 810 ms                                                                 | 734 ms: 1.10x faster                                           |
| deepcopy_reduce            | 4.69 us                                                                | 4.27 us: 1.10x faster                                          |
| deepcopy                   | 476 us                                                                 | 439 us: 1.08x faster                                           |
| gc_traversal               | 8.36 ms                                                                | 7.83 ms: 1.07x faster                                          |
| typing_runtime_protocols   | 291 us                                                                 | 274 us: 1.06x faster                                           |
| async_tree_none_tg         | 452 ms                                                                 | 428 ms: 1.06x faster                                           |
| pidigits                   | 249 ms                                                                 | 238 ms: 1.05x faster                                           |
| python_startup_no_site     | 23.3 ms                                                                | 22.3 ms: 1.05x faster                                          |
| python_startup             | 36.0 ms                                                                | 34.5 ms: 1.04x faster                                          |
| raytrace                   | 659 ms                                                                 | 633 ms: 1.04x faster                                           |
| shortest_path              | 1.12 sec                                                               | 1.08 sec: 1.04x faster                                         |
| bpe_tokeniser              | 8.04 sec                                                               | 7.75 sec: 1.04x faster                                         |
| xml_etree_iterparse        | 135 ms                                                                 | 141 ms: 1.04x slower                                           |
| scimark_fft                | 529 ms                                                                 | 555 ms: 1.05x slower                                           |
| nqueens                    | 135 ms                                                                 | 143 ms: 1.05x slower                                           |
| comprehensions             | 34.8 us                                                                | 36.7 us: 1.05x slower                                          |
| richards                   | 85.9 ms                                                                | 90.6 ms: 1.06x slower                                          |
| regex_dna                  | 317 ms                                                                 | 335 ms: 1.06x slower                                           |
| pprint_pformat             | 2.51 sec                                                               | 2.67 sec: 1.06x slower                                         |
| richards_super             | 92.1 ms                                                                | 98.3 ms: 1.07x slower                                          |
| mdp                        | 4.37 sec                                                               | 4.67 sec: 1.07x slower                                         |
| xml_etree_process          | 108 ms                                                                 | 116 ms: 1.07x slower                                           |
| sphinx                     | 1.69 sec                                                               | 1.82 sec: 1.08x slower                                         |
| regex_v8                   | 37.7 ms                                                                | 40.7 ms: 1.08x slower                                          |
| docutils                   | 4.55 sec                                                               | 4.96 sec: 1.09x slower                                         |
| crypto_pyaes               | 138 ms                                                                 | 151 ms: 1.10x slower                                           |
| scimark_sor                | 230 ms                                                                 | 253 ms: 1.10x slower                                           |
| deltablue                  | 9.83 ms                                                                | 10.8 ms: 1.10x slower                                          |
| deepcopy_memo              | 52.6 us                                                                | 58.0 us: 1.10x slower                                          |
| async_generators           | 647 ms                                                                 | 715 ms: 1.10x slower                                           |
| html5lib                   | 117 ms                                                                 | 130 ms: 1.11x slower                                           |
| async_tree_memoization     | 584 ms                                                                 | 651 ms: 1.11x slower                                           |
| logging_silent             | 226 ns                                                                 | 253 ns: 1.12x slower                                           |
| hexiom                     | 12.6 ms                                                                | 14.2 ms: 1.13x slower                                          |
| go                         | 263 ms                                                                 | 296 ms: 1.13x slower                                           |
| spectral_norm              | 162 ms                                                                 | 184 ms: 1.14x slower                                           |
| sympy_integrate            | 34.1 ms                                                                | 39.0 ms: 1.15x slower                                          |
| logging_format             | 12.0 us                                                                | 13.9 us: 1.15x slower                                          |
| logging_simple             | 11.5 us                                                                | 13.3 us: 1.16x slower                                          |
| sqlalchemy_imperative      | 36.3 ms                                                                | 42.0 ms: 1.16x slower                                          |
| regex_effbot               | 4.17 ms                                                                | 4.83 ms: 1.16x slower                                          |
| thrift                     | 1.31 ms                                                                | 1.53 ms: 1.16x slower                                          |
| dulwich_log                | 112 ms                                                                 | 133 ms: 1.19x slower                                           |
| async_tree_none            | 511 ms                                                                 | 610 ms: 1.19x slower                                           |
| subparsers                 | 38.0 ms                                                                | 46.7 ms: 1.23x slower                                          |
| Geometric mean             | (ref)                                                                  | 1.02x slower                                                   |

Benchmark hidden because not significant (45): bench_thread_pool, sqlglot_transpile, scimark_lu, django_template, float, scimark_sparse_mat_mult, pickle_pure_python, xml_etree_parse, json_loads, chaos, json_dumps, sympy_sum, genshi_xml, connected_components, coroutines, fannkuch, sqlglot_normalize, unpickle_pure_python, 2to3, sqlglot_parse, async_tree_io_tg, pycparser, tomli_loads, scimark_monte_carlo, async_tree_cpu_io_mixed, mako, k_core, generators, pprint_safe_repr, sqlalchemy_declarative, sqlite_synth, pyflate, genshi_text, sympy_str, coverage, xml_etree_generate, regex_compile, async_tree_memoization_tg, sympy_expand, async_tree_io, bench_mp_pool, json, many_optionals, pylint, telco

- Geometric mean (including insignificant results): 1.012x slower

# HPT report

- Reliability score: 99.00% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x