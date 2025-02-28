# Results vs. 3.12.6

- fork: python
- ref: 9211b3dabeacb92713ac
- machine: linux-x86_64
- commit hash: 9211b3d
- commit date: 2025-02-28
- overall geometric mean: 1.005x slower
- HPT reliability: 99.32%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 504 ms: 1.10x slower                                                   |
| html5lib       | 88.9 ms                                                | 97.3 ms: 1.09x slower                                                  |
| Geometric mean | (ref)                                                  | 1.07x slower                                                           |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 738 ms: 2.62x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 797 ms: 2.32x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 427 ms: 2.18x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 330 ms: 2.13x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 513 ms: 1.90x faster                                                   |
| async_tree_none            | 741 ms                                                 | 391 ms: 1.90x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 654 ms: 1.68x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 704 ms: 1.53x faster                                                   |
| async_generators           | 589 ms                                                 | 560 ms: 1.05x faster                                                   |
| coroutines                 | 29.5 ms                                                | 30.6 ms: 1.04x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.66x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 99.4 ms: 1.24x faster                                                  |
| nbody          | 119 ms                                                 | 182 ms: 1.53x slower                                                   |
| Geometric mean | (ref)                                                  | 1.07x slower                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.41 ms: 1.16x faster                                                  |
| regex_dna      | 278 ms                                                 | 303 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                  | 1.02x faster                                                           |

Benchmark hidden because not significant (2): regex_compile, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 169 ms                                                 | 133 ms: 1.28x faster                                                   |
| xml_etree_parse      | 241 ms                                                 | 199 ms: 1.21x faster                                                   |
| tomli_loads          | 2.88 sec                                               | 3.05 sec: 1.06x slower                                                 |
| xml_etree_process    | 83.7 ms                                                | 88.5 ms: 1.06x slower                                                  |
| xml_etree_generate   | 127 ms                                                 | 135 ms: 1.06x slower                                                   |
| json_loads           | 37.9 us                                                | 40.8 us: 1.08x slower                                                  |
| unpickle_pure_python | 300 us                                                 | 333 us: 1.11x slower                                                   |
| pickle_pure_python   | 436 us                                                 | 492 us: 1.13x slower                                                   |
| json_dumps           | 14.3 ms                                                | 17.0 ms: 1.19x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.02x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 20.3 ms: 1.15x slower                                                  |
| python_startup         | 23.7 ms                                                | 30.2 ms: 1.27x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.21x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 44.9 ms                                                | 52.4 ms: 1.17x slower                                                  |
| genshi_text     | 30.2 ms                                                | 37.0 ms: 1.23x slower                                                  |
| genshi_xml      | 67.6 ms                                                | 84.8 ms: 1.25x slower                                                  |
| mako            | 15.7 ms                                                | 22.7 ms: 1.44x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.27x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 738 ms: 2.62x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 797 ms: 2.32x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 427 ms: 2.18x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 330 ms: 2.13x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 513 ms: 1.90x faster                                                   |
| async_tree_none            | 741 ms                                                 | 391 ms: 1.90x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 654 ms: 1.68x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 704 ms: 1.53x faster                                                   |
| gc_traversal               | 5.86 ms                                                | 3.86 ms: 1.52x faster                                                  |
| xml_etree_iterparse        | 169 ms                                                 | 133 ms: 1.28x faster                                                   |
| float                      | 123 ms                                                 | 99.4 ms: 1.24x faster                                                  |
| xml_etree_parse            | 241 ms                                                 | 199 ms: 1.21x faster                                                   |
| regex_effbot               | 5.13 ms                                                | 4.41 ms: 1.16x faster                                                  |
| pycparser                  | 1.79 sec                                               | 1.55 sec: 1.16x faster                                                 |
| deepcopy                   | 468 us                                                 | 411 us: 1.14x faster                                                   |
| sqlite_synth               | 3.87 us                                                | 3.44 us: 1.12x faster                                                  |
| comprehensions             | 27.1 us                                                | 24.3 us: 1.12x faster                                                  |
| spectral_norm              | 156 ms                                                 | 142 ms: 1.10x faster                                                   |
| deepcopy_memo              | 52.4 us                                                | 49.3 us: 1.06x faster                                                  |
| async_generators           | 589 ms                                                 | 560 ms: 1.05x faster                                                   |
| coroutines                 | 29.5 ms                                                | 30.6 ms: 1.04x slower                                                  |
| pyflate                    | 727 ms                                                 | 756 ms: 1.04x slower                                                   |
| json                       | 6.85 ms                                                | 7.18 ms: 1.05x slower                                                  |
| raytrace                   | 408 ms                                                 | 428 ms: 1.05x slower                                                   |
| tomli_loads                | 2.88 sec                                               | 3.05 sec: 1.06x slower                                                 |
| xml_etree_process          | 83.7 ms                                                | 88.5 ms: 1.06x slower                                                  |
| chaos                      | 84.9 ms                                                | 89.8 ms: 1.06x slower                                                  |
| xml_etree_generate         | 127 ms                                                 | 135 ms: 1.06x slower                                                   |
| generators                 | 41.1 ms                                                | 43.9 ms: 1.07x slower                                                  |
| nqueens                    | 117 ms                                                 | 126 ms: 1.08x slower                                                   |
| json_loads                 | 37.9 us                                                | 40.8 us: 1.08x slower                                                  |
| mdp                        | 3.97 sec                                               | 4.28 sec: 1.08x slower                                                 |
| regex_dna                  | 278 ms                                                 | 303 ms: 1.09x slower                                                   |
| richards_super             | 72.8 ms                                                | 79.6 ms: 1.09x slower                                                  |
| html5lib                   | 88.9 ms                                                | 97.3 ms: 1.09x slower                                                  |
| sqlalchemy_imperative      | 24.7 ms                                                | 27.3 ms: 1.10x slower                                                  |
| pprint_safe_repr           | 967 ms                                                 | 1.07 sec: 1.10x slower                                                 |
| 2to3                       | 456 ms                                                 | 504 ms: 1.10x slower                                                   |
| sqlglot_optimize           | 76.0 ms                                                | 84.0 ms: 1.11x slower                                                  |
| deepcopy_reduce            | 4.04 us                                                | 4.46 us: 1.11x slower                                                  |
| sympy_str                  | 385 ms                                                 | 427 ms: 1.11x slower                                                   |
| crypto_pyaes               | 107 ms                                                 | 119 ms: 1.11x slower                                                   |
| unpickle_pure_python       | 300 us                                                 | 333 us: 1.11x slower                                                   |
| pprint_pformat             | 1.98 sec                                               | 2.20 sec: 1.11x slower                                                 |
| sqlglot_transpile          | 2.34 ms                                                | 2.61 ms: 1.12x slower                                                  |
| thrift                     | 1.06 ms                                                | 1.19 ms: 1.12x slower                                                  |
| sympy_integrate            | 29.8 ms                                                | 33.4 ms: 1.12x slower                                                  |
| bpe_tokeniser              | 6.59 sec                                               | 7.41 sec: 1.13x slower                                                 |
| pickle_pure_python         | 436 us                                                 | 492 us: 1.13x slower                                                   |
| scimark_sor                | 167 ms                                                 | 190 ms: 1.14x slower                                                   |
| sympy_sum                  | 222 ms                                                 | 254 ms: 1.15x slower                                                   |
| richards                   | 60.3 ms                                                | 69.5 ms: 1.15x slower                                                  |
| python_startup_no_site     | 17.6 ms                                                | 20.3 ms: 1.15x slower                                                  |
| django_template            | 44.9 ms                                                | 52.4 ms: 1.17x slower                                                  |
| sympy_expand               | 582 ms                                                 | 681 ms: 1.17x slower                                                   |
| logging_format             | 9.59 us                                                | 11.3 us: 1.18x slower                                                  |
| typing_runtime_protocols   | 224 us                                                 | 266 us: 1.19x slower                                                   |
| json_dumps                 | 14.3 ms                                                | 17.0 ms: 1.19x slower                                                  |
| meteor_contest             | 146 ms                                                 | 174 ms: 1.19x slower                                                   |
| hexiom                     | 8.27 ms                                                | 9.90 ms: 1.20x slower                                                  |
| fannkuch                   | 540 ms                                                 | 648 ms: 1.20x slower                                                   |
| deltablue                  | 4.27 ms                                                | 5.17 ms: 1.21x slower                                                  |
| telco                      | 9.59 ms                                                | 11.7 ms: 1.22x slower                                                  |
| genshi_text                | 30.2 ms                                                | 37.0 ms: 1.23x slower                                                  |
| sqlglot_parse              | 1.79 ms                                                | 2.20 ms: 1.23x slower                                                  |
| genshi_xml                 | 67.6 ms                                                | 84.8 ms: 1.25x slower                                                  |
| bench_thread_pool          | 3.48 ms                                                | 4.38 ms: 1.26x slower                                                  |
| python_startup             | 23.7 ms                                                | 30.2 ms: 1.27x slower                                                  |
| scimark_fft                | 500 ms                                                 | 653 ms: 1.31x slower                                                   |
| create_gc_cycles           | 1.94 ms                                                | 2.54 ms: 1.31x slower                                                  |
| scimark_lu                 | 152 ms                                                 | 201 ms: 1.32x slower                                                   |
| scimark_monte_carlo        | 96.4 ms                                                | 130 ms: 1.35x slower                                                   |
| mako                       | 15.7 ms                                                | 22.7 ms: 1.44x slower                                                  |
| coverage                   | 95.4 ms                                                | 139 ms: 1.46x slower                                                   |
| nbody                      | 119 ms                                                 | 182 ms: 1.53x slower                                                   |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 10.5 ms: 1.56x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 88.2 ms: 4.26x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.03x slower                                                           |

Benchmark hidden because not significant (13): sqlglot_normalize, sqlalchemy_declarative, pylint, pidigits, asyncio_websockets, regex_compile, regex_v8, docutils, pathlib, go, logging_silent, dulwich_log, logging_simple
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250228-3.14.0a5+-9211b3d-NOGIL/bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.005x slower

# HPT report

- Reliability score: 99.32% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.35x