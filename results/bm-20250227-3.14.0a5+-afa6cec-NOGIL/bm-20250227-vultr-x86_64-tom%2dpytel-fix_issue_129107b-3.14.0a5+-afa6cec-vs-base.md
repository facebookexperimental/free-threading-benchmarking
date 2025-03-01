# Results vs. base

- fork: tom-pytel
- ref: fix_issue_129107b
- machine: linux-x86_64
- commit hash: afa6cec
- commit date: 2025-02-27
- overall geometric mean: 1.000x slower
- HPT reliability: 56.50%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250227-vultr-x86_64-python-45a24f54af4a65c14cc1-3.14.0a5+-45a24f5 | bm-20250227-vultr-x86_64-tom%2dpytel-fix_issue_129107b-3.14.0a5+-afa6cec |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 306 ms                                                                 | 305 ms: 1.00x faster                                                     |
| html5lib       | 70.6 ms                                                                | 70.0 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20250227-vultr-x86_64-python-45a24f54af4a65c14cc1-3.14.0a5+-45a24f5 | bm-20250227-vultr-x86_64-tom%2dpytel-fix_issue_129107b-3.14.0a5+-afa6cec |
|-------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg        | 556 ms                                                                 | 548 ms: 1.01x faster                                                     |
| async_tree_cpu_io_mixed | 526 ms                                                                 | 521 ms: 1.01x faster                                                     |
| async_tree_io           | 584 ms                                                                 | 579 ms: 1.01x faster                                                     |
| async_tree_none         | 276 ms                                                                 | 274 ms: 1.01x faster                                                     |
| async_generators        | 377 ms                                                                 | 375 ms: 1.00x faster                                                     |
| asyncio_websockets      | 518 ms                                                                 | 516 ms: 1.00x faster                                                     |
| coroutines              | 23.4 ms                                                                | 23.6 ms: 1.01x slower                                                    |
| Geometric mean          | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (4): async_tree_memoization, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250227-vultr-x86_64-python-45a24f54af4a65c14cc1-3.14.0a5+-45a24f5 | bm-20250227-vultr-x86_64-tom%2dpytel-fix_issue_129107b-3.14.0a5+-afa6cec |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 213 ms                                                                 | 203 ms: 1.05x faster                                                     |
| float          | 77.1 ms                                                                | 76.3 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                             |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250227-vultr-x86_64-python-45a24f54af4a65c14cc1-3.14.0a5+-45a24f5 | bm-20250227-vultr-x86_64-tom%2dpytel-fix_issue_129107b-3.14.0a5+-afa6cec |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 2.76 ms                                                                | 2.77 ms: 1.00x slower                                                    |
| regex_compile  | 155 ms                                                                 | 156 ms: 1.00x slower                                                     |
| regex_v8       | 23.2 ms                                                                | 23.4 ms: 1.01x slower                                                    |
| regex_dna      | 169 ms                                                                 | 172 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20250227-vultr-x86_64-python-45a24f54af4a65c14cc1-3.14.0a5+-45a24f5 | bm-20250227-vultr-x86_64-tom%2dpytel-fix_issue_129107b-3.14.0a5+-afa6cec |
|---------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_loads          | 29.6 us                                                                | 29.1 us: 1.02x faster                                                    |
| xml_etree_iterparse | 88.3 ms                                                                | 87.3 ms: 1.01x faster                                                    |
| xml_etree_parse     | 129 ms                                                                 | 128 ms: 1.01x faster                                                     |
| xml_etree_process   | 69.7 ms                                                                | 69.4 ms: 1.00x faster                                                    |
| xml_etree_generate  | 95.5 ms                                                                | 95.1 ms: 1.00x faster                                                    |
| json_dumps          | 12.8 ms                                                                | 13.1 ms: 1.02x slower                                                    |
| Geometric mean      | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (3): unpickle_pure_python, pickle_pure_python, tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250227-vultr-x86_64-python-45a24f54af4a65c14cc1-3.14.0a5+-45a24f5 | bm-20250227-vultr-x86_64-tom%2dpytel-fix_issue_129107b-3.14.0a5+-afa6cec |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 15.6 ms                                                                | 15.6 ms: 1.00x faster                                                    |
| python_startup_no_site | 9.68 ms                                                                | 9.66 ms: 1.00x faster                                                    |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250227-vultr-x86_64-python-45a24f54af4a65c14cc1-3.14.0a5+-45a24f5 | bm-20250227-vultr-x86_64-tom%2dpytel-fix_issue_129107b-3.14.0a5+-afa6cec |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 15.8 ms                                                                | 15.9 ms: 1.01x slower                                                    |
| genshi_xml      | 59.6 ms                                                                | 60.4 ms: 1.01x slower                                                    |
| django_template | 42.3 ms                                                                | 43.0 ms: 1.02x slower                                                    |
| genshi_text     | 27.9 ms                                                                | 28.4 ms: 1.02x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.01x slower                                                             |

All benchmarks:
===============

| Benchmark               | bm-20250227-vultr-x86_64-python-45a24f54af4a65c14cc1-3.14.0a5+-45a24f5 | bm-20250227-vultr-x86_64-tom%2dpytel-fix_issue_129107b-3.14.0a5+-afa6cec |
|-------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits                | 213 ms                                                                 | 203 ms: 1.05x faster                                                     |
| logging_silent          | 114 ns                                                                 | 111 ns: 1.03x faster                                                     |
| crypto_pyaes            | 89.3 ms                                                                | 87.8 ms: 1.02x faster                                                    |
| json_loads              | 29.6 us                                                                | 29.1 us: 1.02x faster                                                    |
| async_tree_io_tg        | 556 ms                                                                 | 548 ms: 1.01x faster                                                     |
| spectral_norm           | 112 ms                                                                 | 111 ms: 1.01x faster                                                     |
| xml_etree_iterparse     | 88.3 ms                                                                | 87.3 ms: 1.01x faster                                                    |
| sqlglot_parse           | 1.60 ms                                                                | 1.58 ms: 1.01x faster                                                    |
| float                   | 77.1 ms                                                                | 76.3 ms: 1.01x faster                                                    |
| async_tree_cpu_io_mixed | 526 ms                                                                 | 521 ms: 1.01x faster                                                     |
| pathlib                 | 19.8 ms                                                                | 19.6 ms: 1.01x faster                                                    |
| hexiom                  | 7.50 ms                                                                | 7.43 ms: 1.01x faster                                                    |
| async_tree_io           | 584 ms                                                                 | 579 ms: 1.01x faster                                                     |
| async_tree_none         | 276 ms                                                                 | 274 ms: 1.01x faster                                                     |
| html5lib                | 70.6 ms                                                                | 70.0 ms: 1.01x faster                                                    |
| richards                | 55.0 ms                                                                | 54.5 ms: 1.01x faster                                                    |
| dulwich_log             | 83.2 ms                                                                | 82.5 ms: 1.01x faster                                                    |
| telco                   | 8.84 ms                                                                | 8.77 ms: 1.01x faster                                                    |
| xml_etree_parse         | 129 ms                                                                 | 128 ms: 1.01x faster                                                     |
| json                    | 5.11 ms                                                                | 5.07 ms: 1.01x faster                                                    |
| bpe_tokeniser           | 4.79 sec                                                               | 4.76 sec: 1.01x faster                                                   |
| xml_etree_process       | 69.7 ms                                                                | 69.4 ms: 1.00x faster                                                    |
| async_generators        | 377 ms                                                                 | 375 ms: 1.00x faster                                                     |
| python_startup          | 15.6 ms                                                                | 15.6 ms: 1.00x faster                                                    |
| xml_etree_generate      | 95.5 ms                                                                | 95.1 ms: 1.00x faster                                                    |
| asyncio_websockets      | 518 ms                                                                 | 516 ms: 1.00x faster                                                     |
| go                      | 140 ms                                                                 | 140 ms: 1.00x faster                                                     |
| 2to3                    | 306 ms                                                                 | 305 ms: 1.00x faster                                                     |
| python_startup_no_site  | 9.68 ms                                                                | 9.66 ms: 1.00x faster                                                    |
| regex_effbot            | 2.76 ms                                                                | 2.77 ms: 1.00x slower                                                    |
| gc_traversal            | 1.71 ms                                                                | 1.72 ms: 1.00x slower                                                    |
| scimark_sor             | 135 ms                                                                 | 136 ms: 1.00x slower                                                     |
| sympy_integrate         | 23.9 ms                                                                | 23.9 ms: 1.00x slower                                                    |
| many_optionals          | 1.16 ms                                                                | 1.17 ms: 1.00x slower                                                    |
| regex_compile           | 155 ms                                                                 | 156 ms: 1.00x slower                                                     |
| regex_v8                | 23.2 ms                                                                | 23.4 ms: 1.01x slower                                                    |
| subparsers              | 25.0 ms                                                                | 25.2 ms: 1.01x slower                                                    |
| raytrace                | 322 ms                                                                 | 324 ms: 1.01x slower                                                     |
| pycparser               | 1.19 sec                                                               | 1.19 sec: 1.01x slower                                                   |
| deltablue               | 3.82 ms                                                                | 3.84 ms: 1.01x slower                                                    |
| sympy_sum               | 186 ms                                                                 | 187 ms: 1.01x slower                                                     |
| scimark_sparse_mat_mult | 5.77 ms                                                                | 5.81 ms: 1.01x slower                                                    |
| coroutines              | 23.4 ms                                                                | 23.6 ms: 1.01x slower                                                    |
| scimark_fft             | 392 ms                                                                 | 395 ms: 1.01x slower                                                     |
| pprint_safe_repr        | 835 ms                                                                 | 842 ms: 1.01x slower                                                     |
| mako                    | 15.8 ms                                                                | 15.9 ms: 1.01x slower                                                    |
| deepcopy                | 307 us                                                                 | 310 us: 1.01x slower                                                     |
| sqlite_synth            | 2.02 us                                                                | 2.04 us: 1.01x slower                                                    |
| genshi_xml              | 59.6 ms                                                                | 60.4 ms: 1.01x slower                                                    |
| deepcopy_reduce         | 3.15 us                                                                | 3.19 us: 1.01x slower                                                    |
| chaos                   | 69.6 ms                                                                | 70.6 ms: 1.01x slower                                                    |
| coverage                | 95.7 ms                                                                | 97.0 ms: 1.01x slower                                                    |
| sympy_expand            | 546 ms                                                                 | 553 ms: 1.01x slower                                                     |
| django_template         | 42.3 ms                                                                | 43.0 ms: 1.02x slower                                                    |
| genshi_text             | 27.9 ms                                                                | 28.4 ms: 1.02x slower                                                    |
| meteor_contest          | 127 ms                                                                 | 130 ms: 1.02x slower                                                     |
| richards_super          | 64.0 ms                                                                | 65.2 ms: 1.02x slower                                                    |
| scimark_monte_carlo     | 83.0 ms                                                                | 84.6 ms: 1.02x slower                                                    |
| nqueens                 | 97.0 ms                                                                | 98.9 ms: 1.02x slower                                                    |
| json_dumps              | 12.8 ms                                                                | 13.1 ms: 1.02x slower                                                    |
| regex_dna               | 169 ms                                                                 | 172 ms: 1.02x slower                                                     |
| scimark_lu              | 140 ms                                                                 | 144 ms: 1.02x slower                                                     |
| Geometric mean          | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (34): sqlglot_transpile, sqlalchemy_imperative, connected_components, sqlglot_optimize, async_tree_memoization, async_tree_cpu_io_mixed_tg, sphinx, unpickle_pure_python, logging_format, sqlglot_normalize, docutils, async_tree_memoization_tg, async_tree_none_tg, mdp, pylint, deepcopy_memo, shortest_path, bench_mp_pool, comprehensions, pickle_pure_python, nbody, sqlalchemy_declarative, pprint_pformat, fannkuch, k_core, tomli_loads, pyflate, create_gc_cycles, generators, bench_thread_pool, thrift, sympy_str, logging_simple, typing_runtime_protocols

- Geometric mean (including insignificant results): 1.000x slower

# HPT report

- Reliability score: 56.50% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x