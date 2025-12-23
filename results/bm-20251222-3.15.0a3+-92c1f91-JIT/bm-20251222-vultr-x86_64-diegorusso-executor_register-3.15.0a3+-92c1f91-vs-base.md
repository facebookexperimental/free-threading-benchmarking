# Results vs. base

- fork: diegorusso
- ref: executor_register
- machine: linux-x86_64
- commit hash: 92c1f91
- commit date: 2025-12-22
- overall geometric mean: 1.000x faster
- HPT reliability: 86.53%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251222-vultr-x86_64-python-ff7f62eb2333ac2a2ce2-3.15.0a3+-ff7f62e | bm-20251222-vultr-x86_64-diegorusso-executor_register-3.15.0a3+-92c1f91 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 248 ms                                                                 | 247 ms: 1.00x faster                                                    |
| docutils       | 2.68 sec                                                               | 2.69 sec: 1.01x slower                                                  |
| html5lib       | 64.2 ms                                                                | 65.6 ms: 1.02x slower                                                   |
| sphinx         | 1.01 sec                                                               | 1.00 sec: 1.01x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20251222-vultr-x86_64-python-ff7f62eb2333ac2a2ce2-3.15.0a3+-ff7f62e | bm-20251222-vultr-x86_64-diegorusso-executor_register-3.15.0a3+-92c1f91 |
|---------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none_tg        | 245 ms                                                                 | 240 ms: 1.02x faster                                                    |
| async_tree_memoization_tg | 309 ms                                                                 | 304 ms: 1.01x faster                                                    |
| async_tree_io_tg          | 592 ms                                                                 | 584 ms: 1.01x faster                                                    |
| async_tree_cpu_io_mixed   | 488 ms                                                                 | 483 ms: 1.01x faster                                                    |
| coroutines                | 24.1 ms                                                                | 23.8 ms: 1.01x faster                                                   |
| asyncio_websockets        | 545 ms                                                                 | 543 ms: 1.00x faster                                                    |
| async_generators          | 359 ms                                                                 | 368 ms: 1.03x slower                                                    |
| Geometric mean            | (ref)                                                                  | 1.01x faster                                                            |

Benchmark hidden because not significant (4): async_tree_memoization, async_tree_io, async_tree_cpu_io_mixed_tg, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251222-vultr-x86_64-python-ff7f62eb2333ac2a2ce2-3.15.0a3+-ff7f62e | bm-20251222-vultr-x86_64-diegorusso-executor_register-3.15.0a3+-92c1f91 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 201 ms                                                                 | 194 ms: 1.03x faster                                                    |
| float          | 60.5 ms                                                                | 59.6 ms: 1.02x faster                                                   |
| nbody          | 73.3 ms                                                                | 75.9 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251222-vultr-x86_64-python-ff7f62eb2333ac2a2ce2-3.15.0a3+-ff7f62e | bm-20251222-vultr-x86_64-diegorusso-executor_register-3.15.0a3+-92c1f91 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_dna      | 173 ms                                                                 | 172 ms: 1.01x faster                                                    |
| regex_compile  | 121 ms                                                                 | 122 ms: 1.00x slower                                                    |
| regex_effbot   | 2.63 ms                                                                | 2.68 ms: 1.02x slower                                                   |
| regex_v8       | 21.2 ms                                                                | 23.6 ms: 1.11x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20251222-vultr-x86_64-python-ff7f62eb2333ac2a2ce2-3.15.0a3+-ff7f62e | bm-20251222-vultr-x86_64-diegorusso-executor_register-3.15.0a3+-92c1f91 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 1.99 sec                                                               | 1.94 sec: 1.02x faster                                                  |
| unpickle_pure_python | 176 us                                                                 | 174 us: 1.01x faster                                                    |
| xml_etree_generate   | 78.0 ms                                                                | 77.2 ms: 1.01x faster                                                   |
| xml_etree_process    | 54.1 ms                                                                | 53.7 ms: 1.01x faster                                                   |
| xml_etree_iterparse  | 83.7 ms                                                                | 83.3 ms: 1.00x faster                                                   |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                            |

Benchmark hidden because not significant (4): json_dumps, pickle_pure_python, json_loads, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251222-vultr-x86_64-python-ff7f62eb2333ac2a2ce2-3.15.0a3+-ff7f62e | bm-20251222-vultr-x86_64-diegorusso-executor_register-3.15.0a3+-92c1f91 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.37 ms                                                                | 7.33 ms: 1.00x faster                                                   |
| python_startup         | 12.6 ms                                                                | 12.5 ms: 1.00x faster                                                   |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20251222-vultr-x86_64-python-ff7f62eb2333ac2a2ce2-3.15.0a3+-ff7f62e | bm-20251222-vultr-x86_64-diegorusso-executor_register-3.15.0a3+-92c1f91 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 10.6 ms                                                                | 10.5 ms: 1.01x faster                                                   |
| genshi_text     | 21.2 ms                                                                | 21.5 ms: 1.01x slower                                                   |
| django_template | 35.0 ms                                                                | 35.6 ms: 1.02x slower                                                   |
| Geometric mean  | (ref)                                                                  | 1.01x slower                                                            |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                 | bm-20251222-vultr-x86_64-python-ff7f62eb2333ac2a2ce2-3.15.0a3+-ff7f62e | bm-20251222-vultr-x86_64-diegorusso-executor_register-3.15.0a3+-92c1f91 |
|---------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| bench_mp_pool             | 244 ms                                                                 | 214 ms: 1.14x faster                                                    |
| gc_traversal              | 4.66 ms                                                                | 4.24 ms: 1.10x faster                                                   |
| pidigits                  | 201 ms                                                                 | 194 ms: 1.03x faster                                                    |
| richards                  | 18.4 ms                                                                | 17.8 ms: 1.03x faster                                                   |
| comprehensions            | 16.2 us                                                                | 15.8 us: 1.03x faster                                                   |
| deepcopy_memo             | 25.6 us                                                                | 24.9 us: 1.03x faster                                                   |
| tomli_loads               | 1.99 sec                                                               | 1.94 sec: 1.02x faster                                                  |
| async_tree_none_tg        | 245 ms                                                                 | 240 ms: 1.02x faster                                                    |
| richards_super            | 22.0 ms                                                                | 21.6 ms: 1.02x faster                                                   |
| chaos                     | 53.2 ms                                                                | 52.2 ms: 1.02x faster                                                   |
| pycparser                 | 1.11 sec                                                               | 1.09 sec: 1.02x faster                                                  |
| float                     | 60.5 ms                                                                | 59.6 ms: 1.02x faster                                                   |
| hexiom                    | 6.06 ms                                                                | 5.97 ms: 1.01x faster                                                   |
| async_tree_memoization_tg | 309 ms                                                                 | 304 ms: 1.01x faster                                                    |
| deepcopy                  | 244 us                                                                 | 240 us: 1.01x faster                                                    |
| unpickle_pure_python      | 176 us                                                                 | 174 us: 1.01x faster                                                    |
| telco                     | 164 ms                                                                 | 161 ms: 1.01x faster                                                    |
| sphinx                    | 1.01 sec                                                               | 1.00 sec: 1.01x faster                                                  |
| async_tree_io_tg          | 592 ms                                                                 | 584 ms: 1.01x faster                                                    |
| async_tree_cpu_io_mixed   | 488 ms                                                                 | 483 ms: 1.01x faster                                                    |
| coroutines                | 24.1 ms                                                                | 23.8 ms: 1.01x faster                                                   |
| xml_etree_generate        | 78.0 ms                                                                | 77.2 ms: 1.01x faster                                                   |
| json                      | 4.95 ms                                                                | 4.91 ms: 1.01x faster                                                   |
| mako                      | 10.6 ms                                                                | 10.5 ms: 1.01x faster                                                   |
| pathlib                   | 17.8 ms                                                                | 17.7 ms: 1.01x faster                                                   |
| xml_etree_process         | 54.1 ms                                                                | 53.7 ms: 1.01x faster                                                   |
| regex_dna                 | 173 ms                                                                 | 172 ms: 1.01x faster                                                    |
| pyflate                   | 365 ms                                                                 | 363 ms: 1.01x faster                                                    |
| xml_etree_iterparse       | 83.7 ms                                                                | 83.3 ms: 1.00x faster                                                   |
| python_startup_no_site    | 7.37 ms                                                                | 7.33 ms: 1.00x faster                                                   |
| fannkuch                  | 354 ms                                                                 | 352 ms: 1.00x faster                                                    |
| logging_silent            | 82.4 ns                                                                | 82.1 ns: 1.00x faster                                                   |
| asyncio_websockets        | 545 ms                                                                 | 543 ms: 1.00x faster                                                    |
| python_startup            | 12.6 ms                                                                | 12.5 ms: 1.00x faster                                                   |
| 2to3                      | 248 ms                                                                 | 247 ms: 1.00x faster                                                    |
| sqlglot_v2_optimize       | 54.1 ms                                                                | 54.3 ms: 1.00x slower                                                   |
| regex_compile             | 121 ms                                                                 | 122 ms: 1.00x slower                                                    |
| sympy_expand              | 507 ms                                                                 | 511 ms: 1.01x slower                                                    |
| docutils                  | 2.68 sec                                                               | 2.69 sec: 1.01x slower                                                  |
| many_optionals            | 991 us                                                                 | 999 us: 1.01x slower                                                    |
| scimark_monte_carlo       | 51.8 ms                                                                | 52.2 ms: 1.01x slower                                                   |
| scimark_lu                | 105 ms                                                                 | 106 ms: 1.01x slower                                                    |
| dulwich_log               | 71.5 ms                                                                | 72.2 ms: 1.01x slower                                                   |
| connected_components      | 374 ms                                                                 | 378 ms: 1.01x slower                                                    |
| genshi_text               | 21.2 ms                                                                | 21.5 ms: 1.01x slower                                                   |
| scimark_fft               | 258 ms                                                                 | 261 ms: 1.01x slower                                                    |
| logging_simple            | 5.93 us                                                                | 6.02 us: 1.01x slower                                                   |
| nqueens                   | 84.4 ms                                                                | 85.6 ms: 1.01x slower                                                   |
| django_template           | 35.0 ms                                                                | 35.6 ms: 1.02x slower                                                   |
| regex_effbot              | 2.63 ms                                                                | 2.68 ms: 1.02x slower                                                   |
| logging_format            | 6.63 us                                                                | 6.77 us: 1.02x slower                                                   |
| html5lib                  | 64.2 ms                                                                | 65.6 ms: 1.02x slower                                                   |
| k_core                    | 1.83 sec                                                               | 1.87 sec: 1.02x slower                                                  |
| spectral_norm             | 85.6 ms                                                                | 87.6 ms: 1.02x slower                                                   |
| coverage                  | 81.2 ms                                                                | 83.2 ms: 1.02x slower                                                   |
| async_generators          | 359 ms                                                                 | 368 ms: 1.03x slower                                                    |
| scimark_sparse_mat_mult   | 4.38 ms                                                                | 4.50 ms: 1.03x slower                                                   |
| deepcopy_reduce           | 2.50 us                                                                | 2.57 us: 1.03x slower                                                   |
| scimark_sor               | 99.6 ms                                                                | 103 ms: 1.03x slower                                                    |
| nbody                     | 73.3 ms                                                                | 75.9 ms: 1.04x slower                                                   |
| regex_v8                  | 21.2 ms                                                                | 23.6 ms: 1.11x slower                                                   |
| Geometric mean            | (ref)                                                                  | 1.00x faster                                                            |

Benchmark hidden because not significant (33): async_tree_memoization, async_tree_io, async_tree_cpu_io_mixed_tg, async_tree_none, sympy_str, json_dumps, sympy_integrate, sqlite_synth, mdp, generators, crypto_pyaes, subparsers, pickle_pure_python, sqlglot_v2_transpile, go, thrift, shortest_path, pprint_safe_repr, pylint, json_loads, sqlglot_v2_normalize, xml_etree_parse, meteor_contest, bpe_tokeniser, sqlglot_v2_parse, sympy_sum, deltablue, typing_runtime_protocols, pprint_pformat, bench_thread_pool, genshi_xml, create_gc_cycles, raytrace

- Geometric mean (including insignificant results): 1.000x faster

# HPT report

- Reliability score: 86.53% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x