# Results vs. base

- fork: mpage
- ref: gh_115999_tlbc_call_
- machine: linux-x86_64
- commit hash: c0d3c19
- commit date: 2024-12-04
- overall geometric mean: 1.010x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 372 ms                                                                 | 367 ms: 1.01x faster                                                  |
| docutils       | 3.13 sec                                                               | 3.10 sec: 1.01x faster                                                |
| html5lib       | 101 ms                                                                 | 98.6 ms: 1.03x faster                                                 |
| sphinx         | 1.20 sec                                                               | 1.19 sec: 1.01x faster                                                |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark              | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| coroutines             | 25.5 ms                                                                | 25.1 ms: 1.02x faster                                                 |
| async_tree_memoization | 476 ms                                                                 | 472 ms: 1.01x faster                                                  |
| async_generators       | 452 ms                                                                 | 459 ms: 1.02x slower                                                  |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (8): async_tree_cpu_io_mixed, asyncio_websockets, async_tree_memoization_tg, async_tree_io_tg, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_none, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 134 ms                                                                 | 127 ms: 1.05x faster                                                  |
| float          | 140 ms                                                                 | 138 ms: 1.01x faster                                                  |
| pidigits       | 184 ms                                                                 | 181 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 181 ms                                                                 | 179 ms: 1.01x faster                                                  |
| regex_dna      | 191 ms                                                                 | 188 ms: 1.01x faster                                                  |
| regex_effbot   | 2.89 ms                                                                | 2.91 ms: 1.01x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|---------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_pure_python  | 527 us                                                                 | 506 us: 1.04x faster                                                  |
| xml_etree_generate  | 98.5 ms                                                                | 97.3 ms: 1.01x faster                                                 |
| xml_etree_iterparse | 91.9 ms                                                                | 91.1 ms: 1.01x faster                                                 |
| json_loads          | 28.6 us                                                                | 28.4 us: 1.01x faster                                                 |
| xml_etree_process   | 77.9 ms                                                                | 77.3 ms: 1.01x faster                                                 |
| json_dumps          | 14.3 ms                                                                | 14.3 ms: 1.00x slower                                                 |
| xml_etree_parse     | 131 ms                                                                 | 132 ms: 1.01x slower                                                  |
| Geometric mean      | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (2): unpickle_pure_python, tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 17.6 ms                                                                | 17.4 ms: 1.01x faster                                                 |
| python_startup_no_site | 10.3 ms                                                                | 10.3 ms: 1.01x faster                                                 |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 65.0 ms                                                                | 63.8 ms: 1.02x faster                                                 |
| django_template | 52.3 ms                                                                | 51.6 ms: 1.01x faster                                                 |
| genshi_text     | 31.8 ms                                                                | 32.0 ms: 1.01x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|--------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal             | 3.53 ms                                                                | 3.19 ms: 1.11x faster                                                 |
| nbody                    | 134 ms                                                                 | 127 ms: 1.05x faster                                                  |
| pickle_pure_python       | 527 us                                                                 | 506 us: 1.04x faster                                                  |
| deepcopy_reduce          | 3.61 us                                                                | 3.48 us: 1.04x faster                                                 |
| deepcopy                 | 339 us                                                                 | 327 us: 1.04x faster                                                  |
| telco                    | 8.94 ms                                                                | 8.64 ms: 1.03x faster                                                 |
| logging_format           | 12.2 us                                                                | 11.8 us: 1.03x faster                                                 |
| create_gc_cycles         | 1.87 ms                                                                | 1.81 ms: 1.03x faster                                                 |
| html5lib                 | 101 ms                                                                 | 98.6 ms: 1.03x faster                                                 |
| pprint_pformat           | 2.05 sec                                                               | 2.00 sec: 1.03x faster                                                |
| coverage                 | 103 ms                                                                 | 101 ms: 1.02x faster                                                  |
| go                       | 276 ms                                                                 | 270 ms: 1.02x faster                                                  |
| deltablue                | 8.22 ms                                                                | 8.05 ms: 1.02x faster                                                 |
| pprint_safe_repr         | 980 ms                                                                 | 961 ms: 1.02x faster                                                  |
| spectral_norm            | 122 ms                                                                 | 120 ms: 1.02x faster                                                  |
| genshi_xml               | 65.0 ms                                                                | 63.8 ms: 1.02x faster                                                 |
| sqlglot_parse            | 2.61 ms                                                                | 2.56 ms: 1.02x faster                                                 |
| logging_silent           | 191 ns                                                                 | 187 ns: 1.02x faster                                                  |
| generators               | 39.7 ms                                                                | 39.0 ms: 1.02x faster                                                 |
| coroutines               | 25.5 ms                                                                | 25.1 ms: 1.02x faster                                                 |
| subparsers               | 31.9 ms                                                                | 31.4 ms: 1.02x faster                                                 |
| sympy_expand             | 967 ms                                                                 | 952 ms: 1.02x faster                                                  |
| raytrace                 | 566 ms                                                                 | 557 ms: 1.02x faster                                                  |
| sympy_str                | 482 ms                                                                 | 475 ms: 1.01x faster                                                  |
| float                    | 140 ms                                                                 | 138 ms: 1.01x faster                                                  |
| shortest_path            | 554 ms                                                                 | 546 ms: 1.01x faster                                                  |
| sqlglot_transpile        | 3.00 ms                                                                | 2.96 ms: 1.01x faster                                                 |
| 2to3                     | 372 ms                                                                 | 367 ms: 1.01x faster                                                  |
| nqueens                  | 99.8 ms                                                                | 98.4 ms: 1.01x faster                                                 |
| pidigits                 | 184 ms                                                                 | 181 ms: 1.01x faster                                                  |
| regex_compile            | 181 ms                                                                 | 179 ms: 1.01x faster                                                  |
| django_template          | 52.3 ms                                                                | 51.6 ms: 1.01x faster                                                 |
| pathlib                  | 20.4 ms                                                                | 20.2 ms: 1.01x faster                                                 |
| typing_runtime_protocols | 207 us                                                                 | 204 us: 1.01x faster                                                  |
| regex_dna                | 191 ms                                                                 | 188 ms: 1.01x faster                                                  |
| pyflate                  | 692 ms                                                                 | 684 ms: 1.01x faster                                                  |
| sympy_sum                | 353 ms                                                                 | 349 ms: 1.01x faster                                                  |
| scimark_monte_carlo      | 119 ms                                                                 | 118 ms: 1.01x faster                                                  |
| xml_etree_generate       | 98.5 ms                                                                | 97.3 ms: 1.01x faster                                                 |
| connected_components     | 504 ms                                                                 | 498 ms: 1.01x faster                                                  |
| logging_simple           | 10.9 us                                                                | 10.8 us: 1.01x faster                                                 |
| sqlglot_normalize        | 139 ms                                                                 | 138 ms: 1.01x faster                                                  |
| sympy_integrate          | 29.8 ms                                                                | 29.5 ms: 1.01x faster                                                 |
| async_tree_memoization   | 476 ms                                                                 | 472 ms: 1.01x faster                                                  |
| docutils                 | 3.13 sec                                                               | 3.10 sec: 1.01x faster                                                |
| sphinx                   | 1.20 sec                                                               | 1.19 sec: 1.01x faster                                                |
| sqlglot_optimize         | 69.9 ms                                                                | 69.3 ms: 1.01x faster                                                 |
| python_startup           | 17.6 ms                                                                | 17.4 ms: 1.01x faster                                                 |
| xml_etree_iterparse      | 91.9 ms                                                                | 91.1 ms: 1.01x faster                                                 |
| bpe_tokeniser            | 5.01 sec                                                               | 4.97 sec: 1.01x faster                                                |
| json_loads               | 28.6 us                                                                | 28.4 us: 1.01x faster                                                 |
| xml_etree_process        | 77.9 ms                                                                | 77.3 ms: 1.01x faster                                                 |
| json                     | 5.12 ms                                                                | 5.08 ms: 1.01x faster                                                 |
| scimark_sor              | 239 ms                                                                 | 237 ms: 1.01x faster                                                  |
| many_optionals           | 1.30 ms                                                                | 1.29 ms: 1.01x faster                                                 |
| python_startup_no_site   | 10.3 ms                                                                | 10.3 ms: 1.01x faster                                                 |
| hexiom                   | 9.98 ms                                                                | 9.92 ms: 1.01x faster                                                 |
| crypto_pyaes             | 92.5 ms                                                                | 91.9 ms: 1.01x faster                                                 |
| sqlalchemy_declarative   | 205 ms                                                                 | 204 ms: 1.01x faster                                                  |
| bench_mp_pool            | 109 ms                                                                 | 109 ms: 1.01x faster                                                  |
| dulwich_log              | 96.7 ms                                                                | 96.1 ms: 1.01x faster                                                 |
| json_dumps               | 14.3 ms                                                                | 14.3 ms: 1.00x slower                                                 |
| genshi_text              | 31.8 ms                                                                | 32.0 ms: 1.01x slower                                                 |
| regex_effbot             | 2.89 ms                                                                | 2.91 ms: 1.01x slower                                                 |
| mdp                      | 2.85 sec                                                               | 2.88 sec: 1.01x slower                                                |
| xml_etree_parse          | 131 ms                                                                 | 132 ms: 1.01x slower                                                  |
| scimark_fft              | 392 ms                                                                 | 397 ms: 1.01x slower                                                  |
| deepcopy_memo            | 40.0 us                                                                | 40.5 us: 1.01x slower                                                 |
| async_generators         | 452 ms                                                                 | 459 ms: 1.02x slower                                                  |
| scimark_sparse_mat_mult  | 5.54 ms                                                                | 5.84 ms: 1.05x slower                                                 |
| Geometric mean           | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (26): pylint, sqlalchemy_imperative, sqlite_synth, scimark_lu, async_tree_cpu_io_mixed, pycparser, richards, mako, fannkuch, asyncio_websockets, richards_super, async_tree_memoization_tg, bench_thread_pool, k_core, comprehensions, async_tree_io_tg, async_tree_cpu_io_mixed_tg, unpickle_pure_python, chaos, async_tree_io, thrift, regex_v8, async_tree_none, tomli_loads, async_tree_none_tg, meteor_contest

- Geometric mean (including insignificant results): 1.010x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x