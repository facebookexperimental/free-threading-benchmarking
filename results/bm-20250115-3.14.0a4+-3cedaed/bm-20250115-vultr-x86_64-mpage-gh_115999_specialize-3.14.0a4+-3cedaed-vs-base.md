# Results vs. base

- fork: mpage
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: 3cedaed
- commit date: 2025-01-15
- overall geometric mean: 1.016x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4+-d05140f | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-3cedaed |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 253 ms                                                                 | 249 ms: 1.02x faster                                                  |
| docutils       | 2.58 sec                                                               | 2.54 sec: 1.02x faster                                                |
| sphinx         | 989 ms                                                                 | 977 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4+-d05140f | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-3cedaed |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| coroutines                 | 21.9 ms                                                                | 20.8 ms: 1.05x faster                                                 |
| async_tree_io_tg           | 612 ms                                                                 | 593 ms: 1.03x faster                                                  |
| async_tree_memoization     | 325 ms                                                                 | 319 ms: 1.02x faster                                                  |
| async_tree_cpu_io_mixed    | 569 ms                                                                 | 560 ms: 1.02x faster                                                  |
| async_tree_none_tg         | 256 ms                                                                 | 252 ms: 1.02x faster                                                  |
| async_generators           | 322 ms                                                                 | 317 ms: 1.01x faster                                                  |
| async_tree_memoization_tg  | 303 ms                                                                 | 299 ms: 1.01x faster                                                  |
| async_tree_cpu_io_mixed_tg | 549 ms                                                                 | 545 ms: 1.01x faster                                                  |
| Geometric mean             | (ref)                                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (3): async_tree_none, async_tree_io, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4+-d05140f | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-3cedaed |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 229 ms                                                                 | 211 ms: 1.09x faster                                                  |
| nbody          | 96.1 ms                                                                | 89.3 ms: 1.08x faster                                                 |
| float          | 74.9 ms                                                                | 72.5 ms: 1.03x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4+-d05140f | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-3cedaed |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 2.80 ms                                                                | 2.69 ms: 1.04x faster                                                 |
| regex_compile  | 127 ms                                                                 | 126 ms: 1.01x faster                                                  |
| regex_v8       | 22.8 ms                                                                | 23.1 ms: 1.01x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4+-d05140f | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-3cedaed |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 11.7 ms                                                                | 11.2 ms: 1.04x faster                                                 |
| pickle_pure_python   | 314 us                                                                 | 304 us: 1.03x faster                                                  |
| unpickle_pure_python | 214 us                                                                 | 209 us: 1.02x faster                                                  |
| xml_etree_iterparse  | 91.5 ms                                                                | 89.7 ms: 1.02x faster                                                 |
| json_loads           | 27.8 us                                                                | 27.3 us: 1.02x faster                                                 |
| xml_etree_process    | 59.0 ms                                                                | 58.4 ms: 1.01x faster                                                 |
| xml_etree_parse      | 128 ms                                                                 | 129 ms: 1.01x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (2): xml_etree_generate, tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4+-d05140f | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-3cedaed |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 14.7 ms                                                                | 14.6 ms: 1.01x faster                                                 |
| python_startup_no_site | 7.46 ms                                                                | 7.42 ms: 1.01x faster                                                 |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4+-d05140f | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-3cedaed |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.8 ms                                                                | 33.7 ms: 1.03x faster                                                 |
| genshi_xml      | 48.1 ms                                                                | 46.9 ms: 1.03x faster                                                 |
| genshi_text     | 20.8 ms                                                                | 20.4 ms: 1.02x faster                                                 |
| mako            | 11.7 ms                                                                | 11.7 ms: 1.00x faster                                                 |
| Geometric mean  | (ref)                                                                  | 1.02x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4+-d05140f | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-3cedaed |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits                   | 229 ms                                                                 | 211 ms: 1.09x faster                                                  |
| nbody                      | 96.1 ms                                                                | 89.3 ms: 1.08x faster                                                 |
| coroutines                 | 21.9 ms                                                                | 20.8 ms: 1.05x faster                                                 |
| generators                 | 28.1 ms                                                                | 26.6 ms: 1.05x faster                                                 |
| deltablue                  | 3.21 ms                                                                | 3.06 ms: 1.05x faster                                                 |
| go                         | 119 ms                                                                 | 114 ms: 1.05x faster                                                  |
| raytrace                   | 268 ms                                                                 | 256 ms: 1.04x faster                                                  |
| pyflate                    | 420 ms                                                                 | 402 ms: 1.04x faster                                                  |
| json_dumps                 | 11.7 ms                                                                | 11.2 ms: 1.04x faster                                                 |
| regex_effbot               | 2.80 ms                                                                | 2.69 ms: 1.04x faster                                                 |
| richards_super             | 49.6 ms                                                                | 47.7 ms: 1.04x faster                                                 |
| richards                   | 43.5 ms                                                                | 42.0 ms: 1.03x faster                                                 |
| pickle_pure_python         | 314 us                                                                 | 304 us: 1.03x faster                                                  |
| chaos                      | 58.6 ms                                                                | 56.7 ms: 1.03x faster                                                 |
| sqlglot_parse              | 1.28 ms                                                                | 1.24 ms: 1.03x faster                                                 |
| django_template            | 34.8 ms                                                                | 33.7 ms: 1.03x faster                                                 |
| float                      | 74.9 ms                                                                | 72.5 ms: 1.03x faster                                                 |
| async_tree_io_tg           | 612 ms                                                                 | 593 ms: 1.03x faster                                                  |
| sqlglot_transpile          | 1.58 ms                                                                | 1.54 ms: 1.03x faster                                                 |
| thrift                     | 747 us                                                                 | 727 us: 1.03x faster                                                  |
| sqlite_synth               | 2.22 us                                                                | 2.16 us: 1.03x faster                                                 |
| meteor_contest             | 99.5 ms                                                                | 96.9 ms: 1.03x faster                                                 |
| genshi_xml                 | 48.1 ms                                                                | 46.9 ms: 1.03x faster                                                 |
| unpickle_pure_python       | 214 us                                                                 | 209 us: 1.02x faster                                                  |
| sqlglot_optimize           | 52.6 ms                                                                | 51.4 ms: 1.02x faster                                                 |
| scimark_monte_carlo        | 64.0 ms                                                                | 62.6 ms: 1.02x faster                                                 |
| subparsers                 | 21.8 ms                                                                | 21.4 ms: 1.02x faster                                                 |
| telco                      | 7.25 ms                                                                | 7.09 ms: 1.02x faster                                                 |
| genshi_text                | 20.8 ms                                                                | 20.4 ms: 1.02x faster                                                 |
| sqlglot_normalize          | 104 ms                                                                 | 101 ms: 1.02x faster                                                  |
| pycparser                  | 1.12 sec                                                               | 1.10 sec: 1.02x faster                                                |
| pathlib                    | 18.2 ms                                                                | 17.9 ms: 1.02x faster                                                 |
| xml_etree_iterparse        | 91.5 ms                                                                | 89.7 ms: 1.02x faster                                                 |
| async_tree_memoization     | 325 ms                                                                 | 319 ms: 1.02x faster                                                  |
| bpe_tokeniser              | 4.25 sec                                                               | 4.17 sec: 1.02x faster                                                |
| scimark_sor                | 116 ms                                                                 | 114 ms: 1.02x faster                                                  |
| many_optionals             | 1.03 ms                                                                | 1.01 ms: 1.02x faster                                                 |
| spectral_norm              | 97.6 ms                                                                | 95.9 ms: 1.02x faster                                                 |
| docutils                   | 2.58 sec                                                               | 2.54 sec: 1.02x faster                                                |
| logging_format             | 6.75 us                                                                | 6.63 us: 1.02x faster                                                 |
| comprehensions             | 16.9 us                                                                | 16.6 us: 1.02x faster                                                 |
| json_loads                 | 27.8 us                                                                | 27.3 us: 1.02x faster                                                 |
| async_tree_cpu_io_mixed    | 569 ms                                                                 | 560 ms: 1.02x faster                                                  |
| async_tree_none_tg         | 256 ms                                                                 | 252 ms: 1.02x faster                                                  |
| 2to3                       | 253 ms                                                                 | 249 ms: 1.02x faster                                                  |
| async_generators           | 322 ms                                                                 | 317 ms: 1.01x faster                                                  |
| json                       | 4.98 ms                                                                | 4.91 ms: 1.01x faster                                                 |
| shortest_path              | 433 ms                                                                 | 427 ms: 1.01x faster                                                  |
| async_tree_memoization_tg  | 303 ms                                                                 | 299 ms: 1.01x faster                                                  |
| sympy_str                  | 271 ms                                                                 | 267 ms: 1.01x faster                                                  |
| sphinx                     | 989 ms                                                                 | 977 ms: 1.01x faster                                                  |
| pprint_safe_repr           | 689 ms                                                                 | 681 ms: 1.01x faster                                                  |
| sqlalchemy_declarative     | 130 ms                                                                 | 128 ms: 1.01x faster                                                  |
| scimark_fft                | 314 ms                                                                 | 311 ms: 1.01x faster                                                  |
| sympy_expand               | 452 ms                                                                 | 448 ms: 1.01x faster                                                  |
| hexiom                     | 5.77 ms                                                                | 5.72 ms: 1.01x faster                                                 |
| sympy_integrate            | 19.7 ms                                                                | 19.5 ms: 1.01x faster                                                 |
| xml_etree_process          | 59.0 ms                                                                | 58.4 ms: 1.01x faster                                                 |
| pprint_pformat             | 1.40 sec                                                               | 1.39 sec: 1.01x faster                                                |
| bench_thread_pool          | 1.04 ms                                                                | 1.03 ms: 1.01x faster                                                 |
| sympy_sum                  | 152 ms                                                                 | 151 ms: 1.01x faster                                                  |
| async_tree_cpu_io_mixed_tg | 549 ms                                                                 | 545 ms: 1.01x faster                                                  |
| bench_mp_pool              | 88.8 ms                                                                | 88.2 ms: 1.01x faster                                                 |
| python_startup             | 14.7 ms                                                                | 14.6 ms: 1.01x faster                                                 |
| regex_compile              | 127 ms                                                                 | 126 ms: 1.01x faster                                                  |
| python_startup_no_site     | 7.46 ms                                                                | 7.42 ms: 1.01x faster                                                 |
| coverage                   | 80.0 ms                                                                | 79.5 ms: 1.01x faster                                                 |
| sqlalchemy_imperative      | 19.2 ms                                                                | 19.1 ms: 1.01x faster                                                 |
| deepcopy                   | 255 us                                                                 | 253 us: 1.01x faster                                                  |
| nqueens                    | 77.2 ms                                                                | 76.9 ms: 1.00x faster                                                 |
| dulwich_log                | 75.5 ms                                                                | 75.2 ms: 1.00x faster                                                 |
| mako                       | 11.7 ms                                                                | 11.7 ms: 1.00x faster                                                 |
| fannkuch                   | 366 ms                                                                 | 368 ms: 1.01x slower                                                  |
| xml_etree_parse            | 128 ms                                                                 | 129 ms: 1.01x slower                                                  |
| crypto_pyaes               | 66.5 ms                                                                | 66.9 ms: 1.01x slower                                                 |
| typing_runtime_protocols   | 154 us                                                                 | 155 us: 1.01x slower                                                  |
| deepcopy_memo              | 30.0 us                                                                | 30.3 us: 1.01x slower                                                 |
| regex_v8                   | 22.8 ms                                                                | 23.1 ms: 1.01x slower                                                 |
| logging_silent             | 105 ns                                                                 | 107 ns: 1.02x slower                                                  |
| scimark_sparse_mat_mult    | 4.18 ms                                                                | 4.33 ms: 1.04x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (15): async_tree_none, async_tree_io, pylint, k_core, xml_etree_generate, tomli_loads, gc_traversal, asyncio_websockets, connected_components, deepcopy_reduce, regex_dna, scimark_lu, logging_simple, mdp, create_gc_cycles

- Geometric mean (including insignificant results): 1.016x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.02x