# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_tlbc_call_
- machine: linux-x86_64
- commit hash: c0d3c19
- commit date: 2024-12-04
- overall geometric mean: 1.019x faster
- HPT reliability: 61.26%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 258 ms: 1.00x faster                                                  |
| docutils       | 2.62 sec                                                     | 2.57 sec: 1.02x faster                                                |
| Geometric mean | (ref)                                                        | 1.01x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 628 ms: 1.45x faster                                                  |
| async_tree_io              | 876 ms                                                       | 627 ms: 1.40x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 340 ms: 1.36x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 315 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 508 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 492 ms: 1.30x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 263 ms: 1.28x faster                                                  |
| async_tree_none            | 354 ms                                                       | 279 ms: 1.27x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 22.3 ms: 1.06x faster                                                 |
| async_generators           | 377 ms                                                       | 368 ms: 1.03x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 522 ms: 1.00x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.24x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 185 ms: 1.17x faster                                                  |
| float          | 77.5 ms                                                      | 79.4 ms: 1.03x slower                                                 |
| nbody          | 85.1 ms                                                      | 95.8 ms: 1.13x slower                                                 |
| Geometric mean | (ref)                                                        | 1.00x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.76 ms: 1.12x faster                                                 |
| regex_dna      | 180 ms                                                       | 178 ms: 1.01x faster                                                  |
| regex_compile  | 132 ms                                                       | 131 ms: 1.01x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 25.2 ms: 1.11x slower                                                 |
| Geometric mean | (ref)                                                        | 1.01x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_loads           | 27.0 us                                                      | 25.1 us: 1.08x faster                                                 |
| xml_etree_parse      | 136 ms                                                       | 129 ms: 1.06x faster                                                  |
| xml_etree_iterparse  | 94.9 ms                                                      | 92.0 ms: 1.03x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 86.1 ms: 1.01x slower                                                 |
| xml_etree_process    | 59.3 ms                                                      | 60.5 ms: 1.02x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 218 us: 1.04x slower                                                  |
| tomli_loads          | 2.01 sec                                                     | 2.11 sec: 1.05x slower                                                |
| pickle_pure_python   | 294 us                                                       | 321 us: 1.09x slower                                                  |
| json_dumps           | 10.5 ms                                                      | 11.5 ms: 1.09x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.01x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.45 ms: 1.01x slower                                                 |
| python_startup         | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.16x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 22.4 ms: 1.04x slower                                                 |
| django_template | 34.1 ms                                                      | 35.6 ms: 1.04x slower                                                 |
| mako            | 11.3 ms                                                      | 11.9 ms: 1.05x slower                                                 |
| genshi_xml      | 48.8 ms                                                      | 52.3 ms: 1.07x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.05x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 628 ms: 1.45x faster                                                  |
| async_tree_io              | 876 ms                                                       | 627 ms: 1.40x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 340 ms: 1.36x faster                                                  |
| deepcopy                   | 355 us                                                       | 268 us: 1.33x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 315 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 508 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 492 ms: 1.30x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 263 ms: 1.28x faster                                                  |
| async_tree_none            | 354 ms                                                       | 279 ms: 1.27x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 31.4 us: 1.24x faster                                                 |
| pidigits                   | 217 ms                                                       | 185 ms: 1.17x faster                                                  |
| go                         | 141 ms                                                       | 121 ms: 1.16x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.69 us: 1.16x faster                                                 |
| regex_effbot               | 3.08 ms                                                      | 2.76 ms: 1.12x faster                                                 |
| pylint                     | 317 ms                                                       | 286 ms: 1.11x faster                                                  |
| telco                      | 7.82 ms                                                      | 7.24 ms: 1.08x faster                                                 |
| json_loads                 | 27.0 us                                                      | 25.1 us: 1.08x faster                                                 |
| json                       | 4.93 ms                                                      | 4.59 ms: 1.07x faster                                                 |
| xml_etree_parse            | 136 ms                                                       | 129 ms: 1.06x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 22.3 ms: 1.06x faster                                                 |
| pathlib                    | 19.2 ms                                                      | 18.3 ms: 1.05x faster                                                 |
| coverage                   | 83.0 ms                                                      | 79.3 ms: 1.05x faster                                                 |
| thrift                     | 778 us                                                       | 746 us: 1.04x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 92.0 ms: 1.03x faster                                                 |
| async_generators           | 377 ms                                                       | 368 ms: 1.03x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.35 sec: 1.02x faster                                                |
| docutils                   | 2.62 sec                                                     | 2.57 sec: 1.02x faster                                                |
| regex_dna                  | 180 ms                                                       | 178 ms: 1.01x faster                                                  |
| regex_compile              | 132 ms                                                       | 131 ms: 1.01x faster                                                  |
| pprint_safe_repr           | 738 ms                                                       | 729 ms: 1.01x faster                                                  |
| meteor_contest             | 102 ms                                                       | 101 ms: 1.01x faster                                                  |
| sympy_sum                  | 156 ms                                                       | 154 ms: 1.01x faster                                                  |
| scimark_fft                | 349 ms                                                       | 346 ms: 1.01x faster                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.49 sec: 1.01x faster                                                |
| 2to3                       | 260 ms                                                       | 258 ms: 1.00x faster                                                  |
| hexiom                     | 5.99 ms                                                      | 5.98 ms: 1.00x faster                                                 |
| spectral_norm              | 111 ms                                                       | 111 ms: 1.00x slower                                                  |
| asyncio_websockets         | 520 ms                                                       | 522 ms: 1.00x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 68.2 ms: 1.00x slower                                                 |
| nqueens                    | 78.6 ms                                                      | 79.0 ms: 1.01x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 86.1 ms: 1.01x slower                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 7.45 ms: 1.01x slower                                                 |
| dulwich_log                | 74.8 ms                                                      | 75.7 ms: 1.01x slower                                                 |
| logging_simple             | 6.16 us                                                      | 6.25 us: 1.02x slower                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 66.4 ms: 1.02x slower                                                 |
| sympy_expand               | 457 ms                                                       | 465 ms: 1.02x slower                                                  |
| sympy_integrate            | 19.8 ms                                                      | 20.2 ms: 1.02x slower                                                 |
| xml_etree_process          | 59.3 ms                                                      | 60.5 ms: 1.02x slower                                                 |
| pycparser                  | 1.12 sec                                                     | 1.14 sec: 1.02x slower                                                |
| logging_format             | 6.84 us                                                      | 6.99 us: 1.02x slower                                                 |
| fannkuch                   | 370 ms                                                       | 379 ms: 1.03x slower                                                  |
| float                      | 77.5 ms                                                      | 79.4 ms: 1.03x slower                                                 |
| sqlite_synth               | 2.21 us                                                      | 2.26 us: 1.03x slower                                                 |
| sqlglot_optimize           | 52.7 ms                                                      | 54.2 ms: 1.03x slower                                                 |
| richards_super             | 51.6 ms                                                      | 53.2 ms: 1.03x slower                                                 |
| sqlglot_normalize          | 106 ms                                                       | 109 ms: 1.03x slower                                                  |
| chaos                      | 57.3 ms                                                      | 59.3 ms: 1.04x slower                                                 |
| genshi_text                | 21.5 ms                                                      | 22.4 ms: 1.04x slower                                                 |
| typing_runtime_protocols   | 155 us                                                       | 161 us: 1.04x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 218 us: 1.04x slower                                                  |
| sqlglot_transpile          | 1.56 ms                                                      | 1.62 ms: 1.04x slower                                                 |
| django_template            | 34.1 ms                                                      | 35.6 ms: 1.04x slower                                                 |
| richards                   | 45.2 ms                                                      | 47.3 ms: 1.04x slower                                                 |
| mako                       | 11.3 ms                                                      | 11.9 ms: 1.05x slower                                                 |
| sqlglot_parse              | 1.25 ms                                                      | 1.31 ms: 1.05x slower                                                 |
| tomli_loads                | 2.01 sec                                                     | 2.11 sec: 1.05x slower                                                |
| deltablue                  | 3.12 ms                                                      | 3.29 ms: 1.05x slower                                                 |
| logging_silent             | 103 ns                                                       | 108 ns: 1.06x slower                                                  |
| comprehensions             | 16.5 us                                                      | 17.5 us: 1.06x slower                                                 |
| genshi_xml                 | 48.8 ms                                                      | 52.3 ms: 1.07x slower                                                 |
| raytrace                   | 253 ms                                                       | 272 ms: 1.08x slower                                                  |
| mdp                        | 2.36 sec                                                     | 2.54 sec: 1.08x slower                                                |
| pickle_pure_python         | 294 us                                                       | 321 us: 1.09x slower                                                  |
| json_dumps                 | 10.5 ms                                                      | 11.5 ms: 1.09x slower                                                 |
| regex_v8                   | 22.7 ms                                                      | 25.2 ms: 1.11x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.03 ms: 1.12x slower                                                 |
| nbody                      | 85.1 ms                                                      | 95.8 ms: 1.13x slower                                                 |
| python_startup             | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.83 ms: 1.36x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 4.69 ms: 1.49x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 88.6 ms: 8.06x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.01x slower                                                          |

Benchmark hidden because not significant (6): scimark_sparse_mat_mult, scimark_lu, scimark_sor, pyflate, generators, sympy_str
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241204-3.14.0a2+-c0d3c19/bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.019x faster

# HPT report

- Reliability score: 61.26% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.09x