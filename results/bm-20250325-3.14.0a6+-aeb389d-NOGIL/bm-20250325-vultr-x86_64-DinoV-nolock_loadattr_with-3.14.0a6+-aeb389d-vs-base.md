# Results vs. base

- fork: DinoV
- ref: nolock_loadattr_with
- machine: linux-x86_64
- commit hash: aeb389d
- commit date: 2025-03-25
- overall geometric mean: 1.003x faster
- HPT reliability: 58.02%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250325-vultr-x86_64-python-a26a301f8b09c1825b28-3.14.0a6+-a26a301 | bm-20250325-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a6+-aeb389d |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 299 ms                                                                 | 298 ms: 1.00x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (3): docutils, html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20250325-vultr-x86_64-python-a26a301f8b09c1825b28-3.14.0a6+-a26a301 | bm-20250325-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a6+-aeb389d |
|---------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| coroutines                | 24.4 ms                                                                | 23.4 ms: 1.04x faster                                                 |
| async_generators          | 385 ms                                                                 | 387 ms: 1.00x slower                                                  |
| async_tree_memoization_tg | 300 ms                                                                 | 302 ms: 1.01x slower                                                  |
| async_tree_io             | 584 ms                                                                 | 588 ms: 1.01x slower                                                  |
| async_tree_io_tg          | 552 ms                                                                 | 557 ms: 1.01x slower                                                  |
| async_tree_cpu_io_mixed   | 518 ms                                                                 | 524 ms: 1.01x slower                                                  |
| async_tree_memoization    | 334 ms                                                                 | 337 ms: 1.01x slower                                                  |
| Geometric mean            | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (4): async_tree_none_tg, async_tree_none, asyncio_websockets, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250325-vultr-x86_64-python-a26a301f8b09c1825b28-3.14.0a6+-a26a301 | bm-20250325-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a6+-aeb389d |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 141 ms                                                                 | 132 ms: 1.06x faster                                                  |
| float          | 78.3 ms                                                                | 76.5 ms: 1.02x faster                                                 |
| pidigits       | 198 ms                                                                 | 208 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250325-vultr-x86_64-python-a26a301f8b09c1825b28-3.14.0a6+-a26a301 | bm-20250325-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a6+-aeb389d |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 182 ms                                                                 | 180 ms: 1.01x faster                                                  |
| regex_effbot   | 2.67 ms                                                                | 2.64 ms: 1.01x faster                                                 |
| regex_v8       | 21.8 ms                                                                | 21.6 ms: 1.01x faster                                                 |
| regex_compile  | 158 ms                                                                 | 158 ms: 1.00x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250325-vultr-x86_64-python-a26a301f8b09c1825b28-3.14.0a6+-a26a301 | bm-20250325-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a6+-aeb389d |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.39 sec                                                               | 2.35 sec: 1.02x faster                                                |
| unpickle_pure_python | 256 us                                                                 | 252 us: 1.01x faster                                                  |
| json_loads           | 29.5 us                                                                | 29.4 us: 1.01x faster                                                 |
| xml_etree_process    | 70.7 ms                                                                | 71.1 ms: 1.01x slower                                                 |
| xml_etree_iterparse  | 87.6 ms                                                                | 88.4 ms: 1.01x slower                                                 |
| pickle_pure_python   | 360 us                                                                 | 364 us: 1.01x slower                                                  |
| json_dumps           | 12.7 ms                                                                | 13.0 ms: 1.03x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (2): xml_etree_parse, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250325-vultr-x86_64-python-a26a301f8b09c1825b28-3.14.0a6+-a26a301 | bm-20250325-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a6+-aeb389d |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 11.1 ms                                                                | 11.1 ms: 1.00x slower                                                 |
| python_startup         | 15.7 ms                                                                | 15.8 ms: 1.00x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250325-vultr-x86_64-python-a26a301f8b09c1825b28-3.14.0a6+-a26a301 | bm-20250325-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a6+-aeb389d |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 43.3 ms                                                                | 42.4 ms: 1.02x faster                                                 |
| mako            | 16.1 ms                                                                | 15.8 ms: 1.02x faster                                                 |
| genshi_text     | 28.6 ms                                                                | 28.3 ms: 1.01x faster                                                 |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                 | bm-20250325-vultr-x86_64-python-a26a301f8b09c1825b28-3.14.0a6+-a26a301 | bm-20250325-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a6+-aeb389d |
|---------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody                     | 141 ms                                                                 | 132 ms: 1.06x faster                                                  |
| coroutines                | 24.4 ms                                                                | 23.4 ms: 1.04x faster                                                 |
| richards_super            | 65.1 ms                                                                | 63.4 ms: 1.03x faster                                                 |
| float                     | 78.3 ms                                                                | 76.5 ms: 1.02x faster                                                 |
| scimark_sor               | 139 ms                                                                 | 136 ms: 1.02x faster                                                  |
| django_template           | 43.3 ms                                                                | 42.4 ms: 1.02x faster                                                 |
| create_gc_cycles          | 1.38 ms                                                                | 1.35 ms: 1.02x faster                                                 |
| nqueens                   | 99.6 ms                                                                | 97.6 ms: 1.02x faster                                                 |
| richards                  | 55.8 ms                                                                | 54.7 ms: 1.02x faster                                                 |
| comprehensions            | 21.1 us                                                                | 20.7 us: 1.02x faster                                                 |
| chaos                     | 69.6 ms                                                                | 68.4 ms: 1.02x faster                                                 |
| scimark_monte_carlo       | 84.8 ms                                                                | 83.4 ms: 1.02x faster                                                 |
| mako                      | 16.1 ms                                                                | 15.8 ms: 1.02x faster                                                 |
| tomli_loads               | 2.39 sec                                                               | 2.35 sec: 1.02x faster                                                |
| crypto_pyaes              | 89.2 ms                                                                | 87.9 ms: 1.02x faster                                                 |
| unpickle_pure_python      | 256 us                                                                 | 252 us: 1.01x faster                                                  |
| deepcopy_memo             | 39.9 us                                                                | 39.3 us: 1.01x faster                                                 |
| go                        | 146 ms                                                                 | 144 ms: 1.01x faster                                                  |
| deltablue                 | 3.92 ms                                                                | 3.86 ms: 1.01x faster                                                 |
| regex_dna                 | 182 ms                                                                 | 180 ms: 1.01x faster                                                  |
| scimark_fft               | 401 ms                                                                 | 397 ms: 1.01x faster                                                  |
| logging_silent            | 114 ns                                                                 | 112 ns: 1.01x faster                                                  |
| regex_effbot              | 2.67 ms                                                                | 2.64 ms: 1.01x faster                                                 |
| pprint_pformat            | 1.74 sec                                                               | 1.73 sec: 1.01x faster                                                |
| raytrace                  | 325 ms                                                                 | 322 ms: 1.01x faster                                                  |
| regex_v8                  | 21.8 ms                                                                | 21.6 ms: 1.01x faster                                                 |
| gc_traversal              | 1.81 ms                                                                | 1.80 ms: 1.01x faster                                                 |
| fannkuch                  | 501 ms                                                                 | 497 ms: 1.01x faster                                                  |
| genshi_text               | 28.6 ms                                                                | 28.3 ms: 1.01x faster                                                 |
| spectral_norm             | 113 ms                                                                 | 112 ms: 1.01x faster                                                  |
| json_loads                | 29.5 us                                                                | 29.4 us: 1.01x faster                                                 |
| pprint_safe_repr          | 843 ms                                                                 | 838 ms: 1.01x faster                                                  |
| hexiom                    | 7.67 ms                                                                | 7.63 ms: 1.01x faster                                                 |
| sqlglot_v2_parse          | 1.61 ms                                                                | 1.60 ms: 1.00x faster                                                 |
| deepcopy_reduce           | 3.20 us                                                                | 3.19 us: 1.00x faster                                                 |
| deepcopy                  | 314 us                                                                 | 313 us: 1.00x faster                                                  |
| bench_thread_pool         | 3.17 ms                                                                | 3.16 ms: 1.00x faster                                                 |
| 2to3                      | 299 ms                                                                 | 298 ms: 1.00x faster                                                  |
| python_startup_no_site    | 11.1 ms                                                                | 11.1 ms: 1.00x slower                                                 |
| python_startup            | 15.7 ms                                                                | 15.8 ms: 1.00x slower                                                 |
| bpe_tokeniser             | 4.86 sec                                                               | 4.88 sec: 1.00x slower                                                |
| k_core                    | 2.30 sec                                                               | 2.31 sec: 1.00x slower                                                |
| regex_compile             | 158 ms                                                                 | 158 ms: 1.00x slower                                                  |
| scimark_lu                | 142 ms                                                                 | 143 ms: 1.00x slower                                                  |
| async_generators          | 385 ms                                                                 | 387 ms: 1.00x slower                                                  |
| bench_mp_pool             | 96.9 ms                                                                | 97.4 ms: 1.01x slower                                                 |
| xml_etree_process         | 70.7 ms                                                                | 71.1 ms: 1.01x slower                                                 |
| many_optionals            | 1.17 ms                                                                | 1.18 ms: 1.01x slower                                                 |
| sympy_str                 | 335 ms                                                                 | 338 ms: 1.01x slower                                                  |
| async_tree_memoization_tg | 300 ms                                                                 | 302 ms: 1.01x slower                                                  |
| sqlglot_v2_optimize       | 61.0 ms                                                                | 61.5 ms: 1.01x slower                                                 |
| async_tree_io             | 584 ms                                                                 | 588 ms: 1.01x slower                                                  |
| xml_etree_iterparse       | 87.6 ms                                                                | 88.4 ms: 1.01x slower                                                 |
| async_tree_io_tg          | 552 ms                                                                 | 557 ms: 1.01x slower                                                  |
| thrift                    | 868 us                                                                 | 876 us: 1.01x slower                                                  |
| meteor_contest            | 129 ms                                                                 | 130 ms: 1.01x slower                                                  |
| pickle_pure_python        | 360 us                                                                 | 364 us: 1.01x slower                                                  |
| async_tree_cpu_io_mixed   | 518 ms                                                                 | 524 ms: 1.01x slower                                                  |
| pathlib                   | 19.8 ms                                                                | 20.1 ms: 1.01x slower                                                 |
| async_tree_memoization    | 334 ms                                                                 | 337 ms: 1.01x slower                                                  |
| logging_simple            | 7.25 us                                                                | 7.34 us: 1.01x slower                                                 |
| sqlglot_v2_normalize      | 120 ms                                                                 | 122 ms: 1.01x slower                                                  |
| typing_runtime_protocols  | 200 us                                                                 | 203 us: 1.02x slower                                                  |
| logging_format            | 8.24 us                                                                | 8.41 us: 1.02x slower                                                 |
| json_dumps                | 12.7 ms                                                                | 13.0 ms: 1.03x slower                                                 |
| pidigits                  | 198 ms                                                                 | 208 ms: 1.05x slower                                                  |
| Geometric mean            | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (30): async_tree_none_tg, genshi_xml, sqlglot_v2_transpile, xml_etree_parse, docutils, sqlalchemy_declarative, pylint, sympy_integrate, pycparser, dulwich_log, sphinx, generators, async_tree_none, connected_components, json, pyflate, mdp, shortest_path, asyncio_websockets, sympy_sum, sympy_expand, xml_etree_generate, scimark_sparse_mat_mult, coverage, async_tree_cpu_io_mixed_tg, html5lib, telco, sqlite_synth, subparsers, sqlalchemy_imperative

- Geometric mean (including insignificant results): 1.003x faster

# HPT report

- Reliability score: 58.02% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x