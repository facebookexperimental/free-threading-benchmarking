# Results vs. base

- fork: DinoV
- ref: heap_ast_types
- machine: linux-x86_64
- commit hash: f1e05f7
- commit date: 2025-09-15
- overall geometric mean: 1.004x slower
- HPT reliability: 97.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250915-vultr-x86_64-python-fa12c6bae47a41dd84e5-3.15.0a0-fa12c6b | bm-20250915-vultr-x86_64-DinoV-heap_ast_types-3.15.0a0-f1e05f7 |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------:|
| docutils       | 2.58 sec                                                              | 2.54 sec: 1.02x faster                                         |
| html5lib       | 63.3 ms                                                               | 61.2 ms: 1.03x faster                                          |
| Geometric mean | (ref)                                                                 | 1.02x faster                                                   |

Benchmark hidden because not significant (2): 2to3, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20250915-vultr-x86_64-python-fa12c6bae47a41dd84e5-3.15.0a0-fa12c6b | bm-20250915-vultr-x86_64-DinoV-heap_ast_types-3.15.0a0-f1e05f7 |
|--------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------:|
| asyncio_websockets | 521 ms                                                                | 517 ms: 1.01x faster                                           |
| async_generators   | 339 ms                                                                | 347 ms: 1.02x slower                                           |
| coroutines         | 23.1 ms                                                               | 23.9 ms: 1.03x slower                                          |
| Geometric mean     | (ref)                                                                 | 1.00x slower                                                   |

Benchmark hidden because not significant (8): async_tree_none, async_tree_cpu_io_mixed, async_tree_memoization, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg, async_tree_none_tg, async_tree_io, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250915-vultr-x86_64-python-fa12c6bae47a41dd84e5-3.15.0a0-fa12c6b | bm-20250915-vultr-x86_64-DinoV-heap_ast_types-3.15.0a0-f1e05f7 |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------:|
| pidigits       | 209 ms                                                                | 200 ms: 1.05x faster                                           |
| float          | 71.3 ms                                                               | 72.0 ms: 1.01x slower                                          |
| Geometric mean | (ref)                                                                 | 1.01x faster                                                   |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250915-vultr-x86_64-python-fa12c6bae47a41dd84e5-3.15.0a0-fa12c6b | bm-20250915-vultr-x86_64-DinoV-heap_ast_types-3.15.0a0-f1e05f7 |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------:|
| regex_compile  | 123 ms                                                                | 123 ms: 1.00x faster                                           |
| regex_dna      | 172 ms                                                                | 175 ms: 1.02x slower                                           |
| regex_effbot   | 2.69 ms                                                               | 2.74 ms: 1.02x slower                                          |
| regex_v8       | 21.3 ms                                                               | 22.2 ms: 1.04x slower                                          |
| Geometric mean | (ref)                                                                 | 1.02x slower                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250915-vultr-x86_64-python-fa12c6bae47a41dd84e5-3.15.0a0-fa12c6b | bm-20250915-vultr-x86_64-DinoV-heap_ast_types-3.15.0a0-f1e05f7 |
|----------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------:|
| pickle_pure_python   | 303 us                                                                | 305 us: 1.01x slower                                           |
| tomli_loads          | 1.89 sec                                                              | 1.90 sec: 1.01x slower                                         |
| xml_etree_iterparse  | 92.8 ms                                                               | 93.5 ms: 1.01x slower                                          |
| json_loads           | 28.0 us                                                               | 28.3 us: 1.01x slower                                          |
| json_dumps           | 9.48 ms                                                               | 9.67 ms: 1.02x slower                                          |
| xml_etree_parse      | 130 ms                                                                | 133 ms: 1.02x slower                                           |
| unpickle_pure_python | 207 us                                                                | 213 us: 1.03x slower                                           |
| Geometric mean       | (ref)                                                                 | 1.01x slower                                                   |

Benchmark hidden because not significant (2): xml_etree_generate, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250915-vultr-x86_64-python-fa12c6bae47a41dd84e5-3.15.0a0-fa12c6b | bm-20250915-vultr-x86_64-DinoV-heap_ast_types-3.15.0a0-f1e05f7 |
|------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------:|
| python_startup_no_site | 7.24 ms                                                               | 7.26 ms: 1.00x slower                                          |
| python_startup         | 12.5 ms                                                               | 12.6 ms: 1.01x slower                                          |
| Geometric mean         | (ref)                                                                 | 1.01x slower                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20250915-vultr-x86_64-python-fa12c6bae47a41dd84e5-3.15.0a0-fa12c6b | bm-20250915-vultr-x86_64-DinoV-heap_ast_types-3.15.0a0-f1e05f7 |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------:|
| genshi_xml     | 49.3 ms                                                               | 47.9 ms: 1.03x faster                                          |
| genshi_text    | 20.4 ms                                                               | 20.2 ms: 1.01x faster                                          |
| mako           | 11.6 ms                                                               | 12.0 ms: 1.04x slower                                          |
| Geometric mean | (ref)                                                                 | 1.00x slower                                                   |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark               | bm-20250915-vultr-x86_64-python-fa12c6bae47a41dd84e5-3.15.0a0-fa12c6b | bm-20250915-vultr-x86_64-DinoV-heap_ast_types-3.15.0a0-f1e05f7 |
|-------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------:|
| gc_traversal            | 4.53 ms                                                               | 4.32 ms: 1.05x faster                                          |
| pidigits                | 209 ms                                                                | 200 ms: 1.05x faster                                           |
| html5lib                | 63.3 ms                                                               | 61.2 ms: 1.03x faster                                          |
| genshi_xml              | 49.3 ms                                                               | 47.9 ms: 1.03x faster                                          |
| docutils                | 2.58 sec                                                              | 2.54 sec: 1.02x faster                                         |
| thrift                  | 768 us                                                                | 759 us: 1.01x faster                                           |
| dulwich_log             | 67.3 ms                                                               | 66.5 ms: 1.01x faster                                          |
| coverage                | 82.3 ms                                                               | 81.5 ms: 1.01x faster                                          |
| logging_silent          | 98.4 ns                                                               | 97.4 ns: 1.01x faster                                          |
| asyncio_websockets      | 521 ms                                                                | 517 ms: 1.01x faster                                           |
| telco                   | 159 ms                                                                | 158 ms: 1.01x faster                                           |
| chaos                   | 57.2 ms                                                               | 56.7 ms: 1.01x faster                                          |
| pprint_pformat          | 1.44 sec                                                              | 1.43 sec: 1.01x faster                                         |
| genshi_text             | 20.4 ms                                                               | 20.2 ms: 1.01x faster                                          |
| richards_super          | 47.1 ms                                                               | 46.8 ms: 1.01x faster                                          |
| sqlglot_v2_parse        | 1.21 ms                                                               | 1.21 ms: 1.00x faster                                          |
| pprint_safe_repr        | 705 ms                                                                | 702 ms: 1.00x faster                                           |
| sqlglot_v2_transpile    | 1.51 ms                                                               | 1.51 ms: 1.00x faster                                          |
| sympy_integrate         | 18.8 ms                                                               | 18.8 ms: 1.00x faster                                          |
| regex_compile           | 123 ms                                                                | 123 ms: 1.00x faster                                           |
| python_startup_no_site  | 7.24 ms                                                               | 7.26 ms: 1.00x slower                                          |
| sqlglot_v2_optimize     | 50.0 ms                                                               | 50.2 ms: 1.00x slower                                          |
| hexiom                  | 5.66 ms                                                               | 5.69 ms: 1.00x slower                                          |
| pickle_pure_python      | 303 us                                                                | 305 us: 1.01x slower                                           |
| tomli_loads             | 1.89 sec                                                              | 1.90 sec: 1.01x slower                                         |
| scimark_lu              | 110 ms                                                                | 111 ms: 1.01x slower                                           |
| go                      | 104 ms                                                                | 105 ms: 1.01x slower                                           |
| xml_etree_iterparse     | 92.8 ms                                                               | 93.5 ms: 1.01x slower                                          |
| python_startup          | 12.5 ms                                                               | 12.6 ms: 1.01x slower                                          |
| sqlglot_v2_normalize    | 99.5 ms                                                               | 100 ms: 1.01x slower                                           |
| shortest_path           | 440 ms                                                                | 443 ms: 1.01x slower                                           |
| deepcopy                | 243 us                                                                | 245 us: 1.01x slower                                           |
| pathlib                 | 18.0 ms                                                               | 18.1 ms: 1.01x slower                                          |
| mdp                     | 1.15 sec                                                              | 1.16 sec: 1.01x slower                                         |
| connected_components    | 400 ms                                                                | 404 ms: 1.01x slower                                           |
| crypto_pyaes            | 68.2 ms                                                               | 68.8 ms: 1.01x slower                                          |
| deltablue               | 3.24 ms                                                               | 3.27 ms: 1.01x slower                                          |
| float                   | 71.3 ms                                                               | 72.0 ms: 1.01x slower                                          |
| create_gc_cycles        | 1.91 ms                                                               | 1.93 ms: 1.01x slower                                          |
| scimark_monte_carlo     | 61.2 ms                                                               | 61.9 ms: 1.01x slower                                          |
| json_loads              | 28.0 us                                                               | 28.3 us: 1.01x slower                                          |
| fannkuch                | 374 ms                                                                | 379 ms: 1.01x slower                                           |
| raytrace                | 252 ms                                                                | 255 ms: 1.01x slower                                           |
| logging_simple          | 5.77 us                                                               | 5.85 us: 1.01x slower                                          |
| scimark_sparse_mat_mult | 4.78 ms                                                               | 4.85 ms: 1.01x slower                                          |
| regex_dna               | 172 ms                                                                | 175 ms: 1.02x slower                                           |
| deepcopy_memo           | 26.3 us                                                               | 26.8 us: 1.02x slower                                          |
| comprehensions          | 15.6 us                                                               | 15.9 us: 1.02x slower                                          |
| nqueens                 | 76.5 ms                                                               | 77.9 ms: 1.02x slower                                          |
| scimark_sor             | 108 ms                                                                | 111 ms: 1.02x slower                                           |
| json                    | 5.06 ms                                                               | 5.15 ms: 1.02x slower                                          |
| json_dumps              | 9.48 ms                                                               | 9.67 ms: 1.02x slower                                          |
| regex_effbot            | 2.69 ms                                                               | 2.74 ms: 1.02x slower                                          |
| xml_etree_parse         | 130 ms                                                                | 133 ms: 1.02x slower                                           |
| deepcopy_reduce         | 2.59 us                                                               | 2.65 us: 1.02x slower                                          |
| async_generators        | 339 ms                                                                | 347 ms: 1.02x slower                                           |
| bpe_tokeniser           | 4.15 sec                                                              | 4.26 sec: 1.03x slower                                         |
| scimark_fft             | 330 ms                                                                | 338 ms: 1.03x slower                                           |
| unpickle_pure_python    | 207 us                                                                | 213 us: 1.03x slower                                           |
| spectral_norm           | 94.1 ms                                                               | 97.0 ms: 1.03x slower                                          |
| coroutines              | 23.1 ms                                                               | 23.9 ms: 1.03x slower                                          |
| pyflate                 | 397 ms                                                                | 412 ms: 1.04x slower                                           |
| mako                    | 11.6 ms                                                               | 12.0 ms: 1.04x slower                                          |
| regex_v8                | 21.3 ms                                                               | 22.2 ms: 1.04x slower                                          |
| Geometric mean          | (ref)                                                                 | 1.00x slower                                                   |

Benchmark hidden because not significant (30): async_tree_none, sphinx, async_tree_cpu_io_mixed, typing_runtime_protocols, async_tree_memoization, richards, bench_thread_pool, nbody, k_core, 2to3, xml_etree_generate, meteor_contest, async_tree_memoization_tg, sympy_sum, async_tree_cpu_io_mixed_tg, many_optionals, generators, subparsers, pycparser, sqlite_synth, logging_format, sympy_str, bench_mp_pool, xml_etree_process, async_tree_none_tg, async_tree_io, django_template, sympy_expand, pylint, async_tree_io_tg

- Geometric mean (including insignificant results): 1.004x slower

# HPT report

- Reliability score: 97.00% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x