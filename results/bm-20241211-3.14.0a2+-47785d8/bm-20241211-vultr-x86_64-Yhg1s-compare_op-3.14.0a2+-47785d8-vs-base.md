# Results vs. base

- fork: Yhg1s
- ref: compare_op
- machine: linux-x86_64
- commit hash: 47785d8
- commit date: 2024-12-11
- overall geometric mean: 1.003x slower
- HPT reliability: 99.60%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241211-vultr-x86_64-python-359389ed51aecc107681-3.14.0a2+-359389e | bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2+-47785d8 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| 2to3           | 253 ms                                                                 | 255 ms: 1.01x slower                                        |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20241211-vultr-x86_64-python-359389ed51aecc107681-3.14.0a2+-359389e | bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2+-47785d8 |
|------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| async_generators | 358 ms                                                                 | 366 ms: 1.02x slower                                        |
| Geometric mean   | (ref)                                                                  | 1.00x slower                                                |

Benchmark hidden because not significant (10): async_tree_io_tg, async_tree_none, async_tree_memoization, async_tree_io, async_tree_memoization_tg, async_tree_none_tg, asyncio_websockets, coroutines, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241211-vultr-x86_64-python-359389ed51aecc107681-3.14.0a2+-359389e | bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2+-47785d8 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| nbody          | 89.3 ms                                                                | 90.3 ms: 1.01x slower                                       |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                |

Benchmark hidden because not significant (2): pidigits, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241211-vultr-x86_64-python-359389ed51aecc107681-3.14.0a2+-359389e | bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2+-47785d8 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| regex_dna      | 178 ms                                                                 | 164 ms: 1.08x faster                                        |
| regex_v8       | 24.7 ms                                                                | 24.1 ms: 1.02x faster                                       |
| regex_compile  | 127 ms                                                                 | 129 ms: 1.01x slower                                        |
| regex_effbot   | 2.73 ms                                                                | 2.79 ms: 1.02x slower                                       |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241211-vultr-x86_64-python-359389ed51aecc107681-3.14.0a2+-359389e | bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2+-47785d8 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| json_loads           | 25.5 us                                                                | 25.0 us: 1.02x faster                                       |
| unpickle_pure_python | 213 us                                                                 | 211 us: 1.01x faster                                        |
| pickle_pure_python   | 313 us                                                                 | 312 us: 1.00x faster                                        |
| xml_etree_generate   | 83.7 ms                                                                | 84.2 ms: 1.01x slower                                       |
| xml_etree_parse      | 129 ms                                                                 | 129 ms: 1.01x slower                                        |
| xml_etree_process    | 58.0 ms                                                                | 58.5 ms: 1.01x slower                                       |
| json_dumps           | 11.4 ms                                                                | 11.5 ms: 1.01x slower                                       |
| tomli_loads          | 2.06 sec                                                               | 2.09 sec: 1.02x slower                                      |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241211-vultr-x86_64-python-359389ed51aecc107681-3.14.0a2+-359389e | bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2+-47785d8 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| python_startup_no_site | 7.46 ms                                                                | 7.49 ms: 1.00x slower                                       |
| python_startup         | 14.6 ms                                                                | 14.7 ms: 1.00x slower                                       |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241211-vultr-x86_64-python-359389ed51aecc107681-3.14.0a2+-359389e | bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2+-47785d8 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| django_template | 35.8 ms                                                                | 35.2 ms: 1.02x faster                                       |
| genshi_text     | 21.9 ms                                                                | 22.1 ms: 1.01x slower                                       |
| genshi_xml      | 49.6 ms                                                                | 50.7 ms: 1.02x slower                                       |
| mako            | 11.3 ms                                                                | 11.6 ms: 1.03x slower                                       |
| Geometric mean  | (ref)                                                                  | 1.01x slower                                                |

All benchmarks:
===============

| Benchmark               | bm-20241211-vultr-x86_64-python-359389ed51aecc107681-3.14.0a2+-359389e | bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2+-47785d8 |
|-------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| gc_traversal            | 4.38 ms                                                                | 4.04 ms: 1.09x faster                                       |
| regex_dna               | 178 ms                                                                 | 164 ms: 1.08x faster                                        |
| crypto_pyaes            | 68.9 ms                                                                | 66.9 ms: 1.03x faster                                       |
| fannkuch                | 377 ms                                                                 | 367 ms: 1.03x faster                                        |
| regex_v8                | 24.7 ms                                                                | 24.1 ms: 1.02x faster                                       |
| json_loads              | 25.5 us                                                                | 25.0 us: 1.02x faster                                       |
| json                    | 4.80 ms                                                                | 4.72 ms: 1.02x faster                                       |
| django_template         | 35.8 ms                                                                | 35.2 ms: 1.02x faster                                       |
| pycparser               | 1.12 sec                                                               | 1.11 sec: 1.01x faster                                      |
| sqlite_synth            | 2.23 us                                                                | 2.20 us: 1.01x faster                                       |
| scimark_lu              | 111 ms                                                                 | 109 ms: 1.01x faster                                        |
| unpickle_pure_python    | 213 us                                                                 | 211 us: 1.01x faster                                        |
| shortest_path           | 442 ms                                                                 | 438 ms: 1.01x faster                                        |
| richards                | 45.4 ms                                                                | 45.0 ms: 1.01x faster                                       |
| create_gc_cycles        | 1.85 ms                                                                | 1.84 ms: 1.01x faster                                       |
| pathlib                 | 18.5 ms                                                                | 18.4 ms: 1.01x faster                                       |
| pickle_pure_python      | 313 us                                                                 | 312 us: 1.00x faster                                        |
| bpe_tokeniser           | 4.27 sec                                                               | 4.28 sec: 1.00x slower                                      |
| python_startup_no_site  | 7.46 ms                                                                | 7.49 ms: 1.00x slower                                       |
| sqlalchemy_declarative  | 126 ms                                                                 | 127 ms: 1.00x slower                                        |
| pprint_safe_repr        | 705 ms                                                                 | 709 ms: 1.00x slower                                        |
| python_startup          | 14.6 ms                                                                | 14.7 ms: 1.00x slower                                       |
| xml_etree_generate      | 83.7 ms                                                                | 84.2 ms: 1.01x slower                                       |
| xml_etree_parse         | 129 ms                                                                 | 129 ms: 1.01x slower                                        |
| chaos                   | 57.6 ms                                                                | 58.0 ms: 1.01x slower                                       |
| 2to3                    | 253 ms                                                                 | 255 ms: 1.01x slower                                        |
| pprint_pformat          | 1.45 sec                                                               | 1.46 sec: 1.01x slower                                      |
| xml_etree_process       | 58.0 ms                                                                | 58.5 ms: 1.01x slower                                       |
| bench_mp_pool           | 88.3 ms                                                                | 89.1 ms: 1.01x slower                                       |
| json_dumps              | 11.4 ms                                                                | 11.5 ms: 1.01x slower                                       |
| raytrace                | 256 ms                                                                 | 259 ms: 1.01x slower                                        |
| nbody                   | 89.3 ms                                                                | 90.3 ms: 1.01x slower                                       |
| genshi_text             | 21.9 ms                                                                | 22.1 ms: 1.01x slower                                       |
| regex_compile           | 127 ms                                                                 | 129 ms: 1.01x slower                                        |
| meteor_contest          | 98.7 ms                                                                | 100 ms: 1.01x slower                                        |
| hexiom                  | 5.79 ms                                                                | 5.88 ms: 1.01x slower                                       |
| logging_format          | 6.71 us                                                                | 6.81 us: 1.01x slower                                       |
| subparsers              | 21.7 ms                                                                | 22.0 ms: 1.02x slower                                       |
| tomli_loads             | 2.06 sec                                                               | 2.09 sec: 1.02x slower                                      |
| scimark_fft             | 326 ms                                                                 | 332 ms: 1.02x slower                                        |
| richards_super          | 50.8 ms                                                                | 51.8 ms: 1.02x slower                                       |
| genshi_xml              | 49.6 ms                                                                | 50.7 ms: 1.02x slower                                       |
| spectral_norm           | 106 ms                                                                 | 109 ms: 1.02x slower                                        |
| regex_effbot            | 2.73 ms                                                                | 2.79 ms: 1.02x slower                                       |
| scimark_monte_carlo     | 62.8 ms                                                                | 64.2 ms: 1.02x slower                                       |
| async_generators        | 358 ms                                                                 | 366 ms: 1.02x slower                                        |
| logging_silent          | 101 ns                                                                 | 103 ns: 1.02x slower                                        |
| mako                    | 11.3 ms                                                                | 11.6 ms: 1.03x slower                                       |
| deepcopy_memo           | 29.2 us                                                                | 30.2 us: 1.04x slower                                       |
| nqueens                 | 77.0 ms                                                                | 80.1 ms: 1.04x slower                                       |
| telco                   | 7.21 ms                                                                | 7.52 ms: 1.04x slower                                       |
| mdp                     | 2.34 sec                                                               | 2.49 sec: 1.06x slower                                      |
| scimark_sparse_mat_mult | 4.31 ms                                                                | 4.61 ms: 1.07x slower                                       |
| Geometric mean          | (ref)                                                                  | 1.00x slower                                                |

Benchmark hidden because not significant (42): async_tree_io_tg, coverage, async_tree_none, deepcopy_reduce, thrift, xml_etree_iterparse, sympy_integrate, deltablue, scimark_sor, comprehensions, async_tree_memoization, sqlglot_transpile, async_tree_io, pyflate, sqlglot_optimize, sqlglot_normalize, async_tree_memoization_tg, async_tree_none_tg, dulwich_log, sympy_str, sympy_expand, asyncio_websockets, coroutines, pidigits, many_optionals, sphinx, docutils, go, async_tree_cpu_io_mixed_tg, generators, deepcopy, connected_components, sqlglot_parse, bench_thread_pool, sympy_sum, sqlalchemy_imperative, logging_simple, async_tree_cpu_io_mixed, typing_runtime_protocols, k_core, pylint, float

- Geometric mean (including insignificant results): 1.003x slower

# HPT report

- Reliability score: 99.60% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x