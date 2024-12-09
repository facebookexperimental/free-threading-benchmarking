# Results vs. 3.12.6

- fork: python
- ref: a03efb533a58fd13fb0c
- machine: linux-x86_64
- commit hash: a03efb5
- commit date: 2024-12-08
- overall geometric mean: 1.156x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241208-linux-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 589 ms: 1.29x slower                                                   |
| docutils       | 4.00 sec                                               | 4.24 sec: 1.06x slower                                                 |
| html5lib       | 88.9 ms                                                | 123 ms: 1.38x slower                                                   |
| Geometric mean | (ref)                                                  | 1.24x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241208-linux-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.03 sec: 1.87x faster                                                 |
| async_tree_io              | 1.85 sec                                               | 1.08 sec: 1.70x faster                                                 |
| async_tree_memoization_tg  | 930 ms                                                 | 600 ms: 1.55x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 458 ms: 1.54x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 648 ms: 1.51x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 762 ms: 1.44x faster                                                   |
| async_tree_none            | 741 ms                                                 | 519 ms: 1.43x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 841 ms: 1.28x faster                                                   |
| asyncio_websockets         | 748 ms                                                 | 725 ms: 1.03x faster                                                   |
| async_generators           | 589 ms                                                 | 644 ms: 1.09x slower                                                   |
| coroutines                 | 29.5 ms                                                | 34.4 ms: 1.17x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.34x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241208-linux-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 250 ms                                                 | 235 ms: 1.07x faster                                                   |
| float          | 123 ms                                                 | 175 ms: 1.43x slower                                                   |
| nbody          | 119 ms                                                 | 173 ms: 1.45x slower                                                   |
| Geometric mean | (ref)                                                  | 1.25x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241208-linux-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.17 ms: 1.23x faster                                                  |
| regex_compile  | 187 ms                                                 | 224 ms: 1.20x slower                                                   |
| Geometric mean | (ref)                                                  | 1.01x slower                                                           |

Benchmark hidden because not significant (2): regex_dna, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241208-linux-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 169 ms                                                 | 139 ms: 1.22x faster                                                   |
| xml_etree_parse      | 241 ms                                                 | 218 ms: 1.10x faster                                                   |
| xml_etree_generate   | 127 ms                                                 | 140 ms: 1.10x slower                                                   |
| tomli_loads          | 2.88 sec                                               | 3.39 sec: 1.17x slower                                                 |
| xml_etree_process    | 83.7 ms                                                | 100 ms: 1.20x slower                                                   |
| json_dumps           | 14.3 ms                                                | 19.0 ms: 1.33x slower                                                  |
| unpickle_pure_python | 300 us                                                 | 404 us: 1.35x slower                                                   |
| pickle_pure_python   | 436 us                                                 | 622 us: 1.43x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.12x slower                                                           |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241208-linux-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 19.3 ms: 1.09x slower                                                  |
| python_startup         | 23.7 ms                                                | 32.5 ms: 1.37x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.22x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241208-linux-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 67.6 ms                                                | 84.8 ms: 1.25x slower                                                  |
| genshi_text     | 30.2 ms                                                | 40.0 ms: 1.32x slower                                                  |
| django_template | 44.9 ms                                                | 63.5 ms: 1.41x slower                                                  |
| mako            | 15.7 ms                                                | 26.8 ms: 1.71x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.41x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241208-linux-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.03 sec: 1.87x faster                                                 |
| async_tree_io              | 1.85 sec                                               | 1.08 sec: 1.70x faster                                                 |
| async_tree_memoization_tg  | 930 ms                                                 | 600 ms: 1.55x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 458 ms: 1.54x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 648 ms: 1.51x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 762 ms: 1.44x faster                                                   |
| async_tree_none            | 741 ms                                                 | 519 ms: 1.43x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 841 ms: 1.28x faster                                                   |
| regex_effbot               | 5.13 ms                                                | 4.17 ms: 1.23x faster                                                  |
| xml_etree_iterparse        | 169 ms                                                 | 139 ms: 1.22x faster                                                   |
| xml_etree_parse            | 241 ms                                                 | 218 ms: 1.10x faster                                                   |
| bench_thread_pool          | 3.48 ms                                                | 3.22 ms: 1.08x faster                                                  |
| pidigits                   | 250 ms                                                 | 235 ms: 1.07x faster                                                   |
| deepcopy                   | 468 us                                                 | 441 us: 1.06x faster                                                   |
| deepcopy_memo              | 52.4 us                                                | 50.0 us: 1.05x faster                                                  |
| gc_traversal               | 5.86 ms                                                | 5.60 ms: 1.05x faster                                                  |
| asyncio_websockets         | 748 ms                                                 | 725 ms: 1.03x faster                                                   |
| docutils                   | 4.00 sec                                               | 4.24 sec: 1.06x slower                                                 |
| bpe_tokeniser              | 6.59 sec                                               | 7.11 sec: 1.08x slower                                                 |
| deepcopy_reduce            | 4.04 us                                                | 4.36 us: 1.08x slower                                                  |
| nqueens                    | 117 ms                                                 | 126 ms: 1.08x slower                                                   |
| sqlglot_normalize          | 157 ms                                                 | 170 ms: 1.08x slower                                                   |
| pycparser                  | 1.79 sec                                               | 1.94 sec: 1.08x slower                                                 |
| async_generators           | 589 ms                                                 | 644 ms: 1.09x slower                                                   |
| python_startup_no_site     | 17.6 ms                                                | 19.3 ms: 1.09x slower                                                  |
| xml_etree_generate         | 127 ms                                                 | 140 ms: 1.10x slower                                                   |
| scimark_fft                | 500 ms                                                 | 559 ms: 1.12x slower                                                   |
| pylint                     | 465 ms                                                 | 523 ms: 1.13x slower                                                   |
| mdp                        | 3.97 sec                                               | 4.48 sec: 1.13x slower                                                 |
| spectral_norm              | 156 ms                                                 | 176 ms: 1.13x slower                                                   |
| sqlglot_optimize           | 76.0 ms                                                | 86.2 ms: 1.13x slower                                                  |
| crypto_pyaes               | 107 ms                                                 | 122 ms: 1.14x slower                                                   |
| comprehensions             | 27.1 us                                                | 30.9 us: 1.14x slower                                                  |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 7.72 ms: 1.15x slower                                                  |
| coroutines                 | 29.5 ms                                                | 34.4 ms: 1.17x slower                                                  |
| tomli_loads                | 2.88 sec                                               | 3.39 sec: 1.17x slower                                                 |
| meteor_contest             | 146 ms                                                 | 173 ms: 1.18x slower                                                   |
| xml_etree_process          | 83.7 ms                                                | 100 ms: 1.20x slower                                                   |
| regex_compile              | 187 ms                                                 | 224 ms: 1.20x slower                                                   |
| dulwich_log                | 100 ms                                                 | 122 ms: 1.21x slower                                                   |
| typing_runtime_protocols   | 224 us                                                 | 279 us: 1.24x slower                                                   |
| telco                      | 9.59 ms                                                | 11.9 ms: 1.25x slower                                                  |
| genshi_xml                 | 67.6 ms                                                | 84.8 ms: 1.25x slower                                                  |
| generators                 | 41.1 ms                                                | 51.9 ms: 1.26x slower                                                  |
| fannkuch                   | 540 ms                                                 | 683 ms: 1.26x slower                                                   |
| sympy_integrate            | 29.8 ms                                                | 38.1 ms: 1.28x slower                                                  |
| sqlalchemy_declarative     | 218 ms                                                 | 279 ms: 1.28x slower                                                   |
| 2to3                       | 456 ms                                                 | 589 ms: 1.29x slower                                                   |
| pprint_safe_repr           | 967 ms                                                 | 1.26 sec: 1.30x slower                                                 |
| genshi_text                | 30.2 ms                                                | 40.0 ms: 1.32x slower                                                  |
| json_dumps                 | 14.3 ms                                                | 19.0 ms: 1.33x slower                                                  |
| pyflate                    | 727 ms                                                 | 980 ms: 1.35x slower                                                   |
| unpickle_pure_python       | 300 us                                                 | 404 us: 1.35x slower                                                   |
| pprint_pformat             | 1.98 sec                                               | 2.68 sec: 1.35x slower                                                 |
| python_startup             | 23.7 ms                                                | 32.5 ms: 1.37x slower                                                  |
| html5lib                   | 88.9 ms                                                | 123 ms: 1.38x slower                                                   |
| thrift                     | 1.06 ms                                                | 1.46 ms: 1.38x slower                                                  |
| logging_simple             | 9.45 us                                                | 13.2 us: 1.39x slower                                                  |
| coverage                   | 95.4 ms                                                | 134 ms: 1.41x slower                                                   |
| django_template            | 44.9 ms                                                | 63.5 ms: 1.41x slower                                                  |
| richards_super             | 72.8 ms                                                | 103 ms: 1.42x slower                                                   |
| float                      | 123 ms                                                 | 175 ms: 1.43x slower                                                   |
| pickle_pure_python         | 436 us                                                 | 622 us: 1.43x slower                                                   |
| nbody                      | 119 ms                                                 | 173 ms: 1.45x slower                                                   |
| sympy_str                  | 385 ms                                                 | 559 ms: 1.45x slower                                                   |
| scimark_lu                 | 152 ms                                                 | 222 ms: 1.46x slower                                                   |
| chaos                      | 84.9 ms                                                | 125 ms: 1.47x slower                                                   |
| richards                   | 60.3 ms                                                | 90.9 ms: 1.51x slower                                                  |
| sqlalchemy_imperative      | 24.7 ms                                                | 37.3 ms: 1.51x slower                                                  |
| raytrace                   | 408 ms                                                 | 623 ms: 1.53x slower                                                   |
| scimark_monte_carlo        | 96.4 ms                                                | 147 ms: 1.53x slower                                                   |
| hexiom                     | 8.27 ms                                                | 12.8 ms: 1.55x slower                                                  |
| logging_silent             | 139 ns                                                 | 215 ns: 1.55x slower                                                   |
| logging_format             | 9.59 us                                                | 14.9 us: 1.55x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 3.12 ms: 1.61x slower                                                  |
| sqlglot_transpile          | 2.34 ms                                                | 3.83 ms: 1.64x slower                                                  |
| mako                       | 15.7 ms                                                | 26.8 ms: 1.71x slower                                                  |
| scimark_sor                | 167 ms                                                 | 285 ms: 1.71x slower                                                   |
| sqlglot_parse              | 1.79 ms                                                | 3.15 ms: 1.76x slower                                                  |
| go                         | 172 ms                                                 | 310 ms: 1.80x slower                                                   |
| sympy_expand               | 582 ms                                                 | 1.09 sec: 1.88x slower                                                 |
| sympy_sum                  | 222 ms                                                 | 429 ms: 1.93x slower                                                   |
| deltablue                  | 4.27 ms                                                | 9.46 ms: 2.22x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 92.9 ms: 4.49x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.20x slower                                                           |

Benchmark hidden because not significant (6): json_loads, pathlib, json, regex_dna, sqlite_synth, regex_v8
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241208-3.14.0a2+-a03efb5-NOGIL/bm-20241208-linux-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.156x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.14x
- 95% likely to have a slowdown of 1.12x
- 99% likely to have a slowdown of 1.10x

# Memory
- memory change: 1.34x