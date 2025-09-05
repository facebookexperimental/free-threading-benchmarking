# Results vs. 3.12.6

- fork: python
- ref: fc0305a2d8bef7cffaa4
- machine: linux-x86_64
- commit hash: fc0305a
- commit date: 2025-09-04
- overall geometric mean: 1.071x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250904-vultr-x86_64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 251 ms: 1.05x faster                                                  |
| docutils       | 2.64 sec                                               | 2.55 sec: 1.03x faster                                                |
| html5lib       | 63.6 ms                                                | 61.5 ms: 1.03x faster                                                 |
| Geometric mean | (ref)                                                  | 1.04x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250904-vultr-x86_64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 622 ms: 1.78x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 609 ms: 1.78x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 313 ms: 1.77x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 316 ms: 1.77x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 252 ms: 1.77x faster                                                  |
| async_tree_none            | 464 ms                                                 | 268 ms: 1.73x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 509 ms: 1.42x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 511 ms: 1.40x faster                                                  |
| async_generators           | 384 ms                                                 | 343 ms: 1.12x faster                                                  |
| coroutines                 | 23.9 ms                                                | 22.9 ms: 1.04x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.47x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250904-vultr-x86_64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 72.4 ms: 1.12x faster                                                 |
| nbody          | 89.3 ms                                                | 92.4 ms: 1.03x slower                                                 |
| pidigits       | 184 ms                                                 | 207 ms: 1.13x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250904-vultr-x86_64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.57 ms: 1.23x faster                                                 |
| regex_compile  | 142 ms                                                 | 123 ms: 1.16x faster                                                  |
| regex_v8       | 20.6 ms                                                | 21.8 ms: 1.06x slower                                                 |
| Geometric mean | (ref)                                                  | 1.08x faster                                                          |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250904-vultr-x86_64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.89 sec: 1.11x faster                                                |
| json_dumps           | 10.4 ms                                                | 9.59 ms: 1.08x faster                                                 |
| unpickle_pure_python | 221 us                                                 | 209 us: 1.05x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 132 ms: 1.05x faster                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 92.8 ms: 1.04x faster                                                 |
| xml_etree_generate   | 85.2 ms                                                | 82.8 ms: 1.03x faster                                                 |
| xml_etree_process    | 59.0 ms                                                | 58.1 ms: 1.02x faster                                                 |
| pickle_pure_python   | 308 us                                                 | 305 us: 1.01x faster                                                  |
| json_loads           | 26.5 us                                                | 28.0 us: 1.06x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.04x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250904-vultr-x86_64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.27 ms: 1.02x slower                                                 |
| python_startup         | 9.93 ms                                                | 12.5 ms: 1.26x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.13x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250904-vultr-x86_64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text    | 22.8 ms                                                | 20.4 ms: 1.12x faster                                                 |
| genshi_xml     | 50.2 ms                                                | 48.7 ms: 1.03x faster                                                 |
| mako           | 11.0 ms                                                | 11.5 ms: 1.04x slower                                                 |
| Geometric mean | (ref)                                                  | 1.03x faster                                                          |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250904-vultr-x86_64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.15 sec: 2.10x faster                                                |
| async_tree_io_tg           | 1.11 sec                                               | 622 ms: 1.78x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 609 ms: 1.78x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 313 ms: 1.77x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 316 ms: 1.77x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 252 ms: 1.77x faster                                                  |
| async_tree_none            | 464 ms                                                 | 268 ms: 1.73x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 26.6 us: 1.51x faster                                                 |
| deepcopy                   | 352 us                                                 | 242 us: 1.45x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 509 ms: 1.42x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 511 ms: 1.40x faster                                                  |
| go                         | 139 ms                                                 | 104 ms: 1.34x faster                                                  |
| comprehensions             | 19.8 us                                                | 15.7 us: 1.26x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.57 ms: 1.23x faster                                                 |
| deepcopy_reduce            | 3.08 us                                                | 2.57 us: 1.20x faster                                                 |
| scimark_sor                | 130 ms                                                 | 109 ms: 1.19x faster                                                  |
| spectral_norm              | 110 ms                                                 | 92.9 ms: 1.19x faster                                                 |
| raytrace                   | 299 ms                                                 | 253 ms: 1.18x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 66.6 ms: 1.18x faster                                                 |
| regex_compile              | 142 ms                                                 | 123 ms: 1.16x faster                                                  |
| pathlib                    | 21.5 ms                                                | 18.8 ms: 1.14x faster                                                 |
| logging_simple             | 6.63 us                                                | 5.81 us: 1.14x faster                                                 |
| pylint                     | 319 ms                                                 | 280 ms: 1.14x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.18 sec: 1.13x faster                                                |
| crypto_pyaes               | 76.6 ms                                                | 67.7 ms: 1.13x faster                                                 |
| logging_format             | 7.35 us                                                | 6.50 us: 1.13x faster                                                 |
| async_generators           | 384 ms                                                 | 343 ms: 1.12x faster                                                  |
| genshi_text                | 22.8 ms                                                | 20.4 ms: 1.12x faster                                                 |
| float                      | 80.8 ms                                                | 72.4 ms: 1.12x faster                                                 |
| generators                 | 32.2 ms                                                | 28.9 ms: 1.12x faster                                                 |
| tomli_loads                | 2.11 sec                                               | 1.89 sec: 1.11x faster                                                |
| logging_silent             | 109 ns                                                 | 97.8 ns: 1.11x faster                                                 |
| pyflate                    | 448 ms                                                 | 402 ms: 1.11x faster                                                  |
| chaos                      | 62.8 ms                                                | 56.5 ms: 1.11x faster                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 61.5 ms: 1.11x faster                                                 |
| richards                   | 45.9 ms                                                | 41.5 ms: 1.11x faster                                                 |
| hexiom                     | 6.17 ms                                                | 5.59 ms: 1.10x faster                                                 |
| richards_super             | 51.9 ms                                                | 47.4 ms: 1.09x faster                                                 |
| sympy_integrate            | 20.5 ms                                                | 18.9 ms: 1.09x faster                                                 |
| sympy_str                  | 292 ms                                                 | 269 ms: 1.08x faster                                                  |
| json_dumps                 | 10.4 ms                                                | 9.59 ms: 1.08x faster                                                 |
| sympy_sum                  | 166 ms                                                 | 154 ms: 1.08x faster                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.41 sec: 1.07x faster                                                |
| pycparser                  | 1.17 sec                                               | 1.09 sec: 1.07x faster                                                |
| typing_runtime_protocols   | 163 us                                                 | 152 us: 1.07x faster                                                  |
| pprint_safe_repr           | 743 ms                                                 | 696 ms: 1.07x faster                                                  |
| thrift                     | 791 us                                                 | 750 us: 1.06x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 209 us: 1.05x faster                                                  |
| 2to3                       | 264 ms                                                 | 251 ms: 1.05x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 132 ms: 1.05x faster                                                  |
| deltablue                  | 3.45 ms                                                | 3.29 ms: 1.05x faster                                                 |
| scimark_lu                 | 114 ms                                                 | 109 ms: 1.04x faster                                                  |
| coroutines                 | 23.9 ms                                                | 22.9 ms: 1.04x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 92.8 ms: 1.04x faster                                                 |
| nqueens                    | 80.1 ms                                                | 77.1 ms: 1.04x faster                                                 |
| meteor_contest             | 104 ms                                                 | 99.8 ms: 1.04x faster                                                 |
| docutils                   | 2.64 sec                                               | 2.55 sec: 1.03x faster                                                |
| html5lib                   | 63.6 ms                                                | 61.5 ms: 1.03x faster                                                 |
| scimark_fft                | 342 ms                                                 | 331 ms: 1.03x faster                                                  |
| genshi_xml                 | 50.2 ms                                                | 48.7 ms: 1.03x faster                                                 |
| xml_etree_generate         | 85.2 ms                                                | 82.8 ms: 1.03x faster                                                 |
| xml_etree_process          | 59.0 ms                                                | 58.1 ms: 1.02x faster                                                 |
| sympy_expand               | 468 ms                                                 | 462 ms: 1.01x faster                                                  |
| pickle_pure_python         | 308 us                                                 | 305 us: 1.01x faster                                                  |
| python_startup_no_site     | 7.16 ms                                                | 7.27 ms: 1.02x slower                                                 |
| fannkuch                   | 372 ms                                                 | 380 ms: 1.02x slower                                                  |
| nbody                      | 89.3 ms                                                | 92.4 ms: 1.03x slower                                                 |
| mako                       | 11.0 ms                                                | 11.5 ms: 1.04x slower                                                 |
| sqlite_synth               | 2.20 us                                                | 2.31 us: 1.05x slower                                                 |
| json_loads                 | 26.5 us                                                | 28.0 us: 1.06x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 21.8 ms: 1.06x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.01 ms: 1.08x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.77 ms: 1.09x slower                                                 |
| pidigits                   | 184 ms                                                 | 207 ms: 1.13x slower                                                  |
| coverage                   | 71.4 ms                                                | 81.0 ms: 1.13x slower                                                 |
| python_startup             | 9.93 ms                                                | 12.5 ms: 1.26x slower                                                 |
| gc_traversal               | 3.46 ms                                                | 4.65 ms: 1.35x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.93 ms: 1.76x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 97.8 ms: 9.06x slower                                                 |
| telco                      | 6.53 ms                                                | 158 ms: 24.17x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                          |

Benchmark hidden because not significant (4): json, django_template, asyncio_websockets, regex_dna
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250904-3.15.0a0-fc0305a/bm-20250904-vultr-x86_64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.071x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.16x