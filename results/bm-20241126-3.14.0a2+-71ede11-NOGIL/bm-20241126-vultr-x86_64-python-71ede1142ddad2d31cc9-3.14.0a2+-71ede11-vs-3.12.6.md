# Results vs. 3.12.6

- fork: python
- ref: 71ede1142ddad2d31cc9
- machine: linux-x86_64
- commit hash: 71ede11
- commit date: 2024-11-26
- overall geometric mean: 1.262x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.21x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241126-vultr-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 380 ms: 1.44x slower                                                   |
| docutils       | 2.64 sec                                               | 3.19 sec: 1.21x slower                                                 |
| html5lib       | 63.6 ms                                                | 100 ms: 1.58x slower                                                   |
| Geometric mean | (ref)                                                  | 1.40x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241126-vultr-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 877 ms: 1.27x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 372 ms: 1.20x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 905 ms: 1.20x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 469 ms: 1.19x faster                                                   |
| async_tree_none            | 464 ms                                                 | 406 ms: 1.14x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 633 ms: 1.14x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 496 ms: 1.12x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 660 ms: 1.08x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 520 ms: 1.01x slower                                                   |
| coroutines                 | 23.9 ms                                                | 28.0 ms: 1.17x slower                                                  |
| async_generators           | 384 ms                                                 | 468 ms: 1.22x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.08x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241126-vultr-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 89.3 ms                                                | 141 ms: 1.58x slower                                                   |
| float          | 80.8 ms                                                | 144 ms: 1.78x slower                                                   |
| Geometric mean | (ref)                                                  | 1.41x slower                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241126-vultr-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.84 ms: 1.12x faster                                                  |
| regex_dna      | 168 ms                                                 | 184 ms: 1.10x slower                                                   |
| regex_v8       | 20.6 ms                                                | 24.6 ms: 1.20x slower                                                  |
| regex_compile  | 142 ms                                                 | 195 ms: 1.37x slower                                                   |
| Geometric mean | (ref)                                                  | 1.13x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241126-vultr-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                   |
| xml_etree_iterparse  | 96.7 ms                                                | 95.0 ms: 1.02x faster                                                  |
| json_loads           | 26.5 us                                                | 28.2 us: 1.06x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 102 ms: 1.20x slower                                                   |
| tomli_loads          | 2.11 sec                                               | 2.92 sec: 1.39x slower                                                 |
| json_dumps           | 10.4 ms                                                | 14.5 ms: 1.40x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 82.8 ms: 1.40x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 376 us: 1.71x slower                                                   |
| pickle_pure_python   | 308 us                                                 | 554 us: 1.80x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.29x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241126-vultr-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.3 ms: 1.43x slower                                                  |
| python_startup         | 9.93 ms                                                | 17.5 ms: 1.76x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.59x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241126-vultr-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 68.1 ms: 1.36x slower                                                  |
| genshi_text     | 22.8 ms                                                | 34.4 ms: 1.51x slower                                                  |
| django_template | 34.7 ms                                                | 55.7 ms: 1.61x slower                                                  |
| mako            | 11.0 ms                                                | 19.6 ms: 1.78x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.56x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241126-vultr-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 877 ms: 1.27x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 372 ms: 1.20x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 905 ms: 1.20x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 469 ms: 1.19x faster                                                   |
| async_tree_none            | 464 ms                                                 | 406 ms: 1.14x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 633 ms: 1.14x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 496 ms: 1.12x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.84 ms: 1.12x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 660 ms: 1.08x faster                                                   |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                   |
| gc_traversal               | 3.46 ms                                                | 3.30 ms: 1.05x faster                                                  |
| pathlib                    | 21.5 ms                                                | 20.7 ms: 1.04x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 95.0 ms: 1.02x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 520 ms: 1.01x slower                                                   |
| deepcopy                   | 352 us                                                 | 358 us: 1.02x slower                                                   |
| json                       | 5.02 ms                                                | 5.15 ms: 1.03x slower                                                  |
| sqlite_synth               | 2.20 us                                                | 2.31 us: 1.05x slower                                                  |
| json_loads                 | 26.5 us                                                | 28.2 us: 1.06x slower                                                  |
| regex_dna                  | 168 ms                                                 | 184 ms: 1.10x slower                                                   |
| deepcopy_memo              | 40.3 us                                                | 45.4 us: 1.13x slower                                                  |
| coroutines                 | 23.9 ms                                                | 28.0 ms: 1.17x slower                                                  |
| scimark_fft                | 342 ms                                                 | 402 ms: 1.18x slower                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 5.58 sec: 1.18x slower                                                 |
| mdp                        | 2.42 sec                                               | 2.89 sec: 1.19x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 24.6 ms: 1.20x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 102 ms: 1.20x slower                                                   |
| spectral_norm              | 110 ms                                                 | 133 ms: 1.21x slower                                                   |
| docutils                   | 2.64 sec                                               | 3.19 sec: 1.21x slower                                                 |
| async_generators           | 384 ms                                                 | 468 ms: 1.22x slower                                                   |
| generators                 | 32.2 ms                                                | 39.3 ms: 1.22x slower                                                  |
| deepcopy_reduce            | 3.08 us                                                | 3.80 us: 1.24x slower                                                  |
| pylint                     | 319 ms                                                 | 396 ms: 1.24x slower                                                   |
| dulwich_log                | 78.9 ms                                                | 99.5 ms: 1.26x slower                                                  |
| typing_runtime_protocols   | 163 us                                                 | 211 us: 1.29x slower                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.76 ms: 1.31x slower                                                  |
| meteor_contest             | 104 ms                                                 | 136 ms: 1.32x slower                                                   |
| nqueens                    | 80.1 ms                                                | 108 ms: 1.35x slower                                                   |
| crypto_pyaes               | 76.6 ms                                                | 103 ms: 1.35x slower                                                   |
| genshi_xml                 | 50.2 ms                                                | 68.1 ms: 1.36x slower                                                  |
| pycparser                  | 1.17 sec                                               | 1.60 sec: 1.37x slower                                                 |
| regex_compile              | 142 ms                                                 | 195 ms: 1.37x slower                                                   |
| telco                      | 6.53 ms                                                | 9.00 ms: 1.38x slower                                                  |
| tomli_loads                | 2.11 sec                                               | 2.92 sec: 1.39x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 14.5 ms: 1.40x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 82.8 ms: 1.40x slower                                                  |
| sqlglot_optimize           | 53.3 ms                                                | 75.5 ms: 1.42x slower                                                  |
| sqlglot_normalize          | 107 ms                                                 | 151 ms: 1.42x slower                                                   |
| coverage                   | 71.4 ms                                                | 102 ms: 1.43x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 10.3 ms: 1.43x slower                                                  |
| pprint_safe_repr           | 743 ms                                                 | 1.07 sec: 1.44x slower                                                 |
| 2to3                       | 264 ms                                                 | 380 ms: 1.44x slower                                                   |
| fannkuch                   | 372 ms                                                 | 545 ms: 1.46x slower                                                   |
| pprint_pformat             | 1.52 sec                                               | 2.23 sec: 1.47x slower                                                 |
| comprehensions             | 19.8 us                                                | 29.1 us: 1.47x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 31.0 ms: 1.51x slower                                                  |
| genshi_text                | 22.8 ms                                                | 34.4 ms: 1.51x slower                                                  |
| thrift                     | 791 us                                                 | 1.21 ms: 1.52x slower                                                  |
| html5lib                   | 63.6 ms                                                | 100 ms: 1.58x slower                                                   |
| nbody                      | 89.3 ms                                                | 141 ms: 1.58x slower                                                   |
| django_template            | 34.7 ms                                                | 55.7 ms: 1.61x slower                                                  |
| pyflate                    | 448 ms                                                 | 737 ms: 1.65x slower                                                   |
| create_gc_cycles           | 1.09 ms                                                | 1.82 ms: 1.66x slower                                                  |
| unpickle_pure_python       | 221 us                                                 | 376 us: 1.71x slower                                                   |
| sympy_str                  | 292 ms                                                 | 498 ms: 1.71x slower                                                   |
| logging_simple             | 6.63 us                                                | 11.4 us: 1.71x slower                                                  |
| logging_format             | 7.35 us                                                | 12.7 us: 1.73x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 199 ms: 1.75x slower                                                   |
| python_startup             | 9.93 ms                                                | 17.5 ms: 1.76x slower                                                  |
| mako                       | 11.0 ms                                                | 19.6 ms: 1.78x slower                                                  |
| float                      | 80.8 ms                                                | 144 ms: 1.78x slower                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 122 ms: 1.79x slower                                                   |
| pickle_pure_python         | 308 us                                                 | 554 us: 1.80x slower                                                   |
| logging_silent             | 109 ns                                                 | 199 ns: 1.83x slower                                                   |
| chaos                      | 62.8 ms                                                | 116 ms: 1.84x slower                                                   |
| richards                   | 45.9 ms                                                | 84.6 ms: 1.84x slower                                                  |
| hexiom                     | 6.17 ms                                                | 11.4 ms: 1.84x slower                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 3.09 ms: 1.85x slower                                                  |
| scimark_sor                | 130 ms                                                 | 243 ms: 1.88x slower                                                   |
| richards_super             | 51.9 ms                                                | 101 ms: 1.94x slower                                                   |
| sqlglot_parse              | 1.36 ms                                                | 2.68 ms: 1.98x slower                                                  |
| raytrace                   | 299 ms                                                 | 608 ms: 2.03x slower                                                   |
| go                         | 139 ms                                                 | 285 ms: 2.05x slower                                                   |
| sympy_expand               | 468 ms                                                 | 987 ms: 2.11x slower                                                   |
| sympy_sum                  | 166 ms                                                 | 360 ms: 2.17x slower                                                   |
| deltablue                  | 3.45 ms                                                | 8.87 ms: 2.57x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 3.41 ms: 3.62x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 110 ms: 10.17x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.41x slower                                                           |

Benchmark hidden because not significant (1): pidigits
Ignored benchmarks (17) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241126-3.14.0a2+-71ede11-NOGIL/bm-20241126-vultr-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.262x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.26x
- 95% likely to have a slowdown of 1.24x
- 99% likely to have a slowdown of 1.21x

# Memory
- memory change: 1.33x