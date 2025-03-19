# Results vs. base

- fork: colesbury
- ref: gh_128421_frame
- machine: linux-x86_64
- commit hash: 44f8c85
- commit date: 2025-03-19
- overall geometric mean: 1.002x slower
- HPT reliability: 99.47%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250319-vultr-x86_64-python-a4832f6b9a62771725b1-3.14.0a6+-a4832f6 | bm-20250319-vultr-x86_64-colesbury-gh_128421_frame-3.14.0a6+-44f8c85 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 299 ms                                                                 | 299 ms: 1.00x faster                                                 |
| html5lib       | 73.0 ms                                                                | 72.6 ms: 1.01x faster                                                |
| sphinx         | 1.10 sec                                                               | 1.09 sec: 1.01x faster                                               |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                         |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250319-vultr-x86_64-python-a4832f6b9a62771725b1-3.14.0a6+-a4832f6 | bm-20250319-vultr-x86_64-colesbury-gh_128421_frame-3.14.0a6+-44f8c85 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_generators           | 380 ms                                                                 | 375 ms: 1.01x faster                                                 |
| async_tree_none_tg         | 241 ms                                                                 | 238 ms: 1.01x faster                                                 |
| async_tree_io_tg           | 556 ms                                                                 | 551 ms: 1.01x faster                                                 |
| async_tree_io              | 586 ms                                                                 | 581 ms: 1.01x faster                                                 |
| async_tree_memoization     | 341 ms                                                                 | 338 ms: 1.01x faster                                                 |
| coroutines                 | 23.1 ms                                                                | 23.3 ms: 1.01x slower                                                |
| async_tree_cpu_io_mixed    | 523 ms                                                                 | 605 ms: 1.16x slower                                                 |
| async_tree_cpu_io_mixed_tg | 492 ms                                                                 | 575 ms: 1.17x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.02x slower                                                         |

Benchmark hidden because not significant (3): async_tree_none, async_tree_memoization_tg, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250319-vultr-x86_64-python-a4832f6b9a62771725b1-3.14.0a6+-a4832f6 | bm-20250319-vultr-x86_64-colesbury-gh_128421_frame-3.14.0a6+-44f8c85 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| nbody          | 136 ms                                                                 | 133 ms: 1.02x faster                                                 |
| float          | 77.9 ms                                                                | 77.6 ms: 1.00x faster                                                |
| pidigits       | 191 ms                                                                 | 222 ms: 1.16x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250319-vultr-x86_64-python-a4832f6b9a62771725b1-3.14.0a6+-a4832f6 | bm-20250319-vultr-x86_64-colesbury-gh_128421_frame-3.14.0a6+-44f8c85 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 2.78 ms                                                                | 2.69 ms: 1.03x faster                                                |
| regex_compile  | 160 ms                                                                 | 158 ms: 1.01x faster                                                 |
| regex_v8       | 21.4 ms                                                                | 21.7 ms: 1.02x slower                                                |
| regex_dna      | 177 ms                                                                 | 182 ms: 1.03x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250319-vultr-x86_64-python-a4832f6b9a62771725b1-3.14.0a6+-a4832f6 | bm-20250319-vultr-x86_64-colesbury-gh_128421_frame-3.14.0a6+-44f8c85 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| tomli_loads          | 2.39 sec                                                               | 2.36 sec: 1.01x faster                                               |
| xml_etree_generate   | 97.0 ms                                                                | 96.3 ms: 1.01x faster                                                |
| json_loads           | 29.1 us                                                                | 29.0 us: 1.00x faster                                                |
| xml_etree_process    | 70.5 ms                                                                | 70.3 ms: 1.00x faster                                                |
| json_dumps           | 12.9 ms                                                                | 12.9 ms: 1.00x faster                                                |
| xml_etree_iterparse  | 88.3 ms                                                                | 88.7 ms: 1.00x slower                                                |
| unpickle_pure_python | 256 us                                                                 | 258 us: 1.01x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                         |

Benchmark hidden because not significant (2): xml_etree_parse, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250319-vultr-x86_64-python-a4832f6b9a62771725b1-3.14.0a6+-a4832f6 | bm-20250319-vultr-x86_64-colesbury-gh_128421_frame-3.14.0a6+-44f8c85 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 15.8 ms                                                                | 15.7 ms: 1.00x faster                                                |
| python_startup_no_site | 11.1 ms                                                                | 11.1 ms: 1.00x faster                                                |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250319-vultr-x86_64-python-a4832f6b9a62771725b1-3.14.0a6+-a4832f6 | bm-20250319-vultr-x86_64-colesbury-gh_128421_frame-3.14.0a6+-44f8c85 |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_text     | 28.9 ms                                                                | 28.3 ms: 1.02x faster                                                |
| genshi_xml      | 61.1 ms                                                                | 60.0 ms: 1.02x faster                                                |
| mako            | 15.9 ms                                                                | 15.9 ms: 1.00x slower                                                |
| django_template | 42.7 ms                                                                | 43.3 ms: 1.02x slower                                                |
| Geometric mean  | (ref)                                                                  | 1.00x faster                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20250319-vultr-x86_64-python-a4832f6b9a62771725b1-3.14.0a6+-a4832f6 | bm-20250319-vultr-x86_64-colesbury-gh_128421_frame-3.14.0a6+-44f8c85 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| spectral_norm              | 117 ms                                                                 | 111 ms: 1.05x faster                                                 |
| create_gc_cycles           | 1.39 ms                                                                | 1.34 ms: 1.04x faster                                                |
| regex_effbot               | 2.78 ms                                                                | 2.69 ms: 1.03x faster                                                |
| telco                      | 9.12 ms                                                                | 8.91 ms: 1.02x faster                                                |
| gc_traversal               | 1.82 ms                                                                | 1.78 ms: 1.02x faster                                                |
| nbody                      | 136 ms                                                                 | 133 ms: 1.02x faster                                                 |
| genshi_text                | 28.9 ms                                                                | 28.3 ms: 1.02x faster                                                |
| mdp                        | 2.73 sec                                                               | 2.68 sec: 1.02x faster                                               |
| meteor_contest             | 132 ms                                                                 | 129 ms: 1.02x faster                                                 |
| sqlite_synth               | 2.04 us                                                                | 2.01 us: 1.02x faster                                                |
| pprint_safe_repr           | 844 ms                                                                 | 829 ms: 1.02x faster                                                 |
| genshi_xml                 | 61.1 ms                                                                | 60.0 ms: 1.02x faster                                                |
| typing_runtime_protocols   | 203 us                                                                 | 199 us: 1.02x faster                                                 |
| pprint_pformat             | 1.74 sec                                                               | 1.71 sec: 1.02x faster                                               |
| async_generators           | 380 ms                                                                 | 375 ms: 1.01x faster                                                 |
| regex_compile              | 160 ms                                                                 | 158 ms: 1.01x faster                                                 |
| bpe_tokeniser              | 4.91 sec                                                               | 4.84 sec: 1.01x faster                                               |
| async_tree_none_tg         | 241 ms                                                                 | 238 ms: 1.01x faster                                                 |
| tomli_loads                | 2.39 sec                                                               | 2.36 sec: 1.01x faster                                               |
| crypto_pyaes               | 89.4 ms                                                                | 88.4 ms: 1.01x faster                                                |
| pyflate                    | 512 ms                                                                 | 507 ms: 1.01x faster                                                 |
| many_optionals             | 1.19 ms                                                                | 1.17 ms: 1.01x faster                                                |
| dulwich_log                | 74.4 ms                                                                | 73.7 ms: 1.01x faster                                                |
| fannkuch                   | 504 ms                                                                 | 499 ms: 1.01x faster                                                 |
| async_tree_io_tg           | 556 ms                                                                 | 551 ms: 1.01x faster                                                 |
| sqlglot_v2_parse           | 1.61 ms                                                                | 1.60 ms: 1.01x faster                                                |
| async_tree_io              | 586 ms                                                                 | 581 ms: 1.01x faster                                                 |
| xml_etree_generate         | 97.0 ms                                                                | 96.3 ms: 1.01x faster                                                |
| async_tree_memoization     | 341 ms                                                                 | 338 ms: 1.01x faster                                                 |
| scimark_monte_carlo        | 84.4 ms                                                                | 83.9 ms: 1.01x faster                                                |
| sphinx                     | 1.10 sec                                                               | 1.09 sec: 1.01x faster                                               |
| html5lib                   | 73.0 ms                                                                | 72.6 ms: 1.01x faster                                                |
| json_loads                 | 29.1 us                                                                | 29.0 us: 1.00x faster                                                |
| k_core                     | 2.31 sec                                                               | 2.31 sec: 1.00x faster                                               |
| float                      | 77.9 ms                                                                | 77.6 ms: 1.00x faster                                                |
| comprehensions             | 20.9 us                                                                | 20.8 us: 1.00x faster                                                |
| xml_etree_process          | 70.5 ms                                                                | 70.3 ms: 1.00x faster                                                |
| python_startup             | 15.8 ms                                                                | 15.7 ms: 1.00x faster                                                |
| python_startup_no_site     | 11.1 ms                                                                | 11.1 ms: 1.00x faster                                                |
| 2to3                       | 299 ms                                                                 | 299 ms: 1.00x faster                                                 |
| hexiom                     | 7.68 ms                                                                | 7.67 ms: 1.00x faster                                                |
| json_dumps                 | 12.9 ms                                                                | 12.9 ms: 1.00x faster                                                |
| mako                       | 15.9 ms                                                                | 15.9 ms: 1.00x slower                                                |
| chaos                      | 69.9 ms                                                                | 70.1 ms: 1.00x slower                                                |
| xml_etree_iterparse        | 88.3 ms                                                                | 88.7 ms: 1.00x slower                                                |
| deepcopy                   | 311 us                                                                 | 313 us: 1.01x slower                                                 |
| deepcopy_memo              | 39.1 us                                                                | 39.3 us: 1.01x slower                                                |
| deltablue                  | 3.86 ms                                                                | 3.89 ms: 1.01x slower                                                |
| unpickle_pure_python       | 256 us                                                                 | 258 us: 1.01x slower                                                 |
| scimark_sor                | 138 ms                                                                 | 139 ms: 1.01x slower                                                 |
| coroutines                 | 23.1 ms                                                                | 23.3 ms: 1.01x slower                                                |
| go                         | 144 ms                                                                 | 145 ms: 1.01x slower                                                 |
| deepcopy_reduce            | 3.18 us                                                                | 3.22 us: 1.01x slower                                                |
| nqueens                    | 98.4 ms                                                                | 99.8 ms: 1.01x slower                                                |
| richards                   | 55.3 ms                                                                | 56.1 ms: 1.01x slower                                                |
| django_template            | 42.7 ms                                                                | 43.3 ms: 1.02x slower                                                |
| raytrace                   | 324 ms                                                                 | 330 ms: 1.02x slower                                                 |
| regex_v8                   | 21.4 ms                                                                | 21.7 ms: 1.02x slower                                                |
| richards_super             | 64.2 ms                                                                | 65.5 ms: 1.02x slower                                                |
| scimark_lu                 | 142 ms                                                                 | 146 ms: 1.02x slower                                                 |
| regex_dna                  | 177 ms                                                                 | 182 ms: 1.03x slower                                                 |
| generators                 | 31.7 ms                                                                | 33.1 ms: 1.05x slower                                                |
| logging_silent             | 113 ns                                                                 | 118 ns: 1.05x slower                                                 |
| coverage                   | 97.4 ms                                                                | 104 ms: 1.06x slower                                                 |
| async_tree_cpu_io_mixed    | 523 ms                                                                 | 605 ms: 1.16x slower                                                 |
| pidigits                   | 191 ms                                                                 | 222 ms: 1.16x slower                                                 |
| async_tree_cpu_io_mixed_tg | 492 ms                                                                 | 575 ms: 1.17x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                         |

Benchmark hidden because not significant (29): sqlglot_v2_transpile, subparsers, docutils, pylint, async_tree_none, sympy_sum, async_tree_memoization_tg, scimark_sparse_mat_mult, sqlglot_v2_normalize, scimark_fft, logging_format, bench_mp_pool, pycparser, sqlglot_v2_optimize, sympy_integrate, shortest_path, sqlalchemy_declarative, sympy_expand, logging_simple, json, thrift, bench_thread_pool, sqlalchemy_imperative, asyncio_websockets, pathlib, sympy_str, xml_etree_parse, pickle_pure_python, connected_components

- Geometric mean (including insignificant results): 1.002x slower

# HPT report

- Reliability score: 99.47% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.99x