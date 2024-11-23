# Results vs. base

- fork: mpage
- ref: gh_115999_tlbc_call_
- machine: linux-x86_64
- commit hash: 26bfc21
- commit date: 2024-11-22
- overall geometric mean: 1.00x faster
- HPT reliability: 99.98%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241122-vultr-x86_64-python-d24a22e9b6377797c3b6-3.14.0a2+-d24a22e | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 257 ms                                                                 | 256 ms: 1.00x faster                                                  |
| docutils       | 2.63 sec                                                               | 2.64 sec: 1.00x slower                                                |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (2): html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241122-vultr-x86_64-python-d24a22e9b6377797c3b6-3.14.0a2+-d24a22e | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_generators           | 376 ms                                                                 | 373 ms: 1.01x faster                                                  |
| coroutines                 | 22.2 ms                                                                | 22.5 ms: 1.01x slower                                                 |
| async_tree_cpu_io_mixed    | 573 ms                                                                 | 628 ms: 1.10x slower                                                  |
| async_tree_cpu_io_mixed_tg | 572 ms                                                                 | 630 ms: 1.10x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.02x slower                                                          |

Benchmark hidden because not significant (7): async_tree_memoization_tg, async_tree_none_tg, asyncio_websockets, async_tree_io, async_tree_memoization, async_tree_io_tg, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241122-vultr-x86_64-python-d24a22e9b6377797c3b6-3.14.0a2+-d24a22e | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 82.1 ms                                                                | 80.4 ms: 1.02x faster                                                 |
| nbody          | 93.7 ms                                                                | 94.9 ms: 1.01x slower                                                 |
| pidigits       | 185 ms                                                                 | 216 ms: 1.17x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.05x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241122-vultr-x86_64-python-d24a22e9b6377797c3b6-3.14.0a2+-d24a22e | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 23.9 ms                                                                | 24.4 ms: 1.02x slower                                                 |
| regex_effbot   | 2.85 ms                                                                | 2.93 ms: 1.03x slower                                                 |
| regex_compile  | 130 ms                                                                 | 136 ms: 1.04x slower                                                  |
| regex_dna      | 177 ms                                                                 | 186 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241122-vultr-x86_64-python-d24a22e9b6377797c3b6-3.14.0a2+-d24a22e | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| unpickle_pure_python | 218 us                                                                 | 214 us: 1.02x faster                                                  |
| xml_etree_parse      | 139 ms                                                                 | 137 ms: 1.02x faster                                                  |
| xml_etree_process    | 61.3 ms                                                                | 60.3 ms: 1.02x faster                                                 |
| pickle_pure_python   | 321 us                                                                 | 318 us: 1.01x faster                                                  |
| tomli_loads          | 2.11 sec                                                               | 2.09 sec: 1.01x faster                                                |
| xml_etree_generate   | 87.2 ms                                                                | 86.7 ms: 1.01x faster                                                 |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (3): json_dumps, xml_etree_iterparse, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241122-vultr-x86_64-python-d24a22e9b6377797c3b6-3.14.0a2+-d24a22e | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 7.39 ms: 1.00x faster                                                 |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241122-vultr-x86_64-python-d24a22e9b6377797c3b6-3.14.0a2+-d24a22e | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 22.7 ms                                                                | 21.9 ms: 1.04x faster                                                 |
| genshi_xml      | 50.9 ms                                                                | 49.8 ms: 1.02x faster                                                 |
| mako            | 11.9 ms                                                                | 11.7 ms: 1.02x faster                                                 |
| django_template | 36.2 ms                                                                | 35.5 ms: 1.02x faster                                                 |
| Geometric mean  | (ref)                                                                  | 1.03x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20241122-vultr-x86_64-python-d24a22e9b6377797c3b6-3.14.0a2+-d24a22e | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| spectral_norm              | 113 ms                                                                 | 108 ms: 1.04x faster                                                  |
| fannkuch                   | 386 ms                                                                 | 371 ms: 1.04x faster                                                  |
| deepcopy_reduce            | 2.69 us                                                                | 2.58 us: 1.04x faster                                                 |
| genshi_text                | 22.7 ms                                                                | 21.9 ms: 1.04x faster                                                 |
| go                         | 123 ms                                                                 | 119 ms: 1.03x faster                                                  |
| deepcopy_memo              | 30.4 us                                                                | 29.6 us: 1.03x faster                                                 |
| richards_super             | 53.8 ms                                                                | 52.5 ms: 1.03x faster                                                 |
| logging_silent             | 109 ns                                                                 | 106 ns: 1.02x faster                                                  |
| scimark_monte_carlo        | 66.5 ms                                                                | 64.9 ms: 1.02x faster                                                 |
| sqlglot_parse              | 1.32 ms                                                                | 1.29 ms: 1.02x faster                                                 |
| genshi_xml                 | 50.9 ms                                                                | 49.8 ms: 1.02x faster                                                 |
| mako                       | 11.9 ms                                                                | 11.7 ms: 1.02x faster                                                 |
| float                      | 82.1 ms                                                                | 80.4 ms: 1.02x faster                                                 |
| django_template            | 36.2 ms                                                                | 35.5 ms: 1.02x faster                                                 |
| unpickle_pure_python       | 218 us                                                                 | 214 us: 1.02x faster                                                  |
| scimark_fft                | 343 ms                                                                 | 337 ms: 1.02x faster                                                  |
| hexiom                     | 6.09 ms                                                                | 5.98 ms: 1.02x faster                                                 |
| pprint_pformat             | 1.48 sec                                                               | 1.45 sec: 1.02x faster                                                |
| deepcopy                   | 263 us                                                                 | 258 us: 1.02x faster                                                  |
| pprint_safe_repr           | 725 ms                                                                 | 713 ms: 1.02x faster                                                  |
| xml_etree_parse            | 139 ms                                                                 | 137 ms: 1.02x faster                                                  |
| deltablue                  | 3.29 ms                                                                | 3.23 ms: 1.02x faster                                                 |
| xml_etree_process          | 61.3 ms                                                                | 60.3 ms: 1.02x faster                                                 |
| chaos                      | 59.2 ms                                                                | 58.3 ms: 1.02x faster                                                 |
| sqlglot_transpile          | 1.62 ms                                                                | 1.60 ms: 1.02x faster                                                 |
| raytrace                   | 266 ms                                                                 | 262 ms: 1.01x faster                                                  |
| logging_simple             | 6.26 us                                                                | 6.18 us: 1.01x faster                                                 |
| richards                   | 47.2 ms                                                                | 46.6 ms: 1.01x faster                                                 |
| bpe_tokeniser              | 4.46 sec                                                               | 4.41 sec: 1.01x faster                                                |
| pyflate                    | 455 ms                                                                 | 449 ms: 1.01x faster                                                  |
| logging_format             | 7.03 us                                                                | 6.94 us: 1.01x faster                                                 |
| pycparser                  | 1.14 sec                                                               | 1.13 sec: 1.01x faster                                                |
| create_gc_cycles           | 1.93 ms                                                                | 1.91 ms: 1.01x faster                                                 |
| sqlite_synth               | 2.23 us                                                                | 2.21 us: 1.01x faster                                                 |
| bench_thread_pool          | 1.03 ms                                                                | 1.02 ms: 1.01x faster                                                 |
| pathlib                    | 18.6 ms                                                                | 18.4 ms: 1.01x faster                                                 |
| crypto_pyaes               | 68.4 ms                                                                | 67.7 ms: 1.01x faster                                                 |
| pickle_pure_python         | 321 us                                                                 | 318 us: 1.01x faster                                                  |
| telco                      | 7.31 ms                                                                | 7.25 ms: 1.01x faster                                                 |
| connected_components       | 404 ms                                                                 | 400 ms: 1.01x faster                                                  |
| async_generators           | 376 ms                                                                 | 373 ms: 1.01x faster                                                  |
| tomli_loads                | 2.11 sec                                                               | 2.09 sec: 1.01x faster                                                |
| scimark_lu                 | 113 ms                                                                 | 112 ms: 1.01x faster                                                  |
| nqueens                    | 79.5 ms                                                                | 79.0 ms: 1.01x faster                                                 |
| shortest_path              | 444 ms                                                                 | 441 ms: 1.01x faster                                                  |
| many_optionals             | 1.03 ms                                                                | 1.02 ms: 1.01x faster                                                 |
| xml_etree_generate         | 87.2 ms                                                                | 86.7 ms: 1.01x faster                                                 |
| 2to3                       | 257 ms                                                                 | 256 ms: 1.00x faster                                                  |
| sqlglot_normalize          | 107 ms                                                                 | 107 ms: 1.00x faster                                                  |
| scimark_sor                | 135 ms                                                                 | 134 ms: 1.00x faster                                                  |
| python_startup_no_site     | 7.41 ms                                                                | 7.39 ms: 1.00x faster                                                 |
| sqlglot_optimize           | 53.7 ms                                                                | 53.6 ms: 1.00x faster                                                 |
| docutils                   | 2.63 sec                                                               | 2.64 sec: 1.00x slower                                                |
| subparsers                 | 22.1 ms                                                                | 22.2 ms: 1.01x slower                                                 |
| sympy_sum                  | 153 ms                                                                 | 154 ms: 1.01x slower                                                  |
| thrift                     | 744 us                                                                 | 753 us: 1.01x slower                                                  |
| meteor_contest             | 99.2 ms                                                                | 100 ms: 1.01x slower                                                  |
| nbody                      | 93.7 ms                                                                | 94.9 ms: 1.01x slower                                                 |
| coroutines                 | 22.2 ms                                                                | 22.5 ms: 1.01x slower                                                 |
| regex_v8                   | 23.9 ms                                                                | 24.4 ms: 1.02x slower                                                 |
| regex_effbot               | 2.85 ms                                                                | 2.93 ms: 1.03x slower                                                 |
| regex_compile              | 130 ms                                                                 | 136 ms: 1.04x slower                                                  |
| regex_dna                  | 177 ms                                                                 | 186 ms: 1.05x slower                                                  |
| async_tree_cpu_io_mixed    | 573 ms                                                                 | 628 ms: 1.10x slower                                                  |
| async_tree_cpu_io_mixed_tg | 572 ms                                                                 | 630 ms: 1.10x slower                                                  |
| gc_traversal               | 3.79 ms                                                                | 4.22 ms: 1.11x slower                                                 |
| pidigits                   | 185 ms                                                                 | 216 ms: 1.17x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (29): scimark_sparse_mat_mult, json_dumps, html5lib, k_core, json, async_tree_memoization_tg, generators, coverage, async_tree_none_tg, xml_etree_iterparse, pylint, sqlalchemy_imperative, json_loads, sqlalchemy_declarative, python_startup, mdp, comprehensions, asyncio_websockets, bench_mp_pool, sympy_integrate, sympy_str, sympy_expand, typing_runtime_protocols, sphinx, async_tree_io, dulwich_log, async_tree_memoization, async_tree_io_tg, async_tree_none

# HPT report

- Reliability score: 99.98% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x