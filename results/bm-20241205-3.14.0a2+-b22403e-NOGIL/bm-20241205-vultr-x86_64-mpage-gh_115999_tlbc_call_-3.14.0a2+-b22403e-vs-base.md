# Results vs. base

- fork: mpage
- ref: gh_115999_tlbc_call_
- machine: linux-x86_64
- commit hash: b22403e
- commit date: 2024-12-05
- overall geometric mean: 1.002x slower
- HPT reliability: 90.72%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| docutils       | 3.07 sec                                                               | 3.11 sec: 1.01x slower                                                |
| html5lib       | 97.1 ms                                                                | 99.2 ms: 1.02x slower                                                 |
| sphinx         | 1.18 sec                                                               | 1.19 sec: 1.01x slower                                                |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|-------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io           | 864 ms                                                                 | 848 ms: 1.02x faster                                                  |
| async_tree_memoization  | 478 ms                                                                 | 469 ms: 1.02x faster                                                  |
| async_generators        | 456 ms                                                                 | 451 ms: 1.01x faster                                                  |
| async_tree_none         | 390 ms                                                                 | 386 ms: 1.01x faster                                                  |
| coroutines              | 24.3 ms                                                                | 24.0 ms: 1.01x faster                                                 |
| async_tree_io_tg        | 832 ms                                                                 | 827 ms: 1.01x faster                                                  |
| async_tree_cpu_io_mixed | 639 ms                                                                 | 644 ms: 1.01x slower                                                  |
| Geometric mean          | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (4): async_tree_none_tg, async_tree_cpu_io_mixed_tg, asyncio_websockets, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 184 ms                                                                 | 184 ms: 1.00x faster                                                  |
| nbody          | 131 ms                                                                 | 131 ms: 1.00x slower                                                  |
| float          | 138 ms                                                                 | 140 ms: 1.01x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 24.6 ms                                                                | 24.9 ms: 1.01x slower                                                 |
| regex_dna      | 183 ms                                                                 | 189 ms: 1.03x slower                                                  |
| regex_effbot   | 2.79 ms                                                                | 2.90 ms: 1.04x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                          |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 14.4 ms                                                                | 14.3 ms: 1.01x faster                                                 |
| xml_etree_parse      | 130 ms                                                                 | 130 ms: 1.00x faster                                                  |
| unpickle_pure_python | 332 us                                                                 | 334 us: 1.00x slower                                                  |
| xml_etree_iterparse  | 90.9 ms                                                                | 91.6 ms: 1.01x slower                                                 |
| json_loads           | 28.4 us                                                                | 28.7 us: 1.01x slower                                                 |
| xml_etree_process    | 77.2 ms                                                                | 78.3 ms: 1.01x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (3): pickle_pure_python, tomli_loads, xml_etree_generate

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup, python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako           | 17.6 ms                                                                | 17.8 ms: 1.01x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (3): django_template, genshi_xml, genshi_text

All benchmarks:
===============

| Benchmark               | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|-------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal            | 3.53 ms                                                                | 3.29 ms: 1.07x faster                                                 |
| deepcopy_reduce         | 3.62 us                                                                | 3.51 us: 1.03x faster                                                 |
| telco                   | 8.83 ms                                                                | 8.63 ms: 1.02x faster                                                 |
| create_gc_cycles        | 1.85 ms                                                                | 1.81 ms: 1.02x faster                                                 |
| spectral_norm           | 122 ms                                                                 | 119 ms: 1.02x faster                                                  |
| pprint_pformat          | 2.03 sec                                                               | 1.99 sec: 1.02x faster                                                |
| async_tree_io           | 864 ms                                                                 | 848 ms: 1.02x faster                                                  |
| async_tree_memoization  | 478 ms                                                                 | 469 ms: 1.02x faster                                                  |
| pprint_safe_repr        | 981 ms                                                                 | 965 ms: 1.02x faster                                                  |
| scimark_lu              | 185 ms                                                                 | 182 ms: 1.01x faster                                                  |
| richards_super          | 86.3 ms                                                                | 85.2 ms: 1.01x faster                                                 |
| async_generators        | 456 ms                                                                 | 451 ms: 1.01x faster                                                  |
| json_dumps              | 14.4 ms                                                                | 14.3 ms: 1.01x faster                                                 |
| async_tree_none         | 390 ms                                                                 | 386 ms: 1.01x faster                                                  |
| thrift                  | 1.17 ms                                                                | 1.16 ms: 1.01x faster                                                 |
| coroutines              | 24.3 ms                                                                | 24.0 ms: 1.01x faster                                                 |
| deepcopy_memo           | 40.1 us                                                                | 39.7 us: 1.01x faster                                                 |
| async_tree_io_tg        | 832 ms                                                                 | 827 ms: 1.01x faster                                                  |
| pathlib                 | 20.4 ms                                                                | 20.3 ms: 1.00x faster                                                 |
| sqlalchemy_declarative  | 205 ms                                                                 | 204 ms: 1.00x faster                                                  |
| pycparser               | 1.53 sec                                                               | 1.52 sec: 1.00x faster                                                |
| xml_etree_parse         | 130 ms                                                                 | 130 ms: 1.00x faster                                                  |
| pidigits                | 184 ms                                                                 | 184 ms: 1.00x faster                                                  |
| fannkuch                | 493 ms                                                                 | 494 ms: 1.00x slower                                                  |
| deepcopy                | 327 us                                                                 | 328 us: 1.00x slower                                                  |
| unpickle_pure_python    | 332 us                                                                 | 334 us: 1.00x slower                                                  |
| nbody                   | 131 ms                                                                 | 131 ms: 1.00x slower                                                  |
| sympy_integrate         | 29.4 ms                                                                | 29.5 ms: 1.00x slower                                                 |
| dulwich_log             | 96.1 ms                                                                | 96.5 ms: 1.00x slower                                                 |
| richards                | 75.5 ms                                                                | 76.0 ms: 1.01x slower                                                 |
| crypto_pyaes            | 91.3 ms                                                                | 92.0 ms: 1.01x slower                                                 |
| hexiom                  | 9.80 ms                                                                | 9.88 ms: 1.01x slower                                                 |
| xml_etree_iterparse     | 90.9 ms                                                                | 91.6 ms: 1.01x slower                                                 |
| sphinx                  | 1.18 sec                                                               | 1.19 sec: 1.01x slower                                                |
| async_tree_cpu_io_mixed | 639 ms                                                                 | 644 ms: 1.01x slower                                                  |
| sqlglot_transpile       | 2.97 ms                                                                | 3.00 ms: 1.01x slower                                                 |
| shortest_path           | 547 ms                                                                 | 552 ms: 1.01x slower                                                  |
| json_loads              | 28.4 us                                                                | 28.7 us: 1.01x slower                                                 |
| float                   | 138 ms                                                                 | 140 ms: 1.01x slower                                                  |
| docutils                | 3.07 sec                                                               | 3.11 sec: 1.01x slower                                                |
| bpe_tokeniser           | 4.95 sec                                                               | 5.01 sec: 1.01x slower                                                |
| mako                    | 17.6 ms                                                                | 17.8 ms: 1.01x slower                                                 |
| nqueens                 | 95.8 ms                                                                | 96.9 ms: 1.01x slower                                                 |
| regex_v8                | 24.6 ms                                                                | 24.9 ms: 1.01x slower                                                 |
| logging_silent          | 184 ns                                                                 | 186 ns: 1.01x slower                                                  |
| logging_format          | 12.0 us                                                                | 12.2 us: 1.01x slower                                                 |
| comprehensions          | 26.8 us                                                                | 27.2 us: 1.01x slower                                                 |
| raytrace                | 543 ms                                                                 | 551 ms: 1.01x slower                                                  |
| scimark_monte_carlo     | 117 ms                                                                 | 119 ms: 1.01x slower                                                  |
| xml_etree_process       | 77.2 ms                                                                | 78.3 ms: 1.01x slower                                                 |
| sqlite_synth            | 2.26 us                                                                | 2.30 us: 1.02x slower                                                 |
| scimark_fft             | 389 ms                                                                 | 395 ms: 1.02x slower                                                  |
| subparsers              | 31.7 ms                                                                | 32.3 ms: 1.02x slower                                                 |
| html5lib                | 97.1 ms                                                                | 99.2 ms: 1.02x slower                                                 |
| json                    | 5.06 ms                                                                | 5.18 ms: 1.02x slower                                                 |
| regex_dna               | 183 ms                                                                 | 189 ms: 1.03x slower                                                  |
| pyflate                 | 676 ms                                                                 | 697 ms: 1.03x slower                                                  |
| regex_effbot            | 2.79 ms                                                                | 2.90 ms: 1.04x slower                                                 |
| mdp                     | 2.77 sec                                                               | 2.89 sec: 1.04x slower                                                |
| scimark_sparse_mat_mult | 5.58 ms                                                                | 5.97 ms: 1.07x slower                                                 |
| Geometric mean          | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (36): sqlalchemy_imperative, async_tree_none_tg, sqlglot_parse, django_template, async_tree_cpu_io_mixed_tg, sqlglot_optimize, sqlglot_normalize, pickle_pure_python, scimark_sor, tomli_loads, many_optionals, genshi_xml, 2to3, sympy_str, bench_mp_pool, deltablue, genshi_text, python_startup, python_startup_no_site, sympy_expand, sympy_sum, xml_etree_generate, regex_compile, go, typing_runtime_protocols, k_core, pylint, logging_simple, meteor_contest, asyncio_websockets, bench_thread_pool, async_tree_memoization_tg, coverage, connected_components, chaos, generators

- Geometric mean (including insignificant results): 1.002x slower

# HPT report

- Reliability score: 90.72% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x