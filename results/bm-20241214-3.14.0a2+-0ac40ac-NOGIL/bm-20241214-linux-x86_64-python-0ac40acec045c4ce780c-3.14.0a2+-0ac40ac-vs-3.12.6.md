# Results vs. 3.12.6

- fork: python
- ref: 0ac40acec045c4ce780c
- machine: linux-x86_64
- commit hash: 0ac40ac
- commit date: 2024-12-14
- overall geometric mean: 1.156x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 577 ms: 1.27x slower                                                   |
| docutils       | 4.00 sec                                               | 4.38 sec: 1.10x slower                                                 |
| html5lib       | 88.9 ms                                                | 120 ms: 1.35x slower                                                   |
| Geometric mean | (ref)                                                  | 1.23x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.01 sec: 1.92x faster                                                 |
| async_tree_io              | 1.85 sec                                               | 1.08 sec: 1.71x faster                                                 |
| async_tree_memoization_tg  | 930 ms                                                 | 585 ms: 1.59x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 451 ms: 1.56x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 644 ms: 1.52x faster                                                   |
| async_tree_none            | 741 ms                                                 | 513 ms: 1.45x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 772 ms: 1.43x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 850 ms: 1.27x faster                                                   |
| async_generators           | 589 ms                                                 | 659 ms: 1.12x slower                                                   |
| coroutines                 | 29.5 ms                                                | 35.3 ms: 1.20x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.34x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 250 ms                                                 | 238 ms: 1.05x faster                                                   |
| float          | 123 ms                                                 | 168 ms: 1.37x slower                                                   |
| nbody          | 119 ms                                                 | 167 ms: 1.40x slower                                                   |
| Geometric mean | (ref)                                                  | 1.22x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.51 ms: 1.14x faster                                                  |
| regex_dna      | 278 ms                                                 | 290 ms: 1.04x slower                                                   |
| regex_compile  | 187 ms                                                 | 235 ms: 1.26x slower                                                   |
| Geometric mean | (ref)                                                  | 1.04x slower                                                           |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 169 ms                                                 | 137 ms: 1.24x faster                                                   |
| xml_etree_parse      | 241 ms                                                 | 204 ms: 1.18x faster                                                   |
| json_loads           | 37.9 us                                                | 35.7 us: 1.06x faster                                                  |
| xml_etree_generate   | 127 ms                                                 | 135 ms: 1.06x slower                                                   |
| tomli_loads          | 2.88 sec                                               | 3.36 sec: 1.17x slower                                                 |
| json_dumps           | 14.3 ms                                                | 17.3 ms: 1.21x slower                                                  |
| xml_etree_process    | 83.7 ms                                                | 104 ms: 1.25x slower                                                   |
| unpickle_pure_python | 300 us                                                 | 411 us: 1.37x slower                                                   |
| pickle_pure_python   | 436 us                                                 | 615 us: 1.41x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.10x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 19.4 ms: 1.10x slower                                                  |
| python_startup         | 23.7 ms                                                | 31.5 ms: 1.33x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.21x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 67.6 ms                                                | 89.0 ms: 1.32x slower                                                  |
| genshi_text     | 30.2 ms                                                | 41.0 ms: 1.36x slower                                                  |
| django_template | 44.9 ms                                                | 61.0 ms: 1.36x slower                                                  |
| mako            | 15.7 ms                                                | 26.3 ms: 1.67x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.42x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.01 sec: 1.92x faster                                                 |
| async_tree_io              | 1.85 sec                                               | 1.08 sec: 1.71x faster                                                 |
| async_tree_memoization_tg  | 930 ms                                                 | 585 ms: 1.59x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 451 ms: 1.56x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 644 ms: 1.52x faster                                                   |
| async_tree_none            | 741 ms                                                 | 513 ms: 1.45x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 772 ms: 1.43x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 850 ms: 1.27x faster                                                   |
| xml_etree_iterparse        | 169 ms                                                 | 137 ms: 1.24x faster                                                   |
| xml_etree_parse            | 241 ms                                                 | 204 ms: 1.18x faster                                                   |
| deepcopy                   | 468 us                                                 | 408 us: 1.15x faster                                                   |
| regex_effbot               | 5.13 ms                                                | 4.51 ms: 1.14x faster                                                  |
| json_loads                 | 37.9 us                                                | 35.7 us: 1.06x faster                                                  |
| sqlite_synth               | 3.87 us                                                | 3.66 us: 1.06x faster                                                  |
| pidigits                   | 250 ms                                                 | 238 ms: 1.05x faster                                                   |
| deepcopy_memo              | 52.4 us                                                | 50.2 us: 1.04x faster                                                  |
| regex_dna                  | 278 ms                                                 | 290 ms: 1.04x slower                                                   |
| xml_etree_generate         | 127 ms                                                 | 135 ms: 1.06x slower                                                   |
| deepcopy_reduce            | 4.04 us                                                | 4.30 us: 1.07x slower                                                  |
| pycparser                  | 1.79 sec                                               | 1.93 sec: 1.08x slower                                                 |
| sqlglot_normalize          | 157 ms                                                 | 169 ms: 1.08x slower                                                   |
| pylint                     | 465 ms                                                 | 501 ms: 1.08x slower                                                   |
| bench_thread_pool          | 3.48 ms                                                | 3.76 ms: 1.08x slower                                                  |
| docutils                   | 4.00 sec                                               | 4.38 sec: 1.10x slower                                                 |
| scimark_fft                | 500 ms                                                 | 550 ms: 1.10x slower                                                   |
| python_startup_no_site     | 17.6 ms                                                | 19.4 ms: 1.10x slower                                                  |
| nqueens                    | 117 ms                                                 | 130 ms: 1.11x slower                                                   |
| mdp                        | 3.97 sec                                               | 4.41 sec: 1.11x slower                                                 |
| async_generators           | 589 ms                                                 | 659 ms: 1.12x slower                                                   |
| bpe_tokeniser              | 6.59 sec                                               | 7.46 sec: 1.13x slower                                                 |
| crypto_pyaes               | 107 ms                                                 | 123 ms: 1.15x slower                                                   |
| gc_traversal               | 5.86 ms                                                | 6.80 ms: 1.16x slower                                                  |
| tomli_loads                | 2.88 sec                                               | 3.36 sec: 1.17x slower                                                 |
| dulwich_log                | 100 ms                                                 | 117 ms: 1.17x slower                                                   |
| meteor_contest             | 146 ms                                                 | 173 ms: 1.18x slower                                                   |
| sqlglot_optimize           | 76.0 ms                                                | 90.9 ms: 1.20x slower                                                  |
| coroutines                 | 29.5 ms                                                | 35.3 ms: 1.20x slower                                                  |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 8.07 ms: 1.20x slower                                                  |
| json_dumps                 | 14.3 ms                                                | 17.3 ms: 1.21x slower                                                  |
| fannkuch                   | 540 ms                                                 | 653 ms: 1.21x slower                                                   |
| typing_runtime_protocols   | 224 us                                                 | 274 us: 1.22x slower                                                   |
| sqlalchemy_declarative     | 218 ms                                                 | 269 ms: 1.24x slower                                                   |
| xml_etree_process          | 83.7 ms                                                | 104 ms: 1.25x slower                                                   |
| regex_compile              | 187 ms                                                 | 235 ms: 1.26x slower                                                   |
| 2to3                       | 456 ms                                                 | 577 ms: 1.27x slower                                                   |
| telco                      | 9.59 ms                                                | 12.2 ms: 1.27x slower                                                  |
| generators                 | 41.1 ms                                                | 52.5 ms: 1.28x slower                                                  |
| logging_simple             | 9.45 us                                                | 12.1 us: 1.28x slower                                                  |
| comprehensions             | 27.1 us                                                | 34.7 us: 1.28x slower                                                  |
| pyflate                    | 727 ms                                                 | 939 ms: 1.29x slower                                                   |
| genshi_xml                 | 67.6 ms                                                | 89.0 ms: 1.32x slower                                                  |
| sympy_integrate            | 29.8 ms                                                | 39.4 ms: 1.32x slower                                                  |
| python_startup             | 23.7 ms                                                | 31.5 ms: 1.33x slower                                                  |
| pprint_safe_repr           | 967 ms                                                 | 1.30 sec: 1.34x slower                                                 |
| html5lib                   | 88.9 ms                                                | 120 ms: 1.35x slower                                                   |
| thrift                     | 1.06 ms                                                | 1.43 ms: 1.35x slower                                                  |
| genshi_text                | 30.2 ms                                                | 41.0 ms: 1.36x slower                                                  |
| django_template            | 44.9 ms                                                | 61.0 ms: 1.36x slower                                                  |
| pprint_pformat             | 1.98 sec                                               | 2.71 sec: 1.37x slower                                                 |
| float                      | 123 ms                                                 | 168 ms: 1.37x slower                                                   |
| unpickle_pure_python       | 300 us                                                 | 411 us: 1.37x slower                                                   |
| nbody                      | 119 ms                                                 | 167 ms: 1.40x slower                                                   |
| pickle_pure_python         | 436 us                                                 | 615 us: 1.41x slower                                                   |
| logging_format             | 9.59 us                                                | 13.6 us: 1.42x slower                                                  |
| chaos                      | 84.9 ms                                                | 123 ms: 1.45x slower                                                   |
| richards_super             | 72.8 ms                                                | 106 ms: 1.46x slower                                                   |
| sqlalchemy_imperative      | 24.7 ms                                                | 36.1 ms: 1.46x slower                                                  |
| coverage                   | 95.4 ms                                                | 141 ms: 1.48x slower                                                   |
| raytrace                   | 408 ms                                                 | 620 ms: 1.52x slower                                                   |
| scimark_lu                 | 152 ms                                                 | 232 ms: 1.53x slower                                                   |
| hexiom                     | 8.27 ms                                                | 12.7 ms: 1.54x slower                                                  |
| sympy_str                  | 385 ms                                                 | 600 ms: 1.56x slower                                                   |
| scimark_monte_carlo        | 96.4 ms                                                | 151 ms: 1.57x slower                                                   |
| logging_silent             | 139 ns                                                 | 220 ns: 1.58x slower                                                   |
| richards                   | 60.3 ms                                                | 96.2 ms: 1.59x slower                                                  |
| sqlglot_transpile          | 2.34 ms                                                | 3.81 ms: 1.63x slower                                                  |
| mako                       | 15.7 ms                                                | 26.3 ms: 1.67x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 3.28 ms: 1.69x slower                                                  |
| sqlglot_parse              | 1.79 ms                                                | 3.05 ms: 1.70x slower                                                  |
| scimark_sor                | 167 ms                                                 | 291 ms: 1.75x slower                                                   |
| go                         | 172 ms                                                 | 303 ms: 1.76x slower                                                   |
| sympy_expand               | 582 ms                                                 | 1.11 sec: 1.91x slower                                                 |
| sympy_sum                  | 222 ms                                                 | 424 ms: 1.91x slower                                                   |
| deltablue                  | 4.27 ms                                                | 11.3 ms: 2.64x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 90.5 ms: 4.37x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.20x slower                                                           |

Benchmark hidden because not significant (5): asyncio_websockets, json, pathlib, regex_v8, spectral_norm
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241214-3.14.0a2+-0ac40ac-NOGIL/bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.156x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.13x
- 95% likely to have a slowdown of 1.12x
- 99% likely to have a slowdown of 1.10x

# Memory
- memory change: 1.34x