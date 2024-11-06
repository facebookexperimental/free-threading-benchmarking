# Results vs. base

- fork: mpage
- ref: gh_115999_tlbc_integ
- machine: linux-x86_64
- commit hash: 0a68813
- commit date: 2024-10-31
- overall geometric mean: 1.05x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241013-linux-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241031-linux-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| docutils       | 5.09 sec                                                              | 4.88 sec: 1.04x faster                                               |
| tornado_http   | 317 ms                                                                | 332 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.01x slower                                                         |

Benchmark hidden because not significant (2): 2to3, html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark       | bm-20241013-linux-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241031-linux-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|-----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| coroutines      | 43.4 ms                                                               | 40.4 ms: 1.07x faster                                                |
| asyncio_tcp_ssl | 3.05 sec                                                              | 3.21 sec: 1.05x slower                                               |
| Geometric mean  | (ref)                                                                 | 1.00x faster                                                         |

Benchmark hidden because not significant (3): async_generators, asyncio_websockets, asyncio_tcp

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241013-linux-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241031-linux-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| nbody          | 340 ms                                                                | 309 ms: 1.10x faster                                                 |
| pidigits       | 249 ms                                                                | 237 ms: 1.05x faster                                                 |
| Geometric mean | (ref)                                                                 | 1.06x faster                                                         |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

Benchmark hidden because not significant (4): regex_compile, regex_v8, regex_effbot, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241013-linux-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241031-linux-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|----------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| unpickle_pure_python | 623 us                                                                | 521 us: 1.20x faster                                                 |
| pickle_pure_python   | 853 us                                                                | 769 us: 1.11x faster                                                 |
| xml_etree_parse      | 250 ms                                                                | 229 ms: 1.09x faster                                                 |
| xml_etree_process    | 139 ms                                                                | 128 ms: 1.09x faster                                                 |
| pickle_list          | 6.42 us                                                               | 5.97 us: 1.07x faster                                                |
| xml_etree_iterparse  | 183 ms                                                                | 173 ms: 1.06x faster                                                 |
| pickle_dict          | 45.2 us                                                               | 43.4 us: 1.04x faster                                                |
| tomli_loads          | 4.47 sec                                                              | 4.33 sec: 1.03x faster                                               |
| pickle               | 15.2 us                                                               | 16.0 us: 1.05x slower                                                |
| Geometric mean       | (ref)                                                                 | 1.04x faster                                                         |

Benchmark hidden because not significant (5): xml_etree_generate, json_loads, unpickle, unpickle_list, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241013-linux-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241031-linux-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 18.7 ms                                                               | 19.4 ms: 1.04x slower                                                |
| Geometric mean         | (ref)                                                                 | 1.02x slower                                                         |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241013-linux-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241031-linux-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|-----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 143 ms                                                                | 117 ms: 1.22x faster                                                 |
| django_template | 92.1 ms                                                               | 83.1 ms: 1.11x faster                                                |
| mako            | 33.4 ms                                                               | 30.6 ms: 1.09x faster                                                |
| genshi_text     | 65.5 ms                                                               | 62.1 ms: 1.05x faster                                                |
| Geometric mean  | (ref)                                                                 | 1.12x faster                                                         |

All benchmarks:
===============

| Benchmark                | bm-20241013-linux-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db | bm-20241031-linux-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|--------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml               | 143 ms                                                                | 117 ms: 1.22x faster                                                 |
| deepcopy_memo            | 82.4 us                                                               | 67.9 us: 1.21x faster                                                |
| unpickle_pure_python     | 623 us                                                                | 521 us: 1.20x faster                                                 |
| scimark_lu               | 325 ms                                                                | 274 ms: 1.19x faster                                                 |
| scimark_sparse_mat_mult  | 9.79 ms                                                               | 8.27 ms: 1.18x faster                                                |
| scimark_fft              | 660 ms                                                                | 564 ms: 1.17x faster                                                 |
| deepcopy                 | 643 us                                                                | 555 us: 1.16x faster                                                 |
| raytrace                 | 858 ms                                                                | 744 ms: 1.15x faster                                                 |
| spectral_norm            | 264 ms                                                                | 231 ms: 1.14x faster                                                 |
| pprint_safe_repr         | 1.78 sec                                                              | 1.55 sec: 1.14x faster                                               |
| scimark_monte_carlo      | 173 ms                                                                | 153 ms: 1.13x faster                                                 |
| pprint_pformat           | 3.64 sec                                                              | 3.22 sec: 1.13x faster                                               |
| chaos                    | 187 ms                                                                | 166 ms: 1.12x faster                                                 |
| logging_silent           | 279 ns                                                                | 249 ns: 1.12x faster                                                 |
| bpe_tokeniser            | 10.4 sec                                                              | 9.26 sec: 1.12x faster                                               |
| pickle_pure_python       | 853 us                                                                | 769 us: 1.11x faster                                                 |
| django_template          | 92.1 ms                                                               | 83.1 ms: 1.11x faster                                                |
| sqlglot_normalize        | 253 ms                                                                | 229 ms: 1.10x faster                                                 |
| deepcopy_reduce          | 6.38 us                                                               | 5.79 us: 1.10x faster                                                |
| nbody                    | 340 ms                                                                | 309 ms: 1.10x faster                                                 |
| go                       | 396 ms                                                                | 361 ms: 1.10x faster                                                 |
| richards                 | 119 ms                                                                | 109 ms: 1.09x faster                                                 |
| mako                     | 33.4 ms                                                               | 30.6 ms: 1.09x faster                                                |
| xml_etree_parse          | 250 ms                                                                | 229 ms: 1.09x faster                                                 |
| xml_etree_process        | 139 ms                                                                | 128 ms: 1.09x faster                                                 |
| sqlglot_optimize         | 129 ms                                                                | 119 ms: 1.09x faster                                                 |
| coverage                 | 152 ms                                                                | 141 ms: 1.08x faster                                                 |
| pickle_list              | 6.42 us                                                               | 5.97 us: 1.07x faster                                                |
| pycparser                | 2.63 sec                                                              | 2.45 sec: 1.07x faster                                               |
| coroutines               | 43.4 ms                                                               | 40.4 ms: 1.07x faster                                                |
| typing_runtime_protocols | 372 us                                                                | 347 us: 1.07x faster                                                 |
| sympy_str                | 706 ms                                                                | 660 ms: 1.07x faster                                                 |
| sqlglot_transpile        | 5.03 ms                                                               | 4.70 ms: 1.07x faster                                                |
| thrift                   | 1.86 ms                                                               | 1.74 ms: 1.07x faster                                                |
| logging_format           | 19.0 us                                                               | 17.9 us: 1.07x faster                                                |
| sympy_expand             | 1.35 sec                                                              | 1.27 sec: 1.07x faster                                               |
| hexiom                   | 16.7 ms                                                               | 15.7 ms: 1.06x faster                                                |
| xml_etree_iterparse      | 183 ms                                                                | 173 ms: 1.06x faster                                                 |
| nqueens                  | 167 ms                                                                | 158 ms: 1.06x faster                                                 |
| sympy_integrate          | 47.1 ms                                                               | 44.6 ms: 1.06x faster                                                |
| genshi_text              | 65.5 ms                                                               | 62.1 ms: 1.05x faster                                                |
| telco                    | 14.9 ms                                                               | 14.1 ms: 1.05x faster                                                |
| bench_mp_pool            | 61.3 ms                                                               | 58.4 ms: 1.05x faster                                                |
| pidigits                 | 249 ms                                                                | 237 ms: 1.05x faster                                                 |
| docutils                 | 5.09 sec                                                              | 4.88 sec: 1.04x faster                                               |
| pickle_dict              | 45.2 us                                                               | 43.4 us: 1.04x faster                                                |
| scimark_sor              | 357 ms                                                                | 344 ms: 1.04x faster                                                 |
| pyflate                  | 1.12 sec                                                              | 1.08 sec: 1.04x faster                                               |
| generators               | 61.1 ms                                                               | 58.8 ms: 1.04x faster                                                |
| fannkuch                 | 795 ms                                                                | 766 ms: 1.04x faster                                                 |
| tomli_loads              | 4.47 sec                                                              | 4.33 sec: 1.03x faster                                               |
| python_startup_no_site   | 18.7 ms                                                               | 19.4 ms: 1.04x slower                                                |
| tornado_http             | 317 ms                                                                | 332 ms: 1.05x slower                                                 |
| mdp                      | 4.92 sec                                                              | 5.15 sec: 1.05x slower                                               |
| asyncio_tcp_ssl          | 3.05 sec                                                              | 3.21 sec: 1.05x slower                                               |
| pickle                   | 15.2 us                                                               | 16.0 us: 1.05x slower                                                |
| Geometric mean           | (ref)                                                                 | 1.05x faster                                                         |

Benchmark hidden because not significant (33): regex_compile, pylint, richards_super, meteor_contest, deltablue, dulwich_log, comprehensions, regex_v8, crypto_pyaes, float, xml_etree_generate, gc_traversal, sqlglot_parse, json, sqlite_synth, sympy_sum, async_generators, bench_thread_pool, json_loads, asyncio_websockets, unpickle, 2to3, logging_simple, pathlib, regex_effbot, python_startup, create_gc_cycles, unpickle_list, asyncio_tcp, unpack_sequence, json_dumps, html5lib, regex_dna

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.02x