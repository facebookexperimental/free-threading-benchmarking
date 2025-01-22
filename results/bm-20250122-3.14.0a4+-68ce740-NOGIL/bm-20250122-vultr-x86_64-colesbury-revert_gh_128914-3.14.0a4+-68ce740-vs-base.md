# Results vs. base

- fork: colesbury
- ref: revert_gh_128914
- machine: linux-x86_64
- commit hash: 68ce740
- commit date: 2025-01-22
- overall geometric mean: 1.025x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250122-vultr-x86_64-python-2ed5ee9a50454b3fce87-3.14.0a4+-2ed5ee9 | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 312 ms                                                                 | 305 ms: 1.02x faster                                                  |
| docutils       | 2.86 sec                                                               | 2.82 sec: 1.01x faster                                                |
| html5lib       | 74.8 ms                                                                | 71.2 ms: 1.05x faster                                                 |
| sphinx         | 1.14 sec                                                               | 1.12 sec: 1.01x faster                                                |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20250122-vultr-x86_64-python-2ed5ee9a50454b3fce87-3.14.0a4+-2ed5ee9 | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|---------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| coroutines                | 24.9 ms                                                                | 23.4 ms: 1.06x faster                                                 |
| async_generators          | 381 ms                                                                 | 368 ms: 1.04x faster                                                  |
| async_tree_io             | 618 ms                                                                 | 601 ms: 1.03x faster                                                  |
| async_tree_memoization    | 355 ms                                                                 | 346 ms: 1.02x faster                                                  |
| async_tree_memoization_tg | 318 ms                                                                 | 311 ms: 1.02x faster                                                  |
| async_tree_none_tg        | 246 ms                                                                 | 241 ms: 1.02x faster                                                  |
| async_tree_none           | 288 ms                                                                 | 283 ms: 1.02x faster                                                  |
| asyncio_websockets        | 516 ms                                                                 | 513 ms: 1.01x faster                                                  |
| Geometric mean            | (ref)                                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (3): async_tree_io_tg, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250122-vultr-x86_64-python-2ed5ee9a50454b3fce87-3.14.0a4+-2ed5ee9 | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 220 ms                                                                 | 195 ms: 1.13x faster                                                  |
| float          | 78.1 ms                                                                | 77.1 ms: 1.01x faster                                                 |
| nbody          | 136 ms                                                                 | 136 ms: 1.01x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250122-vultr-x86_64-python-2ed5ee9a50454b3fce87-3.14.0a4+-2ed5ee9 | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 159 ms                                                                 | 152 ms: 1.05x faster                                                  |
| regex_v8       | 24.3 ms                                                                | 23.6 ms: 1.03x faster                                                 |
| regex_effbot   | 2.89 ms                                                                | 2.84 ms: 1.02x faster                                                 |
| regex_dna      | 180 ms                                                                 | 186 ms: 1.03x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250122-vultr-x86_64-python-2ed5ee9a50454b3fce87-3.14.0a4+-2ed5ee9 | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| unpickle_pure_python | 275 us                                                                 | 250 us: 1.10x faster                                                  |
| xml_etree_process    | 75.7 ms                                                                | 69.5 ms: 1.09x faster                                                 |
| pickle_pure_python   | 397 us                                                                 | 373 us: 1.06x faster                                                  |
| tomli_loads          | 2.43 sec                                                               | 2.37 sec: 1.02x faster                                                |
| xml_etree_generate   | 98.9 ms                                                                | 97.2 ms: 1.02x faster                                                 |
| xml_etree_iterparse  | 89.0 ms                                                                | 87.8 ms: 1.01x faster                                                 |
| xml_etree_parse      | 129 ms                                                                 | 128 ms: 1.01x faster                                                  |
| Geometric mean       | (ref)                                                                  | 1.03x faster                                                          |

Benchmark hidden because not significant (2): json_loads, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250122-vultr-x86_64-python-2ed5ee9a50454b3fce87-3.14.0a4+-2ed5ee9 | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 15.3 ms                                                                | 15.2 ms: 1.01x faster                                                 |
| python_startup_no_site | 9.55 ms                                                                | 9.54 ms: 1.00x faster                                                 |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250122-vultr-x86_64-python-2ed5ee9a50454b3fce87-3.14.0a4+-2ed5ee9 | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 29.6 ms                                                                | 27.5 ms: 1.08x faster                                                 |
| genshi_xml      | 63.8 ms                                                                | 59.9 ms: 1.07x faster                                                 |
| django_template | 44.9 ms                                                                | 43.0 ms: 1.04x faster                                                 |
| mako            | 16.2 ms                                                                | 16.0 ms: 1.01x faster                                                 |
| Geometric mean  | (ref)                                                                  | 1.05x faster                                                          |

All benchmarks:
===============

| Benchmark                 | bm-20250122-vultr-x86_64-python-2ed5ee9a50454b3fce87-3.14.0a4+-2ed5ee9 | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|---------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits                  | 220 ms                                                                 | 195 ms: 1.13x faster                                                  |
| unpickle_pure_python      | 275 us                                                                 | 250 us: 1.10x faster                                                  |
| xml_etree_process         | 75.7 ms                                                                | 69.5 ms: 1.09x faster                                                 |
| genshi_text               | 29.6 ms                                                                | 27.5 ms: 1.08x faster                                                 |
| genshi_xml                | 63.8 ms                                                                | 59.9 ms: 1.07x faster                                                 |
| scimark_sor               | 141 ms                                                                 | 132 ms: 1.06x faster                                                  |
| pickle_pure_python        | 397 us                                                                 | 373 us: 1.06x faster                                                  |
| coroutines                | 24.9 ms                                                                | 23.4 ms: 1.06x faster                                                 |
| deepcopy_reduce           | 3.43 us                                                                | 3.23 us: 1.06x faster                                                 |
| deepcopy_memo             | 40.8 us                                                                | 38.4 us: 1.06x faster                                                 |
| logging_format            | 8.88 us                                                                | 8.37 us: 1.06x faster                                                 |
| logging_silent            | 119 ns                                                                 | 113 ns: 1.06x faster                                                  |
| logging_simple            | 7.76 us                                                                | 7.34 us: 1.06x faster                                                 |
| hexiom                    | 7.69 ms                                                                | 7.29 ms: 1.06x faster                                                 |
| generators                | 33.1 ms                                                                | 31.4 ms: 1.06x faster                                                 |
| html5lib                  | 74.8 ms                                                                | 71.2 ms: 1.05x faster                                                 |
| regex_compile             | 159 ms                                                                 | 152 ms: 1.05x faster                                                  |
| deltablue                 | 4.80 ms                                                                | 4.58 ms: 1.05x faster                                                 |
| django_template           | 44.9 ms                                                                | 43.0 ms: 1.04x faster                                                 |
| typing_runtime_protocols  | 210 us                                                                 | 201 us: 1.04x faster                                                  |
| pycparser                 | 1.24 sec                                                               | 1.19 sec: 1.04x faster                                                |
| go                        | 143 ms                                                                 | 138 ms: 1.04x faster                                                  |
| deepcopy                  | 326 us                                                                 | 314 us: 1.04x faster                                                  |
| subparsers                | 26.5 ms                                                                | 25.5 ms: 1.04x faster                                                 |
| async_generators          | 381 ms                                                                 | 368 ms: 1.04x faster                                                  |
| many_optionals            | 1.22 ms                                                                | 1.18 ms: 1.03x faster                                                 |
| scimark_lu                | 141 ms                                                                 | 136 ms: 1.03x faster                                                  |
| comprehensions            | 21.3 us                                                                | 20.6 us: 1.03x faster                                                 |
| raytrace                  | 340 ms                                                                 | 329 ms: 1.03x faster                                                  |
| sympy_expand              | 567 ms                                                                 | 549 ms: 1.03x faster                                                  |
| sympy_str                 | 345 ms                                                                 | 335 ms: 1.03x faster                                                  |
| regex_v8                  | 24.3 ms                                                                | 23.6 ms: 1.03x faster                                                 |
| scimark_sparse_mat_mult   | 5.65 ms                                                                | 5.48 ms: 1.03x faster                                                 |
| sympy_integrate           | 24.9 ms                                                                | 24.2 ms: 1.03x faster                                                 |
| sympy_sum                 | 192 ms                                                                 | 186 ms: 1.03x faster                                                  |
| async_tree_io             | 618 ms                                                                 | 601 ms: 1.03x faster                                                  |
| thrift                    | 923 us                                                                 | 898 us: 1.03x faster                                                  |
| pyflate                   | 509 ms                                                                 | 496 ms: 1.03x faster                                                  |
| dulwich_log               | 84.6 ms                                                                | 82.4 ms: 1.03x faster                                                 |
| sqlglot_normalize         | 124 ms                                                                 | 121 ms: 1.03x faster                                                  |
| pprint_pformat            | 1.76 sec                                                               | 1.72 sec: 1.03x faster                                                |
| richards_super            | 66.5 ms                                                                | 64.8 ms: 1.03x faster                                                 |
| tomli_loads               | 2.43 sec                                                               | 2.37 sec: 1.02x faster                                                |
| 2to3                      | 312 ms                                                                 | 305 ms: 1.02x faster                                                  |
| pprint_safe_repr          | 850 ms                                                                 | 830 ms: 1.02x faster                                                  |
| async_tree_memoization    | 355 ms                                                                 | 346 ms: 1.02x faster                                                  |
| async_tree_memoization_tg | 318 ms                                                                 | 311 ms: 1.02x faster                                                  |
| chaos                     | 70.9 ms                                                                | 69.3 ms: 1.02x faster                                                 |
| sqlglot_optimize          | 62.3 ms                                                                | 61.0 ms: 1.02x faster                                                 |
| sqlglot_parse             | 1.61 ms                                                                | 1.58 ms: 1.02x faster                                                 |
| async_tree_none_tg        | 246 ms                                                                 | 241 ms: 1.02x faster                                                  |
| nqueens                   | 99.1 ms                                                                | 97.1 ms: 1.02x faster                                                 |
| sqlite_synth              | 2.08 us                                                                | 2.04 us: 1.02x faster                                                 |
| scimark_monte_carlo       | 83.6 ms                                                                | 82.0 ms: 1.02x faster                                                 |
| fannkuch                  | 489 ms                                                                 | 481 ms: 1.02x faster                                                  |
| xml_etree_generate        | 98.9 ms                                                                | 97.2 ms: 1.02x faster                                                 |
| bpe_tokeniser             | 4.82 sec                                                               | 4.74 sec: 1.02x faster                                                |
| regex_effbot              | 2.89 ms                                                                | 2.84 ms: 1.02x faster                                                 |
| connected_components      | 498 ms                                                                 | 490 ms: 1.02x faster                                                  |
| telco                     | 8.65 ms                                                                | 8.51 ms: 1.02x faster                                                 |
| async_tree_none           | 288 ms                                                                 | 283 ms: 1.02x faster                                                  |
| sqlglot_transpile         | 1.99 ms                                                                | 1.96 ms: 1.02x faster                                                 |
| bench_mp_pool             | 95.7 ms                                                                | 94.3 ms: 1.01x faster                                                 |
| mako                      | 16.2 ms                                                                | 16.0 ms: 1.01x faster                                                 |
| float                     | 78.1 ms                                                                | 77.1 ms: 1.01x faster                                                 |
| docutils                  | 2.86 sec                                                               | 2.82 sec: 1.01x faster                                                |
| xml_etree_iterparse       | 89.0 ms                                                                | 87.8 ms: 1.01x faster                                                 |
| spectral_norm             | 113 ms                                                                 | 112 ms: 1.01x faster                                                  |
| sphinx                    | 1.14 sec                                                               | 1.12 sec: 1.01x faster                                                |
| xml_etree_parse           | 129 ms                                                                 | 128 ms: 1.01x faster                                                  |
| richards                  | 57.0 ms                                                                | 56.5 ms: 1.01x faster                                                 |
| shortest_path             | 547 ms                                                                 | 542 ms: 1.01x faster                                                  |
| python_startup            | 15.3 ms                                                                | 15.2 ms: 1.01x faster                                                 |
| gc_traversal              | 3.35 ms                                                                | 3.34 ms: 1.01x faster                                                 |
| asyncio_websockets        | 516 ms                                                                 | 513 ms: 1.01x faster                                                  |
| k_core                    | 2.33 sec                                                               | 2.32 sec: 1.00x faster                                                |
| bench_thread_pool         | 3.32 ms                                                                | 3.31 ms: 1.00x faster                                                 |
| python_startup_no_site    | 9.55 ms                                                                | 9.54 ms: 1.00x faster                                                 |
| nbody                     | 136 ms                                                                 | 136 ms: 1.01x slower                                                  |
| sqlalchemy_declarative    | 162 ms                                                                 | 163 ms: 1.01x slower                                                  |
| mdp                       | 2.69 sec                                                               | 2.70 sec: 1.01x slower                                                |
| scimark_fft               | 386 ms                                                                 | 389 ms: 1.01x slower                                                  |
| pathlib                   | 18.7 ms                                                                | 19.0 ms: 1.01x slower                                                 |
| crypto_pyaes              | 87.0 ms                                                                | 89.2 ms: 1.03x slower                                                 |
| regex_dna                 | 180 ms                                                                 | 186 ms: 1.03x slower                                                  |
| Geometric mean            | (ref)                                                                  | 1.03x faster                                                          |

Benchmark hidden because not significant (11): pylint, sqlalchemy_imperative, async_tree_io_tg, meteor_contest, json, json_loads, json_dumps, async_tree_cpu_io_mixed, coverage, create_gc_cycles, async_tree_cpu_io_mixed_tg

- Geometric mean (including insignificant results): 1.025x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 0.99x