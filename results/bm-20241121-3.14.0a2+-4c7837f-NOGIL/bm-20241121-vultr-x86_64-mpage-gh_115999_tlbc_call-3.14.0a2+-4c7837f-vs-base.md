# Results vs. base

- fork: mpage
- ref: gh_115999_tlbc_call
- machine: linux-x86_64
- commit hash: 4c7837f
- commit date: 2024-11-21
- overall geometric mean: 1.03x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2+-32428cf | bm-20241121-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-4c7837f |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 418 ms                                                                 | 411 ms: 1.02x faster                                                 |
| docutils       | 3.41 sec                                                               | 3.32 sec: 1.03x faster                                               |
| sphinx         | 1.33 sec                                                               | 1.30 sec: 1.03x faster                                               |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                         |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2+-32428cf | bm-20241121-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-4c7837f |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| coroutines                 | 31.8 ms                                                                | 29.2 ms: 1.09x faster                                                |
| async_tree_memoization     | 529 ms                                                                 | 512 ms: 1.03x faster                                                 |
| async_tree_none_tg         | 394 ms                                                                 | 382 ms: 1.03x faster                                                 |
| async_tree_io              | 969 ms                                                                 | 941 ms: 1.03x faster                                                 |
| async_tree_io_tg           | 939 ms                                                                 | 914 ms: 1.03x faster                                                 |
| async_tree_memoization_tg  | 493 ms                                                                 | 481 ms: 1.02x faster                                                 |
| async_tree_none            | 430 ms                                                                 | 421 ms: 1.02x faster                                                 |
| async_generators           | 488 ms                                                                 | 481 ms: 1.01x faster                                                 |
| async_tree_cpu_io_mixed    | 697 ms                                                                 | 687 ms: 1.01x faster                                                 |
| async_tree_cpu_io_mixed_tg | 660 ms                                                                 | 657 ms: 1.01x faster                                                 |
| Geometric mean             | (ref)                                                                  | 1.03x faster                                                         |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2+-32428cf | bm-20241121-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-4c7837f |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 152 ms                                                                 | 148 ms: 1.03x faster                                                 |
| nbody          | 201 ms                                                                 | 200 ms: 1.00x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                         |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2+-32428cf | bm-20241121-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-4c7837f |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_compile  | 230 ms                                                                 | 219 ms: 1.05x faster                                                 |
| regex_effbot   | 2.88 ms                                                                | 2.81 ms: 1.03x faster                                                |
| regex_dna      | 183 ms                                                                 | 185 ms: 1.01x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                         |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2+-32428cf | bm-20241121-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-4c7837f |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| unpickle_pure_python | 428 us                                                                 | 388 us: 1.10x faster                                                 |
| pickle_pure_python   | 633 us                                                                 | 598 us: 1.06x faster                                                 |
| xml_etree_process    | 93.6 ms                                                                | 90.0 ms: 1.04x faster                                                |
| xml_etree_iterparse  | 110 ms                                                                 | 105 ms: 1.04x faster                                                 |
| xml_etree_generate   | 113 ms                                                                 | 110 ms: 1.04x faster                                                 |
| tomli_loads          | 3.25 sec                                                               | 3.16 sec: 1.03x faster                                               |
| json_loads           | 28.7 us                                                                | 28.3 us: 1.01x faster                                                |
| xml_etree_parse      | 133 ms                                                                 | 133 ms: 1.00x faster                                                 |
| Geometric mean       | (ref)                                                                  | 1.03x faster                                                         |

Benchmark hidden because not significant (1): json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2+-32428cf | bm-20241121-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-4c7837f |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup | 17.6 ms                                                                | 17.6 ms: 1.00x faster                                                |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                         |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2+-32428cf | bm-20241121-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-4c7837f |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 21.0 ms                                                                | 19.2 ms: 1.09x faster                                                |
| django_template | 65.3 ms                                                                | 62.3 ms: 1.05x faster                                                |
| genshi_text     | 41.0 ms                                                                | 39.2 ms: 1.05x faster                                                |
| genshi_xml      | 83.2 ms                                                                | 81.0 ms: 1.03x faster                                                |
| Geometric mean  | (ref)                                                                  | 1.05x faster                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2+-32428cf | bm-20241121-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-4c7837f |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| deepcopy_memo              | 54.3 us                                                                | 48.4 us: 1.12x faster                                                |
| unpickle_pure_python       | 428 us                                                                 | 388 us: 1.10x faster                                                 |
| mako                       | 21.0 ms                                                                | 19.2 ms: 1.09x faster                                                |
| bpe_tokeniser              | 6.22 sec                                                               | 5.69 sec: 1.09x faster                                               |
| coroutines                 | 31.8 ms                                                                | 29.2 ms: 1.09x faster                                                |
| deltablue                  | 9.44 ms                                                                | 8.79 ms: 1.07x faster                                                |
| deepcopy_reduce            | 4.64 us                                                                | 4.33 us: 1.07x faster                                                |
| hexiom                     | 12.6 ms                                                                | 11.8 ms: 1.07x faster                                                |
| deepcopy                   | 439 us                                                                 | 413 us: 1.06x faster                                                 |
| chaos                      | 125 ms                                                                 | 117 ms: 1.06x faster                                                 |
| raytrace                   | 640 ms                                                                 | 602 ms: 1.06x faster                                                 |
| pprint_pformat             | 2.76 sec                                                               | 2.60 sec: 1.06x faster                                               |
| sqlglot_normalize          | 184 ms                                                                 | 174 ms: 1.06x faster                                                 |
| sqlglot_optimize           | 91.2 ms                                                                | 85.9 ms: 1.06x faster                                                |
| pprint_safe_repr           | 1.32 sec                                                               | 1.25 sec: 1.06x faster                                               |
| pickle_pure_python         | 633 us                                                                 | 598 us: 1.06x faster                                                 |
| richards                   | 92.8 ms                                                                | 88.1 ms: 1.05x faster                                                |
| logging_silent             | 219 ns                                                                 | 208 ns: 1.05x faster                                                 |
| regex_compile              | 230 ms                                                                 | 219 ms: 1.05x faster                                                 |
| scimark_lu                 | 248 ms                                                                 | 236 ms: 1.05x faster                                                 |
| django_template            | 65.3 ms                                                                | 62.3 ms: 1.05x faster                                                |
| scimark_sor                | 280 ms                                                                 | 267 ms: 1.05x faster                                                 |
| comprehensions             | 30.9 us                                                                | 29.5 us: 1.05x faster                                                |
| genshi_text                | 41.0 ms                                                                | 39.2 ms: 1.05x faster                                                |
| scimark_sparse_mat_mult    | 6.16 ms                                                                | 5.92 ms: 1.04x faster                                                |
| fannkuch                   | 573 ms                                                                 | 551 ms: 1.04x faster                                                 |
| pyflate                    | 782 ms                                                                 | 752 ms: 1.04x faster                                                 |
| richards_super             | 110 ms                                                                 | 106 ms: 1.04x faster                                                 |
| xml_etree_process          | 93.6 ms                                                                | 90.0 ms: 1.04x faster                                                |
| xml_etree_iterparse        | 110 ms                                                                 | 105 ms: 1.04x faster                                                 |
| coverage                   | 104 ms                                                                 | 101 ms: 1.04x faster                                                 |
| xml_etree_generate         | 113 ms                                                                 | 110 ms: 1.04x faster                                                 |
| go                         | 301 ms                                                                 | 291 ms: 1.03x faster                                                 |
| nqueens                    | 117 ms                                                                 | 113 ms: 1.03x faster                                                 |
| sqlglot_parse              | 2.89 ms                                                                | 2.80 ms: 1.03x faster                                                |
| sqlglot_transpile          | 3.41 ms                                                                | 3.30 ms: 1.03x faster                                                |
| typing_runtime_protocols   | 251 us                                                                 | 243 us: 1.03x faster                                                 |
| subparsers                 | 36.4 ms                                                                | 35.3 ms: 1.03x faster                                                |
| async_tree_memoization     | 529 ms                                                                 | 512 ms: 1.03x faster                                                 |
| logging_format             | 13.6 us                                                                | 13.1 us: 1.03x faster                                                |
| async_tree_none_tg         | 394 ms                                                                 | 382 ms: 1.03x faster                                                 |
| spectral_norm              | 162 ms                                                                 | 158 ms: 1.03x faster                                                 |
| pycparser                  | 1.72 sec                                                               | 1.67 sec: 1.03x faster                                               |
| async_tree_io              | 969 ms                                                                 | 941 ms: 1.03x faster                                                 |
| many_optionals             | 1.46 ms                                                                | 1.42 ms: 1.03x faster                                                |
| float                      | 152 ms                                                                 | 148 ms: 1.03x faster                                                 |
| tomli_loads                | 3.25 sec                                                               | 3.16 sec: 1.03x faster                                               |
| async_tree_io_tg           | 939 ms                                                                 | 914 ms: 1.03x faster                                                 |
| scimark_monte_carlo        | 128 ms                                                                 | 125 ms: 1.03x faster                                                 |
| genshi_xml                 | 83.2 ms                                                                | 81.0 ms: 1.03x faster                                                |
| docutils                   | 3.41 sec                                                               | 3.32 sec: 1.03x faster                                               |
| logging_simple             | 12.3 us                                                                | 11.9 us: 1.03x faster                                                |
| scimark_fft                | 428 ms                                                                 | 417 ms: 1.03x faster                                                 |
| sphinx                     | 1.33 sec                                                               | 1.30 sec: 1.03x faster                                               |
| regex_effbot               | 2.88 ms                                                                | 2.81 ms: 1.03x faster                                                |
| async_tree_memoization_tg  | 493 ms                                                                 | 481 ms: 1.02x faster                                                 |
| sympy_integrate            | 33.4 ms                                                                | 32.6 ms: 1.02x faster                                                |
| shortest_path              | 581 ms                                                                 | 569 ms: 1.02x faster                                                 |
| sympy_expand               | 1.06 sec                                                               | 1.04 sec: 1.02x faster                                               |
| async_tree_none            | 430 ms                                                                 | 421 ms: 1.02x faster                                                 |
| sympy_str                  | 544 ms                                                                 | 533 ms: 1.02x faster                                                 |
| crypto_pyaes               | 110 ms                                                                 | 108 ms: 1.02x faster                                                 |
| json                       | 5.27 ms                                                                | 5.17 ms: 1.02x faster                                                |
| meteor_contest             | 145 ms                                                                 | 143 ms: 1.02x faster                                                 |
| 2to3                       | 418 ms                                                                 | 411 ms: 1.02x faster                                                 |
| async_generators           | 488 ms                                                                 | 481 ms: 1.01x faster                                                 |
| async_tree_cpu_io_mixed    | 697 ms                                                                 | 687 ms: 1.01x faster                                                 |
| mdp                        | 3.07 sec                                                               | 3.03 sec: 1.01x faster                                               |
| thrift                     | 1.28 ms                                                                | 1.26 ms: 1.01x faster                                                |
| pathlib                    | 21.9 ms                                                                | 21.6 ms: 1.01x faster                                                |
| dulwich_log                | 105 ms                                                                 | 103 ms: 1.01x faster                                                 |
| json_loads                 | 28.7 us                                                                | 28.3 us: 1.01x faster                                                |
| k_core                     | 2.57 sec                                                               | 2.54 sec: 1.01x faster                                               |
| sqlite_synth               | 2.44 us                                                                | 2.42 us: 1.01x faster                                                |
| sympy_sum                  | 383 ms                                                                 | 379 ms: 1.01x faster                                                 |
| bench_mp_pool              | 112 ms                                                                 | 111 ms: 1.01x faster                                                 |
| async_tree_cpu_io_mixed_tg | 660 ms                                                                 | 657 ms: 1.01x faster                                                 |
| nbody                      | 201 ms                                                                 | 200 ms: 1.00x faster                                                 |
| xml_etree_parse            | 133 ms                                                                 | 133 ms: 1.00x faster                                                 |
| python_startup             | 17.6 ms                                                                | 17.6 ms: 1.00x faster                                                |
| gc_traversal               | 3.48 ms                                                                | 3.50 ms: 1.00x slower                                                |
| create_gc_cycles           | 1.82 ms                                                                | 1.83 ms: 1.01x slower                                                |
| regex_dna                  | 183 ms                                                                 | 185 ms: 1.01x slower                                                 |
| telco                      | 9.29 ms                                                                | 9.46 ms: 1.02x slower                                                |
| Geometric mean             | (ref)                                                                  | 1.03x faster                                                         |

Benchmark hidden because not significant (10): pylint, html5lib, connected_components, asyncio_websockets, generators, bench_thread_pool, pidigits, regex_v8, python_startup_no_site, json_dumps

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.00x