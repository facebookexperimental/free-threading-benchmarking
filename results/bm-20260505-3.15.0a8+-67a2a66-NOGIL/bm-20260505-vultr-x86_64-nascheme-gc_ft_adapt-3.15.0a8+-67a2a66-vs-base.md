# Results vs. base

- fork: nascheme
- ref: gc_ft_adapt
- machine: linux-x86_64
- commit hash: 67a2a66
- commit date: 2026-05-05
- overall geometric mean: 1.004x slower
- HPT reliability: 93.61%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20260505-vultr-x86_64-python-24aa562062fced910e8b-3.15.0a8+-24aa562 | bm-20260505-vultr-x86_64-nascheme-gc_ft_adapt-3.15.0a8+-67a2a66 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------:|
| docutils       | 2.66 sec                                                               | 2.95 sec: 1.11x slower                                          |
| html5lib       | 66.8 ms                                                                | 70.1 ms: 1.05x slower                                           |
| sphinx         | 1.07 sec                                                               | 1.11 sec: 1.04x slower                                          |
| Geometric mean | (ref)                                                                  | 1.07x slower                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20260505-vultr-x86_64-python-24aa562062fced910e8b-3.15.0a8+-24aa562 | bm-20260505-vultr-x86_64-nascheme-gc_ft_adapt-3.15.0a8+-67a2a66 |
|-------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------:|
| async_generators        | 436 ms                                                                 | 394 ms: 1.11x faster                                            |
| async_tree_io_tg        | 633 ms                                                                 | 601 ms: 1.05x faster                                            |
| async_tree_io           | 649 ms                                                                 | 630 ms: 1.03x faster                                            |
| coroutines              | 25.2 ms                                                                | 24.7 ms: 1.02x faster                                           |
| asyncio_websockets      | 512 ms                                                                 | 510 ms: 1.00x faster                                            |
| async_tree_memoization  | 359 ms                                                                 | 368 ms: 1.03x slower                                            |
| async_tree_cpu_io_mixed | 543 ms                                                                 | 557 ms: 1.03x slower                                            |
| async_tree_none_tg      | 266 ms                                                                 | 275 ms: 1.03x slower                                            |
| Geometric mean          | (ref)                                                                  | 1.01x faster                                                    |

Benchmark hidden because not significant (3): async_tree_memoization_tg, async_tree_none, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20260505-vultr-x86_64-python-24aa562062fced910e8b-3.15.0a8+-24aa562 | bm-20260505-vultr-x86_64-nascheme-gc_ft_adapt-3.15.0a8+-67a2a66 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------:|
| pidigits       | 190 ms                                                                 | 188 ms: 1.01x faster                                            |
| float          | 74.9 ms                                                                | 78.7 ms: 1.05x slower                                           |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                    |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20260505-vultr-x86_64-python-24aa562062fced910e8b-3.15.0a8+-24aa562 | bm-20260505-vultr-x86_64-nascheme-gc_ft_adapt-3.15.0a8+-67a2a66 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------:|
| regex_dna      | 186 ms                                                                 | 176 ms: 1.06x faster                                            |
| regex_v8       | 21.4 ms                                                                | 20.4 ms: 1.05x faster                                           |
| regex_effbot   | 3.02 ms                                                                | 3.09 ms: 1.02x slower                                           |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                    |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20260505-vultr-x86_64-python-24aa562062fced910e8b-3.15.0a8+-24aa562 | bm-20260505-vultr-x86_64-nascheme-gc_ft_adapt-3.15.0a8+-67a2a66 |
|---------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------:|
| xml_etree_process   | 72.0 ms                                                                | 70.2 ms: 1.03x faster                                           |
| xml_etree_generate  | 101 ms                                                                 | 99.2 ms: 1.02x faster                                           |
| xml_etree_parse     | 138 ms                                                                 | 136 ms: 1.01x faster                                            |
| json_loads          | 30.9 us                                                                | 31.0 us: 1.00x slower                                           |
| json_dumps          | 10.8 ms                                                                | 10.9 ms: 1.01x slower                                           |
| xml_etree_iterparse | 90.5 ms                                                                | 91.7 ms: 1.01x slower                                           |
| tomli_loads         | 1.94 sec                                                               | 1.98 sec: 1.02x slower                                          |
| Geometric mean      | (ref)                                                                  | 1.00x faster                                                    |

Benchmark hidden because not significant (2): unpickle_pure_python, pickle_pure_python

Benchmarks with tag 'template':
===============================

Benchmark hidden because not significant (2): django_template, mako

All benchmarks:
===============

| Benchmark               | bm-20260505-vultr-x86_64-python-24aa562062fced910e8b-3.15.0a8+-24aa562 | bm-20260505-vultr-x86_64-nascheme-gc_ft_adapt-3.15.0a8+-67a2a66 |
|-------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------:|
| async_generators        | 436 ms                                                                 | 394 ms: 1.11x faster                                            |
| regex_dna               | 186 ms                                                                 | 176 ms: 1.06x faster                                            |
| async_tree_io_tg        | 633 ms                                                                 | 601 ms: 1.05x faster                                            |
| create_gc_cycles        | 1.56 ms                                                                | 1.48 ms: 1.05x faster                                           |
| regex_v8                | 21.4 ms                                                                | 20.4 ms: 1.05x faster                                           |
| async_tree_io           | 649 ms                                                                 | 630 ms: 1.03x faster                                            |
| gc_traversal            | 1.95 ms                                                                | 1.89 ms: 1.03x faster                                           |
| xml_etree_process       | 72.0 ms                                                                | 70.2 ms: 1.03x faster                                           |
| xml_etree_generate      | 101 ms                                                                 | 99.2 ms: 1.02x faster                                           |
| coroutines              | 25.2 ms                                                                | 24.7 ms: 1.02x faster                                           |
| deepcopy_memo           | 32.1 us                                                                | 31.6 us: 1.01x faster                                           |
| sqlglot_v2_optimize     | 58.7 ms                                                                | 57.9 ms: 1.01x faster                                           |
| thrift                  | 919 us                                                                 | 906 us: 1.01x faster                                            |
| sympy_expand            | 537 ms                                                                 | 530 ms: 1.01x faster                                            |
| xml_etree_parse         | 138 ms                                                                 | 136 ms: 1.01x faster                                            |
| k_core                  | 2.29 sec                                                               | 2.27 sec: 1.01x faster                                          |
| deepcopy                | 273 us                                                                 | 270 us: 1.01x faster                                            |
| pidigits                | 190 ms                                                                 | 188 ms: 1.01x faster                                            |
| sympy_str               | 319 ms                                                                 | 316 ms: 1.01x faster                                            |
| generators              | 32.9 ms                                                                | 32.6 ms: 1.01x faster                                           |
| telco                   | 176 ms                                                                 | 175 ms: 1.01x faster                                            |
| deepcopy_reduce         | 3.01 us                                                                | 3.00 us: 1.01x faster                                           |
| asyncio_websockets      | 512 ms                                                                 | 510 ms: 1.00x faster                                            |
| sympy_integrate         | 22.0 ms                                                                | 22.0 ms: 1.00x faster                                           |
| hexiom                  | 6.61 ms                                                                | 6.62 ms: 1.00x slower                                           |
| json_loads              | 30.9 us                                                                | 31.0 us: 1.00x slower                                           |
| go                      | 121 ms                                                                 | 121 ms: 1.00x slower                                            |
| logging_silent          | 105 ns                                                                 | 105 ns: 1.00x slower                                            |
| fannkuch                | 462 ms                                                                 | 464 ms: 1.00x slower                                            |
| bench_mp_pool           | 6.95 ms                                                                | 6.99 ms: 1.00x slower                                           |
| nqueens                 | 88.9 ms                                                                | 89.4 ms: 1.01x slower                                           |
| richards_super          | 58.5 ms                                                                | 58.8 ms: 1.01x slower                                           |
| meteor_contest          | 125 ms                                                                 | 125 ms: 1.01x slower                                            |
| bpe_tokeniser           | 4.39 sec                                                               | 4.42 sec: 1.01x slower                                          |
| pyflate                 | 461 ms                                                                 | 464 ms: 1.01x slower                                            |
| chaos                   | 62.9 ms                                                                | 63.4 ms: 1.01x slower                                           |
| json_dumps              | 10.8 ms                                                                | 10.9 ms: 1.01x slower                                           |
| scimark_sor             | 122 ms                                                                 | 123 ms: 1.01x slower                                            |
| pycparser               | 1.13 sec                                                               | 1.14 sec: 1.01x slower                                          |
| connected_components    | 487 ms                                                                 | 492 ms: 1.01x slower                                            |
| logging_simple          | 6.91 us                                                                | 6.98 us: 1.01x slower                                           |
| dulwich_log             | 71.4 ms                                                                | 72.3 ms: 1.01x slower                                           |
| subparsers              | 10.4 ms                                                                | 10.6 ms: 1.01x slower                                           |
| xml_etree_iterparse     | 90.5 ms                                                                | 91.7 ms: 1.01x slower                                           |
| raytrace                | 303 ms                                                                 | 307 ms: 1.01x slower                                            |
| comprehensions          | 17.8 us                                                                | 18.1 us: 1.02x slower                                           |
| scimark_lu              | 129 ms                                                                 | 131 ms: 1.02x slower                                            |
| regex_effbot            | 3.02 ms                                                                | 3.09 ms: 1.02x slower                                           |
| tomli_loads             | 1.94 sec                                                               | 1.98 sec: 1.02x slower                                          |
| logging_format          | 7.78 us                                                                | 7.94 us: 1.02x slower                                           |
| many_optionals          | 1.02 ms                                                                | 1.04 ms: 1.02x slower                                           |
| coverage                | 114 ms                                                                 | 117 ms: 1.02x slower                                            |
| async_tree_memoization  | 359 ms                                                                 | 368 ms: 1.03x slower                                            |
| async_tree_cpu_io_mixed | 543 ms                                                                 | 557 ms: 1.03x slower                                            |
| scimark_monte_carlo     | 78.9 ms                                                                | 81.0 ms: 1.03x slower                                           |
| spectral_norm           | 112 ms                                                                 | 115 ms: 1.03x slower                                            |
| async_tree_none_tg      | 266 ms                                                                 | 275 ms: 1.03x slower                                            |
| sqlglot_v2_parse        | 1.38 ms                                                                | 1.43 ms: 1.04x slower                                           |
| scimark_fft             | 346 ms                                                                 | 360 ms: 1.04x slower                                            |
| sphinx                  | 1.07 sec                                                               | 1.11 sec: 1.04x slower                                          |
| sqlglot_v2_transpile    | 1.68 ms                                                                | 1.75 ms: 1.04x slower                                           |
| html5lib                | 66.8 ms                                                                | 70.1 ms: 1.05x slower                                           |
| float                   | 74.9 ms                                                                | 78.7 ms: 1.05x slower                                           |
| deltablue               | 3.53 ms                                                                | 3.74 ms: 1.06x slower                                           |
| scimark_sparse_mat_mult | 5.40 ms                                                                | 5.77 ms: 1.07x slower                                           |
| docutils                | 2.66 sec                                                               | 2.95 sec: 1.11x slower                                          |
| Geometric mean          | (ref)                                                                  | 1.00x slower                                                    |

Benchmark hidden because not significant (23): async_tree_memoization_tg, sqlite_synth, async_tree_none, regex_compile, json, pprint_pformat, mdp, shortest_path, sqlglot_v2_normalize, crypto_pyaes, unpickle_pure_python, sympy_sum, django_template, pathlib, pprint_safe_repr, mako, pickle_pure_python, async_tree_cpu_io_mixed_tg, richards, bench_thread_pool, nbody, typing_runtime_protocols, pylint

- Geometric mean (including insignificant results): 1.004x slower

# HPT report

- Reliability score: 93.61% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.98x