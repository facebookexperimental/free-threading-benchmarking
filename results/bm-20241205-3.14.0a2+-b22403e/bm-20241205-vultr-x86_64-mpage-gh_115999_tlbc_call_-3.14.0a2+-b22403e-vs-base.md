# Results vs. base

- fork: mpage
- ref: gh_115999_tlbc_call_
- machine: linux-x86_64
- commit hash: b22403e
- commit date: 2024-12-05
- overall geometric mean: 1.007x faster
- HPT reliability: 98.73%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 257 ms                                                                 | 258 ms: 1.00x slower                                                  |
| docutils       | 2.57 sec                                                               | 2.56 sec: 1.00x faster                                                |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 607 ms                                                                 | 501 ms: 1.21x faster                                                  |
| async_tree_cpu_io_mixed_tg | 587 ms                                                                 | 488 ms: 1.20x faster                                                  |
| async_generators           | 370 ms                                                                 | 364 ms: 1.02x faster                                                  |
| coroutines                 | 21.9 ms                                                                | 22.5 ms: 1.02x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.03x faster                                                          |

Benchmark hidden because not significant (7): async_tree_none, async_tree_none_tg, async_tree_io, asyncio_websockets, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 222 ms                                                                 | 186 ms: 1.19x faster                                                  |
| nbody          | 95.2 ms                                                                | 93.9 ms: 1.01x faster                                                 |
| float          | 78.6 ms                                                                | 77.8 ms: 1.01x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.07x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 130 ms                                                                 | 129 ms: 1.01x faster                                                  |
| regex_effbot   | 2.74 ms                                                                | 2.79 ms: 1.02x slower                                                 |
| regex_dna      | 169 ms                                                                 | 176 ms: 1.04x slower                                                  |
| regex_v8       | 23.3 ms                                                                | 24.7 ms: 1.06x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| unpickle_pure_python | 216 us                                                                 | 214 us: 1.01x faster                                                  |
| xml_etree_process    | 59.6 ms                                                                | 59.1 ms: 1.01x faster                                                 |
| pickle_pure_python   | 316 us                                                                 | 314 us: 1.01x faster                                                  |
| json_dumps           | 11.5 ms                                                                | 11.4 ms: 1.01x faster                                                 |
| tomli_loads          | 2.11 sec                                                               | 2.09 sec: 1.01x faster                                                |
| xml_etree_iterparse  | 92.1 ms                                                                | 91.7 ms: 1.00x faster                                                 |
| xml_etree_parse      | 130 ms                                                                 | 130 ms: 1.00x slower                                                  |
| json_loads           | 25.1 us                                                                | 25.3 us: 1.01x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (1): xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                                | 14.6 ms: 1.00x slower                                                 |
| python_startup_no_site | 7.43 ms                                                                | 7.45 ms: 1.00x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 51.2 ms                                                                | 50.4 ms: 1.02x faster                                                 |
| genshi_text     | 22.3 ms                                                                | 22.0 ms: 1.01x faster                                                 |
| mako            | 11.5 ms                                                                | 11.6 ms: 1.00x slower                                                 |
| django_template | 35.6 ms                                                                | 36.0 ms: 1.01x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.00x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 607 ms                                                                 | 501 ms: 1.21x faster                                                  |
| async_tree_cpu_io_mixed_tg | 587 ms                                                                 | 488 ms: 1.20x faster                                                  |
| pidigits                   | 222 ms                                                                 | 186 ms: 1.19x faster                                                  |
| gc_traversal               | 4.58 ms                                                                | 4.42 ms: 1.04x faster                                                 |
| deepcopy_memo              | 30.7 us                                                                | 29.9 us: 1.03x faster                                                 |
| scimark_monte_carlo        | 65.6 ms                                                                | 63.9 ms: 1.03x faster                                                 |
| hexiom                     | 5.99 ms                                                                | 5.86 ms: 1.02x faster                                                 |
| chaos                      | 60.1 ms                                                                | 58.8 ms: 1.02x faster                                                 |
| sqlite_synth               | 2.28 us                                                                | 2.23 us: 1.02x faster                                                 |
| sqlalchemy_imperative      | 19.4 ms                                                                | 19.0 ms: 1.02x faster                                                 |
| logging_simple             | 6.27 us                                                                | 6.16 us: 1.02x faster                                                 |
| logging_format             | 7.04 us                                                                | 6.92 us: 1.02x faster                                                 |
| richards                   | 46.7 ms                                                                | 45.9 ms: 1.02x faster                                                 |
| async_generators           | 370 ms                                                                 | 364 ms: 1.02x faster                                                  |
| genshi_xml                 | 51.2 ms                                                                | 50.4 ms: 1.02x faster                                                 |
| nbody                      | 95.2 ms                                                                | 93.9 ms: 1.01x faster                                                 |
| generators                 | 29.0 ms                                                                | 28.6 ms: 1.01x faster                                                 |
| richards_super             | 52.7 ms                                                                | 52.0 ms: 1.01x faster                                                 |
| genshi_text                | 22.3 ms                                                                | 22.0 ms: 1.01x faster                                                 |
| fannkuch                   | 376 ms                                                                 | 372 ms: 1.01x faster                                                  |
| float                      | 78.6 ms                                                                | 77.8 ms: 1.01x faster                                                 |
| sympy_str                  | 277 ms                                                                 | 274 ms: 1.01x faster                                                  |
| unpickle_pure_python       | 216 us                                                                 | 214 us: 1.01x faster                                                  |
| regex_compile              | 130 ms                                                                 | 129 ms: 1.01x faster                                                  |
| xml_etree_process          | 59.6 ms                                                                | 59.1 ms: 1.01x faster                                                 |
| crypto_pyaes               | 68.1 ms                                                                | 67.6 ms: 1.01x faster                                                 |
| raytrace                   | 265 ms                                                                 | 263 ms: 1.01x faster                                                  |
| deltablue                  | 3.25 ms                                                                | 3.22 ms: 1.01x faster                                                 |
| sympy_integrate            | 20.1 ms                                                                | 19.9 ms: 1.01x faster                                                 |
| pickle_pure_python         | 316 us                                                                 | 314 us: 1.01x faster                                                  |
| json_dumps                 | 11.5 ms                                                                | 11.4 ms: 1.01x faster                                                 |
| scimark_fft                | 340 ms                                                                 | 338 ms: 1.01x faster                                                  |
| tomli_loads                | 2.11 sec                                                               | 2.09 sec: 1.01x faster                                                |
| shortest_path              | 444 ms                                                                 | 441 ms: 1.01x faster                                                  |
| docutils                   | 2.57 sec                                                               | 2.56 sec: 1.00x faster                                                |
| xml_etree_iterparse        | 92.1 ms                                                                | 91.7 ms: 1.00x faster                                                 |
| dulwich_log                | 76.1 ms                                                                | 75.7 ms: 1.00x faster                                                 |
| deepcopy                   | 262 us                                                                 | 261 us: 1.00x faster                                                  |
| sqlalchemy_declarative     | 127 ms                                                                 | 126 ms: 1.00x faster                                                  |
| bpe_tokeniser              | 4.32 sec                                                               | 4.33 sec: 1.00x slower                                                |
| python_startup             | 14.6 ms                                                                | 14.6 ms: 1.00x slower                                                 |
| python_startup_no_site     | 7.43 ms                                                                | 7.45 ms: 1.00x slower                                                 |
| 2to3                       | 257 ms                                                                 | 258 ms: 1.00x slower                                                  |
| sqlglot_optimize           | 53.6 ms                                                                | 53.8 ms: 1.00x slower                                                 |
| pprint_safe_repr           | 715 ms                                                                 | 718 ms: 1.00x slower                                                  |
| comprehensions             | 17.3 us                                                                | 17.4 us: 1.00x slower                                                 |
| mako                       | 11.5 ms                                                                | 11.6 ms: 1.00x slower                                                 |
| xml_etree_parse            | 130 ms                                                                 | 130 ms: 1.00x slower                                                  |
| bench_thread_pool          | 1.02 ms                                                                | 1.02 ms: 1.01x slower                                                 |
| json_loads                 | 25.1 us                                                                | 25.3 us: 1.01x slower                                                 |
| spectral_norm              | 107 ms                                                                 | 108 ms: 1.01x slower                                                  |
| telco                      | 7.19 ms                                                                | 7.27 ms: 1.01x slower                                                 |
| create_gc_cycles           | 1.83 ms                                                                | 1.85 ms: 1.01x slower                                                 |
| django_template            | 35.6 ms                                                                | 36.0 ms: 1.01x slower                                                 |
| json                       | 4.53 ms                                                                | 4.59 ms: 1.01x slower                                                 |
| pprint_pformat             | 1.45 sec                                                               | 1.47 sec: 1.01x slower                                                |
| subparsers                 | 22.1 ms                                                                | 22.4 ms: 1.01x slower                                                 |
| pycparser                  | 1.13 sec                                                               | 1.15 sec: 1.02x slower                                                |
| scimark_lu                 | 109 ms                                                                 | 111 ms: 1.02x slower                                                  |
| regex_effbot               | 2.74 ms                                                                | 2.79 ms: 1.02x slower                                                 |
| thrift                     | 736 us                                                                 | 751 us: 1.02x slower                                                  |
| coroutines                 | 21.9 ms                                                                | 22.5 ms: 1.02x slower                                                 |
| regex_dna                  | 169 ms                                                                 | 176 ms: 1.04x slower                                                  |
| mdp                        | 2.35 sec                                                               | 2.47 sec: 1.05x slower                                                |
| regex_v8                   | 23.3 ms                                                                | 24.7 ms: 1.06x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (30): deepcopy_reduce, async_tree_none, async_tree_none_tg, pyflate, typing_runtime_protocols, xml_etree_generate, async_tree_io, sqlglot_parse, logging_silent, k_core, pylint, many_optionals, asyncio_websockets, bench_mp_pool, async_tree_io_tg, sphinx, sqlglot_transpile, pathlib, meteor_contest, coverage, connected_components, scimark_sparse_mat_mult, sympy_expand, go, nqueens, async_tree_memoization, sqlglot_normalize, sympy_sum, scimark_sor, async_tree_memoization_tg

- Geometric mean (including insignificant results): 1.007x faster

# HPT report

- Reliability score: 98.73% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x