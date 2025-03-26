# Results vs. base

- fork: colesbury
- ref: gh_131586_lookup_spe
- machine: linux-x86_64
- commit hash: 4c6bf78
- commit date: 2025-03-25
- overall geometric mean: 1.001x faster
- HPT reliability: 93.80%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250321-vultr-x86_64-python-b92ee14b80cc8898f799-3.14.0a6+-b92ee14 | bm-20250325-vultr-x86_64-colesbury-gh_131586_lookup_spe-3.14.0a6+-4c6bf78 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 278 ms                                                                 | 277 ms: 1.01x faster                                                      |
| docutils       | 2.64 sec                                                               | 2.65 sec: 1.01x slower                                                    |
| html5lib       | 65.5 ms                                                                | 63.1 ms: 1.04x faster                                                     |
| sphinx         | 1.04 sec                                                               | 1.03 sec: 1.01x faster                                                    |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20250321-vultr-x86_64-python-b92ee14b80cc8898f799-3.14.0a6+-b92ee14 | bm-20250325-vultr-x86_64-colesbury-gh_131586_lookup_spe-3.14.0a6+-4c6bf78 |
|------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| coroutines       | 20.0 ms                                                                | 19.3 ms: 1.04x faster                                                     |
| async_generators | 333 ms                                                                 | 331 ms: 1.00x faster                                                      |
| Geometric mean   | (ref)                                                                  | 1.00x faster                                                              |

Benchmark hidden because not significant (9): async_tree_memoization, async_tree_io_tg, async_tree_cpu_io_mixed, asyncio_websockets, async_tree_memoization_tg, async_tree_none, async_tree_io, async_tree_cpu_io_mixed_tg, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250321-vultr-x86_64-python-b92ee14b80cc8898f799-3.14.0a6+-b92ee14 | bm-20250325-vultr-x86_64-colesbury-gh_131586_lookup_spe-3.14.0a6+-4c6bf78 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| float          | 68.2 ms                                                                | 68.5 ms: 1.00x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                              |

Benchmark hidden because not significant (2): pidigits, nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250321-vultr-x86_64-python-b92ee14b80cc8898f799-3.14.0a6+-b92ee14 | bm-20250325-vultr-x86_64-colesbury-gh_131586_lookup_spe-3.14.0a6+-4c6bf78 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_v8       | 21.8 ms                                                                | 20.5 ms: 1.06x faster                                                     |
| regex_dna      | 189 ms                                                                 | 184 ms: 1.03x faster                                                      |
| regex_effbot   | 3.08 ms                                                                | 3.01 ms: 1.02x faster                                                     |
| regex_compile  | 140 ms                                                                 | 139 ms: 1.01x faster                                                      |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250321-vultr-x86_64-python-b92ee14b80cc8898f799-3.14.0a6+-b92ee14 | bm-20250325-vultr-x86_64-colesbury-gh_131586_lookup_spe-3.14.0a6+-4c6bf78 |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| unpickle_pure_python | 229 us                                                                 | 227 us: 1.01x faster                                                      |
| tomli_loads          | 2.09 sec                                                               | 2.07 sec: 1.01x faster                                                    |
| xml_etree_parse      | 145 ms                                                                 | 144 ms: 1.01x faster                                                      |
| xml_etree_process    | 61.0 ms                                                                | 61.4 ms: 1.01x slower                                                     |
| xml_etree_iterparse  | 86.3 ms                                                                | 87.2 ms: 1.01x slower                                                     |
| pickle_pure_python   | 324 us                                                                 | 328 us: 1.01x slower                                                      |
| json_dumps           | 12.7 ms                                                                | 12.9 ms: 1.02x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                              |

Benchmark hidden because not significant (2): json_loads, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250321-vultr-x86_64-python-b92ee14b80cc8898f799-3.14.0a6+-b92ee14 | bm-20250325-vultr-x86_64-colesbury-gh_131586_lookup_spe-3.14.0a6+-4c6bf78 |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 10.9 ms                                                                | 11.0 ms: 1.00x slower                                                     |
| python_startup         | 15.5 ms                                                                | 15.5 ms: 1.00x slower                                                     |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20250321-vultr-x86_64-python-b92ee14b80cc8898f799-3.14.0a6+-b92ee14 | bm-20250325-vultr-x86_64-colesbury-gh_131586_lookup_spe-3.14.0a6+-4c6bf78 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| mako           | 14.9 ms                                                                | 15.0 ms: 1.01x slower                                                     |
| genshi_text    | 24.4 ms                                                                | 24.7 ms: 1.01x slower                                                     |
| genshi_xml     | 51.9 ms                                                                | 53.0 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                              |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                | bm-20250321-vultr-x86_64-python-b92ee14b80cc8898f799-3.14.0a6+-b92ee14 | bm-20250325-vultr-x86_64-colesbury-gh_131586_lookup_spe-3.14.0a6+-4c6bf78 |
|--------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_v8                 | 21.8 ms                                                                | 20.5 ms: 1.06x faster                                                     |
| gc_traversal             | 2.17 ms                                                                | 2.06 ms: 1.06x faster                                                     |
| deltablue                | 3.57 ms                                                                | 3.43 ms: 1.04x faster                                                     |
| html5lib                 | 65.5 ms                                                                | 63.1 ms: 1.04x faster                                                     |
| coroutines               | 20.0 ms                                                                | 19.3 ms: 1.04x faster                                                     |
| regex_dna                | 189 ms                                                                 | 184 ms: 1.03x faster                                                      |
| scimark_sparse_mat_mult  | 4.95 ms                                                                | 4.82 ms: 1.03x faster                                                     |
| meteor_contest           | 125 ms                                                                 | 123 ms: 1.02x faster                                                      |
| regex_effbot             | 3.08 ms                                                                | 3.01 ms: 1.02x faster                                                     |
| scimark_fft              | 336 ms                                                                 | 329 ms: 1.02x faster                                                      |
| shortest_path            | 535 ms                                                                 | 529 ms: 1.01x faster                                                      |
| k_core                   | 2.24 sec                                                               | 2.22 sec: 1.01x faster                                                    |
| pycparser                | 1.16 sec                                                               | 1.15 sec: 1.01x faster                                                    |
| nqueens                  | 85.4 ms                                                                | 84.5 ms: 1.01x faster                                                     |
| create_gc_cycles         | 1.35 ms                                                                | 1.34 ms: 1.01x faster                                                     |
| subparsers               | 24.4 ms                                                                | 24.2 ms: 1.01x faster                                                     |
| unpickle_pure_python     | 229 us                                                                 | 227 us: 1.01x faster                                                      |
| tomli_loads              | 2.09 sec                                                               | 2.07 sec: 1.01x faster                                                    |
| xml_etree_parse          | 145 ms                                                                 | 144 ms: 1.01x faster                                                      |
| sphinx                   | 1.04 sec                                                               | 1.03 sec: 1.01x faster                                                    |
| comprehensions           | 17.6 us                                                                | 17.5 us: 1.01x faster                                                     |
| regex_compile            | 140 ms                                                                 | 139 ms: 1.01x faster                                                      |
| hexiom                   | 6.74 ms                                                                | 6.70 ms: 1.01x faster                                                     |
| many_optionals           | 1.11 ms                                                                | 1.10 ms: 1.01x faster                                                     |
| 2to3                     | 278 ms                                                                 | 277 ms: 1.01x faster                                                      |
| async_generators         | 333 ms                                                                 | 331 ms: 1.00x faster                                                      |
| spectral_norm            | 92.0 ms                                                                | 91.5 ms: 1.00x faster                                                     |
| logging_silent           | 92.3 ns                                                                | 91.9 ns: 1.00x faster                                                     |
| deepcopy_memo            | 34.2 us                                                                | 34.1 us: 1.00x faster                                                     |
| raytrace                 | 286 ms                                                                 | 286 ms: 1.00x slower                                                      |
| python_startup_no_site   | 10.9 ms                                                                | 11.0 ms: 1.00x slower                                                     |
| python_startup           | 15.5 ms                                                                | 15.5 ms: 1.00x slower                                                     |
| bpe_tokeniser            | 4.41 sec                                                               | 4.43 sec: 1.00x slower                                                    |
| sqlglot_v2_parse         | 1.42 ms                                                                | 1.42 ms: 1.00x slower                                                     |
| float                    | 68.2 ms                                                                | 68.5 ms: 1.00x slower                                                     |
| scimark_sor              | 112 ms                                                                 | 112 ms: 1.00x slower                                                      |
| deepcopy                 | 272 us                                                                 | 273 us: 1.01x slower                                                      |
| richards_super           | 56.2 ms                                                                | 56.5 ms: 1.01x slower                                                     |
| xml_etree_process        | 61.0 ms                                                                | 61.4 ms: 1.01x slower                                                     |
| sympy_expand             | 506 ms                                                                 | 509 ms: 1.01x slower                                                      |
| docutils                 | 2.64 sec                                                               | 2.65 sec: 1.01x slower                                                    |
| typing_runtime_protocols | 173 us                                                                 | 174 us: 1.01x slower                                                      |
| mako                     | 14.9 ms                                                                | 15.0 ms: 1.01x slower                                                     |
| pathlib                  | 18.7 ms                                                                | 18.9 ms: 1.01x slower                                                     |
| sqlglot_v2_normalize     | 106 ms                                                                 | 107 ms: 1.01x slower                                                      |
| thrift                   | 824 us                                                                 | 830 us: 1.01x slower                                                      |
| scimark_monte_carlo      | 70.3 ms                                                                | 70.8 ms: 1.01x slower                                                     |
| deepcopy_reduce          | 2.75 us                                                                | 2.78 us: 1.01x slower                                                     |
| fannkuch                 | 434 ms                                                                 | 438 ms: 1.01x slower                                                      |
| xml_etree_iterparse      | 86.3 ms                                                                | 87.2 ms: 1.01x slower                                                     |
| sqlalchemy_declarative   | 149 ms                                                                 | 151 ms: 1.01x slower                                                      |
| pickle_pure_python       | 324 us                                                                 | 328 us: 1.01x slower                                                      |
| scimark_lu               | 115 ms                                                                 | 116 ms: 1.01x slower                                                      |
| sqlite_synth             | 1.96 us                                                                | 1.98 us: 1.01x slower                                                     |
| genshi_text              | 24.4 ms                                                                | 24.7 ms: 1.01x slower                                                     |
| go                       | 124 ms                                                                 | 126 ms: 1.01x slower                                                      |
| generators               | 27.4 ms                                                                | 27.8 ms: 1.01x slower                                                     |
| crypto_pyaes             | 80.4 ms                                                                | 81.6 ms: 1.02x slower                                                     |
| pprint_pformat           | 1.58 sec                                                               | 1.61 sec: 1.02x slower                                                    |
| logging_format           | 7.45 us                                                                | 7.58 us: 1.02x slower                                                     |
| json_dumps               | 12.7 ms                                                                | 12.9 ms: 1.02x slower                                                     |
| richards                 | 47.2 ms                                                                | 48.1 ms: 1.02x slower                                                     |
| pprint_safe_repr         | 769 ms                                                                 | 783 ms: 1.02x slower                                                      |
| genshi_xml               | 51.9 ms                                                                | 53.0 ms: 1.02x slower                                                     |
| logging_simple           | 6.58 us                                                                | 6.76 us: 1.03x slower                                                     |
| pyflate                  | 459 ms                                                                 | 471 ms: 1.03x slower                                                      |
| mdp                      | 2.64 sec                                                               | 2.74 sec: 1.04x slower                                                    |
| Geometric mean           | (ref)                                                                  | 1.00x faster                                                              |

Benchmark hidden because not significant (29): json, connected_components, django_template, sympy_str, async_tree_memoization, async_tree_io_tg, pidigits, async_tree_cpu_io_mixed, asyncio_websockets, dulwich_log, nbody, bench_mp_pool, json_loads, async_tree_memoization_tg, bench_thread_pool, async_tree_none, chaos, async_tree_io, xml_etree_generate, sympy_integrate, async_tree_cpu_io_mixed_tg, sympy_sum, coverage, pylint, telco, sqlglot_v2_optimize, sqlglot_v2_transpile, sqlalchemy_imperative, async_tree_none_tg

- Geometric mean (including insignificant results): 1.001x faster

# HPT report

- Reliability score: 93.80% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x