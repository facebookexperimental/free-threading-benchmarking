# Results vs. 3.12.6

- fork: python
- ref: 1a8e5742cdcf3dba7fc5
- machine: linux-x86_64
- commit hash: 1a8e574
- commit date: 2025-03-13
- overall geometric mean: 1.060x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 258 ms: 1.02x faster                                                   |
| docutils       | 2.64 sec                                               | 2.61 sec: 1.01x faster                                                 |
| Geometric mean | (ref)                                                  | 1.02x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 628 ms: 1.77x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 318 ms: 1.76x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 630 ms: 1.72x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 329 ms: 1.69x faster                                                   |
| async_tree_none            | 464 ms                                                 | 277 ms: 1.68x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 267 ms: 1.67x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 504 ms: 1.43x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 517 ms: 1.38x faster                                                   |
| async_generators           | 384 ms                                                 | 339 ms: 1.13x faster                                                   |
| coroutines                 | 23.9 ms                                                | 23.4 ms: 1.02x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.45x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 75.8 ms: 1.07x faster                                                  |
| pidigits       | 184 ms                                                 | 187 ms: 1.02x slower                                                   |
| nbody          | 89.3 ms                                                | 102 ms: 1.14x slower                                                   |
| Geometric mean | (ref)                                                  | 1.03x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.77 ms: 1.14x faster                                                  |
| regex_compile  | 142 ms                                                 | 130 ms: 1.10x faster                                                   |
| regex_dna      | 168 ms                                                 | 179 ms: 1.07x slower                                                   |
| regex_v8       | 20.6 ms                                                | 24.5 ms: 1.19x slower                                                  |
| Geometric mean | (ref)                                                  | 1.00x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                                   |
| tomli_loads          | 2.11 sec                                               | 2.00 sec: 1.05x faster                                                 |
| xml_etree_iterparse  | 96.7 ms                                                | 93.4 ms: 1.04x faster                                                  |
| xml_etree_generate   | 85.2 ms                                                | 86.5 ms: 1.01x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 224 us: 1.02x slower                                                   |
| json_loads           | 26.5 us                                                | 27.0 us: 1.02x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 60.1 ms: 1.02x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 324 us: 1.05x slower                                                   |
| json_dumps           | 10.4 ms                                                | 11.2 ms: 1.09x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.01x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 8.63 ms: 1.21x slower                                                  |
| python_startup         | 9.93 ms                                                | 14.9 ms: 1.50x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.35x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 21.9 ms: 1.04x faster                                                  |
| genshi_xml      | 50.2 ms                                                | 51.0 ms: 1.02x slower                                                  |
| django_template | 34.7 ms                                                | 37.2 ms: 1.07x slower                                                  |
| mako            | 11.0 ms                                                | 12.1 ms: 1.10x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.04x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 628 ms: 1.77x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 318 ms: 1.76x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 630 ms: 1.72x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 329 ms: 1.69x faster                                                   |
| async_tree_none            | 464 ms                                                 | 277 ms: 1.68x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 267 ms: 1.67x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 504 ms: 1.43x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 517 ms: 1.38x faster                                                   |
| deepcopy                   | 352 us                                                 | 261 us: 1.35x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 30.8 us: 1.31x faster                                                  |
| go                         | 139 ms                                                 | 113 ms: 1.23x faster                                                   |
| dulwich_log                | 78.9 ms                                                | 67.5 ms: 1.17x faster                                                  |
| comprehensions             | 19.8 us                                                | 17.2 us: 1.15x faster                                                  |
| spectral_norm              | 110 ms                                                 | 95.9 ms: 1.15x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.77 ms: 1.14x faster                                                  |
| async_generators           | 384 ms                                                 | 339 ms: 1.13x faster                                                   |
| deepcopy_reduce            | 3.08 us                                                | 2.73 us: 1.13x faster                                                  |
| raytrace                   | 299 ms                                                 | 267 ms: 1.12x faster                                                   |
| scimark_sor                | 130 ms                                                 | 116 ms: 1.12x faster                                                   |
| pylint                     | 319 ms                                                 | 285 ms: 1.12x faster                                                   |
| deltablue                  | 3.45 ms                                                | 3.12 ms: 1.11x faster                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.8 ms: 1.10x faster                                                  |
| pathlib                    | 21.5 ms                                                | 19.6 ms: 1.10x faster                                                  |
| regex_compile              | 142 ms                                                 | 130 ms: 1.10x faster                                                   |
| logging_simple             | 6.63 us                                                | 6.05 us: 1.10x faster                                                  |
| logging_silent             | 109 ns                                                 | 99.6 ns: 1.09x faster                                                  |
| logging_format             | 7.35 us                                                | 6.73 us: 1.09x faster                                                  |
| sqlalchemy_declarative     | 143 ms                                                 | 131 ms: 1.09x faster                                                   |
| generators                 | 32.2 ms                                                | 29.7 ms: 1.09x faster                                                  |
| richards                   | 45.9 ms                                                | 42.7 ms: 1.08x faster                                                  |
| chaos                      | 62.8 ms                                                | 58.5 ms: 1.07x faster                                                  |
| crypto_pyaes               | 76.6 ms                                                | 71.5 ms: 1.07x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.43 sec: 1.07x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                                   |
| float                      | 80.8 ms                                                | 75.8 ms: 1.07x faster                                                  |
| sympy_sum                  | 166 ms                                                 | 156 ms: 1.07x faster                                                   |
| pyflate                    | 448 ms                                                 | 425 ms: 1.05x faster                                                   |
| tomli_loads                | 2.11 sec                                               | 2.00 sec: 1.05x faster                                                 |
| thrift                     | 791 us                                                 | 754 us: 1.05x faster                                                   |
| sympy_str                  | 292 ms                                                 | 278 ms: 1.05x faster                                                   |
| genshi_text                | 22.8 ms                                                | 21.9 ms: 1.04x faster                                                  |
| richards_super             | 51.9 ms                                                | 49.8 ms: 1.04x faster                                                  |
| typing_runtime_protocols   | 163 us                                                 | 158 us: 1.04x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 93.4 ms: 1.04x faster                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 1.62 ms: 1.03x faster                                                  |
| sqlglot_parse              | 1.36 ms                                                | 1.32 ms: 1.03x faster                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 66.6 ms: 1.03x faster                                                  |
| json                       | 5.02 ms                                                | 4.89 ms: 1.03x faster                                                  |
| sympy_integrate            | 20.5 ms                                                | 20.1 ms: 1.02x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.4 ms: 1.02x faster                                                  |
| scimark_fft                | 342 ms                                                 | 334 ms: 1.02x faster                                                   |
| meteor_contest             | 104 ms                                                 | 101 ms: 1.02x faster                                                   |
| 2to3                       | 264 ms                                                 | 258 ms: 1.02x faster                                                   |
| sqlglot_normalize          | 107 ms                                                 | 104 ms: 1.02x faster                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.50 sec: 1.01x faster                                                 |
| docutils                   | 2.64 sec                                               | 2.61 sec: 1.01x faster                                                 |
| hexiom                     | 6.17 ms                                                | 6.10 ms: 1.01x faster                                                  |
| sqlglot_optimize           | 53.3 ms                                                | 52.7 ms: 1.01x faster                                                  |
| pprint_safe_repr           | 743 ms                                                 | 737 ms: 1.01x faster                                                   |
| pycparser                  | 1.17 sec                                               | 1.16 sec: 1.01x faster                                                 |
| xml_etree_generate         | 85.2 ms                                                | 86.5 ms: 1.01x slower                                                  |
| pidigits                   | 184 ms                                                 | 187 ms: 1.02x slower                                                   |
| unpickle_pure_python       | 221 us                                                 | 224 us: 1.02x slower                                                   |
| nqueens                    | 80.1 ms                                                | 81.4 ms: 1.02x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 51.0 ms: 1.02x slower                                                  |
| json_loads                 | 26.5 us                                                | 27.0 us: 1.02x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 60.1 ms: 1.02x slower                                                  |
| mdp                        | 2.42 sec                                               | 2.50 sec: 1.03x slower                                                 |
| pickle_pure_python         | 308 us                                                 | 324 us: 1.05x slower                                                   |
| regex_dna                  | 168 ms                                                 | 179 ms: 1.07x slower                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.70 ms: 1.07x slower                                                  |
| django_template            | 34.7 ms                                                | 37.2 ms: 1.07x slower                                                  |
| fannkuch                   | 372 ms                                                 | 401 ms: 1.08x slower                                                   |
| json_dumps                 | 10.4 ms                                                | 11.2 ms: 1.09x slower                                                  |
| mako                       | 11.0 ms                                                | 12.1 ms: 1.10x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.05 ms: 1.12x slower                                                  |
| coverage                   | 71.4 ms                                                | 81.1 ms: 1.14x slower                                                  |
| nbody                      | 89.3 ms                                                | 102 ms: 1.14x slower                                                   |
| telco                      | 6.53 ms                                                | 7.64 ms: 1.17x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 24.5 ms: 1.19x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 8.63 ms: 1.21x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 4.76 ms: 1.38x slower                                                  |
| python_startup             | 9.93 ms                                                | 14.9 ms: 1.50x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.83 ms: 1.67x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 88.2 ms: 8.16x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (4): sympy_expand, asyncio_websockets, scimark_lu, sqlite_synth
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250313-3.14.0a5+-1a8e574/bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.060x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.12x