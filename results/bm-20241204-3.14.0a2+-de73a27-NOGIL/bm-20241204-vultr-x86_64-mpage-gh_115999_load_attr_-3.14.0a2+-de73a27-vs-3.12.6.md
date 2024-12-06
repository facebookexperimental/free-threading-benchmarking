# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: de73a27
- commit date: 2024-12-04
- overall geometric mean: 1.219x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.16x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 363 ms: 1.38x slower                                                  |
| docutils       | 2.64 sec                                               | 3.08 sec: 1.17x slower                                                |
| html5lib       | 63.6 ms                                                | 97.9 ms: 1.54x slower                                                 |
| Geometric mean | (ref)                                                  | 1.35x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 804 ms: 1.38x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 821 ms: 1.32x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 439 ms: 1.28x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 350 ms: 1.27x faster                                                  |
| async_tree_none            | 464 ms                                                 | 379 ms: 1.23x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 459 ms: 1.21x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 606 ms: 1.19x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 626 ms: 1.14x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 520 ms: 1.01x slower                                                  |
| coroutines                 | 23.9 ms                                                | 25.5 ms: 1.07x slower                                                 |
| async_generators           | 384 ms                                                 | 459 ms: 1.20x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.15x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 181 ms: 1.01x faster                                                  |
| nbody          | 89.3 ms                                                | 126 ms: 1.41x slower                                                  |
| float          | 80.8 ms                                                | 139 ms: 1.72x slower                                                  |
| Geometric mean | (ref)                                                  | 1.34x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.89 ms: 1.10x faster                                                 |
| regex_dna      | 168 ms                                                 | 185 ms: 1.11x slower                                                  |
| regex_v8       | 20.6 ms                                                | 24.7 ms: 1.20x slower                                                 |
| regex_compile  | 142 ms                                                 | 178 ms: 1.25x slower                                                  |
| Geometric mean | (ref)                                                  | 1.11x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 91.2 ms: 1.06x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                  |
| json_loads           | 26.5 us                                                | 28.3 us: 1.06x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 97.6 ms: 1.15x slower                                                 |
| tomli_loads          | 2.11 sec                                               | 2.64 sec: 1.25x slower                                                |
| xml_etree_process    | 59.0 ms                                                | 78.2 ms: 1.33x slower                                                 |
| json_dumps           | 10.4 ms                                                | 13.9 ms: 1.35x slower                                                 |
| unpickle_pure_python | 221 us                                                 | 332 us: 1.50x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 512 us: 1.66x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.22x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.3 ms: 1.44x slower                                                 |
| python_startup         | 9.93 ms                                                | 17.2 ms: 1.74x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.58x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 62.7 ms: 1.25x slower                                                 |
| genshi_text     | 22.8 ms                                                | 30.3 ms: 1.33x slower                                                 |
| django_template | 34.7 ms                                                | 50.5 ms: 1.46x slower                                                 |
| mako            | 11.0 ms                                                | 16.9 ms: 1.54x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.39x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 804 ms: 1.38x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 821 ms: 1.32x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 439 ms: 1.28x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 350 ms: 1.27x faster                                                  |
| async_tree_none            | 464 ms                                                 | 379 ms: 1.23x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 459 ms: 1.21x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 606 ms: 1.19x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 626 ms: 1.14x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.89 ms: 1.10x faster                                                 |
| deepcopy                   | 352 us                                                 | 325 us: 1.08x faster                                                  |
| pathlib                    | 21.5 ms                                                | 20.1 ms: 1.07x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 91.2 ms: 1.06x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                  |
| pidigits                   | 184 ms                                                 | 181 ms: 1.01x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 40.1 us: 1.01x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 520 ms: 1.01x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 3.53 ms: 1.02x slower                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 5.04 sec: 1.06x slower                                                |
| json_loads                 | 26.5 us                                                | 28.3 us: 1.06x slower                                                 |
| coroutines                 | 23.9 ms                                                | 25.5 ms: 1.07x slower                                                 |
| spectral_norm              | 110 ms                                                 | 121 ms: 1.10x slower                                                  |
| regex_dna                  | 168 ms                                                 | 185 ms: 1.11x slower                                                  |
| deepcopy_reduce            | 3.08 us                                                | 3.46 us: 1.12x slower                                                 |
| scimark_fft                | 342 ms                                                 | 388 ms: 1.13x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 97.6 ms: 1.15x slower                                                 |
| mdp                        | 2.42 sec                                               | 2.79 sec: 1.16x slower                                                |
| pylint                     | 319 ms                                                 | 371 ms: 1.16x slower                                                  |
| docutils                   | 2.64 sec                                               | 3.08 sec: 1.17x slower                                                |
| crypto_pyaes               | 76.6 ms                                                | 90.5 ms: 1.18x slower                                                 |
| nqueens                    | 80.1 ms                                                | 95.6 ms: 1.19x slower                                                 |
| async_generators           | 384 ms                                                 | 459 ms: 1.20x slower                                                  |
| generators                 | 32.2 ms                                                | 38.6 ms: 1.20x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 24.7 ms: 1.20x slower                                                 |
| dulwich_log                | 78.9 ms                                                | 94.9 ms: 1.20x slower                                                 |
| regex_compile              | 142 ms                                                 | 178 ms: 1.25x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 62.7 ms: 1.25x slower                                                 |
| tomli_loads                | 2.11 sec                                               | 2.64 sec: 1.25x slower                                                |
| typing_runtime_protocols   | 163 us                                                 | 205 us: 1.25x slower                                                  |
| sqlglot_optimize           | 53.3 ms                                                | 67.0 ms: 1.26x slower                                                 |
| meteor_contest             | 104 ms                                                 | 132 ms: 1.27x slower                                                  |
| sqlglot_normalize          | 107 ms                                                 | 136 ms: 1.28x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.62 ms: 1.28x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 954 ms: 1.28x slower                                                  |
| pycparser                  | 1.17 sec                                               | 1.52 sec: 1.30x slower                                                |
| pprint_pformat             | 1.52 sec                                               | 1.98 sec: 1.30x slower                                                |
| fannkuch                   | 372 ms                                                 | 489 ms: 1.31x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 78.2 ms: 1.33x slower                                                 |
| genshi_text                | 22.8 ms                                                | 30.3 ms: 1.33x slower                                                 |
| sqlalchemy_imperative      | 21.8 ms                                                | 29.2 ms: 1.34x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 13.9 ms: 1.35x slower                                                 |
| telco                      | 6.53 ms                                                | 8.84 ms: 1.35x slower                                                 |
| 2to3                       | 264 ms                                                 | 363 ms: 1.38x slower                                                  |
| comprehensions             | 19.8 us                                                | 27.8 us: 1.40x slower                                                 |
| sqlalchemy_declarative     | 143 ms                                                 | 201 ms: 1.41x slower                                                  |
| nbody                      | 89.3 ms                                                | 126 ms: 1.41x slower                                                  |
| coverage                   | 71.4 ms                                                | 101 ms: 1.42x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 29.5 ms: 1.44x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 10.3 ms: 1.44x slower                                                 |
| thrift                     | 791 us                                                 | 1.15 ms: 1.45x slower                                                 |
| django_template            | 34.7 ms                                                | 50.5 ms: 1.46x slower                                                 |
| logging_format             | 7.35 us                                                | 11.0 us: 1.50x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 332 us: 1.50x slower                                                  |
| logging_simple             | 6.63 us                                                | 10.2 us: 1.53x slower                                                 |
| mako                       | 11.0 ms                                                | 16.9 ms: 1.54x slower                                                 |
| html5lib                   | 63.6 ms                                                | 97.9 ms: 1.54x slower                                                 |
| pyflate                    | 448 ms                                                 | 703 ms: 1.57x slower                                                  |
| hexiom                     | 6.17 ms                                                | 9.82 ms: 1.59x slower                                                 |
| sympy_str                  | 292 ms                                                 | 476 ms: 1.63x slower                                                  |
| chaos                      | 62.8 ms                                                | 103 ms: 1.63x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 187 ms: 1.64x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 512 us: 1.66x slower                                                  |
| richards_super             | 51.9 ms                                                | 88.0 ms: 1.70x slower                                                 |
| logging_silent             | 109 ns                                                 | 186 ns: 1.70x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.87 ms: 1.71x slower                                                 |
| richards                   | 45.9 ms                                                | 78.8 ms: 1.71x slower                                                 |
| float                      | 80.8 ms                                                | 139 ms: 1.72x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 118 ms: 1.72x slower                                                  |
| python_startup             | 9.93 ms                                                | 17.2 ms: 1.74x slower                                                 |
| sqlglot_transpile          | 1.67 ms                                                | 2.96 ms: 1.77x slower                                                 |
| scimark_sor                | 130 ms                                                 | 237 ms: 1.83x slower                                                  |
| raytrace                   | 299 ms                                                 | 559 ms: 1.87x slower                                                  |
| sqlglot_parse              | 1.36 ms                                                | 2.57 ms: 1.90x slower                                                 |
| go                         | 139 ms                                                 | 270 ms: 1.94x slower                                                  |
| sympy_expand               | 468 ms                                                 | 955 ms: 2.04x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 349 ms: 2.10x slower                                                  |
| deltablue                  | 3.45 ms                                                | 8.20 ms: 2.38x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.34 ms: 3.55x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 108 ms: 10.02x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.33x slower                                                          |

Benchmark hidden because not significant (2): json, sqlite_synth
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241204-3.14.0a2+-de73a27-NOGIL/bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.219x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.20x
- 95% likely to have a slowdown of 1.19x
- 99% likely to have a slowdown of 1.16x

# Memory
- memory change: 1.34x