# Results vs. 3.12.6

- fork: python
- ref: cfeaa992ba9bad9be268
- machine: linux-x86_64
- commit hash: cfeaa99
- commit date: 2024-12-16
- overall geometric mean: 1.158x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 583 ms: 1.28x slower                                                   |
| docutils       | 4.00 sec                                               | 4.37 sec: 1.09x slower                                                 |
| html5lib       | 88.9 ms                                                | 123 ms: 1.38x slower                                                   |
| Geometric mean | (ref)                                                  | 1.24x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.01 sec: 1.91x faster                                                 |
| async_tree_io              | 1.85 sec                                               | 1.05 sec: 1.75x faster                                                 |
| async_tree_memoization_tg  | 930 ms                                                 | 572 ms: 1.63x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 444 ms: 1.59x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 641 ms: 1.52x faster                                                   |
| async_tree_none            | 741 ms                                                 | 521 ms: 1.42x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 810 ms: 1.36x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 828 ms: 1.30x faster                                                   |
| async_generators           | 589 ms                                                 | 651 ms: 1.11x slower                                                   |
| coroutines                 | 29.5 ms                                                | 35.3 ms: 1.19x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.34x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 250 ms                                                 | 231 ms: 1.08x faster                                                   |
| float          | 123 ms                                                 | 167 ms: 1.36x slower                                                   |
| nbody          | 119 ms                                                 | 173 ms: 1.46x slower                                                   |
| Geometric mean | (ref)                                                  | 1.22x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.09 ms: 1.26x faster                                                  |
| regex_dna      | 278 ms                                                 | 290 ms: 1.04x slower                                                   |
| regex_v8       | 32.5 ms                                                | 34.6 ms: 1.06x slower                                                  |
| regex_compile  | 187 ms                                                 | 214 ms: 1.14x slower                                                   |
| Geometric mean | (ref)                                                  | 1.00x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 169 ms                                                 | 137 ms: 1.23x faster                                                   |
| xml_etree_parse      | 241 ms                                                 | 205 ms: 1.17x faster                                                   |
| json_loads           | 37.9 us                                                | 36.0 us: 1.05x faster                                                  |
| xml_etree_generate   | 127 ms                                                 | 137 ms: 1.08x slower                                                   |
| tomli_loads          | 2.88 sec                                               | 3.31 sec: 1.15x slower                                                 |
| json_dumps           | 14.3 ms                                                | 17.5 ms: 1.22x slower                                                  |
| xml_etree_process    | 83.7 ms                                                | 103 ms: 1.23x slower                                                   |
| unpickle_pure_python | 300 us                                                 | 414 us: 1.38x slower                                                   |
| pickle_pure_python   | 436 us                                                 | 679 us: 1.56x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.11x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 19.3 ms: 1.10x slower                                                  |
| python_startup         | 23.7 ms                                                | 31.2 ms: 1.32x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.20x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 67.6 ms                                                | 88.9 ms: 1.31x slower                                                  |
| genshi_text     | 30.2 ms                                                | 39.9 ms: 1.32x slower                                                  |
| django_template | 44.9 ms                                                | 61.0 ms: 1.36x slower                                                  |
| mako            | 15.7 ms                                                | 25.3 ms: 1.61x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.40x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.01 sec: 1.91x faster                                                 |
| async_tree_io              | 1.85 sec                                               | 1.05 sec: 1.75x faster                                                 |
| async_tree_memoization_tg  | 930 ms                                                 | 572 ms: 1.63x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 444 ms: 1.59x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 641 ms: 1.52x faster                                                   |
| async_tree_none            | 741 ms                                                 | 521 ms: 1.42x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 810 ms: 1.36x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 828 ms: 1.30x faster                                                   |
| regex_effbot               | 5.13 ms                                                | 4.09 ms: 1.26x faster                                                  |
| xml_etree_iterparse        | 169 ms                                                 | 137 ms: 1.23x faster                                                   |
| xml_etree_parse            | 241 ms                                                 | 205 ms: 1.17x faster                                                   |
| deepcopy                   | 468 us                                                 | 401 us: 1.17x faster                                                   |
| pidigits                   | 250 ms                                                 | 231 ms: 1.08x faster                                                   |
| json_loads                 | 37.9 us                                                | 36.0 us: 1.05x faster                                                  |
| regex_dna                  | 278 ms                                                 | 290 ms: 1.04x slower                                                   |
| regex_v8                   | 32.5 ms                                                | 34.6 ms: 1.06x slower                                                  |
| scimark_fft                | 500 ms                                                 | 536 ms: 1.07x slower                                                   |
| xml_etree_generate         | 127 ms                                                 | 137 ms: 1.08x slower                                                   |
| pycparser                  | 1.79 sec                                               | 1.93 sec: 1.08x slower                                                 |
| docutils                   | 4.00 sec                                               | 4.37 sec: 1.09x slower                                                 |
| python_startup_no_site     | 17.6 ms                                                | 19.3 ms: 1.10x slower                                                  |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 7.35 ms: 1.10x slower                                                  |
| nqueens                    | 117 ms                                                 | 129 ms: 1.10x slower                                                   |
| async_generators           | 589 ms                                                 | 651 ms: 1.11x slower                                                   |
| deepcopy_reduce            | 4.04 us                                                | 4.47 us: 1.11x slower                                                  |
| sqlglot_normalize          | 157 ms                                                 | 175 ms: 1.12x slower                                                   |
| sqlglot_optimize           | 76.0 ms                                                | 85.0 ms: 1.12x slower                                                  |
| pylint                     | 465 ms                                                 | 522 ms: 1.12x slower                                                   |
| mdp                        | 3.97 sec                                               | 4.46 sec: 1.12x slower                                                 |
| dulwich_log                | 100 ms                                                 | 113 ms: 1.12x slower                                                   |
| regex_compile              | 187 ms                                                 | 214 ms: 1.14x slower                                                   |
| bpe_tokeniser              | 6.59 sec                                               | 7.55 sec: 1.15x slower                                                 |
| tomli_loads                | 2.88 sec                                               | 3.31 sec: 1.15x slower                                                 |
| bench_thread_pool          | 3.48 ms                                                | 3.99 ms: 1.15x slower                                                  |
| crypto_pyaes               | 107 ms                                                 | 124 ms: 1.15x slower                                                   |
| gc_traversal               | 5.86 ms                                                | 6.93 ms: 1.18x slower                                                  |
| coroutines                 | 29.5 ms                                                | 35.3 ms: 1.19x slower                                                  |
| comprehensions             | 27.1 us                                                | 32.6 us: 1.20x slower                                                  |
| meteor_contest             | 146 ms                                                 | 178 ms: 1.22x slower                                                   |
| json_dumps                 | 14.3 ms                                                | 17.5 ms: 1.22x slower                                                  |
| xml_etree_process          | 83.7 ms                                                | 103 ms: 1.23x slower                                                   |
| typing_runtime_protocols   | 224 us                                                 | 279 us: 1.24x slower                                                   |
| sqlalchemy_declarative     | 218 ms                                                 | 272 ms: 1.25x slower                                                   |
| fannkuch                   | 540 ms                                                 | 683 ms: 1.26x slower                                                   |
| 2to3                       | 456 ms                                                 | 583 ms: 1.28x slower                                                   |
| sympy_integrate            | 29.8 ms                                                | 38.3 ms: 1.29x slower                                                  |
| pyflate                    | 727 ms                                                 | 943 ms: 1.30x slower                                                   |
| logging_simple             | 9.45 us                                                | 12.3 us: 1.30x slower                                                  |
| genshi_xml                 | 67.6 ms                                                | 88.9 ms: 1.31x slower                                                  |
| python_startup             | 23.7 ms                                                | 31.2 ms: 1.32x slower                                                  |
| generators                 | 41.1 ms                                                | 54.3 ms: 1.32x slower                                                  |
| genshi_text                | 30.2 ms                                                | 39.9 ms: 1.32x slower                                                  |
| pprint_safe_repr           | 967 ms                                                 | 1.29 sec: 1.33x slower                                                 |
| telco                      | 9.59 ms                                                | 12.8 ms: 1.33x slower                                                  |
| pprint_pformat             | 1.98 sec                                               | 2.65 sec: 1.34x slower                                                 |
| django_template            | 44.9 ms                                                | 61.0 ms: 1.36x slower                                                  |
| float                      | 123 ms                                                 | 167 ms: 1.36x slower                                                   |
| logging_format             | 9.59 us                                                | 13.2 us: 1.37x slower                                                  |
| html5lib                   | 88.9 ms                                                | 123 ms: 1.38x slower                                                   |
| unpickle_pure_python       | 300 us                                                 | 414 us: 1.38x slower                                                   |
| thrift                     | 1.06 ms                                                | 1.47 ms: 1.38x slower                                                  |
| coverage                   | 95.4 ms                                                | 134 ms: 1.40x slower                                                   |
| nbody                      | 119 ms                                                 | 173 ms: 1.46x slower                                                   |
| richards_super             | 72.8 ms                                                | 106 ms: 1.46x slower                                                   |
| scimark_lu                 | 152 ms                                                 | 222 ms: 1.46x slower                                                   |
| sqlalchemy_imperative      | 24.7 ms                                                | 36.9 ms: 1.50x slower                                                  |
| chaos                      | 84.9 ms                                                | 129 ms: 1.51x slower                                                   |
| sympy_str                  | 385 ms                                                 | 586 ms: 1.52x slower                                                   |
| richards                   | 60.3 ms                                                | 92.4 ms: 1.53x slower                                                  |
| hexiom                     | 8.27 ms                                                | 12.8 ms: 1.55x slower                                                  |
| raytrace                   | 408 ms                                                 | 635 ms: 1.56x slower                                                   |
| pickle_pure_python         | 436 us                                                 | 679 us: 1.56x slower                                                   |
| scimark_monte_carlo        | 96.4 ms                                                | 151 ms: 1.57x slower                                                   |
| logging_silent             | 139 ns                                                 | 221 ns: 1.59x slower                                                   |
| mako                       | 15.7 ms                                                | 25.3 ms: 1.61x slower                                                  |
| sqlglot_transpile          | 2.34 ms                                                | 3.99 ms: 1.71x slower                                                  |
| sympy_sum                  | 222 ms                                                 | 400 ms: 1.80x slower                                                   |
| scimark_sor                | 167 ms                                                 | 302 ms: 1.81x slower                                                   |
| go                         | 172 ms                                                 | 315 ms: 1.83x slower                                                   |
| sqlglot_parse              | 1.79 ms                                                | 3.30 ms: 1.84x slower                                                  |
| sympy_expand               | 582 ms                                                 | 1.09 sec: 1.88x slower                                                 |
| create_gc_cycles           | 1.94 ms                                                | 3.72 ms: 1.92x slower                                                  |
| deltablue                  | 4.27 ms                                                | 11.4 ms: 2.68x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 92.3 ms: 4.46x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.21x slower                                                           |

Benchmark hidden because not significant (6): asyncio_websockets, pathlib, deepcopy_memo, spectral_norm, json, sqlite_synth
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241216-3.14.0a2+-cfeaa99-NOGIL/bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.158x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.14x
- 95% likely to have a slowdown of 1.13x
- 99% likely to have a slowdown of 1.10x

# Memory
- memory change: 1.34x