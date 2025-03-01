# Results vs. base

- fork: tom-pytel
- ref: fix_issue_128942
- machine: linux-x86_64
- commit hash: 0bcde5c
- commit date: 2025-02-27
- overall geometric mean: 1.015x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250227-vultr-x86_64-python-45a24f54af4a65c14cc1-3.14.0a5+-45a24f5 | bm-20250227-vultr-x86_64-tom%2dpytel-fix_issue_128942-3.14.0a5+-0bcde5c |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| docutils       | 2.79 sec                                                               | 2.81 sec: 1.01x slower                                                  |
| html5lib       | 70.6 ms                                                                | 71.8 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                            |

Benchmark hidden because not significant (2): 2to3, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250227-vultr-x86_64-python-45a24f54af4a65c14cc1-3.14.0a5+-45a24f5 | bm-20250227-vultr-x86_64-tom%2dpytel-fix_issue_128942-3.14.0a5+-0bcde5c |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_generators           | 377 ms                                                                 | 372 ms: 1.01x faster                                                    |
| asyncio_websockets         | 518 ms                                                                 | 515 ms: 1.00x faster                                                    |
| coroutines                 | 23.4 ms                                                                | 23.5 ms: 1.01x slower                                                   |
| async_tree_io              | 584 ms                                                                 | 588 ms: 1.01x slower                                                    |
| async_tree_none_tg         | 237 ms                                                                 | 241 ms: 1.02x slower                                                    |
| async_tree_cpu_io_mixed    | 526 ms                                                                 | 543 ms: 1.03x slower                                                    |
| async_tree_cpu_io_mixed_tg | 490 ms                                                                 | 512 ms: 1.05x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                            |

Benchmark hidden because not significant (4): async_tree_io_tg, async_tree_memoization, async_tree_none, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250227-vultr-x86_64-python-45a24f54af4a65c14cc1-3.14.0a5+-45a24f5 | bm-20250227-vultr-x86_64-tom%2dpytel-fix_issue_128942-3.14.0a5+-0bcde5c |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| nbody          | 134 ms                                                                 | 133 ms: 1.01x faster                                                    |
| pidigits       | 213 ms                                                                 | 216 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                            |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250227-vultr-x86_64-python-45a24f54af4a65c14cc1-3.14.0a5+-45a24f5 | bm-20250227-vultr-x86_64-tom%2dpytel-fix_issue_128942-3.14.0a5+-0bcde5c |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 155 ms                                                                 | 156 ms: 1.01x slower                                                    |
| regex_v8       | 23.2 ms                                                                | 23.7 ms: 1.02x slower                                                   |
| regex_effbot   | 2.76 ms                                                                | 2.86 ms: 1.04x slower                                                   |
| regex_dna      | 169 ms                                                                 | 176 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250227-vultr-x86_64-python-45a24f54af4a65c14cc1-3.14.0a5+-45a24f5 | bm-20250227-vultr-x86_64-tom%2dpytel-fix_issue_128942-3.14.0a5+-0bcde5c |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_loads           | 29.6 us                                                                | 29.4 us: 1.01x faster                                                   |
| xml_etree_iterparse  | 88.3 ms                                                                | 87.9 ms: 1.00x faster                                                   |
| unpickle_pure_python | 250 us                                                                 | 251 us: 1.00x slower                                                    |
| xml_etree_process    | 69.7 ms                                                                | 70.4 ms: 1.01x slower                                                   |
| json_dumps           | 12.8 ms                                                                | 13.0 ms: 1.01x slower                                                   |
| xml_etree_generate   | 95.5 ms                                                                | 96.7 ms: 1.01x slower                                                   |
| tomli_loads          | 2.37 sec                                                               | 2.41 sec: 1.02x slower                                                  |
| pickle_pure_python   | 360 us                                                                 | 369 us: 1.02x slower                                                    |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                            |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20250227-vultr-x86_64-python-45a24f54af4a65c14cc1-3.14.0a5+-45a24f5 | bm-20250227-vultr-x86_64-tom%2dpytel-fix_issue_128942-3.14.0a5+-0bcde5c |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup | 15.6 ms                                                                | 15.6 ms: 1.00x faster                                                   |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                            |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20250227-vultr-x86_64-python-45a24f54af4a65c14cc1-3.14.0a5+-45a24f5 | bm-20250227-vultr-x86_64-tom%2dpytel-fix_issue_128942-3.14.0a5+-0bcde5c |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml     | 59.6 ms                                                                | 60.6 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                            |

Benchmark hidden because not significant (3): mako, genshi_text, django_template

All benchmarks:
===============

| Benchmark                  | bm-20250227-vultr-x86_64-python-45a24f54af4a65c14cc1-3.14.0a5+-45a24f5 | bm-20250227-vultr-x86_64-tom%2dpytel-fix_issue_128942-3.14.0a5+-0bcde5c |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| generators                 | 32.8 ms                                                                | 31.6 ms: 1.04x faster                                                   |
| telco                      | 8.84 ms                                                                | 8.59 ms: 1.03x faster                                                   |
| async_generators           | 377 ms                                                                 | 372 ms: 1.01x faster                                                    |
| nbody                      | 134 ms                                                                 | 133 ms: 1.01x faster                                                    |
| crypto_pyaes               | 89.3 ms                                                                | 88.5 ms: 1.01x faster                                                   |
| json                       | 5.11 ms                                                                | 5.06 ms: 1.01x faster                                                   |
| hexiom                     | 7.50 ms                                                                | 7.44 ms: 1.01x faster                                                   |
| json_loads                 | 29.6 us                                                                | 29.4 us: 1.01x faster                                                   |
| dulwich_log                | 83.2 ms                                                                | 82.7 ms: 1.01x faster                                                   |
| nqueens                    | 97.0 ms                                                                | 96.4 ms: 1.01x faster                                                   |
| asyncio_websockets         | 518 ms                                                                 | 515 ms: 1.00x faster                                                    |
| pprint_pformat             | 1.73 sec                                                               | 1.72 sec: 1.00x faster                                                  |
| xml_etree_iterparse        | 88.3 ms                                                                | 87.9 ms: 1.00x faster                                                   |
| logging_silent             | 114 ns                                                                 | 113 ns: 1.00x faster                                                    |
| python_startup             | 15.6 ms                                                                | 15.6 ms: 1.00x faster                                                   |
| unpickle_pure_python       | 250 us                                                                 | 251 us: 1.00x slower                                                    |
| sqlglot_parse              | 1.60 ms                                                                | 1.60 ms: 1.00x slower                                                   |
| chaos                      | 69.6 ms                                                                | 70.0 ms: 1.01x slower                                                   |
| many_optionals             | 1.16 ms                                                                | 1.17 ms: 1.01x slower                                                   |
| coroutines                 | 23.4 ms                                                                | 23.5 ms: 1.01x slower                                                   |
| go                         | 140 ms                                                                 | 141 ms: 1.01x slower                                                    |
| mdp                        | 2.72 sec                                                               | 2.73 sec: 1.01x slower                                                  |
| sympy_str                  | 335 ms                                                                 | 337 ms: 1.01x slower                                                    |
| async_tree_io              | 584 ms                                                                 | 588 ms: 1.01x slower                                                    |
| deepcopy_memo              | 38.1 us                                                                | 38.4 us: 1.01x slower                                                   |
| regex_compile              | 155 ms                                                                 | 156 ms: 1.01x slower                                                    |
| sqlalchemy_declarative     | 155 ms                                                                 | 157 ms: 1.01x slower                                                    |
| sqlglot_optimize           | 61.3 ms                                                                | 61.8 ms: 1.01x slower                                                   |
| docutils                   | 2.79 sec                                                               | 2.81 sec: 1.01x slower                                                  |
| xml_etree_process          | 69.7 ms                                                                | 70.4 ms: 1.01x slower                                                   |
| k_core                     | 2.30 sec                                                               | 2.33 sec: 1.01x slower                                                  |
| sqlglot_normalize          | 121 ms                                                                 | 122 ms: 1.01x slower                                                    |
| coverage                   | 95.7 ms                                                                | 96.7 ms: 1.01x slower                                                   |
| json_dumps                 | 12.8 ms                                                                | 13.0 ms: 1.01x slower                                                   |
| bpe_tokeniser              | 4.79 sec                                                               | 4.85 sec: 1.01x slower                                                  |
| fannkuch                   | 492 ms                                                                 | 498 ms: 1.01x slower                                                    |
| spectral_norm              | 112 ms                                                                 | 114 ms: 1.01x slower                                                    |
| sqlite_synth               | 2.02 us                                                                | 2.04 us: 1.01x slower                                                   |
| typing_runtime_protocols   | 197 us                                                                 | 200 us: 1.01x slower                                                    |
| xml_etree_generate         | 95.5 ms                                                                | 96.7 ms: 1.01x slower                                                   |
| sympy_sum                  | 186 ms                                                                 | 188 ms: 1.01x slower                                                    |
| sympy_integrate            | 23.9 ms                                                                | 24.2 ms: 1.01x slower                                                   |
| subparsers                 | 25.0 ms                                                                | 25.4 ms: 1.01x slower                                                   |
| genshi_xml                 | 59.6 ms                                                                | 60.6 ms: 1.02x slower                                                   |
| pidigits                   | 213 ms                                                                 | 216 ms: 1.02x slower                                                    |
| async_tree_none_tg         | 237 ms                                                                 | 241 ms: 1.02x slower                                                    |
| sympy_expand               | 546 ms                                                                 | 554 ms: 1.02x slower                                                    |
| html5lib                   | 70.6 ms                                                                | 71.8 ms: 1.02x slower                                                   |
| logging_format             | 8.16 us                                                                | 8.30 us: 1.02x slower                                                   |
| tomli_loads                | 2.37 sec                                                               | 2.41 sec: 1.02x slower                                                  |
| deepcopy                   | 307 us                                                                 | 313 us: 1.02x slower                                                    |
| regex_v8                   | 23.2 ms                                                                | 23.7 ms: 1.02x slower                                                   |
| thrift                     | 869 us                                                                 | 886 us: 1.02x slower                                                    |
| meteor_contest             | 127 ms                                                                 | 130 ms: 1.02x slower                                                    |
| richards                   | 55.0 ms                                                                | 56.2 ms: 1.02x slower                                                   |
| deepcopy_reduce            | 3.15 us                                                                | 3.22 us: 1.02x slower                                                   |
| pickle_pure_python         | 360 us                                                                 | 369 us: 1.02x slower                                                    |
| async_tree_cpu_io_mixed    | 526 ms                                                                 | 543 ms: 1.03x slower                                                    |
| regex_effbot               | 2.76 ms                                                                | 2.86 ms: 1.04x slower                                                   |
| regex_dna                  | 169 ms                                                                 | 176 ms: 1.04x slower                                                    |
| async_tree_cpu_io_mixed_tg | 490 ms                                                                 | 512 ms: 1.05x slower                                                    |
| richards_super             | 64.0 ms                                                                | 67.4 ms: 1.05x slower                                                   |
| scimark_sor                | 135 ms                                                                 | 145 ms: 1.07x slower                                                    |
| scimark_lu                 | 140 ms                                                                 | 158 ms: 1.13x slower                                                    |
| scimark_monte_carlo        | 83.0 ms                                                                | 96.4 ms: 1.16x slower                                                   |
| scimark_fft                | 392 ms                                                                 | 500 ms: 1.27x slower                                                    |
| scimark_sparse_mat_mult    | 5.77 ms                                                                | 7.78 ms: 1.35x slower                                                   |
| Geometric mean             | (ref)                                                                  | 1.02x slower                                                            |

Benchmark hidden because not significant (29): connected_components, shortest_path, logging_simple, float, pathlib, pyflate, bench_thread_pool, comprehensions, pycparser, create_gc_cycles, python_startup_no_site, pprint_safe_repr, 2to3, deltablue, xml_etree_parse, raytrace, gc_traversal, mako, bench_mp_pool, genshi_text, async_tree_io_tg, django_template, async_tree_memoization, sqlalchemy_imperative, sqlglot_transpile, async_tree_none, async_tree_memoization_tg, pylint, sphinx

- Geometric mean (including insignificant results): 1.015x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x