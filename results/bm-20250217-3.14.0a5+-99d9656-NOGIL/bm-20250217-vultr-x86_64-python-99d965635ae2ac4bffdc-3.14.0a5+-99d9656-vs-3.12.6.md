# Results vs. 3.12.6

- fork: python
- ref: 99d965635ae2ac4bffdc
- machine: linux-x86_64
- commit hash: 99d9656
- commit date: 2025-02-17
- overall geometric mean: 1.048x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250217-vultr-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 302 ms: 1.15x slower                                                   |
| docutils       | 2.64 sec                                               | 2.80 sec: 1.06x slower                                                 |
| html5lib       | 63.6 ms                                                | 72.1 ms: 1.13x slower                                                  |
| Geometric mean | (ref)                                                  | 1.11x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250217-vultr-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 582 ms: 1.91x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 609 ms: 1.78x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 251 ms: 1.78x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 321 ms: 1.75x faster                                                   |
| async_tree_none            | 464 ms                                                 | 288 ms: 1.62x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 352 ms: 1.58x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 505 ms: 1.43x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 537 ms: 1.33x faster                                                   |
| async_generators           | 384 ms                                                 | 375 ms: 1.03x faster                                                   |
| coroutines                 | 23.9 ms                                                | 23.6 ms: 1.01x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 515 ms: 1.00x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.44x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250217-vultr-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 75.5 ms: 1.07x faster                                                  |
| pidigits       | 184 ms                                                 | 208 ms: 1.13x slower                                                   |
| nbody          | 89.3 ms                                                | 129 ms: 1.44x slower                                                   |
| Geometric mean | (ref)                                                  | 1.15x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250217-vultr-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.78 ms: 1.14x faster                                                  |
| regex_dna      | 168 ms                                                 | 181 ms: 1.08x slower                                                   |
| regex_compile  | 142 ms                                                 | 154 ms: 1.08x slower                                                   |
| regex_v8       | 20.6 ms                                                | 23.7 ms: 1.15x slower                                                  |
| Geometric mean | (ref)                                                  | 1.04x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250217-vultr-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.2 ms: 1.10x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.08x faster                                                   |
| tomli_loads          | 2.11 sec                                               | 2.36 sec: 1.12x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 96.0 ms: 1.13x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 252 us: 1.14x slower                                                   |
| pickle_pure_python   | 308 us                                                 | 361 us: 1.17x slower                                                   |
| json_loads           | 26.5 us                                                | 31.2 us: 1.18x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 70.2 ms: 1.19x slower                                                  |
| json_dumps           | 10.4 ms                                                | 12.8 ms: 1.24x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.11x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250217-vultr-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.60 ms: 1.34x slower                                                  |
| python_startup         | 9.93 ms                                                | 15.3 ms: 1.54x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.44x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250217-vultr-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 59.2 ms: 1.18x slower                                                  |
| django_template | 34.7 ms                                                | 42.0 ms: 1.21x slower                                                  |
| genshi_text     | 22.8 ms                                                | 27.7 ms: 1.21x slower                                                  |
| mako            | 11.0 ms                                                | 15.8 ms: 1.43x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.26x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250217-vultr-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal               | 3.46 ms                                                | 1.73 ms: 1.99x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 582 ms: 1.91x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 609 ms: 1.78x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 251 ms: 1.78x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 321 ms: 1.75x faster                                                   |
| async_tree_none            | 464 ms                                                 | 288 ms: 1.62x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 352 ms: 1.58x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 505 ms: 1.43x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 537 ms: 1.33x faster                                                   |
| deepcopy                   | 352 us                                                 | 307 us: 1.15x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.78 ms: 1.14x faster                                                  |
| pathlib                    | 21.5 ms                                                | 19.5 ms: 1.10x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 88.2 ms: 1.10x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                                   |
| sqlite_synth               | 2.20 us                                                | 2.03 us: 1.08x faster                                                  |
| float                      | 80.8 ms                                                | 75.5 ms: 1.07x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 38.3 us: 1.05x faster                                                  |
| async_generators           | 384 ms                                                 | 375 ms: 1.03x faster                                                   |
| coroutines                 | 23.9 ms                                                | 23.6 ms: 1.01x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.69 sec: 1.01x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 515 ms: 1.00x faster                                                   |
| comprehensions             | 19.8 us                                                | 19.9 us: 1.00x slower                                                  |
| generators                 | 32.2 ms                                                | 32.5 ms: 1.01x slower                                                  |
| go                         | 139 ms                                                 | 141 ms: 1.01x slower                                                   |
| deepcopy_reduce            | 3.08 us                                                | 3.12 us: 1.01x slower                                                  |
| spectral_norm              | 110 ms                                                 | 112 ms: 1.01x slower                                                   |
| pycparser                  | 1.17 sec                                               | 1.19 sec: 1.02x slower                                                 |
| scimark_sor                | 130 ms                                                 | 134 ms: 1.03x slower                                                   |
| dulwich_log                | 78.9 ms                                                | 82.4 ms: 1.05x slower                                                  |
| logging_silent             | 109 ns                                                 | 115 ns: 1.05x slower                                                   |
| docutils                   | 2.64 sec                                               | 2.80 sec: 1.06x slower                                                 |
| json                       | 5.02 ms                                                | 5.38 ms: 1.07x slower                                                  |
| mdp                        | 2.42 sec                                               | 2.60 sec: 1.07x slower                                                 |
| regex_dna                  | 168 ms                                                 | 181 ms: 1.08x slower                                                   |
| regex_compile              | 142 ms                                                 | 154 ms: 1.08x slower                                                   |
| logging_simple             | 6.63 us                                                | 7.18 us: 1.08x slower                                                  |
| raytrace                   | 299 ms                                                 | 326 ms: 1.09x slower                                                   |
| sqlalchemy_declarative     | 143 ms                                                 | 156 ms: 1.09x slower                                                   |
| sqlalchemy_imperative      | 21.8 ms                                                | 23.8 ms: 1.09x slower                                                  |
| pprint_safe_repr           | 743 ms                                                 | 814 ms: 1.10x slower                                                   |
| pyflate                    | 448 ms                                                 | 496 ms: 1.11x slower                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.69 sec: 1.11x slower                                                 |
| logging_format             | 7.35 us                                                | 8.18 us: 1.11x slower                                                  |
| tomli_loads                | 2.11 sec                                               | 2.36 sec: 1.12x slower                                                 |
| sympy_sum                  | 166 ms                                                 | 186 ms: 1.12x slower                                                   |
| chaos                      | 62.8 ms                                                | 70.3 ms: 1.12x slower                                                  |
| sqlglot_normalize          | 107 ms                                                 | 120 ms: 1.12x slower                                                   |
| xml_etree_generate         | 85.2 ms                                                | 96.0 ms: 1.13x slower                                                  |
| pidigits                   | 184 ms                                                 | 208 ms: 1.13x slower                                                   |
| html5lib                   | 63.6 ms                                                | 72.1 ms: 1.13x slower                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 1.90 ms: 1.14x slower                                                  |
| deltablue                  | 3.45 ms                                                | 3.92 ms: 1.14x slower                                                  |
| unpickle_pure_python       | 221 us                                                 | 252 us: 1.14x slower                                                   |
| thrift                     | 791 us                                                 | 906 us: 1.15x slower                                                   |
| 2to3                       | 264 ms                                                 | 302 ms: 1.15x slower                                                   |
| sympy_str                  | 292 ms                                                 | 335 ms: 1.15x slower                                                   |
| regex_v8                   | 20.6 ms                                                | 23.7 ms: 1.15x slower                                                  |
| sqlglot_optimize           | 53.3 ms                                                | 61.5 ms: 1.15x slower                                                  |
| crypto_pyaes               | 76.6 ms                                                | 88.4 ms: 1.15x slower                                                  |
| sqlglot_parse              | 1.36 ms                                                | 1.58 ms: 1.16x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 24.0 ms: 1.17x slower                                                  |
| sympy_expand               | 468 ms                                                 | 547 ms: 1.17x slower                                                   |
| pickle_pure_python         | 308 us                                                 | 361 us: 1.17x slower                                                   |
| json_loads                 | 26.5 us                                                | 31.2 us: 1.18x slower                                                  |
| scimark_fft                | 342 ms                                                 | 403 ms: 1.18x slower                                                   |
| genshi_xml                 | 50.2 ms                                                | 59.2 ms: 1.18x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 70.2 ms: 1.19x slower                                                  |
| hexiom                     | 6.17 ms                                                | 7.39 ms: 1.20x slower                                                  |
| richards                   | 45.9 ms                                                | 55.3 ms: 1.20x slower                                                  |
| django_template            | 34.7 ms                                                | 42.0 ms: 1.21x slower                                                  |
| genshi_text                | 22.8 ms                                                | 27.7 ms: 1.21x slower                                                  |
| typing_runtime_protocols   | 163 us                                                 | 198 us: 1.21x slower                                                   |
| nqueens                    | 80.1 ms                                                | 97.4 ms: 1.22x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 83.3 ms: 1.22x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 12.8 ms: 1.24x slower                                                  |
| richards_super             | 51.9 ms                                                | 64.3 ms: 1.24x slower                                                  |
| meteor_contest             | 104 ms                                                 | 129 ms: 1.25x slower                                                   |
| scimark_lu                 | 114 ms                                                 | 143 ms: 1.25x slower                                                   |
| create_gc_cycles           | 1.09 ms                                                | 1.38 ms: 1.26x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.76 ms: 1.31x slower                                                  |
| telco                      | 6.53 ms                                                | 8.63 ms: 1.32x slower                                                  |
| fannkuch                   | 372 ms                                                 | 494 ms: 1.33x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 9.60 ms: 1.34x slower                                                  |
| coverage                   | 71.4 ms                                                | 98.1 ms: 1.37x slower                                                  |
| mako                       | 11.0 ms                                                | 15.8 ms: 1.43x slower                                                  |
| nbody                      | 89.3 ms                                                | 129 ms: 1.44x slower                                                   |
| python_startup             | 9.93 ms                                                | 15.3 ms: 1.54x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 3.31 ms: 3.52x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 95.0 ms: 8.80x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.09x slower                                                           |

Benchmark hidden because not significant (1): pylint
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250217-3.14.0a5+-99d9656-NOGIL/bm-20250217-vultr-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.048x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.36x