# Results vs. 3.12.6

- fork: python
- ref: 151d1bfd1bb7ca9a36bb
- machine: linux-x86_64
- commit hash: 151d1bf
- commit date: 2025-03-26
- overall geometric mean: 1.007x slower
- HPT reliability: 98.76%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.38x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 530 ms: 1.16x slower                                                   |
| html5lib       | 88.9 ms                                                | 103 ms: 1.15x slower                                                   |
| Geometric mean | (ref)                                                  | 1.10x slower                                                           |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 734 ms: 2.64x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 830 ms: 2.23x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 445 ms: 2.09x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 349 ms: 2.02x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 487 ms: 2.01x faster                                                   |
| async_tree_none            | 741 ms                                                 | 389 ms: 1.91x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 646 ms: 1.70x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 730 ms: 1.48x faster                                                   |
| async_generators           | 589 ms                                                 | 563 ms: 1.05x faster                                                   |
| coroutines                 | 29.5 ms                                                | 31.7 ms: 1.08x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.64x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 103 ms: 1.20x faster                                                   |
| pidigits       | 250 ms                                                 | 239 ms: 1.05x faster                                                   |
| nbody          | 119 ms                                                 | 181 ms: 1.52x slower                                                   |
| Geometric mean | (ref)                                                  | 1.07x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.38 ms: 1.17x faster                                                  |
| regex_v8       | 32.5 ms                                                | 29.8 ms: 1.09x faster                                                  |
| regex_dna      | 278 ms                                                 | 287 ms: 1.03x slower                                                   |
| regex_compile  | 187 ms                                                 | 205 ms: 1.10x slower                                                   |
| Geometric mean | (ref)                                                  | 1.03x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|---------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse | 169 ms                                                 | 143 ms: 1.18x faster                                                   |
| xml_etree_parse     | 241 ms                                                 | 219 ms: 1.10x faster                                                   |
| pickle_pure_python  | 436 us                                                 | 458 us: 1.05x slower                                                   |
| tomli_loads         | 2.88 sec                                               | 3.04 sec: 1.05x slower                                                 |
| xml_etree_process   | 83.7 ms                                                | 96.0 ms: 1.15x slower                                                  |
| json_loads          | 37.9 us                                                | 44.5 us: 1.17x slower                                                  |
| json_dumps          | 14.3 ms                                                | 17.4 ms: 1.22x slower                                                  |
| Geometric mean      | (ref)                                                  | 1.04x slower                                                           |

Benchmark hidden because not significant (2): xml_etree_generate, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 23.8 ms: 1.35x slower                                                  |
| python_startup         | 23.7 ms                                                | 32.3 ms: 1.36x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.36x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 44.9 ms                                                | 55.6 ms: 1.24x slower                                                  |
| genshi_xml      | 67.6 ms                                                | 84.4 ms: 1.25x slower                                                  |
| genshi_text     | 30.2 ms                                                | 41.9 ms: 1.39x slower                                                  |
| mako            | 15.7 ms                                                | 22.0 ms: 1.40x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.31x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 734 ms: 2.64x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 830 ms: 2.23x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 445 ms: 2.09x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 349 ms: 2.02x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 487 ms: 2.01x faster                                                   |
| async_tree_none            | 741 ms                                                 | 389 ms: 1.91x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 646 ms: 1.70x faster                                                   |
| gc_traversal               | 5.86 ms                                                | 3.64 ms: 1.61x faster                                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 730 ms: 1.48x faster                                                   |
| float                      | 123 ms                                                 | 103 ms: 1.20x faster                                                   |
| xml_etree_iterparse        | 169 ms                                                 | 143 ms: 1.18x faster                                                   |
| regex_effbot               | 5.13 ms                                                | 4.38 ms: 1.17x faster                                                  |
| pycparser                  | 1.79 sec                                               | 1.55 sec: 1.16x faster                                                 |
| dulwich_log                | 100 ms                                                 | 87.7 ms: 1.14x faster                                                  |
| xml_etree_parse            | 241 ms                                                 | 219 ms: 1.10x faster                                                   |
| deepcopy                   | 468 us                                                 | 427 us: 1.10x faster                                                   |
| regex_v8                   | 32.5 ms                                                | 29.8 ms: 1.09x faster                                                  |
| sqlite_synth               | 3.87 us                                                | 3.61 us: 1.07x faster                                                  |
| spectral_norm              | 156 ms                                                 | 146 ms: 1.07x faster                                                   |
| async_generators           | 589 ms                                                 | 563 ms: 1.05x faster                                                   |
| comprehensions             | 27.1 us                                                | 25.9 us: 1.05x faster                                                  |
| pidigits                   | 250 ms                                                 | 239 ms: 1.05x faster                                                   |
| regex_dna                  | 278 ms                                                 | 287 ms: 1.03x slower                                                   |
| mdp                        | 3.97 sec                                               | 4.16 sec: 1.05x slower                                                 |
| raytrace                   | 408 ms                                                 | 428 ms: 1.05x slower                                                   |
| pickle_pure_python         | 436 us                                                 | 458 us: 1.05x slower                                                   |
| tomli_loads                | 2.88 sec                                               | 3.04 sec: 1.05x slower                                                 |
| scimark_fft                | 500 ms                                                 | 537 ms: 1.07x slower                                                   |
| coroutines                 | 29.5 ms                                                | 31.7 ms: 1.08x slower                                                  |
| sympy_str                  | 385 ms                                                 | 415 ms: 1.08x slower                                                   |
| json                       | 6.85 ms                                                | 7.39 ms: 1.08x slower                                                  |
| logging_simple             | 9.45 us                                                | 10.3 us: 1.09x slower                                                  |
| nqueens                    | 117 ms                                                 | 128 ms: 1.10x slower                                                   |
| regex_compile              | 187 ms                                                 | 205 ms: 1.10x slower                                                   |
| go                         | 172 ms                                                 | 189 ms: 1.10x slower                                                   |
| logging_format             | 9.59 us                                                | 10.6 us: 1.10x slower                                                  |
| chaos                      | 84.9 ms                                                | 94.2 ms: 1.11x slower                                                  |
| sympy_sum                  | 222 ms                                                 | 247 ms: 1.11x slower                                                   |
| pprint_pformat             | 1.98 sec                                               | 2.22 sec: 1.12x slower                                                 |
| logging_silent             | 139 ns                                                 | 157 ns: 1.12x slower                                                   |
| pprint_safe_repr           | 967 ms                                                 | 1.09 sec: 1.12x slower                                                 |
| bpe_tokeniser              | 6.59 sec                                               | 7.42 sec: 1.13x slower                                                 |
| sympy_integrate            | 29.8 ms                                                | 33.8 ms: 1.14x slower                                                  |
| scimark_sor                | 167 ms                                                 | 190 ms: 1.14x slower                                                   |
| generators                 | 41.1 ms                                                | 47.0 ms: 1.14x slower                                                  |
| bench_thread_pool          | 3.48 ms                                                | 3.98 ms: 1.14x slower                                                  |
| xml_etree_process          | 83.7 ms                                                | 96.0 ms: 1.15x slower                                                  |
| richards                   | 60.3 ms                                                | 69.3 ms: 1.15x slower                                                  |
| html5lib                   | 88.9 ms                                                | 103 ms: 1.15x slower                                                   |
| richards_super             | 72.8 ms                                                | 84.1 ms: 1.15x slower                                                  |
| crypto_pyaes               | 107 ms                                                 | 124 ms: 1.16x slower                                                   |
| 2to3                       | 456 ms                                                 | 530 ms: 1.16x slower                                                   |
| thrift                     | 1.06 ms                                                | 1.23 ms: 1.16x slower                                                  |
| json_loads                 | 37.9 us                                                | 44.5 us: 1.17x slower                                                  |
| scimark_lu                 | 152 ms                                                 | 179 ms: 1.18x slower                                                   |
| fannkuch                   | 540 ms                                                 | 640 ms: 1.19x slower                                                   |
| sympy_expand               | 582 ms                                                 | 702 ms: 1.21x slower                                                   |
| json_dumps                 | 14.3 ms                                                | 17.4 ms: 1.22x slower                                                  |
| typing_runtime_protocols   | 224 us                                                 | 273 us: 1.22x slower                                                   |
| scimark_monte_carlo        | 96.4 ms                                                | 118 ms: 1.22x slower                                                   |
| hexiom                     | 8.27 ms                                                | 10.1 ms: 1.22x slower                                                  |
| sqlalchemy_imperative      | 24.7 ms                                                | 30.4 ms: 1.23x slower                                                  |
| meteor_contest             | 146 ms                                                 | 181 ms: 1.24x slower                                                   |
| django_template            | 44.9 ms                                                | 55.6 ms: 1.24x slower                                                  |
| deltablue                  | 4.27 ms                                                | 5.33 ms: 1.25x slower                                                  |
| genshi_xml                 | 67.6 ms                                                | 84.4 ms: 1.25x slower                                                  |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 8.44 ms: 1.26x slower                                                  |
| telco                      | 9.59 ms                                                | 12.1 ms: 1.27x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 2.62 ms: 1.35x slower                                                  |
| python_startup_no_site     | 17.6 ms                                                | 23.8 ms: 1.35x slower                                                  |
| python_startup             | 23.7 ms                                                | 32.3 ms: 1.36x slower                                                  |
| genshi_text                | 30.2 ms                                                | 41.9 ms: 1.39x slower                                                  |
| mako                       | 15.7 ms                                                | 22.0 ms: 1.40x slower                                                  |
| nbody                      | 119 ms                                                 | 181 ms: 1.52x slower                                                   |
| coverage                   | 95.4 ms                                                | 160 ms: 1.67x slower                                                   |
| bench_mp_pool              | 20.7 ms                                                | 93.3 ms: 4.51x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.04x slower                                                           |

Benchmark hidden because not significant (10): pylint, asyncio_websockets, deepcopy_reduce, docutils, sqlalchemy_declarative, deepcopy_memo, pathlib, pyflate, xml_etree_generate, unpickle_pure_python
Ignored benchmarks (19) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250326-3.14.0a6+-151d1bf-NOGIL/bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.007x slower

# HPT report

- Reliability score: 98.76% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.38x