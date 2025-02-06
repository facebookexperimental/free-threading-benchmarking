# Results vs. base

- fork: wrongnull
- ref: ft_new_reference_dat
- machine: linux-x86_64
- commit hash: d7cb09f
- commit date: 2025-02-05
- overall geometric mean: 1.001x faster
- HPT reliability: 88.78%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250203-vultr-x86_64-python-75b628adebd4594529da-3.14.0a4+-75b628a | bm-20250205-vultr-x86_64-wrongnull-ft_new_reference_dat-3.14.0a4+-d7cb09f |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| html5lib       | 71.9 ms                                                                | 71.0 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                              |

Benchmark hidden because not significant (3): 2to3, docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20250203-vultr-x86_64-python-75b628adebd4594529da-3.14.0a4+-75b628a | bm-20250205-vultr-x86_64-wrongnull-ft_new_reference_dat-3.14.0a4+-d7cb09f |
|-------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed | 538 ms                                                                 | 535 ms: 1.01x faster                                                      |
| async_generators        | 375 ms                                                                 | 379 ms: 1.01x slower                                                      |
| Geometric mean          | (ref)                                                                  | 1.00x faster                                                              |

Benchmark hidden because not significant (9): async_tree_memoization_tg, async_tree_cpu_io_mixed_tg, async_tree_none, async_tree_io_tg, async_tree_io, async_tree_memoization, async_tree_none_tg, coroutines, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250203-vultr-x86_64-python-75b628adebd4594529da-3.14.0a4+-75b628a | bm-20250205-vultr-x86_64-wrongnull-ft_new_reference_dat-3.14.0a4+-d7cb09f |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits       | 196 ms                                                                 | 191 ms: 1.02x faster                                                      |
| float          | 77.5 ms                                                                | 75.9 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                              |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250203-vultr-x86_64-python-75b628adebd4594529da-3.14.0a4+-75b628a | bm-20250205-vultr-x86_64-wrongnull-ft_new_reference_dat-3.14.0a4+-d7cb09f |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_v8       | 23.6 ms                                                                | 23.2 ms: 1.02x faster                                                     |
| regex_dna      | 184 ms                                                                 | 182 ms: 1.01x faster                                                      |
| regex_compile  | 151 ms                                                                 | 150 ms: 1.00x faster                                                      |
| regex_effbot   | 2.76 ms                                                                | 2.84 ms: 1.03x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250203-vultr-x86_64-python-75b628adebd4594529da-3.14.0a4+-75b628a | bm-20250205-vultr-x86_64-wrongnull-ft_new_reference_dat-3.14.0a4+-d7cb09f |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| xml_etree_parse      | 128 ms                                                                 | 127 ms: 1.01x faster                                                      |
| unpickle_pure_python | 246 us                                                                 | 245 us: 1.00x faster                                                      |
| xml_etree_process    | 67.8 ms                                                                | 68.0 ms: 1.00x slower                                                     |
| json_loads           | 31.0 us                                                                | 31.1 us: 1.00x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                              |

Benchmark hidden because not significant (5): json_dumps, pickle_pure_python, xml_etree_iterparse, xml_etree_generate, tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250203-vultr-x86_64-python-75b628adebd4594529da-3.14.0a4+-75b628a | bm-20250205-vultr-x86_64-wrongnull-ft_new_reference_dat-3.14.0a4+-d7cb09f |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 9.62 ms                                                                | 9.65 ms: 1.00x slower                                                     |
| python_startup         | 15.3 ms                                                                | 15.4 ms: 1.00x slower                                                     |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20250203-vultr-x86_64-python-75b628adebd4594529da-3.14.0a4+-75b628a | bm-20250205-vultr-x86_64-wrongnull-ft_new_reference_dat-3.14.0a4+-d7cb09f |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| genshi_xml     | 59.4 ms                                                                | 58.0 ms: 1.02x faster                                                     |
| genshi_text    | 27.5 ms                                                                | 27.3 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                              |

Benchmark hidden because not significant (2): django_template, mako

All benchmarks:
===============

| Benchmark               | bm-20250203-vultr-x86_64-python-75b628adebd4594529da-3.14.0a4+-75b628a | bm-20250205-vultr-x86_64-wrongnull-ft_new_reference_dat-3.14.0a4+-d7cb09f |
|-------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| mdp                     | 2.68 sec                                                               | 2.57 sec: 1.04x faster                                                    |
| pidigits                | 196 ms                                                                 | 191 ms: 1.02x faster                                                      |
| logging_simple          | 7.32 us                                                                | 7.15 us: 1.02x faster                                                     |
| genshi_xml              | 59.4 ms                                                                | 58.0 ms: 1.02x faster                                                     |
| float                   | 77.5 ms                                                                | 75.9 ms: 1.02x faster                                                     |
| regex_v8                | 23.6 ms                                                                | 23.2 ms: 1.02x faster                                                     |
| sqlalchemy_imperative   | 24.4 ms                                                                | 24.0 ms: 1.01x faster                                                     |
| thrift                  | 906 us                                                                 | 893 us: 1.01x faster                                                      |
| spectral_norm           | 112 ms                                                                 | 111 ms: 1.01x faster                                                      |
| html5lib                | 71.9 ms                                                                | 71.0 ms: 1.01x faster                                                     |
| sqlglot_parse           | 1.59 ms                                                                | 1.57 ms: 1.01x faster                                                     |
| logging_format          | 8.31 us                                                                | 8.21 us: 1.01x faster                                                     |
| many_optionals          | 1.19 ms                                                                | 1.17 ms: 1.01x faster                                                     |
| regex_dna               | 184 ms                                                                 | 182 ms: 1.01x faster                                                      |
| hexiom                  | 7.46 ms                                                                | 7.39 ms: 1.01x faster                                                     |
| xml_etree_parse         | 128 ms                                                                 | 127 ms: 1.01x faster                                                      |
| subparsers              | 25.5 ms                                                                | 25.3 ms: 1.01x faster                                                     |
| dulwich_log             | 82.6 ms                                                                | 82.0 ms: 1.01x faster                                                     |
| async_tree_cpu_io_mixed | 538 ms                                                                 | 535 ms: 1.01x faster                                                      |
| genshi_text             | 27.5 ms                                                                | 27.3 ms: 1.01x faster                                                     |
| scimark_fft             | 387 ms                                                                 | 384 ms: 1.01x faster                                                      |
| pprint_safe_repr        | 798 ms                                                                 | 794 ms: 1.01x faster                                                      |
| pycparser               | 1.18 sec                                                               | 1.17 sec: 1.00x faster                                                    |
| unpickle_pure_python    | 246 us                                                                 | 245 us: 1.00x faster                                                      |
| bench_thread_pool       | 3.31 ms                                                                | 3.30 ms: 1.00x faster                                                     |
| bpe_tokeniser           | 4.63 sec                                                               | 4.62 sec: 1.00x faster                                                    |
| regex_compile           | 151 ms                                                                 | 150 ms: 1.00x faster                                                      |
| python_startup_no_site  | 9.62 ms                                                                | 9.65 ms: 1.00x slower                                                     |
| xml_etree_process       | 67.8 ms                                                                | 68.0 ms: 1.00x slower                                                     |
| json_loads              | 31.0 us                                                                | 31.1 us: 1.00x slower                                                     |
| sqlalchemy_declarative  | 156 ms                                                                 | 156 ms: 1.00x slower                                                      |
| python_startup          | 15.3 ms                                                                | 15.4 ms: 1.00x slower                                                     |
| sympy_integrate         | 23.9 ms                                                                | 24.0 ms: 1.00x slower                                                     |
| coverage                | 96.6 ms                                                                | 97.0 ms: 1.00x slower                                                     |
| sqlglot_normalize       | 118 ms                                                                 | 119 ms: 1.01x slower                                                      |
| sympy_sum               | 184 ms                                                                 | 185 ms: 1.01x slower                                                      |
| go                      | 138 ms                                                                 | 139 ms: 1.01x slower                                                      |
| scimark_monte_carlo     | 81.5 ms                                                                | 82.1 ms: 1.01x slower                                                     |
| deltablue               | 4.63 ms                                                                | 4.67 ms: 1.01x slower                                                     |
| deepcopy                | 304 us                                                                 | 307 us: 1.01x slower                                                      |
| comprehensions          | 19.6 us                                                                | 19.8 us: 1.01x slower                                                     |
| logging_silent          | 110 ns                                                                 | 111 ns: 1.01x slower                                                      |
| gc_traversal            | 1.65 ms                                                                | 1.67 ms: 1.01x slower                                                     |
| fannkuch                | 486 ms                                                                 | 491 ms: 1.01x slower                                                      |
| crypto_pyaes            | 88.6 ms                                                                | 89.6 ms: 1.01x slower                                                     |
| async_generators        | 375 ms                                                                 | 379 ms: 1.01x slower                                                      |
| create_gc_cycles        | 1.38 ms                                                                | 1.40 ms: 1.02x slower                                                     |
| deepcopy_memo           | 37.3 us                                                                | 37.9 us: 1.02x slower                                                     |
| richards_super          | 64.4 ms                                                                | 65.7 ms: 1.02x slower                                                     |
| richards                | 55.5 ms                                                                | 56.5 ms: 1.02x slower                                                     |
| pyflate                 | 490 ms                                                                 | 504 ms: 1.03x slower                                                      |
| regex_effbot            | 2.76 ms                                                                | 2.84 ms: 1.03x slower                                                     |
| Geometric mean          | (ref)                                                                  | 1.00x faster                                                              |

Benchmark hidden because not significant (44): sqlglot_transpile, json_dumps, docutils, async_tree_memoization_tg, shortest_path, async_tree_cpu_io_mixed_tg, async_tree_none, async_tree_io_tg, async_tree_io, meteor_contest, sphinx, scimark_sparse_mat_mult, django_template, pickle_pure_python, xml_etree_iterparse, async_tree_memoization, mako, scimark_sor, nqueens, pathlib, deepcopy_reduce, generators, raytrace, pprint_pformat, sqlite_synth, xml_etree_generate, chaos, nbody, connected_components, json, k_core, async_tree_none_tg, 2to3, pylint, coroutines, sympy_str, tomli_loads, asyncio_websockets, scimark_lu, typing_runtime_protocols, sympy_expand, sqlglot_optimize, bench_mp_pool, telco

- Geometric mean (including insignificant results): 1.001x faster

# HPT report

- Reliability score: 88.78% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x