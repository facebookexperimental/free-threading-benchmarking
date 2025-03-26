# Results vs. base

- fork: colesbury
- ref: gh_128421_fix_perf_r
- machine: linux-x86_64
- commit hash: 80e36d7
- commit date: 2025-03-25
- overall geometric mean: 1.002x faster
- HPT reliability: 97.75%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250325-vultr-x86_64-python-8ada7a9e1435302ec2cb-3.14.0a6+-8ada7a9 | bm-20250325-vultr-x86_64-colesbury-gh_128421_fix_perf_r-3.14.0a6+-80e36d7 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 299 ms                                                                 | 297 ms: 1.01x faster                                                      |
| html5lib       | 71.3 ms                                                                | 72.5 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                              |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250325-vultr-x86_64-python-8ada7a9e1435302ec2cb-3.14.0a6+-8ada7a9 | bm-20250325-vultr-x86_64-colesbury-gh_128421_fix_perf_r-3.14.0a6+-80e36d7 |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| coroutines                 | 23.8 ms                                                                | 23.2 ms: 1.03x faster                                                     |
| async_tree_memoization_tg  | 302 ms                                                                 | 299 ms: 1.01x faster                                                      |
| async_tree_io              | 585 ms                                                                 | 580 ms: 1.01x faster                                                      |
| async_tree_cpu_io_mixed_tg | 487 ms                                                                 | 485 ms: 1.00x faster                                                      |
| async_generators           | 389 ms                                                                 | 391 ms: 1.01x slower                                                      |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                              |

Benchmark hidden because not significant (6): async_tree_none, async_tree_io_tg, async_tree_cpu_io_mixed, async_tree_memoization, asyncio_websockets, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250325-vultr-x86_64-python-8ada7a9e1435302ec2cb-3.14.0a6+-8ada7a9 | bm-20250325-vultr-x86_64-colesbury-gh_128421_fix_perf_r-3.14.0a6+-80e36d7 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits       | 196 ms                                                                 | 191 ms: 1.03x faster                                                      |
| float          | 77.3 ms                                                                | 77.7 ms: 1.00x slower                                                     |
| nbody          | 135 ms                                                                 | 137 ms: 1.02x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250325-vultr-x86_64-python-8ada7a9e1435302ec2cb-3.14.0a6+-8ada7a9 | bm-20250325-vultr-x86_64-colesbury-gh_128421_fix_perf_r-3.14.0a6+-80e36d7 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_v8       | 21.8 ms                                                                | 20.9 ms: 1.04x faster                                                     |
| regex_dna      | 182 ms                                                                 | 175 ms: 1.04x faster                                                      |
| regex_compile  | 159 ms                                                                 | 157 ms: 1.01x faster                                                      |
| regex_effbot   | 2.78 ms                                                                | 2.76 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250325-vultr-x86_64-python-8ada7a9e1435302ec2cb-3.14.0a6+-8ada7a9 | bm-20250325-vultr-x86_64-colesbury-gh_128421_fix_perf_r-3.14.0a6+-80e36d7 |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| tomli_loads          | 2.38 sec                                                               | 2.35 sec: 1.01x faster                                                    |
| unpickle_pure_python | 257 us                                                                 | 254 us: 1.01x faster                                                      |
| pickle_pure_python   | 361 us                                                                 | 358 us: 1.01x faster                                                      |
| xml_etree_iterparse  | 88.8 ms                                                                | 88.1 ms: 1.01x faster                                                     |
| json_dumps           | 13.0 ms                                                                | 12.9 ms: 1.01x faster                                                     |
| xml_etree_parse      | 130 ms                                                                 | 129 ms: 1.01x faster                                                      |
| xml_etree_generate   | 97.2 ms                                                                | 96.9 ms: 1.00x faster                                                     |
| xml_etree_process    | 70.7 ms                                                                | 70.9 ms: 1.00x slower                                                     |
| json_loads           | 29.4 us                                                                | 30.5 us: 1.04x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250325-vultr-x86_64-python-8ada7a9e1435302ec2cb-3.14.0a6+-8ada7a9 | bm-20250325-vultr-x86_64-colesbury-gh_128421_fix_perf_r-3.14.0a6+-80e36d7 |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 11.1 ms                                                                | 11.1 ms: 1.00x faster                                                     |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                              |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250325-vultr-x86_64-python-8ada7a9e1435302ec2cb-3.14.0a6+-8ada7a9 | bm-20250325-vultr-x86_64-colesbury-gh_128421_fix_perf_r-3.14.0a6+-80e36d7 |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| genshi_text     | 28.6 ms                                                                | 28.4 ms: 1.01x faster                                                     |
| mako            | 16.1 ms                                                                | 16.0 ms: 1.01x faster                                                     |
| django_template | 42.5 ms                                                                | 42.7 ms: 1.00x slower                                                     |
| Geometric mean  | (ref)                                                                  | 1.00x faster                                                              |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20250325-vultr-x86_64-python-8ada7a9e1435302ec2cb-3.14.0a6+-8ada7a9 | bm-20250325-vultr-x86_64-colesbury-gh_128421_fix_perf_r-3.14.0a6+-80e36d7 |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| coverage                   | 108 ms                                                                 | 99.6 ms: 1.09x faster                                                     |
| regex_v8                   | 21.8 ms                                                                | 20.9 ms: 1.04x faster                                                     |
| regex_dna                  | 182 ms                                                                 | 175 ms: 1.04x faster                                                      |
| coroutines                 | 23.8 ms                                                                | 23.2 ms: 1.03x faster                                                     |
| pidigits                   | 196 ms                                                                 | 191 ms: 1.03x faster                                                      |
| go                         | 147 ms                                                                 | 144 ms: 1.03x faster                                                      |
| logging_silent             | 118 ns                                                                 | 116 ns: 1.02x faster                                                      |
| comprehensions             | 21.1 us                                                                | 20.6 us: 1.02x faster                                                     |
| scimark_monte_carlo        | 85.4 ms                                                                | 83.5 ms: 1.02x faster                                                     |
| create_gc_cycles           | 1.37 ms                                                                | 1.35 ms: 1.02x faster                                                     |
| mdp                        | 2.67 sec                                                               | 2.62 sec: 1.02x faster                                                    |
| tomli_loads                | 2.38 sec                                                               | 2.35 sec: 1.01x faster                                                    |
| hexiom                     | 7.70 ms                                                                | 7.60 ms: 1.01x faster                                                     |
| regex_compile              | 159 ms                                                                 | 157 ms: 1.01x faster                                                      |
| unpickle_pure_python       | 257 us                                                                 | 254 us: 1.01x faster                                                      |
| raytrace                   | 329 ms                                                                 | 325 ms: 1.01x faster                                                      |
| gc_traversal               | 1.81 ms                                                                | 1.79 ms: 1.01x faster                                                     |
| sympy_integrate            | 23.8 ms                                                                | 23.5 ms: 1.01x faster                                                     |
| async_tree_memoization_tg  | 302 ms                                                                 | 299 ms: 1.01x faster                                                      |
| regex_effbot               | 2.78 ms                                                                | 2.76 ms: 1.01x faster                                                     |
| pickle_pure_python         | 361 us                                                                 | 358 us: 1.01x faster                                                      |
| thrift                     | 883 us                                                                 | 876 us: 1.01x faster                                                      |
| scimark_sor                | 139 ms                                                                 | 138 ms: 1.01x faster                                                      |
| genshi_text                | 28.6 ms                                                                | 28.4 ms: 1.01x faster                                                     |
| mako                       | 16.1 ms                                                                | 16.0 ms: 1.01x faster                                                     |
| xml_etree_iterparse        | 88.8 ms                                                                | 88.1 ms: 1.01x faster                                                     |
| json_dumps                 | 13.0 ms                                                                | 12.9 ms: 1.01x faster                                                     |
| async_tree_io              | 585 ms                                                                 | 580 ms: 1.01x faster                                                      |
| xml_etree_parse            | 130 ms                                                                 | 129 ms: 1.01x faster                                                      |
| sympy_expand               | 552 ms                                                                 | 549 ms: 1.01x faster                                                      |
| 2to3                       | 299 ms                                                                 | 297 ms: 1.01x faster                                                      |
| deltablue                  | 3.93 ms                                                                | 3.91 ms: 1.01x faster                                                     |
| chaos                      | 69.2 ms                                                                | 68.9 ms: 1.00x faster                                                     |
| richards_super             | 64.9 ms                                                                | 64.6 ms: 1.00x faster                                                     |
| async_tree_cpu_io_mixed_tg | 487 ms                                                                 | 485 ms: 1.00x faster                                                      |
| richards                   | 56.1 ms                                                                | 55.9 ms: 1.00x faster                                                     |
| nqueens                    | 98.6 ms                                                                | 98.3 ms: 1.00x faster                                                     |
| xml_etree_generate         | 97.2 ms                                                                | 96.9 ms: 1.00x faster                                                     |
| python_startup_no_site     | 11.1 ms                                                                | 11.1 ms: 1.00x faster                                                     |
| bpe_tokeniser              | 4.85 sec                                                               | 4.84 sec: 1.00x faster                                                    |
| xml_etree_process          | 70.7 ms                                                                | 70.9 ms: 1.00x slower                                                     |
| sqlglot_v2_parse           | 1.59 ms                                                                | 1.60 ms: 1.00x slower                                                     |
| float                      | 77.3 ms                                                                | 77.7 ms: 1.00x slower                                                     |
| django_template            | 42.5 ms                                                                | 42.7 ms: 1.00x slower                                                     |
| fannkuch                   | 497 ms                                                                 | 500 ms: 1.01x slower                                                      |
| shortest_path              | 547 ms                                                                 | 551 ms: 1.01x slower                                                      |
| async_generators           | 389 ms                                                                 | 391 ms: 1.01x slower                                                      |
| sqlite_synth               | 2.00 us                                                                | 2.02 us: 1.01x slower                                                     |
| scimark_fft                | 396 ms                                                                 | 400 ms: 1.01x slower                                                      |
| pathlib                    | 19.6 ms                                                                | 19.9 ms: 1.01x slower                                                     |
| nbody                      | 135 ms                                                                 | 137 ms: 1.02x slower                                                      |
| typing_runtime_protocols   | 199 us                                                                 | 202 us: 1.02x slower                                                      |
| html5lib                   | 71.3 ms                                                                | 72.5 ms: 1.02x slower                                                     |
| pyflate                    | 508 ms                                                                 | 518 ms: 1.02x slower                                                      |
| scimark_sparse_mat_mult    | 5.74 ms                                                                | 5.85 ms: 1.02x slower                                                     |
| meteor_contest             | 130 ms                                                                 | 133 ms: 1.02x slower                                                      |
| json                       | 5.04 ms                                                                | 5.22 ms: 1.04x slower                                                     |
| json_loads                 | 29.4 us                                                                | 30.5 us: 1.04x slower                                                     |
| generators                 | 31.1 ms                                                                | 32.8 ms: 1.05x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                              |

Benchmark hidden because not significant (37): async_tree_none, scimark_lu, async_tree_io_tg, async_tree_cpu_io_mixed, logging_simple, telco, sympy_str, async_tree_memoization, bench_mp_pool, asyncio_websockets, deepcopy_memo, k_core, many_optionals, sqlglot_v2_transpile, pylint, sphinx, crypto_pyaes, sqlglot_v2_optimize, python_startup, genshi_xml, pprint_pformat, pycparser, pprint_safe_repr, async_tree_none_tg, bench_thread_pool, sqlglot_v2_normalize, sympy_sum, docutils, sqlalchemy_declarative, deepcopy_reduce, deepcopy, connected_components, dulwich_log, spectral_norm, logging_format, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.002x faster

# HPT report

- Reliability score: 97.75% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.99x