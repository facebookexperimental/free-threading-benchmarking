# Results vs. base

- fork: mpage
- ref: aa_test_6
- machine: linux-x86_64
- commit hash: 01bcf13
- commit date: 2025-01-21
- overall geometric mean: 1.006x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250121-vultr-x86_64-python-29caec62ee0650493c83-3.14.0a4+-29caec6 | bm-20250121-vultr-x86_64-mpage-aa_test_6-3.14.0a4+-01bcf13 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| 2to3           | 254 ms                                                                 | 257 ms: 1.01x slower                                       |
| docutils       | 2.55 sec                                                               | 2.58 sec: 1.01x slower                                     |
| Geometric mean | (ref)                                                                  | 1.01x slower                                               |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250121-vultr-x86_64-python-29caec62ee0650493c83-3.14.0a4+-29caec6 | bm-20250121-vultr-x86_64-mpage-aa_test_6-3.14.0a4+-01bcf13 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| asyncio_websockets         | 517 ms                                                                 | 516 ms: 1.00x faster                                       |
| async_generators           | 319 ms                                                                 | 320 ms: 1.01x slower                                       |
| async_tree_memoization_tg  | 302 ms                                                                 | 304 ms: 1.01x slower                                       |
| async_tree_cpu_io_mixed_tg | 476 ms                                                                 | 480 ms: 1.01x slower                                       |
| async_tree_cpu_io_mixed    | 488 ms                                                                 | 493 ms: 1.01x slower                                       |
| async_tree_memoization     | 320 ms                                                                 | 323 ms: 1.01x slower                                       |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                               |

Benchmark hidden because not significant (5): coroutines, async_tree_none, async_tree_io_tg, async_tree_none_tg, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250121-vultr-x86_64-python-29caec62ee0650493c83-3.14.0a4+-29caec6 | bm-20250121-vultr-x86_64-mpage-aa_test_6-3.14.0a4+-01bcf13 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| pidigits       | 196 ms                                                                 | 206 ms: 1.05x slower                                       |
| Geometric mean | (ref)                                                                  | 1.02x slower                                               |

Benchmark hidden because not significant (2): nbody, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250121-vultr-x86_64-python-29caec62ee0650493c83-3.14.0a4+-29caec6 | bm-20250121-vultr-x86_64-mpage-aa_test_6-3.14.0a4+-01bcf13 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| regex_dna      | 168 ms                                                                 | 165 ms: 1.02x faster                                       |
| regex_compile  | 127 ms                                                                 | 129 ms: 1.02x slower                                       |
| regex_v8       | 23.5 ms                                                                | 24.3 ms: 1.03x slower                                      |
| regex_effbot   | 2.57 ms                                                                | 2.66 ms: 1.04x slower                                      |
| Geometric mean | (ref)                                                                  | 1.02x slower                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250121-vultr-x86_64-python-29caec62ee0650493c83-3.14.0a4+-29caec6 | bm-20250121-vultr-x86_64-mpage-aa_test_6-3.14.0a4+-01bcf13 |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| xml_etree_parse      | 129 ms                                                                 | 127 ms: 1.01x faster                                       |
| xml_etree_iterparse  | 90.8 ms                                                                | 89.8 ms: 1.01x faster                                      |
| xml_etree_process    | 60.6 ms                                                                | 60.0 ms: 1.01x faster                                      |
| xml_etree_generate   | 83.2 ms                                                                | 82.9 ms: 1.00x faster                                      |
| unpickle_pure_python | 224 us                                                                 | 226 us: 1.01x slower                                       |
| json_dumps           | 11.4 ms                                                                | 11.5 ms: 1.01x slower                                      |
| tomli_loads          | 1.95 sec                                                               | 1.97 sec: 1.01x slower                                     |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                               |

Benchmark hidden because not significant (2): pickle_pure_python, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250121-vultr-x86_64-python-29caec62ee0650493c83-3.14.0a4+-29caec6 | bm-20250121-vultr-x86_64-mpage-aa_test_6-3.14.0a4+-01bcf13 |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| python_startup_no_site | 7.43 ms                                                                | 7.48 ms: 1.01x slower                                      |
| python_startup         | 14.6 ms                                                                | 14.7 ms: 1.01x slower                                      |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250121-vultr-x86_64-python-29caec62ee0650493c83-3.14.0a4+-29caec6 | bm-20250121-vultr-x86_64-mpage-aa_test_6-3.14.0a4+-01bcf13 |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| mako            | 11.7 ms                                                                | 11.7 ms: 1.00x slower                                      |
| genshi_xml      | 48.9 ms                                                                | 49.7 ms: 1.02x slower                                      |
| genshi_text     | 21.3 ms                                                                | 21.7 ms: 1.02x slower                                      |
| django_template | 35.0 ms                                                                | 35.6 ms: 1.02x slower                                      |
| Geometric mean  | (ref)                                                                  | 1.01x slower                                               |

All benchmarks:
===============

| Benchmark                  | bm-20250121-vultr-x86_64-python-29caec62ee0650493c83-3.14.0a4+-29caec6 | bm-20250121-vultr-x86_64-mpage-aa_test_6-3.14.0a4+-01bcf13 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| gc_traversal               | 4.19 ms                                                                | 3.99 ms: 1.05x faster                                      |
| pyflate                    | 421 ms                                                                 | 412 ms: 1.02x faster                                       |
| generators                 | 27.7 ms                                                                | 27.2 ms: 1.02x faster                                      |
| crypto_pyaes               | 67.3 ms                                                                | 66.0 ms: 1.02x faster                                      |
| regex_dna                  | 168 ms                                                                 | 165 ms: 1.02x faster                                       |
| logging_silent             | 103 ns                                                                 | 102 ns: 1.02x faster                                       |
| xml_etree_parse            | 129 ms                                                                 | 127 ms: 1.01x faster                                       |
| xml_etree_iterparse        | 90.8 ms                                                                | 89.8 ms: 1.01x faster                                      |
| richards                   | 41.6 ms                                                                | 41.2 ms: 1.01x faster                                      |
| richards_super             | 47.9 ms                                                                | 47.4 ms: 1.01x faster                                      |
| xml_etree_process          | 60.6 ms                                                                | 60.0 ms: 1.01x faster                                      |
| coverage                   | 80.5 ms                                                                | 80.0 ms: 1.01x faster                                      |
| xml_etree_generate         | 83.2 ms                                                                | 82.9 ms: 1.00x faster                                      |
| asyncio_websockets         | 517 ms                                                                 | 516 ms: 1.00x faster                                       |
| scimark_fft                | 313 ms                                                                 | 313 ms: 1.00x faster                                       |
| spectral_norm              | 93.5 ms                                                                | 93.6 ms: 1.00x slower                                      |
| mako                       | 11.7 ms                                                                | 11.7 ms: 1.00x slower                                      |
| sqlglot_optimize           | 52.6 ms                                                                | 52.7 ms: 1.00x slower                                      |
| go                         | 113 ms                                                                 | 114 ms: 1.00x slower                                       |
| deepcopy                   | 254 us                                                                 | 255 us: 1.00x slower                                       |
| bench_thread_pool          | 1.03 ms                                                                | 1.04 ms: 1.01x slower                                      |
| deepcopy_reduce            | 2.55 us                                                                | 2.57 us: 1.01x slower                                      |
| async_generators           | 319 ms                                                                 | 320 ms: 1.01x slower                                       |
| mdp                        | 2.29 sec                                                               | 2.30 sec: 1.01x slower                                     |
| python_startup_no_site     | 7.43 ms                                                                | 7.48 ms: 1.01x slower                                      |
| async_tree_memoization_tg  | 302 ms                                                                 | 304 ms: 1.01x slower                                       |
| raytrace                   | 261 ms                                                                 | 263 ms: 1.01x slower                                       |
| scimark_lu                 | 111 ms                                                                 | 112 ms: 1.01x slower                                       |
| sqlalchemy_declarative     | 129 ms                                                                 | 130 ms: 1.01x slower                                       |
| sqlglot_normalize          | 104 ms                                                                 | 105 ms: 1.01x slower                                       |
| thrift                     | 740 us                                                                 | 746 us: 1.01x slower                                       |
| python_startup             | 14.6 ms                                                                | 14.7 ms: 1.01x slower                                      |
| unpickle_pure_python       | 224 us                                                                 | 226 us: 1.01x slower                                       |
| shortest_path              | 427 ms                                                                 | 430 ms: 1.01x slower                                       |
| json_dumps                 | 11.4 ms                                                                | 11.5 ms: 1.01x slower                                      |
| chaos                      | 55.9 ms                                                                | 56.4 ms: 1.01x slower                                      |
| sympy_integrate            | 19.8 ms                                                                | 20.0 ms: 1.01x slower                                      |
| async_tree_cpu_io_mixed_tg | 476 ms                                                                 | 480 ms: 1.01x slower                                       |
| scimark_sparse_mat_mult    | 4.33 ms                                                                | 4.37 ms: 1.01x slower                                      |
| fannkuch                   | 372 ms                                                                 | 375 ms: 1.01x slower                                       |
| deepcopy_memo              | 29.8 us                                                                | 30.1 us: 1.01x slower                                      |
| dulwich_log                | 75.9 ms                                                                | 76.7 ms: 1.01x slower                                      |
| bench_mp_pool              | 88.7 ms                                                                | 89.7 ms: 1.01x slower                                      |
| async_tree_cpu_io_mixed    | 488 ms                                                                 | 493 ms: 1.01x slower                                       |
| sympy_sum                  | 154 ms                                                                 | 155 ms: 1.01x slower                                       |
| async_tree_memoization     | 320 ms                                                                 | 323 ms: 1.01x slower                                       |
| tomli_loads                | 1.95 sec                                                               | 1.97 sec: 1.01x slower                                     |
| meteor_contest             | 98.3 ms                                                                | 99.6 ms: 1.01x slower                                      |
| deltablue                  | 3.07 ms                                                                | 3.10 ms: 1.01x slower                                      |
| hexiom                     | 5.74 ms                                                                | 5.81 ms: 1.01x slower                                      |
| 2to3                       | 254 ms                                                                 | 257 ms: 1.01x slower                                       |
| pathlib                    | 18.3 ms                                                                | 18.5 ms: 1.01x slower                                      |
| scimark_monte_carlo        | 62.5 ms                                                                | 63.4 ms: 1.01x slower                                      |
| docutils                   | 2.55 sec                                                               | 2.58 sec: 1.01x slower                                     |
| sympy_str                  | 272 ms                                                                 | 276 ms: 1.01x slower                                       |
| nqueens                    | 77.2 ms                                                                | 78.3 ms: 1.01x slower                                      |
| typing_runtime_protocols   | 157 us                                                                 | 159 us: 1.02x slower                                       |
| regex_compile              | 127 ms                                                                 | 129 ms: 1.02x slower                                       |
| genshi_xml                 | 48.9 ms                                                                | 49.7 ms: 1.02x slower                                      |
| sqlglot_transpile          | 1.52 ms                                                                | 1.55 ms: 1.02x slower                                      |
| sympy_expand               | 457 ms                                                                 | 465 ms: 1.02x slower                                       |
| pycparser                  | 1.12 sec                                                               | 1.14 sec: 1.02x slower                                     |
| pprint_pformat             | 1.42 sec                                                               | 1.45 sec: 1.02x slower                                     |
| genshi_text                | 21.3 ms                                                                | 21.7 ms: 1.02x slower                                      |
| django_template            | 35.0 ms                                                                | 35.6 ms: 1.02x slower                                      |
| sqlglot_parse              | 1.22 ms                                                                | 1.24 ms: 1.02x slower                                      |
| many_optionals             | 1.03 ms                                                                | 1.05 ms: 1.02x slower                                      |
| scimark_sor                | 112 ms                                                                 | 114 ms: 1.02x slower                                       |
| subparsers                 | 22.1 ms                                                                | 22.6 ms: 1.02x slower                                      |
| pprint_safe_repr           | 700 ms                                                                 | 714 ms: 1.02x slower                                       |
| regex_v8                   | 23.5 ms                                                                | 24.3 ms: 1.03x slower                                      |
| regex_effbot               | 2.57 ms                                                                | 2.66 ms: 1.04x slower                                      |
| logging_format             | 7.07 us                                                                | 7.35 us: 1.04x slower                                      |
| logging_simple             | 6.34 us                                                                | 6.63 us: 1.04x slower                                      |
| pidigits                   | 196 ms                                                                 | 206 ms: 1.05x slower                                       |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                               |

Benchmark hidden because not significant (20): telco, connected_components, coroutines, sqlite_synth, pickle_pure_python, create_gc_cycles, bpe_tokeniser, nbody, sqlalchemy_imperative, json, float, comprehensions, sphinx, json_loads, async_tree_none, k_core, async_tree_io_tg, pylint, async_tree_none_tg, async_tree_io

- Geometric mean (including insignificant results): 1.006x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x