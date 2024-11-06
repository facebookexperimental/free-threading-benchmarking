# Results vs. base

- fork: mpage
- ref: gh_115999_tlbc_integ
- machine: linux-x86_64
- commit hash: 0a68813
- commit date: 2024-10-31
- overall geometric mean: 1.04x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241013-linux-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241031-linux-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| docutils       | 5.09 sec                                                              | 4.80 sec: 1.06x faster                                               |
| tornado_http   | 317 ms                                                                | 345 ms: 1.09x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.01x slower                                                         |

Benchmark hidden because not significant (2): 2to3, html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20241013-linux-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241031-linux-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| coroutines       | 43.4 ms                                                               | 40.1 ms: 1.08x faster                                                |
| async_generators | 742 ms                                                                | 701 ms: 1.06x faster                                                 |
| asyncio_tcp_ssl  | 3.05 sec                                                              | 3.30 sec: 1.08x slower                                               |
| Geometric mean   | (ref)                                                                 | 1.02x faster                                                         |

Benchmark hidden because not significant (2): asyncio_websockets, asyncio_tcp

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241013-linux-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241031-linux-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| nbody          | 340 ms                                                                | 304 ms: 1.12x faster                                                 |
| Geometric mean | (ref)                                                                 | 1.04x faster                                                         |

Benchmark hidden because not significant (2): pidigits, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241013-linux-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241031-linux-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_compile  | 324 ms                                                                | 301 ms: 1.08x faster                                                 |
| regex_dna      | 291 ms                                                                | 281 ms: 1.04x faster                                                 |
| Geometric mean | (ref)                                                                 | 1.02x faster                                                         |

Benchmark hidden because not significant (2): regex_effbot, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241013-linux-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241031-linux-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|----------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_parse      | 250 ms                                                                | 224 ms: 1.11x faster                                                 |
| unpickle_pure_python | 623 us                                                                | 566 us: 1.10x faster                                                 |
| pickle_pure_python   | 853 us                                                                | 785 us: 1.09x faster                                                 |
| xml_etree_generate   | 169 ms                                                                | 159 ms: 1.06x faster                                                 |
| xml_etree_process    | 139 ms                                                                | 131 ms: 1.06x faster                                                 |
| tomli_loads          | 4.47 sec                                                              | 4.24 sec: 1.05x faster                                               |
| xml_etree_iterparse  | 183 ms                                                                | 176 ms: 1.04x faster                                                 |
| unpickle_list        | 8.18 us                                                               | 8.47 us: 1.04x slower                                                |
| unpickle             | 25.9 us                                                               | 27.2 us: 1.05x slower                                                |
| json_loads           | 43.4 us                                                               | 45.8 us: 1.06x slower                                                |
| Geometric mean       | (ref)                                                                 | 1.03x faster                                                         |

Benchmark hidden because not significant (4): json_dumps, pickle_list, pickle_dict, pickle

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup, python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241013-linux-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241031-linux-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|-----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 143 ms                                                                | 128 ms: 1.12x faster                                                 |
| django_template | 92.1 ms                                                               | 83.0 ms: 1.11x faster                                                |
| mako            | 33.4 ms                                                               | 31.1 ms: 1.08x faster                                                |
| genshi_text     | 65.5 ms                                                               | 61.6 ms: 1.06x faster                                                |
| Geometric mean  | (ref)                                                                 | 1.09x faster                                                         |

All benchmarks:
===============

| Benchmark                | bm-20241013-linux-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241031-linux-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|--------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| chaos                    | 187 ms                                                                | 159 ms: 1.18x faster                                                 |
| deepcopy_memo            | 82.4 us                                                               | 70.2 us: 1.17x faster                                                |
| spectral_norm            | 264 ms                                                                | 226 ms: 1.17x faster                                                 |
| scimark_lu               | 325 ms                                                                | 279 ms: 1.17x faster                                                 |
| pprint_safe_repr         | 1.78 sec                                                              | 1.56 sec: 1.14x faster                                               |
| scimark_sparse_mat_mult  | 9.79 ms                                                               | 8.57 ms: 1.14x faster                                                |
| deepcopy                 | 643 us                                                                | 568 us: 1.13x faster                                                 |
| bpe_tokeniser            | 10.4 sec                                                              | 9.16 sec: 1.13x faster                                               |
| typing_runtime_protocols | 372 us                                                                | 330 us: 1.13x faster                                                 |
| pprint_pformat           | 3.64 sec                                                              | 3.24 sec: 1.12x faster                                               |
| nbody                    | 340 ms                                                                | 304 ms: 1.12x faster                                                 |
| comprehensions           | 46.5 us                                                               | 41.6 us: 1.12x faster                                                |
| genshi_xml               | 143 ms                                                                | 128 ms: 1.12x faster                                                 |
| xml_etree_parse          | 250 ms                                                                | 224 ms: 1.11x faster                                                 |
| bench_thread_pool        | 3.75 ms                                                               | 3.38 ms: 1.11x faster                                                |
| django_template          | 92.1 ms                                                               | 83.0 ms: 1.11x faster                                                |
| logging_silent           | 279 ns                                                                | 253 ns: 1.11x faster                                                 |
| scimark_monte_carlo      | 173 ms                                                                | 157 ms: 1.10x faster                                                 |
| unpickle_pure_python     | 623 us                                                                | 566 us: 1.10x faster                                                 |
| raytrace                 | 858 ms                                                                | 783 ms: 1.10x faster                                                 |
| scimark_fft              | 660 ms                                                                | 606 ms: 1.09x faster                                                 |
| richards_super           | 145 ms                                                                | 134 ms: 1.09x faster                                                 |
| sqlglot_optimize         | 129 ms                                                                | 119 ms: 1.09x faster                                                 |
| pickle_pure_python       | 853 us                                                                | 785 us: 1.09x faster                                                 |
| coroutines               | 43.4 ms                                                               | 40.1 ms: 1.08x faster                                                |
| sqlglot_normalize        | 253 ms                                                                | 234 ms: 1.08x faster                                                 |
| regex_compile            | 324 ms                                                                | 301 ms: 1.08x faster                                                 |
| mako                     | 33.4 ms                                                               | 31.1 ms: 1.08x faster                                                |
| logging_format           | 19.0 us                                                               | 17.8 us: 1.07x faster                                                |
| scimark_sor              | 357 ms                                                                | 335 ms: 1.07x faster                                                 |
| pyflate                  | 1.12 sec                                                              | 1.05 sec: 1.06x faster                                               |
| genshi_text              | 65.5 ms                                                               | 61.6 ms: 1.06x faster                                                |
| xml_etree_generate       | 169 ms                                                                | 159 ms: 1.06x faster                                                 |
| xml_etree_process        | 139 ms                                                                | 131 ms: 1.06x faster                                                 |
| docutils                 | 5.09 sec                                                              | 4.80 sec: 1.06x faster                                               |
| async_generators         | 742 ms                                                                | 701 ms: 1.06x faster                                                 |
| deepcopy_reduce          | 6.38 us                                                               | 6.03 us: 1.06x faster                                                |
| tomli_loads              | 4.47 sec                                                              | 4.24 sec: 1.05x faster                                               |
| bench_mp_pool            | 61.3 ms                                                               | 58.4 ms: 1.05x faster                                                |
| pycparser                | 2.63 sec                                                              | 2.51 sec: 1.05x faster                                               |
| go                       | 396 ms                                                                | 379 ms: 1.04x faster                                                 |
| xml_etree_iterparse      | 183 ms                                                                | 176 ms: 1.04x faster                                                 |
| hexiom                   | 16.7 ms                                                               | 16.1 ms: 1.04x faster                                                |
| regex_dna                | 291 ms                                                                | 281 ms: 1.04x faster                                                 |
| sympy_expand             | 1.35 sec                                                              | 1.31 sec: 1.03x faster                                               |
| sympy_str                | 706 ms                                                                | 682 ms: 1.03x faster                                                 |
| fannkuch                 | 795 ms                                                                | 769 ms: 1.03x faster                                                 |
| sympy_sum                | 483 ms                                                                | 469 ms: 1.03x faster                                                 |
| mdp                      | 4.92 sec                                                              | 5.10 sec: 1.04x slower                                               |
| unpickle_list            | 8.18 us                                                               | 8.47 us: 1.04x slower                                                |
| unpickle                 | 25.9 us                                                               | 27.2 us: 1.05x slower                                                |
| json_loads               | 43.4 us                                                               | 45.8 us: 1.06x slower                                                |
| asyncio_tcp_ssl          | 3.05 sec                                                              | 3.30 sec: 1.08x slower                                               |
| tornado_http             | 317 ms                                                                | 345 ms: 1.09x slower                                                 |
| Geometric mean           | (ref)                                                                 | 1.04x faster                                                         |

Benchmark hidden because not significant (35): gc_traversal, meteor_contest, logging_simple, pidigits, asyncio_websockets, 2to3, asyncio_tcp, nqueens, deltablue, json_dumps, sympy_integrate, pylint, sqlglot_transpile, pathlib, unpack_sequence, generators, thrift, python_startup, richards, telco, pickle_list, coverage, pickle_dict, pickle, regex_effbot, float, create_gc_cycles, dulwich_log, sqlglot_parse, python_startup_no_site, sqlite_synth, regex_v8, crypto_pyaes, json, html5lib

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.02x