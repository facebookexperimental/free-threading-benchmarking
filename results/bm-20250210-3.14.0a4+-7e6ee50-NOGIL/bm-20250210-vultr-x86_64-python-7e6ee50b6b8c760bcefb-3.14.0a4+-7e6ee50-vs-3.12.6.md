# Results vs. 3.12.6

- fork: python
- ref: 7e6ee50b6b8c760bcefb
- machine: linux-x86_64
- commit hash: 7e6ee50
- commit date: 2025-02-10
- overall geometric mean: 1.044x slower
- HPT reliability: 99.97%
- HPT 99th percentile: 1.02x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 301 ms: 1.14x slower                                                   |
| docutils       | 2.64 sec                                               | 2.79 sec: 1.06x slower                                                 |
| html5lib       | 63.6 ms                                                | 68.8 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                  | 1.09x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 571 ms: 1.94x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 605 ms: 1.79x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 318 ms: 1.76x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 257 ms: 1.74x faster                                                   |
| async_tree_none            | 464 ms                                                 | 286 ms: 1.62x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 349 ms: 1.59x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 504 ms: 1.43x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 537 ms: 1.33x faster                                                   |
| coroutines                 | 23.9 ms                                                | 23.3 ms: 1.03x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.44x faster                                                           |

Benchmark hidden because not significant (2): asyncio_websockets, async_generators

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 75.8 ms: 1.07x faster                                                  |
| pidigits       | 184 ms                                                 | 191 ms: 1.04x slower                                                   |
| nbody          | 89.3 ms                                                | 130 ms: 1.46x slower                                                   |
| Geometric mean | (ref)                                                  | 1.12x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.77 ms: 1.14x faster                                                  |
| regex_dna      | 168 ms                                                 | 177 ms: 1.05x slower                                                   |
| regex_compile  | 142 ms                                                 | 150 ms: 1.05x slower                                                   |
| regex_v8       | 20.6 ms                                                | 23.3 ms: 1.13x slower                                                  |
| Geometric mean | (ref)                                                  | 1.02x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.9 ms: 1.10x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.08x faster                                                   |
| tomli_loads          | 2.11 sec                                               | 2.32 sec: 1.10x slower                                                 |
| unpickle_pure_python | 221 us                                                 | 245 us: 1.11x slower                                                   |
| xml_etree_generate   | 85.2 ms                                                | 96.6 ms: 1.13x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 69.0 ms: 1.17x slower                                                  |
| json_loads           | 26.5 us                                                | 31.3 us: 1.18x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 366 us: 1.19x slower                                                   |
| json_dumps           | 10.4 ms                                                | 12.8 ms: 1.23x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.10x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.55 ms: 1.33x slower                                                  |
| python_startup         | 9.93 ms                                                | 15.2 ms: 1.53x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.43x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 59.2 ms: 1.18x slower                                                  |
| django_template | 34.7 ms                                                | 42.5 ms: 1.23x slower                                                  |
| genshi_text     | 22.8 ms                                                | 28.0 ms: 1.23x slower                                                  |
| mako            | 11.0 ms                                                | 16.0 ms: 1.45x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.27x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal               | 3.46 ms                                                | 1.73 ms: 2.00x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 571 ms: 1.94x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 605 ms: 1.79x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 318 ms: 1.76x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 257 ms: 1.74x faster                                                   |
| async_tree_none            | 464 ms                                                 | 286 ms: 1.62x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 349 ms: 1.59x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 504 ms: 1.43x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 537 ms: 1.33x faster                                                   |
| deepcopy                   | 352 us                                                 | 306 us: 1.15x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.77 ms: 1.14x faster                                                  |
| pathlib                    | 21.5 ms                                                | 19.0 ms: 1.13x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 87.9 ms: 1.10x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                                   |
| sqlite_synth               | 2.20 us                                                | 2.05 us: 1.07x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 37.7 us: 1.07x faster                                                  |
| float                      | 80.8 ms                                                | 75.8 ms: 1.07x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.3 ms: 1.03x faster                                                  |
| generators                 | 32.2 ms                                                | 31.6 ms: 1.02x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.67 sec: 1.01x faster                                                 |
| spectral_norm              | 110 ms                                                 | 109 ms: 1.01x faster                                                   |
| go                         | 139 ms                                                 | 139 ms: 1.00x faster                                                   |
| pycparser                  | 1.17 sec                                               | 1.18 sec: 1.01x slower                                                 |
| comprehensions             | 19.8 us                                                | 20.1 us: 1.01x slower                                                  |
| deepcopy_reduce            | 3.08 us                                                | 3.14 us: 1.02x slower                                                  |
| scimark_sor                | 130 ms                                                 | 134 ms: 1.03x slower                                                   |
| logging_silent             | 109 ns                                                 | 113 ns: 1.03x slower                                                   |
| pidigits                   | 184 ms                                                 | 191 ms: 1.04x slower                                                   |
| dulwich_log                | 78.9 ms                                                | 81.8 ms: 1.04x slower                                                  |
| regex_dna                  | 168 ms                                                 | 177 ms: 1.05x slower                                                   |
| regex_compile              | 142 ms                                                 | 150 ms: 1.05x slower                                                   |
| docutils                   | 2.64 sec                                               | 2.79 sec: 1.06x slower                                                 |
| json                       | 5.02 ms                                                | 5.38 ms: 1.07x slower                                                  |
| html5lib                   | 63.6 ms                                                | 68.8 ms: 1.08x slower                                                  |
| pprint_safe_repr           | 743 ms                                                 | 808 ms: 1.09x slower                                                   |
| sqlalchemy_declarative     | 143 ms                                                 | 156 ms: 1.09x slower                                                   |
| raytrace                   | 299 ms                                                 | 326 ms: 1.09x slower                                                   |
| chaos                      | 62.8 ms                                                | 68.8 ms: 1.09x slower                                                  |
| mdp                        | 2.42 sec                                               | 2.65 sec: 1.09x slower                                                 |
| pyflate                    | 448 ms                                                 | 491 ms: 1.10x slower                                                   |
| logging_simple             | 6.63 us                                                | 7.30 us: 1.10x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.67 sec: 1.10x slower                                                 |
| tomli_loads                | 2.11 sec                                               | 2.32 sec: 1.10x slower                                                 |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.1 ms: 1.10x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 184 ms: 1.11x slower                                                   |
| unpickle_pure_python       | 221 us                                                 | 245 us: 1.11x slower                                                   |
| sqlglot_normalize          | 107 ms                                                 | 119 ms: 1.12x slower                                                   |
| sqlglot_transpile          | 1.67 ms                                                | 1.88 ms: 1.12x slower                                                  |
| logging_format             | 7.35 us                                                | 8.27 us: 1.13x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 23.3 ms: 1.13x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 96.6 ms: 1.13x slower                                                  |
| scimark_fft                | 342 ms                                                 | 388 ms: 1.14x slower                                                   |
| thrift                     | 791 us                                                 | 899 us: 1.14x slower                                                   |
| crypto_pyaes               | 76.6 ms                                                | 87.2 ms: 1.14x slower                                                  |
| 2to3                       | 264 ms                                                 | 301 ms: 1.14x slower                                                   |
| sympy_str                  | 292 ms                                                 | 333 ms: 1.14x slower                                                   |
| sqlglot_optimize           | 53.3 ms                                                | 61.0 ms: 1.14x slower                                                  |
| sqlglot_parse              | 1.36 ms                                                | 1.56 ms: 1.15x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 23.9 ms: 1.16x slower                                                  |
| sympy_expand               | 468 ms                                                 | 544 ms: 1.16x slower                                                   |
| xml_etree_process          | 59.0 ms                                                | 69.0 ms: 1.17x slower                                                  |
| json_loads                 | 26.5 us                                                | 31.3 us: 1.18x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 59.2 ms: 1.18x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 366 us: 1.19x slower                                                   |
| hexiom                     | 6.17 ms                                                | 7.40 ms: 1.20x slower                                                  |
| nqueens                    | 80.1 ms                                                | 96.1 ms: 1.20x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 82.4 ms: 1.20x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 138 ms: 1.21x slower                                                   |
| typing_runtime_protocols   | 163 us                                                 | 200 us: 1.22x slower                                                   |
| django_template            | 34.7 ms                                                | 42.5 ms: 1.23x slower                                                  |
| genshi_text                | 22.8 ms                                                | 28.0 ms: 1.23x slower                                                  |
| richards                   | 45.9 ms                                                | 56.5 ms: 1.23x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 12.8 ms: 1.23x slower                                                  |
| meteor_contest             | 104 ms                                                 | 129 ms: 1.25x slower                                                   |
| richards_super             | 51.9 ms                                                | 65.1 ms: 1.25x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.38 ms: 1.26x slower                                                  |
| fannkuch                   | 372 ms                                                 | 490 ms: 1.31x slower                                                   |
| telco                      | 6.53 ms                                                | 8.62 ms: 1.32x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.80 ms: 1.32x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 9.55 ms: 1.33x slower                                                  |
| coverage                   | 71.4 ms                                                | 97.1 ms: 1.36x slower                                                  |
| deltablue                  | 3.45 ms                                                | 4.70 ms: 1.36x slower                                                  |
| mako                       | 11.0 ms                                                | 16.0 ms: 1.45x slower                                                  |
| nbody                      | 89.3 ms                                                | 130 ms: 1.46x slower                                                   |
| python_startup             | 9.93 ms                                                | 15.2 ms: 1.53x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 3.32 ms: 3.53x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 94.3 ms: 8.74x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.09x slower                                                           |

Benchmark hidden because not significant (3): pylint, asyncio_websockets, async_generators
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250210-3.14.0a4+-7e6ee50-NOGIL/bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.044x slower

# HPT report

- Reliability score: 99.97% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.04x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: 1.36x