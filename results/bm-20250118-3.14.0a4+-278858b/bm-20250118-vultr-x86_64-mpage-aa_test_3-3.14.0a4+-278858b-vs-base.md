# Results vs. base

- fork: mpage
- ref: aa_test_3
- machine: linux-x86_64
- commit hash: 278858b
- commit date: 2025-01-18
- overall geometric mean: 1.007x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250118-vultr-x86_64-python-61b35f74aa4a6ac60663-3.14.0a4+-61b35f7 | bm-20250118-vultr-x86_64-mpage-aa_test_3-3.14.0a4+-278858b |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| 2to3           | 253 ms                                                                 | 255 ms: 1.01x slower                                       |
| docutils       | 2.56 sec                                                               | 2.57 sec: 1.00x slower                                     |
| sphinx         | 980 ms                                                                 | 989 ms: 1.01x slower                                       |
| Geometric mean | (ref)                                                                  | 1.01x slower                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250118-vultr-x86_64-python-61b35f74aa4a6ac60663-3.14.0a4+-61b35f7 | bm-20250118-vultr-x86_64-mpage-aa_test_3-3.14.0a4+-278858b |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| coroutines                 | 22.1 ms                                                                | 21.7 ms: 1.02x faster                                      |
| async_tree_cpu_io_mixed_tg | 484 ms                                                                 | 475 ms: 1.02x faster                                       |
| async_tree_cpu_io_mixed    | 502 ms                                                                 | 495 ms: 1.01x faster                                       |
| async_tree_memoization_tg  | 305 ms                                                                 | 307 ms: 1.01x slower                                       |
| async_tree_none_tg         | 255 ms                                                                 | 258 ms: 1.01x slower                                       |
| async_generators           | 325 ms                                                                 | 329 ms: 1.01x slower                                       |
| async_tree_io_tg           | 613 ms                                                                 | 623 ms: 1.02x slower                                       |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                               |

Benchmark hidden because not significant (4): async_tree_io, asyncio_websockets, async_tree_none, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250118-vultr-x86_64-python-61b35f74aa4a6ac60663-3.14.0a4+-61b35f7 | bm-20250118-vultr-x86_64-mpage-aa_test_3-3.14.0a4+-278858b |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| float          | 71.4 ms                                                                | 73.2 ms: 1.03x slower                                      |
| nbody          | 85.4 ms                                                                | 87.8 ms: 1.03x slower                                      |
| pidigits       | 192 ms                                                                 | 214 ms: 1.12x slower                                       |
| Geometric mean | (ref)                                                                  | 1.06x slower                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250118-vultr-x86_64-python-61b35f74aa4a6ac60663-3.14.0a4+-61b35f7 | bm-20250118-vultr-x86_64-mpage-aa_test_3-3.14.0a4+-278858b |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| regex_dna      | 174 ms                                                                 | 168 ms: 1.03x faster                                       |
| regex_v8       | 23.2 ms                                                                | 23.5 ms: 1.01x slower                                      |
| regex_effbot   | 2.68 ms                                                                | 2.76 ms: 1.03x slower                                      |
| Geometric mean | (ref)                                                                  | 1.00x slower                                               |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20250118-vultr-x86_64-python-61b35f74aa4a6ac60663-3.14.0a4+-61b35f7 | bm-20250118-vultr-x86_64-mpage-aa_test_3-3.14.0a4+-278858b |
|--------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| xml_etree_process  | 60.3 ms                                                                | 59.7 ms: 1.01x faster                                      |
| pickle_pure_python | 319 us                                                                 | 316 us: 1.01x faster                                       |
| xml_etree_parse    | 129 ms                                                                 | 128 ms: 1.01x faster                                       |
| xml_etree_generate | 85.0 ms                                                                | 84.6 ms: 1.01x faster                                      |
| json_loads         | 27.4 us                                                                | 27.7 us: 1.01x slower                                      |
| tomli_loads        | 1.89 sec                                                               | 1.93 sec: 1.02x slower                                     |
| Geometric mean     | (ref)                                                                  | 1.00x slower                                               |

Benchmark hidden because not significant (3): json_dumps, xml_etree_iterparse, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250118-vultr-x86_64-python-61b35f74aa4a6ac60663-3.14.0a4+-61b35f7 | bm-20250118-vultr-x86_64-mpage-aa_test_3-3.14.0a4+-278858b |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| python_startup_no_site | 7.48 ms                                                                | 7.47 ms: 1.00x faster                                      |
| python_startup         | 14.7 ms                                                                | 14.7 ms: 1.00x faster                                      |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250118-vultr-x86_64-python-61b35f74aa4a6ac60663-3.14.0a4+-61b35f7 | bm-20250118-vultr-x86_64-mpage-aa_test_3-3.14.0a4+-278858b |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| django_template | 35.9 ms                                                                | 35.4 ms: 1.01x faster                                      |
| genshi_xml      | 48.4 ms                                                                | 49.0 ms: 1.01x slower                                      |
| genshi_text     | 21.1 ms                                                                | 21.5 ms: 1.02x slower                                      |
| Geometric mean  | (ref)                                                                  | 1.00x slower                                               |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                  | bm-20250118-vultr-x86_64-python-61b35f74aa4a6ac60663-3.14.0a4+-61b35f7 | bm-20250118-vultr-x86_64-mpage-aa_test_3-3.14.0a4+-278858b |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| gc_traversal               | 4.56 ms                                                                | 4.28 ms: 1.07x faster                                      |
| mdp                        | 2.48 sec                                                               | 2.35 sec: 1.05x faster                                     |
| logging_silent             | 106 ns                                                                 | 102 ns: 1.04x faster                                       |
| regex_dna                  | 174 ms                                                                 | 168 ms: 1.03x faster                                       |
| deepcopy_reduce            | 2.70 us                                                                | 2.62 us: 1.03x faster                                      |
| coroutines                 | 22.1 ms                                                                | 21.7 ms: 1.02x faster                                      |
| async_tree_cpu_io_mixed_tg | 484 ms                                                                 | 475 ms: 1.02x faster                                       |
| django_template            | 35.9 ms                                                                | 35.4 ms: 1.01x faster                                      |
| create_gc_cycles           | 1.85 ms                                                                | 1.82 ms: 1.01x faster                                      |
| async_tree_cpu_io_mixed    | 502 ms                                                                 | 495 ms: 1.01x faster                                       |
| logging_format             | 6.89 us                                                                | 6.81 us: 1.01x faster                                      |
| xml_etree_process          | 60.3 ms                                                                | 59.7 ms: 1.01x faster                                      |
| pickle_pure_python         | 319 us                                                                 | 316 us: 1.01x faster                                       |
| sqlite_synth               | 2.19 us                                                                | 2.17 us: 1.01x faster                                      |
| xml_etree_parse            | 129 ms                                                                 | 128 ms: 1.01x faster                                       |
| bench_mp_pool              | 89.3 ms                                                                | 88.7 ms: 1.01x faster                                      |
| go                         | 116 ms                                                                 | 115 ms: 1.01x faster                                       |
| xml_etree_generate         | 85.0 ms                                                                | 84.6 ms: 1.01x faster                                      |
| deepcopy                   | 260 us                                                                 | 259 us: 1.00x faster                                       |
| python_startup_no_site     | 7.48 ms                                                                | 7.47 ms: 1.00x faster                                      |
| python_startup             | 14.7 ms                                                                | 14.7 ms: 1.00x faster                                      |
| crypto_pyaes               | 66.7 ms                                                                | 67.0 ms: 1.00x slower                                      |
| richards                   | 42.3 ms                                                                | 42.5 ms: 1.00x slower                                      |
| docutils                   | 2.56 sec                                                               | 2.57 sec: 1.00x slower                                     |
| sqlglot_optimize           | 52.6 ms                                                                | 52.9 ms: 1.00x slower                                      |
| shortest_path              | 433 ms                                                                 | 435 ms: 1.00x slower                                       |
| comprehensions             | 16.8 us                                                                | 16.9 us: 1.01x slower                                      |
| deltablue                  | 3.13 ms                                                                | 3.16 ms: 1.01x slower                                      |
| sqlalchemy_declarative     | 128 ms                                                                 | 129 ms: 1.01x slower                                       |
| 2to3                       | 253 ms                                                                 | 255 ms: 1.01x slower                                       |
| sqlglot_normalize          | 105 ms                                                                 | 106 ms: 1.01x slower                                       |
| bench_thread_pool          | 1.04 ms                                                                | 1.04 ms: 1.01x slower                                      |
| sympy_expand               | 458 ms                                                                 | 462 ms: 1.01x slower                                       |
| json                       | 4.98 ms                                                                | 5.02 ms: 1.01x slower                                      |
| fannkuch                   | 369 ms                                                                 | 372 ms: 1.01x slower                                       |
| async_tree_memoization_tg  | 305 ms                                                                 | 307 ms: 1.01x slower                                       |
| sympy_str                  | 272 ms                                                                 | 274 ms: 1.01x slower                                       |
| logging_simple             | 6.13 us                                                                | 6.19 us: 1.01x slower                                      |
| sphinx                     | 980 ms                                                                 | 989 ms: 1.01x slower                                       |
| pycparser                  | 1.10 sec                                                               | 1.11 sec: 1.01x slower                                     |
| subparsers                 | 21.9 ms                                                                | 22.1 ms: 1.01x slower                                      |
| json_loads                 | 27.4 us                                                                | 27.7 us: 1.01x slower                                      |
| coverage                   | 79.6 ms                                                                | 80.4 ms: 1.01x slower                                      |
| async_tree_none_tg         | 255 ms                                                                 | 258 ms: 1.01x slower                                       |
| regex_v8                   | 23.2 ms                                                                | 23.5 ms: 1.01x slower                                      |
| sympy_integrate            | 19.7 ms                                                                | 19.9 ms: 1.01x slower                                      |
| genshi_xml                 | 48.4 ms                                                                | 49.0 ms: 1.01x slower                                      |
| typing_runtime_protocols   | 158 us                                                                 | 160 us: 1.01x slower                                       |
| bpe_tokeniser              | 4.21 sec                                                               | 4.26 sec: 1.01x slower                                     |
| async_generators           | 325 ms                                                                 | 329 ms: 1.01x slower                                       |
| nqueens                    | 77.7 ms                                                                | 78.8 ms: 1.02x slower                                      |
| pathlib                    | 18.0 ms                                                                | 18.3 ms: 1.02x slower                                      |
| scimark_sor                | 114 ms                                                                 | 116 ms: 1.02x slower                                       |
| scimark_lu                 | 111 ms                                                                 | 113 ms: 1.02x slower                                       |
| async_tree_io_tg           | 613 ms                                                                 | 623 ms: 1.02x slower                                       |
| genshi_text                | 21.1 ms                                                                | 21.5 ms: 1.02x slower                                      |
| sqlglot_parse              | 1.25 ms                                                                | 1.27 ms: 1.02x slower                                      |
| pprint_safe_repr           | 702 ms                                                                 | 715 ms: 1.02x slower                                       |
| sqlglot_transpile          | 1.55 ms                                                                | 1.58 ms: 1.02x slower                                      |
| tomli_loads                | 1.89 sec                                                               | 1.93 sec: 1.02x slower                                     |
| pprint_pformat             | 1.42 sec                                                               | 1.45 sec: 1.02x slower                                     |
| scimark_monte_carlo        | 63.5 ms                                                                | 65.1 ms: 1.02x slower                                      |
| float                      | 71.4 ms                                                                | 73.2 ms: 1.03x slower                                      |
| nbody                      | 85.4 ms                                                                | 87.8 ms: 1.03x slower                                      |
| regex_effbot               | 2.68 ms                                                                | 2.76 ms: 1.03x slower                                      |
| generators                 | 28.1 ms                                                                | 28.9 ms: 1.03x slower                                      |
| scimark_fft                | 310 ms                                                                 | 320 ms: 1.03x slower                                       |
| spectral_norm              | 92.1 ms                                                                | 95.1 ms: 1.03x slower                                      |
| raytrace                   | 260 ms                                                                 | 268 ms: 1.03x slower                                       |
| deepcopy_memo              | 29.6 us                                                                | 30.7 us: 1.04x slower                                      |
| chaos                      | 54.7 ms                                                                | 56.8 ms: 1.04x slower                                      |
| scimark_sparse_mat_mult    | 4.06 ms                                                                | 4.38 ms: 1.08x slower                                      |
| pidigits                   | 192 ms                                                                 | 214 ms: 1.12x slower                                       |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                               |

Benchmark hidden because not significant (22): json_dumps, telco, meteor_contest, many_optionals, richards_super, pyflate, mako, async_tree_io, xml_etree_iterparse, sympy_sum, asyncio_websockets, hexiom, k_core, regex_compile, dulwich_log, thrift, sqlalchemy_imperative, pylint, connected_components, async_tree_none, async_tree_memoization, unpickle_pure_python

- Geometric mean (including insignificant results): 1.007x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.98x