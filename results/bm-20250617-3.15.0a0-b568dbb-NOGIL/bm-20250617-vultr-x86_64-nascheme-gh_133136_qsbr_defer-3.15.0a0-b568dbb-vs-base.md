# Results vs. base

- fork: nascheme
- ref: gh_133136_qsbr_defer
- machine: linux-x86_64
- commit hash: b568dbb
- commit date: 2025-06-17
- overall geometric mean: 1.003x faster
- HPT reliability: 99.91%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250617-vultr-x86_64-python-fba5dded6df3c2b19435-3.15.0a0-fba5dde | bm-20250617-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-b568dbb |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 283 ms                                                                | 282 ms: 1.00x faster                                                    |
| html5lib       | 66.2 ms                                                               | 64.9 ms: 1.02x faster                                                   |
| sphinx         | 1.06 sec                                                              | 1.03 sec: 1.02x faster                                                  |
| Geometric mean | (ref)                                                                 | 1.01x faster                                                            |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20250617-vultr-x86_64-python-fba5dded6df3c2b19435-3.15.0a0-fba5dde | bm-20250617-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-b568dbb |
|---------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_memoization    | 316 ms                                                                | 312 ms: 1.01x faster                                                    |
| async_tree_memoization_tg | 288 ms                                                                | 285 ms: 1.01x faster                                                    |
| async_tree_io             | 554 ms                                                                | 551 ms: 1.01x faster                                                    |
| asyncio_websockets        | 515 ms                                                                | 513 ms: 1.00x faster                                                    |
| async_generators          | 370 ms                                                                | 372 ms: 1.01x slower                                                    |
| Geometric mean            | (ref)                                                                 | 1.00x faster                                                            |

Benchmark hidden because not significant (6): async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io_tg, coroutines, async_tree_none, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250617-vultr-x86_64-python-fba5dded6df3c2b19435-3.15.0a0-fba5dde | bm-20250617-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-b568dbb |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| nbody          | 123 ms                                                                | 121 ms: 1.02x faster                                                    |
| float          | 69.5 ms                                                               | 69.2 ms: 1.00x faster                                                   |
| pidigits       | 186 ms                                                                | 211 ms: 1.14x slower                                                    |
| Geometric mean | (ref)                                                                 | 1.04x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250617-vultr-x86_64-python-fba5dded6df3c2b19435-3.15.0a0-fba5dde | bm-20250617-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-b568dbb |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_dna      | 175 ms                                                                | 164 ms: 1.07x faster                                                    |
| regex_compile  | 144 ms                                                                | 142 ms: 1.02x faster                                                    |
| regex_effbot   | 2.69 ms                                                               | 2.65 ms: 1.01x faster                                                   |
| regex_v8       | 20.1 ms                                                               | 20.4 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                                 | 1.02x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250617-vultr-x86_64-python-fba5dded6df3c2b19435-3.15.0a0-fba5dde | bm-20250617-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-b568dbb |
|----------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_loads           | 31.9 us                                                               | 30.8 us: 1.03x faster                                                   |
| xml_etree_parse      | 131 ms                                                                | 129 ms: 1.01x faster                                                    |
| json_dumps           | 12.0 ms                                                               | 12.0 ms: 1.00x faster                                                   |
| unpickle_pure_python | 230 us                                                                | 229 us: 1.00x faster                                                    |
| pickle_pure_python   | 335 us                                                                | 337 us: 1.01x slower                                                    |
| tomli_loads          | 2.13 sec                                                              | 2.15 sec: 1.01x slower                                                  |
| xml_etree_process    | 68.4 ms                                                               | 69.2 ms: 1.01x slower                                                   |
| Geometric mean       | (ref)                                                                 | 1.00x faster                                                            |

Benchmark hidden because not significant (2): xml_etree_iterparse, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250617-vultr-x86_64-python-fba5dded6df3c2b19435-3.15.0a0-fba5dde | bm-20250617-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-b568dbb |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 16.0 ms                                                               | 16.0 ms: 1.00x faster                                                   |
| python_startup_no_site | 9.61 ms                                                               | 9.58 ms: 1.00x faster                                                   |
| Geometric mean         | (ref)                                                                 | 1.00x faster                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250617-vultr-x86_64-python-fba5dded6df3c2b19435-3.15.0a0-fba5dde | bm-20250617-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-b568dbb |
|-----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| django_template | 40.2 ms                                                               | 38.9 ms: 1.03x faster                                                   |
| genshi_text     | 26.6 ms                                                               | 26.7 ms: 1.01x slower                                                   |
| genshi_xml      | 57.4 ms                                                               | 58.1 ms: 1.01x slower                                                   |
| mako            | 15.7 ms                                                               | 16.0 ms: 1.02x slower                                                   |
| Geometric mean  | (ref)                                                                 | 1.00x slower                                                            |

All benchmarks:
===============

| Benchmark                 | bm-20250617-vultr-x86_64-python-fba5dded6df3c2b19435-3.15.0a0-fba5dde | bm-20250617-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-b568dbb |
|---------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_dna                 | 175 ms                                                                | 164 ms: 1.07x faster                                                    |
| pyflate                   | 475 ms                                                                | 459 ms: 1.04x faster                                                    |
| json_loads                | 31.9 us                                                               | 30.8 us: 1.03x faster                                                   |
| django_template           | 40.2 ms                                                               | 38.9 ms: 1.03x faster                                                   |
| meteor_contest            | 124 ms                                                                | 120 ms: 1.03x faster                                                    |
| deltablue                 | 3.60 ms                                                               | 3.49 ms: 1.03x faster                                                   |
| comprehensions            | 17.9 us                                                               | 17.4 us: 1.03x faster                                                   |
| subparsers                | 28.5 ms                                                               | 27.7 ms: 1.03x faster                                                   |
| sphinx                    | 1.06 sec                                                              | 1.03 sec: 1.02x faster                                                  |
| html5lib                  | 66.2 ms                                                               | 64.9 ms: 1.02x faster                                                   |
| scimark_lu                | 129 ms                                                                | 127 ms: 1.02x faster                                                    |
| nbody                     | 123 ms                                                                | 121 ms: 1.02x faster                                                    |
| regex_compile             | 144 ms                                                                | 142 ms: 1.02x faster                                                    |
| xml_etree_parse           | 131 ms                                                                | 129 ms: 1.01x faster                                                    |
| json                      | 5.37 ms                                                               | 5.29 ms: 1.01x faster                                                   |
| regex_effbot              | 2.69 ms                                                               | 2.65 ms: 1.01x faster                                                   |
| async_tree_memoization    | 316 ms                                                                | 312 ms: 1.01x faster                                                    |
| hexiom                    | 6.38 ms                                                               | 6.30 ms: 1.01x faster                                                   |
| go                        | 122 ms                                                                | 120 ms: 1.01x faster                                                    |
| scimark_sparse_mat_mult   | 5.58 ms                                                               | 5.51 ms: 1.01x faster                                                   |
| dulwich_log               | 71.5 ms                                                               | 70.6 ms: 1.01x faster                                                   |
| mdp                       | 1.32 sec                                                              | 1.30 sec: 1.01x faster                                                  |
| sympy_str                 | 315 ms                                                                | 311 ms: 1.01x faster                                                    |
| sympy_expand              | 522 ms                                                                | 517 ms: 1.01x faster                                                    |
| sympy_sum                 | 180 ms                                                                | 178 ms: 1.01x faster                                                    |
| async_tree_memoization_tg | 288 ms                                                                | 285 ms: 1.01x faster                                                    |
| sqlglot_v2_normalize      | 114 ms                                                                | 113 ms: 1.01x faster                                                    |
| thrift                    | 882 us                                                                | 874 us: 1.01x faster                                                    |
| sympy_integrate           | 22.1 ms                                                               | 21.9 ms: 1.01x faster                                                   |
| fannkuch                  | 464 ms                                                                | 461 ms: 1.01x faster                                                    |
| async_tree_io             | 554 ms                                                                | 551 ms: 1.01x faster                                                    |
| scimark_monte_carlo       | 75.8 ms                                                               | 75.4 ms: 1.01x faster                                                   |
| float                     | 69.5 ms                                                               | 69.2 ms: 1.00x faster                                                   |
| raytrace                  | 294 ms                                                                | 292 ms: 1.00x faster                                                    |
| asyncio_websockets        | 515 ms                                                                | 513 ms: 1.00x faster                                                    |
| json_dumps                | 12.0 ms                                                               | 12.0 ms: 1.00x faster                                                   |
| pprint_safe_repr          | 874 ms                                                                | 871 ms: 1.00x faster                                                    |
| unpickle_pure_python      | 230 us                                                                | 229 us: 1.00x faster                                                    |
| python_startup            | 16.0 ms                                                               | 16.0 ms: 1.00x faster                                                   |
| 2to3                      | 283 ms                                                                | 282 ms: 1.00x faster                                                    |
| python_startup_no_site    | 9.61 ms                                                               | 9.58 ms: 1.00x faster                                                   |
| scimark_fft               | 362 ms                                                                | 363 ms: 1.00x slower                                                    |
| nqueens                   | 85.6 ms                                                               | 85.8 ms: 1.00x slower                                                   |
| deepcopy_memo             | 34.4 us                                                               | 34.6 us: 1.01x slower                                                   |
| scimark_sor               | 122 ms                                                                | 123 ms: 1.01x slower                                                    |
| pickle_pure_python        | 335 us                                                                | 337 us: 1.01x slower                                                    |
| bpe_tokeniser             | 4.36 sec                                                              | 4.39 sec: 1.01x slower                                                  |
| genshi_text               | 26.6 ms                                                               | 26.7 ms: 1.01x slower                                                   |
| async_generators          | 370 ms                                                                | 372 ms: 1.01x slower                                                    |
| gc_traversal              | 1.90 ms                                                               | 1.92 ms: 1.01x slower                                                   |
| bench_mp_pool             | 103 ms                                                                | 104 ms: 1.01x slower                                                    |
| tomli_loads               | 2.13 sec                                                              | 2.15 sec: 1.01x slower                                                  |
| deepcopy_reduce           | 2.99 us                                                               | 3.01 us: 1.01x slower                                                   |
| telco                     | 8.43 ms                                                               | 8.51 ms: 1.01x slower                                                   |
| regex_v8                  | 20.1 ms                                                               | 20.4 ms: 1.01x slower                                                   |
| logging_silent            | 526 ns                                                                | 531 ns: 1.01x slower                                                    |
| typing_runtime_protocols  | 188 us                                                                | 190 us: 1.01x slower                                                    |
| deepcopy                  | 285 us                                                                | 288 us: 1.01x slower                                                    |
| xml_etree_process         | 68.4 ms                                                               | 69.2 ms: 1.01x slower                                                   |
| genshi_xml                | 57.4 ms                                                               | 58.1 ms: 1.01x slower                                                   |
| bench_thread_pool         | 3.10 ms                                                               | 3.15 ms: 1.02x slower                                                   |
| create_gc_cycles          | 1.47 ms                                                               | 1.50 ms: 1.02x slower                                                   |
| logging_simple            | 7.54 us                                                               | 7.69 us: 1.02x slower                                                   |
| logging_format            | 8.52 us                                                               | 8.70 us: 1.02x slower                                                   |
| mako                      | 15.7 ms                                                               | 16.0 ms: 1.02x slower                                                   |
| spectral_norm             | 111 ms                                                                | 114 ms: 1.02x slower                                                    |
| pidigits                  | 186 ms                                                                | 211 ms: 1.14x slower                                                    |
| Geometric mean            | (ref)                                                                 | 1.00x faster                                                            |

Benchmark hidden because not significant (27): generators, xml_etree_iterparse, pathlib, pycparser, coverage, many_optionals, sqlglot_v2_transpile, connected_components, richards_super, async_tree_cpu_io_mixed, richards, docutils, async_tree_cpu_io_mixed_tg, crypto_pyaes, chaos, async_tree_io_tg, pprint_pformat, sqlite_synth, k_core, coroutines, async_tree_none, sqlglot_v2_optimize, xml_etree_generate, async_tree_none_tg, pylint, shortest_path, sqlglot_v2_parse

- Geometric mean (including insignificant results): 1.003x faster

# HPT report

- Reliability score: 99.91% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.99x