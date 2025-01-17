# Results vs. 3.12.6

- fork: python
- ref: b44ff6d0df9ec2d60be6
- machine: linux-x86_64
- commit hash: b44ff6d
- commit date: 2025-01-16
- overall geometric mean: 1.047x slower
- HPT reliability: 99.94%
- HPT 99th percentile: 1.02x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 302 ms: 1.15x slower                                                   |
| docutils       | 2.64 sec                                               | 2.79 sec: 1.06x slower                                                 |
| html5lib       | 63.6 ms                                                | 69.4 ms: 1.09x slower                                                  |
| Geometric mean | (ref)                                                  | 1.10x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 576 ms: 1.93x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 239 ms: 1.87x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 308 ms: 1.82x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 601 ms: 1.80x faster                                                   |
| async_tree_none            | 464 ms                                                 | 287 ms: 1.62x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 349 ms: 1.59x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 493 ms: 1.47x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 532 ms: 1.34x faster                                                   |
| async_generators           | 384 ms                                                 | 367 ms: 1.05x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 515 ms: 1.00x faster                                                   |
| coroutines                 | 23.9 ms                                                | 24.2 ms: 1.01x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.46x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 73.4 ms: 1.10x faster                                                  |
| pidigits       | 184 ms                                                 | 190 ms: 1.03x slower                                                   |
| nbody          | 89.3 ms                                                | 134 ms: 1.50x slower                                                   |
| Geometric mean | (ref)                                                  | 1.12x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.79 ms: 1.13x faster                                                  |
| regex_compile  | 142 ms                                                 | 150 ms: 1.05x slower                                                   |
| regex_dna      | 168 ms                                                 | 183 ms: 1.09x slower                                                   |
| regex_v8       | 20.6 ms                                                | 23.1 ms: 1.12x slower                                                  |
| Geometric mean | (ref)                                                  | 1.03x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.7 ms: 1.10x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 127 ms: 1.09x faster                                                   |
| tomli_loads          | 2.11 sec                                               | 2.30 sec: 1.09x slower                                                 |
| unpickle_pure_python | 221 us                                                 | 245 us: 1.11x slower                                                   |
| xml_etree_generate   | 85.2 ms                                                | 96.1 ms: 1.13x slower                                                  |
| json_loads           | 26.5 us                                                | 30.7 us: 1.16x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 68.7 ms: 1.16x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 373 us: 1.21x slower                                                   |
| json_dumps           | 10.4 ms                                                | 12.7 ms: 1.23x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.10x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.54 ms: 1.33x slower                                                  |
| python_startup         | 9.93 ms                                                | 15.2 ms: 1.53x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.43x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 60.2 ms: 1.20x slower                                                  |
| genshi_text     | 22.8 ms                                                | 27.5 ms: 1.21x slower                                                  |
| django_template | 34.7 ms                                                | 43.4 ms: 1.25x slower                                                  |
| mako            | 11.0 ms                                                | 15.6 ms: 1.42x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.27x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 576 ms: 1.93x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 239 ms: 1.87x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 308 ms: 1.82x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 601 ms: 1.80x faster                                                   |
| async_tree_none            | 464 ms                                                 | 287 ms: 1.62x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 349 ms: 1.59x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 493 ms: 1.47x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 532 ms: 1.34x faster                                                   |
| pathlib                    | 21.5 ms                                                | 18.6 ms: 1.16x faster                                                  |
| deepcopy                   | 352 us                                                 | 310 us: 1.14x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.79 ms: 1.13x faster                                                  |
| gc_traversal               | 3.46 ms                                                | 3.13 ms: 1.10x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 87.7 ms: 1.10x faster                                                  |
| float                      | 80.8 ms                                                | 73.4 ms: 1.10x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 127 ms: 1.09x faster                                                   |
| sqlite_synth               | 2.20 us                                                | 2.03 us: 1.09x faster                                                  |
| spectral_norm              | 110 ms                                                 | 103 ms: 1.07x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 37.9 us: 1.06x faster                                                  |
| async_generators           | 384 ms                                                 | 367 ms: 1.05x faster                                                   |
| generators                 | 32.2 ms                                                | 31.3 ms: 1.03x faster                                                  |
| go                         | 139 ms                                                 | 136 ms: 1.02x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 515 ms: 1.00x faster                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 4.72 sec: 1.00x faster                                                 |
| coroutines                 | 23.9 ms                                                | 24.2 ms: 1.01x slower                                                  |
| logging_silent             | 109 ns                                                 | 110 ns: 1.01x slower                                                   |
| pycparser                  | 1.17 sec                                               | 1.19 sec: 1.02x slower                                                 |
| pidigits                   | 184 ms                                                 | 190 ms: 1.03x slower                                                   |
| dulwich_log                | 78.9 ms                                                | 81.9 ms: 1.04x slower                                                  |
| regex_compile              | 142 ms                                                 | 150 ms: 1.05x slower                                                   |
| deepcopy_reduce            | 3.08 us                                                | 3.24 us: 1.05x slower                                                  |
| comprehensions             | 19.8 us                                                | 20.9 us: 1.05x slower                                                  |
| docutils                   | 2.64 sec                                               | 2.79 sec: 1.06x slower                                                 |
| json                       | 5.02 ms                                                | 5.34 ms: 1.06x slower                                                  |
| chaos                      | 62.8 ms                                                | 67.7 ms: 1.08x slower                                                  |
| logging_simple             | 6.63 us                                                | 7.15 us: 1.08x slower                                                  |
| raytrace                   | 299 ms                                                 | 323 ms: 1.08x slower                                                   |
| scimark_fft                | 342 ms                                                 | 372 ms: 1.09x slower                                                   |
| html5lib                   | 63.6 ms                                                | 69.4 ms: 1.09x slower                                                  |
| regex_dna                  | 168 ms                                                 | 183 ms: 1.09x slower                                                   |
| tomli_loads                | 2.11 sec                                               | 2.30 sec: 1.09x slower                                                 |
| pyflate                    | 448 ms                                                 | 491 ms: 1.10x slower                                                   |
| pprint_safe_repr           | 743 ms                                                 | 816 ms: 1.10x slower                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.68 sec: 1.11x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 245 us: 1.11x slower                                                   |
| mdp                        | 2.42 sec                                               | 2.69 sec: 1.11x slower                                                 |
| logging_format             | 7.35 us                                                | 8.18 us: 1.11x slower                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.4 ms: 1.12x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 23.1 ms: 1.12x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 186 ms: 1.12x slower                                                   |
| xml_etree_generate         | 85.2 ms                                                | 96.1 ms: 1.13x slower                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 1.89 ms: 1.13x slower                                                  |
| sqlglot_normalize          | 107 ms                                                 | 121 ms: 1.13x slower                                                   |
| crypto_pyaes               | 76.6 ms                                                | 87.2 ms: 1.14x slower                                                  |
| sympy_str                  | 292 ms                                                 | 332 ms: 1.14x slower                                                   |
| sqlalchemy_declarative     | 143 ms                                                 | 163 ms: 1.14x slower                                                   |
| thrift                     | 791 us                                                 | 908 us: 1.15x slower                                                   |
| 2to3                       | 264 ms                                                 | 302 ms: 1.15x slower                                                   |
| sqlglot_optimize           | 53.3 ms                                                | 61.5 ms: 1.15x slower                                                  |
| json_loads                 | 26.5 us                                                | 30.7 us: 1.16x slower                                                  |
| sqlglot_parse              | 1.36 ms                                                | 1.57 ms: 1.16x slower                                                  |
| sympy_expand               | 468 ms                                                 | 543 ms: 1.16x slower                                                   |
| xml_etree_process          | 59.0 ms                                                | 68.7 ms: 1.16x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 134 ms: 1.17x slower                                                   |
| sympy_integrate            | 20.5 ms                                                | 24.2 ms: 1.18x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 80.6 ms: 1.18x slower                                                  |
| hexiom                     | 6.17 ms                                                | 7.36 ms: 1.19x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 60.2 ms: 1.20x slower                                                  |
| genshi_text                | 22.8 ms                                                | 27.5 ms: 1.21x slower                                                  |
| richards                   | 45.9 ms                                                | 55.6 ms: 1.21x slower                                                  |
| nqueens                    | 80.1 ms                                                | 96.8 ms: 1.21x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 373 us: 1.21x slower                                                   |
| create_gc_cycles           | 1.09 ms                                                | 1.34 ms: 1.22x slower                                                  |
| typing_runtime_protocols   | 163 us                                                 | 200 us: 1.23x slower                                                   |
| json_dumps                 | 10.4 ms                                                | 12.7 ms: 1.23x slower                                                  |
| richards_super             | 51.9 ms                                                | 64.7 ms: 1.25x slower                                                  |
| django_template            | 34.7 ms                                                | 43.4 ms: 1.25x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.50 ms: 1.25x slower                                                  |
| meteor_contest             | 104 ms                                                 | 131 ms: 1.26x slower                                                   |
| fannkuch                   | 372 ms                                                 | 471 ms: 1.27x slower                                                   |
| telco                      | 6.53 ms                                                | 8.52 ms: 1.30x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 9.54 ms: 1.33x slower                                                  |
| deltablue                  | 3.45 ms                                                | 4.60 ms: 1.33x slower                                                  |
| coverage                   | 71.4 ms                                                | 98.0 ms: 1.37x slower                                                  |
| mako                       | 11.0 ms                                                | 15.6 ms: 1.42x slower                                                  |
| nbody                      | 89.3 ms                                                | 134 ms: 1.50x slower                                                   |
| python_startup             | 9.93 ms                                                | 15.2 ms: 1.53x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 3.32 ms: 3.53x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 94.2 ms: 8.73x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.09x slower                                                           |

Benchmark hidden because not significant (2): pylint, scimark_sor
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250116-3.14.0a4+-b44ff6d-NOGIL/bm-20250116-vultr-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.047x slower

# HPT report

- Reliability score: 99.94% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.04x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: 1.36x