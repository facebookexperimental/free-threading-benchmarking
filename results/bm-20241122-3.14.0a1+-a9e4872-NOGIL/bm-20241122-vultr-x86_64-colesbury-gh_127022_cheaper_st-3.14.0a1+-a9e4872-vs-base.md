# Results vs. base

- fork: colesbury
- ref: gh_127022_cheaper_st
- machine: linux-x86_64
- commit hash: a9e4872
- commit date: 2024-11-22
- overall geometric mean: 1.03x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241119-vultr-x86_64-python-29cbcbd73bbfd8c953c0-3.14.0a1+-29cbcbd | bm-20241122-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1+-a9e4872 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 422 ms                                                                 | 411 ms: 1.03x faster                                                      |
| docutils       | 3.40 sec                                                               | 3.32 sec: 1.02x faster                                                    |
| html5lib       | 107 ms                                                                 | 102 ms: 1.05x faster                                                      |
| sphinx         | 1.33 sec                                                               | 1.30 sec: 1.02x faster                                                    |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241119-vultr-x86_64-python-29cbcbd73bbfd8c953c0-3.14.0a1+-29cbcbd | bm-20241122-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1+-a9e4872 |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_none_tg         | 394 ms                                                                 | 373 ms: 1.05x faster                                                      |
| async_tree_memoization_tg  | 494 ms                                                                 | 474 ms: 1.04x faster                                                      |
| async_tree_io_tg           | 940 ms                                                                 | 903 ms: 1.04x faster                                                      |
| async_generators           | 491 ms                                                                 | 473 ms: 1.04x faster                                                      |
| async_tree_none            | 427 ms                                                                 | 412 ms: 1.04x faster                                                      |
| async_tree_memoization     | 525 ms                                                                 | 507 ms: 1.03x faster                                                      |
| coroutines                 | 31.1 ms                                                                | 30.1 ms: 1.03x faster                                                     |
| async_tree_io              | 964 ms                                                                 | 936 ms: 1.03x faster                                                      |
| async_tree_cpu_io_mixed    | 692 ms                                                                 | 672 ms: 1.03x faster                                                      |
| async_tree_cpu_io_mixed_tg | 659 ms                                                                 | 640 ms: 1.03x faster                                                      |
| Geometric mean             | (ref)                                                                  | 1.03x faster                                                              |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241119-vultr-x86_64-python-29cbcbd73bbfd8c953c0-3.14.0a1+-29cbcbd | bm-20241122-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1+-a9e4872 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| nbody          | 202 ms                                                                 | 189 ms: 1.07x faster                                                      |
| float          | 153 ms                                                                 | 146 ms: 1.05x faster                                                      |
| pidigits       | 187 ms                                                                 | 184 ms: 1.02x faster                                                      |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241119-vultr-x86_64-python-29cbcbd73bbfd8c953c0-3.14.0a1+-29cbcbd | bm-20241122-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1+-a9e4872 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 2.88 ms                                                                | 2.77 ms: 1.04x faster                                                     |
| regex_compile  | 230 ms                                                                 | 222 ms: 1.04x faster                                                      |
| regex_dna      | 182 ms                                                                 | 181 ms: 1.00x faster                                                      |
| regex_v8       | 25.1 ms                                                                | 25.6 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241119-vultr-x86_64-python-29cbcbd73bbfd8c953c0-3.14.0a1+-29cbcbd | bm-20241122-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1+-a9e4872 |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| tomli_loads          | 3.28 sec                                                               | 3.14 sec: 1.04x faster                                                    |
| xml_etree_process    | 93.9 ms                                                                | 90.6 ms: 1.04x faster                                                     |
| xml_etree_generate   | 115 ms                                                                 | 111 ms: 1.04x faster                                                      |
| json_dumps           | 15.5 ms                                                                | 15.2 ms: 1.02x faster                                                     |
| unpickle_pure_python | 422 us                                                                 | 413 us: 1.02x faster                                                      |
| pickle_pure_python   | 624 us                                                                 | 615 us: 1.01x faster                                                      |
| xml_etree_iterparse  | 109 ms                                                                 | 108 ms: 1.01x faster                                                      |
| xml_etree_parse      | 134 ms                                                                 | 133 ms: 1.01x faster                                                      |
| Geometric mean       | (ref)                                                                  | 1.02x faster                                                              |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241119-vultr-x86_64-python-29cbcbd73bbfd8c953c0-3.14.0a1+-29cbcbd | bm-20241122-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1+-a9e4872 |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup         | 17.5 ms                                                                | 17.5 ms: 1.00x faster                                                     |
| python_startup_no_site | 10.3 ms                                                                | 10.3 ms: 1.00x faster                                                     |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241119-vultr-x86_64-python-29cbcbd73bbfd8c953c0-3.14.0a1+-29cbcbd | bm-20241122-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1+-a9e4872 |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| genshi_xml      | 82.6 ms                                                                | 78.8 ms: 1.05x faster                                                     |
| genshi_text     | 40.7 ms                                                                | 39.0 ms: 1.04x faster                                                     |
| django_template | 65.3 ms                                                                | 63.1 ms: 1.04x faster                                                     |
| mako            | 21.2 ms                                                                | 20.9 ms: 1.01x faster                                                     |
| Geometric mean  | (ref)                                                                  | 1.04x faster                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20241119-vultr-x86_64-python-29cbcbd73bbfd8c953c0-3.14.0a1+-29cbcbd | bm-20241122-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1+-a9e4872 |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| scimark_sparse_mat_mult    | 6.00 ms                                                                | 5.50 ms: 1.09x faster                                                     |
| nbody                      | 202 ms                                                                 | 189 ms: 1.07x faster                                                      |
| scimark_fft                | 419 ms                                                                 | 394 ms: 1.06x faster                                                      |
| generators                 | 41.4 ms                                                                | 39.2 ms: 1.06x faster                                                     |
| sqlglot_transpile          | 3.43 ms                                                                | 3.25 ms: 1.06x faster                                                     |
| async_tree_none_tg         | 394 ms                                                                 | 373 ms: 1.05x faster                                                      |
| spectral_norm              | 165 ms                                                                 | 157 ms: 1.05x faster                                                      |
| sqlglot_parse              | 2.93 ms                                                                | 2.79 ms: 1.05x faster                                                     |
| html5lib                   | 107 ms                                                                 | 102 ms: 1.05x faster                                                      |
| genshi_xml                 | 82.6 ms                                                                | 78.8 ms: 1.05x faster                                                     |
| float                      | 153 ms                                                                 | 146 ms: 1.05x faster                                                      |
| scimark_sor                | 273 ms                                                                 | 261 ms: 1.05x faster                                                      |
| logging_silent             | 222 ns                                                                 | 212 ns: 1.05x faster                                                      |
| genshi_text                | 40.7 ms                                                                | 39.0 ms: 1.04x faster                                                     |
| tomli_loads                | 3.28 sec                                                               | 3.14 sec: 1.04x faster                                                    |
| async_tree_memoization_tg  | 494 ms                                                                 | 474 ms: 1.04x faster                                                      |
| shortest_path              | 582 ms                                                                 | 559 ms: 1.04x faster                                                      |
| connected_components       | 535 ms                                                                 | 514 ms: 1.04x faster                                                      |
| richards                   | 92.3 ms                                                                | 88.7 ms: 1.04x faster                                                     |
| async_tree_io_tg           | 940 ms                                                                 | 903 ms: 1.04x faster                                                      |
| scimark_monte_carlo        | 129 ms                                                                 | 124 ms: 1.04x faster                                                      |
| go                         | 303 ms                                                                 | 292 ms: 1.04x faster                                                      |
| async_generators           | 491 ms                                                                 | 473 ms: 1.04x faster                                                      |
| deltablue                  | 9.33 ms                                                                | 8.99 ms: 1.04x faster                                                     |
| chaos                      | 123 ms                                                                 | 119 ms: 1.04x faster                                                      |
| richards_super             | 110 ms                                                                 | 106 ms: 1.04x faster                                                      |
| async_tree_none            | 427 ms                                                                 | 412 ms: 1.04x faster                                                      |
| comprehensions             | 30.9 us                                                                | 29.8 us: 1.04x faster                                                     |
| regex_effbot               | 2.88 ms                                                                | 2.77 ms: 1.04x faster                                                     |
| xml_etree_process          | 93.9 ms                                                                | 90.6 ms: 1.04x faster                                                     |
| django_template            | 65.3 ms                                                                | 63.1 ms: 1.04x faster                                                     |
| regex_compile              | 230 ms                                                                 | 222 ms: 1.04x faster                                                      |
| xml_etree_generate         | 115 ms                                                                 | 111 ms: 1.04x faster                                                      |
| async_tree_memoization     | 525 ms                                                                 | 507 ms: 1.03x faster                                                      |
| crypto_pyaes               | 109 ms                                                                 | 105 ms: 1.03x faster                                                      |
| deepcopy_reduce            | 4.59 us                                                                | 4.44 us: 1.03x faster                                                     |
| meteor_contest             | 147 ms                                                                 | 142 ms: 1.03x faster                                                      |
| logging_format             | 13.6 us                                                                | 13.2 us: 1.03x faster                                                     |
| coroutines                 | 31.1 ms                                                                | 30.1 ms: 1.03x faster                                                     |
| json                       | 5.40 ms                                                                | 5.23 ms: 1.03x faster                                                     |
| deepcopy                   | 437 us                                                                 | 424 us: 1.03x faster                                                      |
| async_tree_io              | 964 ms                                                                 | 936 ms: 1.03x faster                                                      |
| async_tree_cpu_io_mixed    | 692 ms                                                                 | 672 ms: 1.03x faster                                                      |
| async_tree_cpu_io_mixed_tg | 659 ms                                                                 | 640 ms: 1.03x faster                                                      |
| logging_simple             | 12.3 us                                                                | 11.9 us: 1.03x faster                                                     |
| 2to3                       | 422 ms                                                                 | 411 ms: 1.03x faster                                                      |
| raytrace                   | 642 ms                                                                 | 626 ms: 1.03x faster                                                      |
| json_dumps                 | 15.5 ms                                                                | 15.2 ms: 1.02x faster                                                     |
| docutils                   | 3.40 sec                                                               | 3.32 sec: 1.02x faster                                                    |
| thrift                     | 1.29 ms                                                                | 1.26 ms: 1.02x faster                                                     |
| hexiom                     | 12.5 ms                                                                | 12.3 ms: 1.02x faster                                                     |
| mdp                        | 3.06 sec                                                               | 2.99 sec: 1.02x faster                                                    |
| bpe_tokeniser              | 6.14 sec                                                               | 6.01 sec: 1.02x faster                                                    |
| unpickle_pure_python       | 422 us                                                                 | 413 us: 1.02x faster                                                      |
| sqlglot_optimize           | 92.2 ms                                                                | 90.2 ms: 1.02x faster                                                     |
| nqueens                    | 115 ms                                                                 | 113 ms: 1.02x faster                                                      |
| telco                      | 9.72 ms                                                                | 9.51 ms: 1.02x faster                                                     |
| pprint_safe_repr           | 1.33 sec                                                               | 1.30 sec: 1.02x faster                                                    |
| sphinx                     | 1.33 sec                                                               | 1.30 sec: 1.02x faster                                                    |
| pyflate                    | 783 ms                                                                 | 767 ms: 1.02x faster                                                      |
| pycparser                  | 1.71 sec                                                               | 1.67 sec: 1.02x faster                                                    |
| k_core                     | 2.56 sec                                                               | 2.52 sec: 1.02x faster                                                    |
| scimark_lu                 | 247 ms                                                                 | 243 ms: 1.02x faster                                                      |
| pprint_pformat             | 2.77 sec                                                               | 2.72 sec: 1.02x faster                                                    |
| deepcopy_memo              | 53.7 us                                                                | 52.7 us: 1.02x faster                                                     |
| fannkuch                   | 564 ms                                                                 | 554 ms: 1.02x faster                                                      |
| sympy_str                  | 543 ms                                                                 | 534 ms: 1.02x faster                                                      |
| pidigits                   | 187 ms                                                                 | 184 ms: 1.02x faster                                                      |
| dulwich_log                | 104 ms                                                                 | 103 ms: 1.02x faster                                                      |
| pickle_pure_python         | 624 us                                                                 | 615 us: 1.01x faster                                                      |
| mako                       | 21.2 ms                                                                | 20.9 ms: 1.01x faster                                                     |
| sympy_expand               | 1.06 sec                                                               | 1.05 sec: 1.01x faster                                                    |
| sympy_integrate            | 33.2 ms                                                                | 32.8 ms: 1.01x faster                                                     |
| subparsers                 | 36.3 ms                                                                | 36.0 ms: 1.01x faster                                                     |
| sqlglot_normalize          | 183 ms                                                                 | 181 ms: 1.01x faster                                                      |
| bench_thread_pool          | 3.52 ms                                                                | 3.49 ms: 1.01x faster                                                     |
| xml_etree_iterparse        | 109 ms                                                                 | 108 ms: 1.01x faster                                                      |
| xml_etree_parse            | 134 ms                                                                 | 133 ms: 1.01x faster                                                      |
| many_optionals             | 1.46 ms                                                                | 1.45 ms: 1.01x faster                                                     |
| sympy_sum                  | 383 ms                                                                 | 381 ms: 1.00x faster                                                      |
| bench_mp_pool              | 110 ms                                                                 | 110 ms: 1.00x faster                                                      |
| regex_dna                  | 182 ms                                                                 | 181 ms: 1.00x faster                                                      |
| python_startup             | 17.5 ms                                                                | 17.5 ms: 1.00x faster                                                     |
| python_startup_no_site     | 10.3 ms                                                                | 10.3 ms: 1.00x faster                                                     |
| coverage                   | 103 ms                                                                 | 103 ms: 1.00x slower                                                      |
| regex_v8                   | 25.1 ms                                                                | 25.6 ms: 1.02x slower                                                     |
| gc_traversal               | 3.09 ms                                                                | 3.31 ms: 1.07x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.03x faster                                                              |

Benchmark hidden because not significant (7): pylint, json_loads, create_gc_cycles, typing_runtime_protocols, asyncio_websockets, pathlib, sqlite_synth

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.01x