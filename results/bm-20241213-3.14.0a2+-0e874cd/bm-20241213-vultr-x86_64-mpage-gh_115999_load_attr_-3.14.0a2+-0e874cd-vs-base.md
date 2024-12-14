# Results vs. base

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: 0e874cd
- commit date: 2024-12-13
- overall geometric mean: 1.004x faster
- HPT reliability: 95.92%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2+-5dd775b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-0e874cd |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 255 ms                                                                 | 255 ms: 1.00x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2+-5dd775b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-0e874cd |
|------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_generators | 359 ms                                                                 | 352 ms: 1.02x faster                                                  |
| coroutines       | 21.7 ms                                                                | 22.2 ms: 1.02x slower                                                 |
| Geometric mean   | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (9): async_tree_memoization_tg, async_tree_io, async_tree_none_tg, async_tree_cpu_io_mixed, asyncio_websockets, async_tree_none, async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization

Benchmarks with tag 'math':
===========================

Benchmark hidden because not significant (3): nbody, float, pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2+-5dd775b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-0e874cd |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 2.81 ms                                                                | 2.73 ms: 1.03x faster                                                 |
| regex_dna      | 179 ms                                                                 | 176 ms: 1.02x faster                                                  |
| regex_v8       | 25.0 ms                                                                | 24.7 ms: 1.01x faster                                                 |
| regex_compile  | 126 ms                                                                 | 127 ms: 1.01x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2+-5dd775b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-0e874cd |
|--------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_pure_python | 321 us                                                                 | 315 us: 1.02x faster                                                  |
| json_loads         | 26.2 us                                                                | 26.1 us: 1.00x faster                                                 |
| json_dumps         | 11.3 ms                                                                | 11.4 ms: 1.01x slower                                                 |
| Geometric mean     | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (6): xml_etree_parse, xml_etree_process, xml_etree_iterparse, unpickle_pure_python, xml_etree_generate, tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2+-5dd775b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-0e874cd |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.51 ms                                                                | 7.53 ms: 1.00x slower                                                 |
| python_startup         | 14.6 ms                                                                | 14.7 ms: 1.00x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2+-5dd775b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-0e874cd |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 36.1 ms                                                                | 35.0 ms: 1.03x faster                                                 |
| genshi_xml      | 49.6 ms                                                                | 50.0 ms: 1.01x slower                                                 |
| genshi_text     | 21.5 ms                                                                | 22.1 ms: 1.03x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark               | bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2+-5dd775b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-0e874cd |
|-------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                     | 2.46 sec                                                               | 2.35 sec: 1.04x faster                                                |
| nqueens                 | 80.6 ms                                                                | 77.4 ms: 1.04x faster                                                 |
| scimark_fft             | 318 ms                                                                 | 308 ms: 1.03x faster                                                  |
| richards                | 45.1 ms                                                                | 43.6 ms: 1.03x faster                                                 |
| thrift                  | 758 us                                                                 | 734 us: 1.03x faster                                                  |
| deepcopy_memo           | 29.8 us                                                                | 28.9 us: 1.03x faster                                                 |
| django_template         | 36.1 ms                                                                | 35.0 ms: 1.03x faster                                                 |
| regex_effbot            | 2.81 ms                                                                | 2.73 ms: 1.03x faster                                                 |
| fannkuch                | 378 ms                                                                 | 367 ms: 1.03x faster                                                  |
| scimark_sor             | 127 ms                                                                 | 124 ms: 1.03x faster                                                  |
| richards_super          | 50.9 ms                                                                | 49.5 ms: 1.03x faster                                                 |
| chaos                   | 58.6 ms                                                                | 57.4 ms: 1.02x faster                                                 |
| async_generators        | 359 ms                                                                 | 352 ms: 1.02x faster                                                  |
| pickle_pure_python      | 321 us                                                                 | 315 us: 1.02x faster                                                  |
| regex_dna               | 179 ms                                                                 | 176 ms: 1.02x faster                                                  |
| spectral_norm           | 101 ms                                                                 | 99.1 ms: 1.01x faster                                                 |
| sqlglot_normalize       | 104 ms                                                                 | 102 ms: 1.01x faster                                                  |
| regex_v8                | 25.0 ms                                                                | 24.7 ms: 1.01x faster                                                 |
| pprint_safe_repr        | 712 ms                                                                 | 704 ms: 1.01x faster                                                  |
| hexiom                  | 5.86 ms                                                                | 5.80 ms: 1.01x faster                                                 |
| deepcopy_reduce         | 2.58 us                                                                | 2.55 us: 1.01x faster                                                 |
| raytrace                | 258 ms                                                                 | 256 ms: 1.01x faster                                                  |
| sqlglot_optimize        | 52.1 ms                                                                | 51.7 ms: 1.01x faster                                                 |
| scimark_monte_carlo     | 62.8 ms                                                                | 62.3 ms: 1.01x faster                                                 |
| deepcopy                | 253 us                                                                 | 251 us: 1.01x faster                                                  |
| pprint_pformat          | 1.46 sec                                                               | 1.45 sec: 1.01x faster                                                |
| sympy_integrate         | 19.9 ms                                                                | 19.7 ms: 1.01x faster                                                 |
| sympy_str               | 273 ms                                                                 | 271 ms: 1.01x faster                                                  |
| sympy_sum               | 153 ms                                                                 | 152 ms: 1.01x faster                                                  |
| sqlalchemy_declarative  | 126 ms                                                                 | 125 ms: 1.01x faster                                                  |
| create_gc_cycles        | 1.85 ms                                                                | 1.84 ms: 1.01x faster                                                 |
| logging_silent          | 106 ns                                                                 | 106 ns: 1.01x faster                                                  |
| comprehensions          | 17.2 us                                                                | 17.1 us: 1.00x faster                                                 |
| sympy_expand            | 459 ms                                                                 | 457 ms: 1.00x faster                                                  |
| json_loads              | 26.2 us                                                                | 26.1 us: 1.00x faster                                                 |
| dulwich_log             | 75.7 ms                                                                | 75.5 ms: 1.00x faster                                                 |
| 2to3                    | 255 ms                                                                 | 255 ms: 1.00x slower                                                  |
| scimark_sparse_mat_mult | 4.22 ms                                                                | 4.23 ms: 1.00x slower                                                 |
| python_startup_no_site  | 7.51 ms                                                                | 7.53 ms: 1.00x slower                                                 |
| python_startup          | 14.6 ms                                                                | 14.7 ms: 1.00x slower                                                 |
| coverage                | 79.0 ms                                                                | 79.4 ms: 1.00x slower                                                 |
| pyflate                 | 423 ms                                                                 | 424 ms: 1.00x slower                                                  |
| regex_compile           | 126 ms                                                                 | 127 ms: 1.01x slower                                                  |
| subparsers              | 22.0 ms                                                                | 22.2 ms: 1.01x slower                                                 |
| deltablue               | 3.16 ms                                                                | 3.18 ms: 1.01x slower                                                 |
| sqlglot_transpile       | 1.56 ms                                                                | 1.57 ms: 1.01x slower                                                 |
| meteor_contest          | 98.2 ms                                                                | 99.0 ms: 1.01x slower                                                 |
| genshi_xml              | 49.6 ms                                                                | 50.0 ms: 1.01x slower                                                 |
| json_dumps              | 11.3 ms                                                                | 11.4 ms: 1.01x slower                                                 |
| bpe_tokeniser           | 4.21 sec                                                               | 4.27 sec: 1.01x slower                                                |
| sqlglot_parse           | 1.25 ms                                                                | 1.27 ms: 1.02x slower                                                 |
| scimark_lu              | 110 ms                                                                 | 112 ms: 1.02x slower                                                  |
| logging_simple          | 6.02 us                                                                | 6.12 us: 1.02x slower                                                 |
| coroutines              | 21.7 ms                                                                | 22.2 ms: 1.02x slower                                                 |
| genshi_text             | 21.5 ms                                                                | 22.1 ms: 1.03x slower                                                 |
| telco                   | 7.10 ms                                                                | 7.30 ms: 1.03x slower                                                 |
| crypto_pyaes            | 67.0 ms                                                                | 68.9 ms: 1.03x slower                                                 |
| gc_traversal            | 4.02 ms                                                                | 4.19 ms: 1.04x slower                                                 |
| Geometric mean          | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (37): nbody, typing_runtime_protocols, async_tree_memoization_tg, k_core, generators, sphinx, pylint, logging_format, async_tree_io, xml_etree_parse, sqlalchemy_imperative, go, xml_etree_process, mako, xml_etree_iterparse, async_tree_none_tg, async_tree_cpu_io_mixed, float, pathlib, shortest_path, pycparser, bench_thread_pool, asyncio_websockets, unpickle_pure_python, pidigits, docutils, async_tree_none, many_optionals, async_tree_cpu_io_mixed_tg, xml_etree_generate, json, tomli_loads, sqlite_synth, bench_mp_pool, connected_components, async_tree_io_tg, async_tree_memoization

- Geometric mean (including insignificant results): 1.004x faster

# HPT report

- Reliability score: 95.92% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x