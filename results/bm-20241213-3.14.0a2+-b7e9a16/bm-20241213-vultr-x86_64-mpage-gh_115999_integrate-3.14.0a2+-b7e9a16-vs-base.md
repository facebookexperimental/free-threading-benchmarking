# Results vs. base

- fork: mpage
- ref: gh_115999_integrate
- machine: linux-x86_64
- commit hash: b7e9a16
- commit date: 2024-12-13
- overall geometric mean: 1.001x faster
- HPT reliability: 91.82%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 256 ms                                                                 | 254 ms: 1.01x faster                                                 |
| docutils       | 2.55 sec                                                               | 2.54 sec: 1.00x faster                                               |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                         |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io    | 627 ms                                                                 | 619 ms: 1.01x faster                                                 |
| async_generators | 352 ms                                                                 | 354 ms: 1.01x slower                                                 |
| coroutines       | 21.6 ms                                                                | 21.9 ms: 1.01x slower                                                |
| Geometric mean   | (ref)                                                                  | 1.00x faster                                                         |

Benchmark hidden because not significant (8): async_tree_none, async_tree_io_tg, async_tree_none_tg, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, asyncio_websockets, async_tree_memoization, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

Benchmark hidden because not significant (3): float, pidigits, nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_dna      | 175 ms                                                                 | 174 ms: 1.00x faster                                                 |
| regex_effbot   | 2.69 ms                                                                | 2.70 ms: 1.00x slower                                                |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                         |

Benchmark hidden because not significant (2): regex_compile, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| unpickle_pure_python | 213 us                                                                 | 211 us: 1.01x faster                                                 |
| pickle_pure_python   | 323 us                                                                 | 321 us: 1.01x faster                                                 |
| json_loads           | 26.1 us                                                                | 26.2 us: 1.01x slower                                                |
| xml_etree_generate   | 84.5 ms                                                                | 85.1 ms: 1.01x slower                                                |
| json_dumps           | 11.3 ms                                                                | 11.4 ms: 1.01x slower                                                |
| xml_etree_process    | 58.8 ms                                                                | 59.6 ms: 1.01x slower                                                |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                         |

Benchmark hidden because not significant (3): tomli_loads, xml_etree_iterparse, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 7.49 ms                                                                | 7.45 ms: 1.01x faster                                                |
| python_startup         | 14.6 ms                                                                | 14.6 ms: 1.00x faster                                                |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                         |

Benchmarks with tag 'template':
===============================

Benchmark hidden because not significant (4): genshi_xml, mako, django_template, genshi_text

All benchmarks:
===============

| Benchmark               | bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|-------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| scimark_sparse_mat_mult | 4.38 ms                                                                | 4.15 ms: 1.06x faster                                                |
| scimark_sor             | 128 ms                                                                 | 123 ms: 1.03x faster                                                 |
| richards                | 44.7 ms                                                                | 43.2 ms: 1.03x faster                                                |
| nqueens                 | 80.3 ms                                                                | 77.8 ms: 1.03x faster                                                |
| scimark_monte_carlo     | 64.7 ms                                                                | 63.1 ms: 1.02x faster                                                |
| deepcopy_reduce         | 2.60 us                                                                | 2.54 us: 1.02x faster                                                |
| comprehensions          | 17.2 us                                                                | 16.9 us: 1.02x faster                                                |
| deepcopy                | 256 us                                                                 | 252 us: 1.02x faster                                                 |
| richards_super          | 50.7 ms                                                                | 49.9 ms: 1.01x faster                                                |
| logging_simple          | 6.14 us                                                                | 6.06 us: 1.01x faster                                                |
| subparsers              | 22.2 ms                                                                | 21.9 ms: 1.01x faster                                                |
| hexiom                  | 5.84 ms                                                                | 5.76 ms: 1.01x faster                                                |
| logging_silent          | 106 ns                                                                 | 104 ns: 1.01x faster                                                 |
| async_tree_io           | 627 ms                                                                 | 619 ms: 1.01x faster                                                 |
| dulwich_log             | 76.6 ms                                                                | 75.7 ms: 1.01x faster                                                |
| raytrace                | 260 ms                                                                 | 258 ms: 1.01x faster                                                 |
| deltablue               | 3.17 ms                                                                | 3.14 ms: 1.01x faster                                                |
| sympy_integrate         | 19.9 ms                                                                | 19.7 ms: 1.01x faster                                                |
| logging_format          | 6.79 us                                                                | 6.74 us: 1.01x faster                                                |
| unpickle_pure_python    | 213 us                                                                 | 211 us: 1.01x faster                                                 |
| 2to3                    | 256 ms                                                                 | 254 ms: 1.01x faster                                                 |
| sqlglot_parse           | 1.25 ms                                                                | 1.24 ms: 1.01x faster                                                |
| mdp                     | 2.33 sec                                                               | 2.32 sec: 1.01x faster                                               |
| sqlglot_transpile       | 1.57 ms                                                                | 1.56 ms: 1.01x faster                                                |
| sympy_sum               | 152 ms                                                                 | 151 ms: 1.01x faster                                                 |
| pickle_pure_python      | 323 us                                                                 | 321 us: 1.01x faster                                                 |
| python_startup_no_site  | 7.49 ms                                                                | 7.45 ms: 1.01x faster                                                |
| bench_thread_pool       | 1.04 ms                                                                | 1.03 ms: 1.01x faster                                                |
| python_startup          | 14.6 ms                                                                | 14.6 ms: 1.00x faster                                                |
| sqlglot_optimize        | 52.1 ms                                                                | 51.9 ms: 1.00x faster                                                |
| docutils                | 2.55 sec                                                               | 2.54 sec: 1.00x faster                                               |
| regex_dna               | 175 ms                                                                 | 174 ms: 1.00x faster                                                 |
| chaos                   | 58.4 ms                                                                | 58.5 ms: 1.00x slower                                                |
| regex_effbot            | 2.69 ms                                                                | 2.70 ms: 1.00x slower                                                |
| scimark_lu              | 110 ms                                                                 | 110 ms: 1.00x slower                                                 |
| json_loads              | 26.1 us                                                                | 26.2 us: 1.01x slower                                                |
| xml_etree_generate      | 84.5 ms                                                                | 85.1 ms: 1.01x slower                                                |
| async_generators        | 352 ms                                                                 | 354 ms: 1.01x slower                                                 |
| pprint_pformat          | 1.45 sec                                                               | 1.46 sec: 1.01x slower                                               |
| json_dumps              | 11.3 ms                                                                | 11.4 ms: 1.01x slower                                                |
| sqlalchemy_imperative   | 19.1 ms                                                                | 19.3 ms: 1.01x slower                                                |
| telco                   | 7.18 ms                                                                | 7.25 ms: 1.01x slower                                                |
| create_gc_cycles        | 1.83 ms                                                                | 1.84 ms: 1.01x slower                                                |
| pycparser               | 1.12 sec                                                               | 1.13 sec: 1.01x slower                                               |
| pprint_safe_repr        | 710 ms                                                                 | 718 ms: 1.01x slower                                                 |
| scimark_fft             | 314 ms                                                                 | 317 ms: 1.01x slower                                                 |
| xml_etree_process       | 58.8 ms                                                                | 59.6 ms: 1.01x slower                                                |
| sqlalchemy_declarative  | 126 ms                                                                 | 128 ms: 1.01x slower                                                 |
| coroutines              | 21.6 ms                                                                | 21.9 ms: 1.01x slower                                                |
| generators              | 27.1 ms                                                                | 27.6 ms: 1.02x slower                                                |
| pyflate                 | 421 ms                                                                 | 429 ms: 1.02x slower                                                 |
| crypto_pyaes            | 65.4 ms                                                                | 67.9 ms: 1.04x slower                                                |
| spectral_norm           | 96.3 ms                                                                | 100 ms: 1.04x slower                                                 |
| gc_traversal            | 4.27 ms                                                                | 4.46 ms: 1.04x slower                                                |
| Geometric mean          | (ref)                                                                  | 1.00x faster                                                         |

Benchmark hidden because not significant (41): async_tree_none, async_tree_io_tg, async_tree_none_tg, sphinx, sqlite_synth, float, async_tree_cpu_io_mixed_tg, bench_mp_pool, sqlglot_normalize, thrift, go, async_tree_cpu_io_mixed, meteor_contest, many_optionals, sympy_str, json, deepcopy_memo, asyncio_websockets, pidigits, nbody, genshi_xml, bpe_tokeniser, k_core, shortest_path, regex_compile, mako, tomli_loads, async_tree_memoization, coverage, async_tree_memoization_tg, typing_runtime_protocols, connected_components, pathlib, django_template, genshi_text, pylint, xml_etree_iterparse, regex_v8, fannkuch, xml_etree_parse, sympy_expand

- Geometric mean (including insignificant results): 1.001x faster

# HPT report

- Reliability score: 91.82% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x