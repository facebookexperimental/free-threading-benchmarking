# Results vs. base

- fork: nascheme
- ref: gh_129201_gc_mark_pr
- machine: linux-x86_64
- commit hash: 1b4e8c3
- commit date: 2025-01-22
- overall geometric mean: 1.009x slower
- HPT reliability: 91.45%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250117-vultr-x86_64-python-3829104ab412a47bf3f3-3.14.0a4+-3829104 | bm-20250122-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-1b4e8c3 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 306 ms                                                                 | 307 ms: 1.00x slower                                                     |
| html5lib       | 69.2 ms                                                                | 71.3 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                             |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250117-vultr-x86_64-python-3829104ab412a47bf3f3-3.14.0a4+-3829104 | bm-20250122-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-1b4e8c3 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_none_tg         | 244 ms                                                                 | 240 ms: 1.01x faster                                                     |
| async_tree_io              | 615 ms                                                                 | 608 ms: 1.01x faster                                                     |
| async_generators           | 374 ms                                                                 | 370 ms: 1.01x faster                                                     |
| async_tree_memoization     | 354 ms                                                                 | 350 ms: 1.01x faster                                                     |
| coroutines                 | 23.7 ms                                                                | 24.7 ms: 1.04x slower                                                    |
| async_tree_cpu_io_mixed    | 536 ms                                                                 | 621 ms: 1.16x slower                                                     |
| async_tree_cpu_io_mixed_tg | 499 ms                                                                 | 583 ms: 1.17x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.03x slower                                                             |

Benchmark hidden because not significant (4): async_tree_none, async_tree_memoization_tg, async_tree_io_tg, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250117-vultr-x86_64-python-3829104ab412a47bf3f3-3.14.0a4+-3829104 | bm-20250122-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-1b4e8c3 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 77.8 ms                                                                | 75.3 ms: 1.03x faster                                                    |
| nbody          | 132 ms                                                                 | 135 ms: 1.02x slower                                                     |
| pidigits       | 215 ms                                                                 | 221 ms: 1.03x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250117-vultr-x86_64-python-3829104ab412a47bf3f3-3.14.0a4+-3829104 | bm-20250122-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-1b4e8c3 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 151 ms                                                                 | 150 ms: 1.01x faster                                                     |
| regex_v8       | 24.2 ms                                                                | 24.1 ms: 1.00x faster                                                    |
| regex_dna      | 182 ms                                                                 | 186 ms: 1.03x slower                                                     |
| regex_effbot   | 2.85 ms                                                                | 2.95 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250117-vultr-x86_64-python-3829104ab412a47bf3f3-3.14.0a4+-3829104 | bm-20250122-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-1b4e8c3 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| unpickle_pure_python | 254 us                                                                 | 248 us: 1.02x faster                                                     |
| pickle_pure_python   | 380 us                                                                 | 373 us: 1.02x faster                                                     |
| tomli_loads          | 2.33 sec                                                               | 2.31 sec: 1.01x faster                                                   |
| json_loads           | 30.4 us                                                                | 30.5 us: 1.00x slower                                                    |
| json_dumps           | 12.9 ms                                                                | 13.0 ms: 1.00x slower                                                    |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250117-vultr-x86_64-python-3829104ab412a47bf3f3-3.14.0a4+-3829104 | bm-20250122-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-1b4e8c3 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 15.2 ms                                                                | 15.5 ms: 1.02x slower                                                    |
| python_startup_no_site | 9.57 ms                                                                | 9.78 ms: 1.02x slower                                                    |
| Geometric mean         | (ref)                                                                  | 1.02x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250117-vultr-x86_64-python-3829104ab412a47bf3f3-3.14.0a4+-3829104 | bm-20250122-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-1b4e8c3 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| django_template | 44.1 ms                                                                | 43.2 ms: 1.02x faster                                                    |
| genshi_text     | 28.4 ms                                                                | 28.1 ms: 1.01x faster                                                    |
| genshi_xml      | 60.6 ms                                                                | 60.0 ms: 1.01x faster                                                    |
| mako            | 15.9 ms                                                                | 15.8 ms: 1.01x faster                                                    |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20250117-vultr-x86_64-python-3829104ab412a47bf3f3-3.14.0a4+-3829104 | bm-20250122-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-1b4e8c3 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| deepcopy_reduce            | 3.38 us                                                                | 3.25 us: 1.04x faster                                                    |
| sqlglot_parse              | 1.62 ms                                                                | 1.57 ms: 1.03x faster                                                    |
| deepcopy_memo              | 39.0 us                                                                | 37.7 us: 1.03x faster                                                    |
| float                      | 77.8 ms                                                                | 75.3 ms: 1.03x faster                                                    |
| logging_silent             | 118 ns                                                                 | 114 ns: 1.03x faster                                                     |
| deepcopy                   | 319 us                                                                 | 312 us: 1.02x faster                                                     |
| chaos                      | 70.1 ms                                                                | 68.6 ms: 1.02x faster                                                    |
| unpickle_pure_python       | 254 us                                                                 | 248 us: 1.02x faster                                                     |
| mdp                        | 2.77 sec                                                               | 2.72 sec: 1.02x faster                                                   |
| django_template            | 44.1 ms                                                                | 43.2 ms: 1.02x faster                                                    |
| pickle_pure_python         | 380 us                                                                 | 373 us: 1.02x faster                                                     |
| sqlglot_transpile          | 1.95 ms                                                                | 1.91 ms: 1.02x faster                                                    |
| thrift                     | 933 us                                                                 | 916 us: 1.02x faster                                                     |
| pycparser                  | 1.20 sec                                                               | 1.18 sec: 1.02x faster                                                   |
| richards                   | 56.6 ms                                                                | 55.7 ms: 1.02x faster                                                    |
| logging_format             | 8.43 us                                                                | 8.30 us: 1.02x faster                                                    |
| scimark_lu                 | 137 ms                                                                 | 135 ms: 1.02x faster                                                     |
| nqueens                    | 97.4 ms                                                                | 95.9 ms: 1.02x faster                                                    |
| logging_simple             | 7.33 us                                                                | 7.22 us: 1.02x faster                                                    |
| scimark_fft                | 387 ms                                                                 | 382 ms: 1.01x faster                                                     |
| async_tree_none_tg         | 244 ms                                                                 | 240 ms: 1.01x faster                                                     |
| async_tree_io              | 615 ms                                                                 | 608 ms: 1.01x faster                                                     |
| regex_compile              | 151 ms                                                                 | 150 ms: 1.01x faster                                                     |
| genshi_text                | 28.4 ms                                                                | 28.1 ms: 1.01x faster                                                    |
| genshi_xml                 | 60.6 ms                                                                | 60.0 ms: 1.01x faster                                                    |
| async_generators           | 374 ms                                                                 | 370 ms: 1.01x faster                                                     |
| typing_runtime_protocols   | 204 us                                                                 | 202 us: 1.01x faster                                                     |
| sqlite_synth               | 2.06 us                                                                | 2.04 us: 1.01x faster                                                    |
| async_tree_memoization     | 354 ms                                                                 | 350 ms: 1.01x faster                                                     |
| sqlglot_optimize           | 62.2 ms                                                                | 61.7 ms: 1.01x faster                                                    |
| pyflate                    | 498 ms                                                                 | 494 ms: 1.01x faster                                                     |
| pprint_safe_repr           | 832 ms                                                                 | 825 ms: 1.01x faster                                                     |
| tomli_loads                | 2.33 sec                                                               | 2.31 sec: 1.01x faster                                                   |
| pathlib                    | 18.9 ms                                                                | 18.8 ms: 1.01x faster                                                    |
| sqlglot_normalize          | 122 ms                                                                 | 121 ms: 1.01x faster                                                     |
| bpe_tokeniser              | 4.72 sec                                                               | 4.69 sec: 1.01x faster                                                   |
| go                         | 140 ms                                                                 | 139 ms: 1.01x faster                                                     |
| scimark_sparse_mat_mult    | 5.43 ms                                                                | 5.40 ms: 1.01x faster                                                    |
| scimark_monte_carlo        | 82.3 ms                                                                | 81.8 ms: 1.01x faster                                                    |
| mako                       | 15.9 ms                                                                | 15.8 ms: 1.01x faster                                                    |
| k_core                     | 2.32 sec                                                               | 2.31 sec: 1.00x faster                                                   |
| pprint_pformat             | 1.71 sec                                                               | 1.70 sec: 1.00x faster                                                   |
| regex_v8                   | 24.2 ms                                                                | 24.1 ms: 1.00x faster                                                    |
| raytrace                   | 331 ms                                                                 | 331 ms: 1.00x faster                                                     |
| json_loads                 | 30.4 us                                                                | 30.5 us: 1.00x slower                                                    |
| sqlalchemy_declarative     | 163 ms                                                                 | 163 ms: 1.00x slower                                                     |
| json_dumps                 | 12.9 ms                                                                | 13.0 ms: 1.00x slower                                                    |
| 2to3                       | 306 ms                                                                 | 307 ms: 1.00x slower                                                     |
| bench_thread_pool          | 3.30 ms                                                                | 3.32 ms: 1.00x slower                                                    |
| sympy_str                  | 334 ms                                                                 | 336 ms: 1.01x slower                                                     |
| sympy_sum                  | 186 ms                                                                 | 188 ms: 1.01x slower                                                     |
| crypto_pyaes               | 87.2 ms                                                                | 88.1 ms: 1.01x slower                                                    |
| bench_mp_pool              | 94.3 ms                                                                | 95.2 ms: 1.01x slower                                                    |
| telco                      | 8.54 ms                                                                | 8.63 ms: 1.01x slower                                                    |
| spectral_norm              | 106 ms                                                                 | 108 ms: 1.01x slower                                                     |
| hexiom                     | 7.31 ms                                                                | 7.43 ms: 1.02x slower                                                    |
| python_startup             | 15.2 ms                                                                | 15.5 ms: 1.02x slower                                                    |
| python_startup_no_site     | 9.57 ms                                                                | 9.78 ms: 1.02x slower                                                    |
| nbody                      | 132 ms                                                                 | 135 ms: 1.02x slower                                                     |
| regex_dna                  | 182 ms                                                                 | 186 ms: 1.03x slower                                                     |
| pidigits                   | 215 ms                                                                 | 221 ms: 1.03x slower                                                     |
| html5lib                   | 69.2 ms                                                                | 71.3 ms: 1.03x slower                                                    |
| regex_effbot               | 2.85 ms                                                                | 2.95 ms: 1.04x slower                                                    |
| coroutines                 | 23.7 ms                                                                | 24.7 ms: 1.04x slower                                                    |
| async_tree_cpu_io_mixed    | 536 ms                                                                 | 621 ms: 1.16x slower                                                     |
| async_tree_cpu_io_mixed_tg | 499 ms                                                                 | 583 ms: 1.17x slower                                                     |
| create_gc_cycles           | 1.33 ms                                                                | 1.71 ms: 1.28x slower                                                    |
| gc_traversal               | 3.24 ms                                                                | 5.43 ms: 1.68x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                             |

Benchmark hidden because not significant (24): sqlalchemy_imperative, generators, async_tree_none, scimark_sor, async_tree_memoization_tg, many_optionals, async_tree_io_tg, deltablue, coverage, fannkuch, sympy_integrate, comprehensions, dulwich_log, docutils, subparsers, richards_super, asyncio_websockets, sphinx, pylint, json, shortest_path, sympy_expand, connected_components, meteor_contest
Ignored benchmarks (4) of results/bm-20250117-3.14.0a4+-3829104-NOGIL/bm-20250117-vultr-x86_64-python-3829104ab412a47bf3f3-3.14.0a4+-3829104.json: xml_etree_generate, xml_etree_iterparse, xml_etree_parse, xml_etree_process

- Geometric mean (including insignificant results): 1.009x slower

# HPT report

- Reliability score: 91.45% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x