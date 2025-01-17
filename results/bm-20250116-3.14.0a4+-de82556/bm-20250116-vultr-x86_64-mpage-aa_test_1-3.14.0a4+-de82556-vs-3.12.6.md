# Results vs. 3.12.6

- fork: mpage
- ref: aa_test_1
- machine: linux-x86_64
- commit hash: de82556
- commit date: 2025-01-16
- overall geometric mean: 1.092x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-vultr-x86_64-mpage-aa_test_1-3.14.0a4+-de82556 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 253 ms: 1.04x faster                                       |
| docutils       | 2.64 sec                                               | 2.59 sec: 1.02x faster                                     |
| Geometric mean | (ref)                                                  | 1.03x faster                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-vultr-x86_64-mpage-aa_test_1-3.14.0a4+-de82556 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 303 ms: 1.85x faster                                       |
| async_tree_io_tg           | 1.11 sec                                               | 612 ms: 1.81x faster                                       |
| async_tree_io              | 1.08 sec                                               | 610 ms: 1.78x faster                                       |
| async_tree_none_tg         | 446 ms                                                 | 253 ms: 1.76x faster                                       |
| async_tree_none            | 464 ms                                                 | 266 ms: 1.75x faster                                       |
| async_tree_memoization     | 555 ms                                                 | 325 ms: 1.71x faster                                       |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 473 ms: 1.53x faster                                       |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 494 ms: 1.45x faster                                       |
| async_generators           | 384 ms                                                 | 326 ms: 1.18x faster                                       |
| coroutines                 | 23.9 ms                                                | 22.2 ms: 1.08x faster                                      |
| asyncio_websockets         | 517 ms                                                 | 522 ms: 1.01x slower                                       |
| Geometric mean             | (ref)                                                  | 1.50x faster                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-vultr-x86_64-mpage-aa_test_1-3.14.0a4+-de82556 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| float          | 80.8 ms                                                | 72.5 ms: 1.11x faster                                      |
| nbody          | 89.3 ms                                                | 86.3 ms: 1.03x faster                                      |
| pidigits       | 184 ms                                                 | 192 ms: 1.04x slower                                       |
| Geometric mean | (ref)                                                  | 1.03x faster                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-vultr-x86_64-mpage-aa_test_1-3.14.0a4+-de82556 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.73 ms: 1.16x faster                                      |
| regex_compile  | 142 ms                                                 | 127 ms: 1.12x faster                                       |
| regex_dna      | 168 ms                                                 | 171 ms: 1.02x slower                                       |
| regex_v8       | 20.6 ms                                                | 25.0 ms: 1.21x slower                                      |
| Geometric mean | (ref)                                                  | 1.01x faster                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-vultr-x86_64-mpage-aa_test_1-3.14.0a4+-de82556 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.87 sec: 1.13x faster                                     |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.08x faster                                       |
| xml_etree_iterparse  | 96.7 ms                                                | 90.6 ms: 1.07x faster                                      |
| unpickle_pure_python | 221 us                                                 | 213 us: 1.04x faster                                       |
| xml_etree_generate   | 85.2 ms                                                | 83.9 ms: 1.02x faster                                      |
| pickle_pure_python   | 308 us                                                 | 309 us: 1.00x slower                                       |
| xml_etree_process    | 59.0 ms                                                | 59.6 ms: 1.01x slower                                      |
| json_loads           | 26.5 us                                                | 27.8 us: 1.05x slower                                      |
| json_dumps           | 10.4 ms                                                | 11.4 ms: 1.10x slower                                      |
| Geometric mean       | (ref)                                                  | 1.02x faster                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-vultr-x86_64-mpage-aa_test_1-3.14.0a4+-de82556 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.45 ms: 1.04x slower                                      |
| python_startup         | 9.93 ms                                                | 14.7 ms: 1.48x slower                                      |
| Geometric mean         | (ref)                                                  | 1.24x slower                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-vultr-x86_64-mpage-aa_test_1-3.14.0a4+-de82556 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 21.0 ms: 1.09x faster                                      |
| genshi_xml      | 50.2 ms                                                | 48.1 ms: 1.04x faster                                      |
| django_template | 34.7 ms                                                | 36.1 ms: 1.04x slower                                      |
| mako            | 11.0 ms                                                | 11.6 ms: 1.05x slower                                      |
| Geometric mean  | (ref)                                                  | 1.01x faster                                               |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-vultr-x86_64-mpage-aa_test_1-3.14.0a4+-de82556 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 303 ms: 1.85x faster                                       |
| async_tree_io_tg           | 1.11 sec                                               | 612 ms: 1.81x faster                                       |
| async_tree_io              | 1.08 sec                                               | 610 ms: 1.78x faster                                       |
| async_tree_none_tg         | 446 ms                                                 | 253 ms: 1.76x faster                                       |
| async_tree_none            | 464 ms                                                 | 266 ms: 1.75x faster                                       |
| async_tree_memoization     | 555 ms                                                 | 325 ms: 1.71x faster                                       |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 473 ms: 1.53x faster                                       |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 494 ms: 1.45x faster                                       |
| deepcopy                   | 352 us                                                 | 257 us: 1.37x faster                                       |
| deepcopy_memo              | 40.3 us                                                | 30.0 us: 1.34x faster                                      |
| spectral_norm              | 110 ms                                                 | 90.8 ms: 1.21x faster                                      |
| pathlib                    | 21.5 ms                                                | 18.0 ms: 1.20x faster                                      |
| go                         | 139 ms                                                 | 117 ms: 1.19x faster                                       |
| deepcopy_reduce            | 3.08 us                                                | 2.59 us: 1.19x faster                                      |
| async_generators           | 384 ms                                                 | 326 ms: 1.18x faster                                       |
| comprehensions             | 19.8 us                                                | 16.9 us: 1.17x faster                                      |
| regex_effbot               | 3.17 ms                                                | 2.73 ms: 1.16x faster                                      |
| chaos                      | 62.8 ms                                                | 54.7 ms: 1.15x faster                                      |
| crypto_pyaes               | 76.6 ms                                                | 66.9 ms: 1.15x faster                                      |
| generators                 | 32.2 ms                                                | 28.2 ms: 1.14x faster                                      |
| pylint                     | 319 ms                                                 | 280 ms: 1.14x faster                                       |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.3 ms: 1.13x faster                                      |
| raytrace                   | 299 ms                                                 | 265 ms: 1.13x faster                                       |
| tomli_loads                | 2.11 sec                                               | 1.87 sec: 1.13x faster                                     |
| bpe_tokeniser              | 4.74 sec                                               | 4.21 sec: 1.12x faster                                     |
| regex_compile              | 142 ms                                                 | 127 ms: 1.12x faster                                       |
| float                      | 80.8 ms                                                | 72.5 ms: 1.11x faster                                      |
| scimark_sor                | 130 ms                                                 | 116 ms: 1.11x faster                                       |
| sqlalchemy_declarative     | 143 ms                                                 | 128 ms: 1.11x faster                                       |
| scimark_fft                | 342 ms                                                 | 310 ms: 1.10x faster                                       |
| pyflate                    | 448 ms                                                 | 411 ms: 1.09x faster                                       |
| genshi_text                | 22.8 ms                                                | 21.0 ms: 1.09x faster                                      |
| sympy_sum                  | 166 ms                                                 | 153 ms: 1.09x faster                                       |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                       |
| richards                   | 45.9 ms                                                | 42.4 ms: 1.08x faster                                      |
| coroutines                 | 23.9 ms                                                | 22.2 ms: 1.08x faster                                      |
| deltablue                  | 3.45 ms                                                | 3.20 ms: 1.08x faster                                      |
| sympy_str                  | 292 ms                                                 | 271 ms: 1.08x faster                                       |
| thrift                     | 791 us                                                 | 736 us: 1.08x faster                                       |
| pprint_pformat             | 1.52 sec                                               | 1.41 sec: 1.07x faster                                     |
| logging_simple             | 6.63 us                                                | 6.18 us: 1.07x faster                                      |
| pprint_safe_repr           | 743 ms                                                 | 693 ms: 1.07x faster                                       |
| richards_super             | 51.9 ms                                                | 48.4 ms: 1.07x faster                                      |
| sqlglot_parse              | 1.36 ms                                                | 1.26 ms: 1.07x faster                                      |
| scimark_monte_carlo        | 68.4 ms                                                | 63.9 ms: 1.07x faster                                      |
| sqlglot_transpile          | 1.67 ms                                                | 1.56 ms: 1.07x faster                                      |
| xml_etree_iterparse        | 96.7 ms                                                | 90.6 ms: 1.07x faster                                      |
| hexiom                     | 6.17 ms                                                | 5.81 ms: 1.06x faster                                      |
| typing_runtime_protocols   | 163 us                                                 | 155 us: 1.05x faster                                       |
| logging_format             | 7.35 us                                                | 6.99 us: 1.05x faster                                      |
| meteor_contest             | 104 ms                                                 | 98.6 ms: 1.05x faster                                      |
| mdp                        | 2.42 sec                                               | 2.32 sec: 1.04x faster                                     |
| genshi_xml                 | 50.2 ms                                                | 48.1 ms: 1.04x faster                                      |
| pycparser                  | 1.17 sec                                               | 1.12 sec: 1.04x faster                                     |
| sympy_integrate            | 20.5 ms                                                | 19.8 ms: 1.04x faster                                      |
| dulwich_log                | 78.9 ms                                                | 75.8 ms: 1.04x faster                                      |
| 2to3                       | 264 ms                                                 | 253 ms: 1.04x faster                                       |
| unpickle_pure_python       | 221 us                                                 | 213 us: 1.04x faster                                       |
| nbody                      | 89.3 ms                                                | 86.3 ms: 1.03x faster                                      |
| logging_silent             | 109 ns                                                 | 106 ns: 1.03x faster                                       |
| scimark_lu                 | 114 ms                                                 | 111 ms: 1.03x faster                                       |
| nqueens                    | 80.1 ms                                                | 78.0 ms: 1.03x faster                                      |
| docutils                   | 2.64 sec                                               | 2.59 sec: 1.02x faster                                     |
| sympy_expand               | 468 ms                                                 | 458 ms: 1.02x faster                                       |
| fannkuch                   | 372 ms                                                 | 366 ms: 1.02x faster                                       |
| xml_etree_generate         | 85.2 ms                                                | 83.9 ms: 1.02x faster                                      |
| sqlglot_optimize           | 53.3 ms                                                | 52.6 ms: 1.01x faster                                      |
| sqlglot_normalize          | 107 ms                                                 | 105 ms: 1.01x faster                                       |
| json                       | 5.02 ms                                                | 4.96 ms: 1.01x faster                                      |
| pickle_pure_python         | 308 us                                                 | 309 us: 1.00x slower                                       |
| asyncio_websockets         | 517 ms                                                 | 522 ms: 1.01x slower                                       |
| xml_etree_process          | 59.0 ms                                                | 59.6 ms: 1.01x slower                                      |
| sqlite_synth               | 2.20 us                                                | 2.23 us: 1.01x slower                                      |
| regex_dna                  | 168 ms                                                 | 171 ms: 1.02x slower                                       |
| python_startup_no_site     | 7.16 ms                                                | 7.45 ms: 1.04x slower                                      |
| django_template            | 34.7 ms                                                | 36.1 ms: 1.04x slower                                      |
| pidigits                   | 184 ms                                                 | 192 ms: 1.04x slower                                       |
| json_loads                 | 26.5 us                                                | 27.8 us: 1.05x slower                                      |
| mako                       | 11.0 ms                                                | 11.6 ms: 1.05x slower                                      |
| bench_thread_pool          | 941 us                                                 | 1.04 ms: 1.10x slower                                      |
| json_dumps                 | 10.4 ms                                                | 11.4 ms: 1.10x slower                                      |
| telco                      | 6.53 ms                                                | 7.25 ms: 1.11x slower                                      |
| coverage                   | 71.4 ms                                                | 81.0 ms: 1.13x slower                                      |
| regex_v8                   | 20.6 ms                                                | 25.0 ms: 1.21x slower                                      |
| gc_traversal               | 3.46 ms                                                | 4.37 ms: 1.26x slower                                      |
| python_startup             | 9.93 ms                                                | 14.7 ms: 1.48x slower                                      |
| create_gc_cycles           | 1.09 ms                                                | 1.84 ms: 1.68x slower                                      |
| bench_mp_pool              | 10.8 ms                                                | 88.8 ms: 8.23x slower                                      |
| Geometric mean             | (ref)                                                  | 1.06x faster                                               |

Benchmark hidden because not significant (1): scimark_sparse_mat_mult
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250116-3.14.0a4+-de82556/bm-20250116-vultr-x86_64-mpage-aa_test_1-3.14.0a4+-de82556.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.092x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.11x