# Results vs. 3.12.6

- fork: python
- ref: bfb0788bfcaab7474c1b
- machine: linux-x86_64
- commit hash: bfb0788
- commit date: 2024-12-03
- overall geometric mean: 1.059x faster
- HPT reliability: 99.98%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 259 ms: 1.02x faster                                                   |
| docutils       | 2.64 sec                                               | 2.58 sec: 1.02x faster                                                 |
| Geometric mean | (ref)                                                  | 1.02x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 314 ms: 1.78x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 629 ms: 1.77x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 629 ms: 1.72x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 264 ms: 1.69x faster                                                   |
| async_tree_none            | 464 ms                                                 | 278 ms: 1.67x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 341 ms: 1.63x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 487 ms: 1.48x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 503 ms: 1.42x faster                                                   |
| coroutines                 | 23.9 ms                                                | 22.5 ms: 1.06x faster                                                  |
| async_generators           | 384 ms                                                 | 366 ms: 1.05x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 523 ms: 1.01x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.45x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 79.2 ms: 1.02x faster                                                  |
| pidigits       | 184 ms                                                 | 185 ms: 1.00x slower                                                   |
| nbody          | 89.3 ms                                                | 95.5 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                  | 1.02x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.79 ms: 1.14x faster                                                  |
| regex_compile  | 142 ms                                                 | 131 ms: 1.09x faster                                                   |
| regex_dna      | 168 ms                                                 | 171 ms: 1.02x slower                                                   |
| regex_v8       | 20.6 ms                                                | 23.7 ms: 1.15x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                                   |
| xml_etree_iterparse  | 96.7 ms                                                | 92.3 ms: 1.05x faster                                                  |
| json_loads           | 26.5 us                                                | 25.4 us: 1.04x faster                                                  |
| xml_etree_generate   | 85.2 ms                                                | 85.8 ms: 1.01x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 222 us: 1.01x slower                                                   |
| xml_etree_process    | 59.0 ms                                                | 60.1 ms: 1.02x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 322 us: 1.05x slower                                                   |
| json_dumps           | 10.4 ms                                                | 11.4 ms: 1.10x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.00x slower                                                           |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.50 ms: 1.05x slower                                                  |
| python_startup         | 9.93 ms                                                | 14.7 ms: 1.48x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.24x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 22.1 ms: 1.03x faster                                                  |
| genshi_xml      | 50.2 ms                                                | 50.5 ms: 1.01x slower                                                  |
| django_template | 34.7 ms                                                | 36.3 ms: 1.05x slower                                                  |
| mako            | 11.0 ms                                                | 11.6 ms: 1.06x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.02x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 314 ms: 1.78x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 629 ms: 1.77x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 629 ms: 1.72x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 264 ms: 1.69x faster                                                   |
| async_tree_none            | 464 ms                                                 | 278 ms: 1.67x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 341 ms: 1.63x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 487 ms: 1.48x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 503 ms: 1.42x faster                                                   |
| deepcopy                   | 352 us                                                 | 266 us: 1.32x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 31.1 us: 1.30x faster                                                  |
| pathlib                    | 21.5 ms                                                | 18.2 ms: 1.18x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.68 us: 1.15x faster                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.2 ms: 1.14x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.79 ms: 1.14x faster                                                  |
| crypto_pyaes               | 76.6 ms                                                | 67.6 ms: 1.13x faster                                                  |
| go                         | 139 ms                                                 | 124 ms: 1.12x faster                                                   |
| sqlalchemy_declarative     | 143 ms                                                 | 128 ms: 1.12x faster                                                   |
| pylint                     | 319 ms                                                 | 285 ms: 1.12x faster                                                   |
| comprehensions             | 19.8 us                                                | 17.8 us: 1.11x faster                                                  |
| generators                 | 32.2 ms                                                | 29.1 ms: 1.11x faster                                                  |
| json                       | 5.02 ms                                                | 4.56 ms: 1.10x faster                                                  |
| raytrace                   | 299 ms                                                 | 272 ms: 1.10x faster                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 4.34 sec: 1.09x faster                                                 |
| regex_compile              | 142 ms                                                 | 131 ms: 1.09x faster                                                   |
| sympy_sum                  | 166 ms                                                 | 154 ms: 1.07x faster                                                   |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                                   |
| thrift                     | 791 us                                                 | 744 us: 1.06x faster                                                   |
| coroutines                 | 23.9 ms                                                | 22.5 ms: 1.06x faster                                                  |
| sympy_str                  | 292 ms                                                 | 277 ms: 1.05x faster                                                   |
| async_generators           | 384 ms                                                 | 366 ms: 1.05x faster                                                   |
| chaos                      | 62.8 ms                                                | 60.0 ms: 1.05x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 92.3 ms: 1.05x faster                                                  |
| json_loads                 | 26.5 us                                                | 25.4 us: 1.04x faster                                                  |
| logging_simple             | 6.63 us                                                | 6.36 us: 1.04x faster                                                  |
| typing_runtime_protocols   | 163 us                                                 | 157 us: 1.04x faster                                                   |
| dulwich_log                | 78.9 ms                                                | 76.2 ms: 1.04x faster                                                  |
| genshi_text                | 22.8 ms                                                | 22.1 ms: 1.03x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.13 sec: 1.03x faster                                                 |
| logging_format             | 7.35 us                                                | 7.12 us: 1.03x faster                                                  |
| meteor_contest             | 104 ms                                                 | 100 ms: 1.03x faster                                                   |
| mdp                        | 2.42 sec                                               | 2.34 sec: 1.03x faster                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 66.4 ms: 1.03x faster                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.48 sec: 1.03x faster                                                 |
| sqlglot_parse              | 1.36 ms                                                | 1.32 ms: 1.03x faster                                                  |
| deltablue                  | 3.45 ms                                                | 3.36 ms: 1.03x faster                                                  |
| docutils                   | 2.64 sec                                               | 2.58 sec: 1.02x faster                                                 |
| float                      | 80.8 ms                                                | 79.2 ms: 1.02x faster                                                  |
| sympy_integrate            | 20.5 ms                                                | 20.2 ms: 1.02x faster                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 1.64 ms: 1.02x faster                                                  |
| pprint_safe_repr           | 743 ms                                                 | 729 ms: 1.02x faster                                                   |
| 2to3                       | 264 ms                                                 | 259 ms: 1.02x faster                                                   |
| scimark_fft                | 342 ms                                                 | 338 ms: 1.01x faster                                                   |
| hexiom                     | 6.17 ms                                                | 6.10 ms: 1.01x faster                                                  |
| nqueens                    | 80.1 ms                                                | 79.8 ms: 1.00x faster                                                  |
| pidigits                   | 184 ms                                                 | 185 ms: 1.00x slower                                                   |
| xml_etree_generate         | 85.2 ms                                                | 85.8 ms: 1.01x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 50.5 ms: 1.01x slower                                                  |
| sqlglot_normalize          | 107 ms                                                 | 107 ms: 1.01x slower                                                   |
| unpickle_pure_python       | 221 us                                                 | 222 us: 1.01x slower                                                   |
| asyncio_websockets         | 517 ms                                                 | 523 ms: 1.01x slower                                                   |
| fannkuch                   | 372 ms                                                 | 378 ms: 1.01x slower                                                   |
| sqlglot_optimize           | 53.3 ms                                                | 54.1 ms: 1.02x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.47 ms: 1.02x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 60.1 ms: 1.02x slower                                                  |
| pyflate                    | 448 ms                                                 | 457 ms: 1.02x slower                                                   |
| regex_dna                  | 168 ms                                                 | 171 ms: 1.02x slower                                                   |
| spectral_norm              | 110 ms                                                 | 113 ms: 1.02x slower                                                   |
| logging_silent             | 109 ns                                                 | 112 ns: 1.03x slower                                                   |
| richards_super             | 51.9 ms                                                | 54.0 ms: 1.04x slower                                                  |
| richards                   | 45.9 ms                                                | 47.9 ms: 1.04x slower                                                  |
| django_template            | 34.7 ms                                                | 36.3 ms: 1.05x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 322 us: 1.05x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 7.50 ms: 1.05x slower                                                  |
| mako                       | 11.0 ms                                                | 11.6 ms: 1.06x slower                                                  |
| scimark_sor                | 130 ms                                                 | 137 ms: 1.06x slower                                                   |
| nbody                      | 89.3 ms                                                | 95.5 ms: 1.07x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.02 ms: 1.09x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 11.4 ms: 1.10x slower                                                  |
| coverage                   | 71.4 ms                                                | 78.9 ms: 1.10x slower                                                  |
| telco                      | 6.53 ms                                                | 7.37 ms: 1.13x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 23.7 ms: 1.15x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 4.28 ms: 1.24x slower                                                  |
| python_startup             | 9.93 ms                                                | 14.7 ms: 1.48x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.82 ms: 1.67x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 89.6 ms: 8.30x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (4): sympy_expand, tomli_loads, scimark_lu, sqlite_synth
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241203-3.14.0a2+-bfb0788/bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.059x faster

# HPT report

- Reliability score: 99.98% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.11x