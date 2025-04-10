# Results vs. 3.12.6

- fork: python
- ref: 180ee43bde99b8ce4c4f
- machine: linux-x86_64
- commit hash: 180ee43
- commit date: 2025-01-28
- overall geometric mean: 1.094x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-vultr-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 253 ms: 1.04x faster                                                   |
| docutils       | 2.64 sec                                               | 2.56 sec: 1.03x faster                                                 |
| Geometric mean | (ref)                                                  | 1.04x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-vultr-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 623 ms: 1.78x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 316 ms: 1.77x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 620 ms: 1.75x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 322 ms: 1.73x faster                                                   |
| async_tree_none            | 464 ms                                                 | 271 ms: 1.72x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 263 ms: 1.69x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 483 ms: 1.49x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 497 ms: 1.44x faster                                                   |
| async_generators           | 384 ms                                                 | 325 ms: 1.18x faster                                                   |
| coroutines                 | 23.9 ms                                                | 21.7 ms: 1.10x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.49x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-vultr-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 72.5 ms: 1.11x faster                                                  |
| nbody          | 89.3 ms                                                | 88.0 ms: 1.02x faster                                                  |
| pidigits       | 184 ms                                                 | 200 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-vultr-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.76 ms: 1.15x faster                                                  |
| regex_compile  | 142 ms                                                 | 126 ms: 1.13x faster                                                   |
| regex_dna      | 168 ms                                                 | 169 ms: 1.01x slower                                                   |
| regex_v8       | 20.6 ms                                                | 23.7 ms: 1.15x slower                                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-vultr-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 126 ms: 1.10x faster                                                   |
| tomli_loads          | 2.11 sec                                               | 1.92 sec: 1.10x faster                                                 |
| xml_etree_iterparse  | 96.7 ms                                                | 90.5 ms: 1.07x faster                                                  |
| unpickle_pure_python | 221 us                                                 | 212 us: 1.04x faster                                                   |
| xml_etree_generate   | 85.2 ms                                                | 83.3 ms: 1.02x faster                                                  |
| xml_etree_process    | 59.0 ms                                                | 58.4 ms: 1.01x faster                                                  |
| pickle_pure_python   | 308 us                                                 | 313 us: 1.02x slower                                                   |
| json_loads           | 26.5 us                                                | 28.7 us: 1.08x slower                                                  |
| json_dumps           | 10.4 ms                                                | 11.2 ms: 1.08x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-vultr-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.41 ms: 1.04x slower                                                  |
| python_startup         | 9.93 ms                                                | 14.6 ms: 1.47x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.23x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-vultr-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 21.0 ms: 1.08x faster                                                  |
| genshi_xml      | 50.2 ms                                                | 48.3 ms: 1.04x faster                                                  |
| django_template | 34.7 ms                                                | 35.1 ms: 1.01x slower                                                  |
| mako            | 11.0 ms                                                | 11.6 ms: 1.05x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.01x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-vultr-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 623 ms: 1.78x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 316 ms: 1.77x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 620 ms: 1.75x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 322 ms: 1.73x faster                                                   |
| async_tree_none            | 464 ms                                                 | 271 ms: 1.72x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 263 ms: 1.69x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 483 ms: 1.49x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 497 ms: 1.44x faster                                                   |
| deepcopy                   | 352 us                                                 | 256 us: 1.37x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 29.9 us: 1.35x faster                                                  |
| go                         | 139 ms                                                 | 115 ms: 1.21x faster                                                   |
| pathlib                    | 21.5 ms                                                | 18.0 ms: 1.19x faster                                                  |
| spectral_norm              | 110 ms                                                 | 92.6 ms: 1.19x faster                                                  |
| comprehensions             | 19.8 us                                                | 16.7 us: 1.19x faster                                                  |
| async_generators           | 384 ms                                                 | 325 ms: 1.18x faster                                                   |
| deepcopy_reduce            | 3.08 us                                                | 2.63 us: 1.17x faster                                                  |
| crypto_pyaes               | 76.6 ms                                                | 65.9 ms: 1.16x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.76 ms: 1.15x faster                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.1 ms: 1.14x faster                                                  |
| pylint                     | 319 ms                                                 | 279 ms: 1.14x faster                                                   |
| raytrace                   | 299 ms                                                 | 263 ms: 1.14x faster                                                   |
| scimark_sor                | 130 ms                                                 | 114 ms: 1.14x faster                                                   |
| regex_compile              | 142 ms                                                 | 126 ms: 1.13x faster                                                   |
| chaos                      | 62.8 ms                                                | 55.7 ms: 1.13x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.22 sec: 1.12x faster                                                 |
| sqlalchemy_declarative     | 143 ms                                                 | 127 ms: 1.12x faster                                                   |
| deltablue                  | 3.45 ms                                                | 3.08 ms: 1.12x faster                                                  |
| generators                 | 32.2 ms                                                | 28.9 ms: 1.12x faster                                                  |
| float                      | 80.8 ms                                                | 72.5 ms: 1.11x faster                                                  |
| coroutines                 | 23.9 ms                                                | 21.7 ms: 1.10x faster                                                  |
| scimark_fft                | 342 ms                                                 | 310 ms: 1.10x faster                                                   |
| richards                   | 45.9 ms                                                | 41.7 ms: 1.10x faster                                                  |
| logging_simple             | 6.63 us                                                | 6.03 us: 1.10x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 126 ms: 1.10x faster                                                   |
| tomli_loads                | 2.11 sec                                               | 1.92 sec: 1.10x faster                                                 |
| sqlglot_parse              | 1.36 ms                                                | 1.24 ms: 1.09x faster                                                  |
| logging_format             | 7.35 us                                                | 6.75 us: 1.09x faster                                                  |
| sympy_sum                  | 166 ms                                                 | 153 ms: 1.09x faster                                                   |
| genshi_text                | 22.8 ms                                                | 21.0 ms: 1.08x faster                                                  |
| hexiom                     | 6.17 ms                                                | 5.70 ms: 1.08x faster                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 1.54 ms: 1.08x faster                                                  |
| pyflate                    | 448 ms                                                 | 414 ms: 1.08x faster                                                   |
| thrift                     | 791 us                                                 | 732 us: 1.08x faster                                                   |
| richards_super             | 51.9 ms                                                | 48.2 ms: 1.08x faster                                                  |
| sympy_str                  | 292 ms                                                 | 271 ms: 1.08x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 90.5 ms: 1.07x faster                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.12 ms: 1.07x faster                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 64.3 ms: 1.06x faster                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.43 sec: 1.06x faster                                                 |
| meteor_contest             | 104 ms                                                 | 97.7 ms: 1.06x faster                                                  |
| pprint_safe_repr           | 743 ms                                                 | 705 ms: 1.05x faster                                                   |
| logging_silent             | 109 ns                                                 | 103 ns: 1.05x faster                                                   |
| pycparser                  | 1.17 sec                                               | 1.11 sec: 1.05x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 75.1 ms: 1.05x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 212 us: 1.04x faster                                                   |
| 2to3                       | 264 ms                                                 | 253 ms: 1.04x faster                                                   |
| typing_runtime_protocols   | 163 us                                                 | 157 us: 1.04x faster                                                   |
| sympy_integrate            | 20.5 ms                                                | 19.8 ms: 1.04x faster                                                  |
| genshi_xml                 | 50.2 ms                                                | 48.3 ms: 1.04x faster                                                  |
| scimark_lu                 | 114 ms                                                 | 111 ms: 1.03x faster                                                   |
| docutils                   | 2.64 sec                                               | 2.56 sec: 1.03x faster                                                 |
| nqueens                    | 80.1 ms                                                | 78.2 ms: 1.02x faster                                                  |
| xml_etree_generate         | 85.2 ms                                                | 83.3 ms: 1.02x faster                                                  |
| sqlglot_optimize           | 53.3 ms                                                | 52.1 ms: 1.02x faster                                                  |
| sqlglot_normalize          | 107 ms                                                 | 104 ms: 1.02x faster                                                   |
| sympy_expand               | 468 ms                                                 | 459 ms: 1.02x faster                                                   |
| nbody                      | 89.3 ms                                                | 88.0 ms: 1.02x faster                                                  |
| xml_etree_process          | 59.0 ms                                                | 58.4 ms: 1.01x faster                                                  |
| fannkuch                   | 372 ms                                                 | 371 ms: 1.00x faster                                                   |
| regex_dna                  | 168 ms                                                 | 169 ms: 1.01x slower                                                   |
| json                       | 5.02 ms                                                | 5.07 ms: 1.01x slower                                                  |
| django_template            | 34.7 ms                                                | 35.1 ms: 1.01x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 313 us: 1.02x slower                                                   |
| mdp                        | 2.42 sec                                               | 2.47 sec: 1.02x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 7.41 ms: 1.04x slower                                                  |
| mako                       | 11.0 ms                                                | 11.6 ms: 1.05x slower                                                  |
| json_loads                 | 26.5 us                                                | 28.7 us: 1.08x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 11.2 ms: 1.08x slower                                                  |
| pidigits                   | 184 ms                                                 | 200 ms: 1.09x slower                                                   |
| telco                      | 6.53 ms                                                | 7.14 ms: 1.09x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.03 ms: 1.10x slower                                                  |
| coverage                   | 71.4 ms                                                | 79.6 ms: 1.12x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 23.7 ms: 1.15x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 4.37 ms: 1.27x slower                                                  |
| python_startup             | 9.93 ms                                                | 14.6 ms: 1.47x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.85 ms: 1.69x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 88.1 ms: 8.16x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                           |

Benchmark hidden because not significant (2): sqlite_synth, asyncio_websockets
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250128-3.14.0a4+-180ee43/bm-20250128-vultr-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.094x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.11x