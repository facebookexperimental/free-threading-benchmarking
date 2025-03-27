# Results vs. 3.13.0rc2

- fork: python
- ref: 151d1bfd1bb7ca9a36bb
- machine: linux-x86_64
- commit hash: 151d1bf
- commit date: 2025-03-26
- overall geometric mean: 1.123x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.09x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250326-vultr-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 314 ms: 1.21x slower                                                   |
| docutils       | 2.63 sec                                                               | 2.87 sec: 1.09x slower                                                 |
| html5lib       | 68.6 ms                                                                | 75.6 ms: 1.10x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.13x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250326-vultr-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 576 ms: 1.57x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 604 ms: 1.46x faster                                                   |
| async_tree_memoization     | 459 ms                                                                 | 343 ms: 1.34x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 250 ms: 1.33x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 314 ms: 1.31x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 284 ms: 1.24x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 517 ms: 1.23x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 547 ms: 1.22x faster                                                   |
| async_generators           | 375 ms                                                                 | 399 ms: 1.07x slower                                                   |
| coroutines                 | 23.3 ms                                                                | 25.7 ms: 1.10x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.21x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250326-vultr-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 208 ms: 1.04x faster                                                   |
| float          | 76.7 ms                                                                | 81.2 ms: 1.06x slower                                                  |
| nbody          | 85.3 ms                                                                | 153 ms: 1.79x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.22x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250326-vultr-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.76 ms: 1.16x faster                                                  |
| regex_v8       | 23.2 ms                                                                | 21.0 ms: 1.11x faster                                                  |
| regex_dna      | 189 ms                                                                 | 171 ms: 1.10x faster                                                   |
| regex_compile  | 131 ms                                                                 | 170 ms: 1.29x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250326-vultr-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                                 | 130 ms: 1.04x faster                                                   |
| xml_etree_iterparse  | 94.4 ms                                                                | 92.5 ms: 1.02x faster                                                  |
| json_loads           | 27.3 us                                                                | 29.5 us: 1.08x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                                | 101 ms: 1.18x slower                                                   |
| xml_etree_process    | 59.2 ms                                                                | 73.6 ms: 1.24x slower                                                  |
| json_dumps           | 10.6 ms                                                                | 13.3 ms: 1.25x slower                                                  |
| tomli_loads          | 2.01 sec                                                               | 2.54 sec: 1.26x slower                                                 |
| pickle_pure_python   | 292 us                                                                 | 388 us: 1.33x slower                                                   |
| unpickle_pure_python | 208 us                                                                 | 277 us: 1.33x slower                                                   |
| Geometric mean       | (ref)                                                                  | 1.17x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250326-vultr-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 15.8 ms: 1.44x slower                                                  |
| python_startup_no_site | 7.41 ms                                                                | 11.2 ms: 1.50x slower                                                  |
| Geometric mean         | (ref)                                                                  | 1.47x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250326-vultr-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 34.2 ms                                                                | 44.7 ms: 1.31x slower                                                  |
| genshi_xml      | 49.1 ms                                                                | 66.2 ms: 1.35x slower                                                  |
| genshi_text     | 21.7 ms                                                                | 30.7 ms: 1.41x slower                                                  |
| mako            | 11.2 ms                                                                | 16.5 ms: 1.47x slower                                                  |
| Geometric mean  | (ref)                                                                  | 1.38x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250326-vultr-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.80 ms: 1.84x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 576 ms: 1.57x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 604 ms: 1.46x faster                                                   |
| async_tree_memoization     | 459 ms                                                                 | 343 ms: 1.34x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 250 ms: 1.33x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 314 ms: 1.31x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 284 ms: 1.24x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 517 ms: 1.23x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 547 ms: 1.22x faster                                                   |
| regex_effbot               | 3.21 ms                                                                | 2.76 ms: 1.16x faster                                                  |
| regex_v8                   | 23.2 ms                                                                | 21.0 ms: 1.11x faster                                                  |
| regex_dna                  | 189 ms                                                                 | 171 ms: 1.10x faster                                                   |
| sqlite_synth               | 2.25 us                                                                | 2.08 us: 1.08x faster                                                  |
| deepcopy                   | 357 us                                                                 | 334 us: 1.07x faster                                                   |
| xml_etree_parse            | 136 ms                                                                 | 130 ms: 1.04x faster                                                   |
| pidigits                   | 216 ms                                                                 | 208 ms: 1.04x faster                                                   |
| xml_etree_iterparse        | 94.4 ms                                                                | 92.5 ms: 1.02x faster                                                  |
| create_gc_cycles           | 1.33 ms                                                                | 1.35 ms: 1.02x slower                                                  |
| pathlib                    | 19.3 ms                                                                | 19.9 ms: 1.03x slower                                                  |
| json                       | 4.98 ms                                                                | 5.16 ms: 1.04x slower                                                  |
| dulwich_log                | 74.5 ms                                                                | 77.4 ms: 1.04x slower                                                  |
| float                      | 76.7 ms                                                                | 81.2 ms: 1.06x slower                                                  |
| async_generators           | 375 ms                                                                 | 399 ms: 1.07x slower                                                   |
| json_loads                 | 27.3 us                                                                | 29.5 us: 1.08x slower                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 3.37 us: 1.08x slower                                                  |
| docutils                   | 2.63 sec                                                               | 2.87 sec: 1.09x slower                                                 |
| html5lib                   | 68.6 ms                                                                | 75.6 ms: 1.10x slower                                                  |
| coroutines                 | 23.3 ms                                                                | 25.7 ms: 1.10x slower                                                  |
| deepcopy_memo              | 38.1 us                                                                | 42.3 us: 1.11x slower                                                  |
| pycparser                  | 1.12 sec                                                               | 1.24 sec: 1.11x slower                                                 |
| bpe_tokeniser              | 4.46 sec                                                               | 5.05 sec: 1.13x slower                                                 |
| go                         | 141 ms                                                                 | 160 ms: 1.14x slower                                                   |
| spectral_norm              | 108 ms                                                                 | 123 ms: 1.15x slower                                                   |
| mdp                        | 2.34 sec                                                               | 2.70 sec: 1.16x slower                                                 |
| thrift                     | 772 us                                                                 | 908 us: 1.18x slower                                                   |
| telco                      | 7.77 ms                                                                | 9.19 ms: 1.18x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                                | 101 ms: 1.18x slower                                                   |
| scimark_fft                | 348 ms                                                                 | 415 ms: 1.19x slower                                                   |
| 2to3                       | 259 ms                                                                 | 314 ms: 1.21x slower                                                   |
| pyflate                    | 449 ms                                                                 | 543 ms: 1.21x slower                                                   |
| scimark_sor                | 134 ms                                                                 | 164 ms: 1.23x slower                                                   |
| pprint_safe_repr           | 719 ms                                                                 | 887 ms: 1.23x slower                                                   |
| xml_etree_process          | 59.2 ms                                                                | 73.6 ms: 1.24x slower                                                  |
| sympy_integrate            | 19.7 ms                                                                | 24.6 ms: 1.25x slower                                                  |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.94 ms: 1.25x slower                                                  |
| json_dumps                 | 10.6 ms                                                                | 13.3 ms: 1.25x slower                                                  |
| sympy_sum                  | 154 ms                                                                 | 194 ms: 1.26x slower                                                   |
| pprint_pformat             | 1.46 sec                                                               | 1.83 sec: 1.26x slower                                                 |
| tomli_loads                | 2.01 sec                                                               | 2.54 sec: 1.26x slower                                                 |
| sympy_expand               | 454 ms                                                                 | 582 ms: 1.28x slower                                                   |
| logging_silent             | 98.2 ns                                                                | 126 ns: 1.28x slower                                                   |
| sympy_str                  | 274 ms                                                                 | 352 ms: 1.28x slower                                                   |
| regex_compile              | 131 ms                                                                 | 170 ms: 1.29x slower                                                   |
| nqueens                    | 77.7 ms                                                                | 101 ms: 1.30x slower                                                   |
| scimark_lu                 | 112 ms                                                                 | 147 ms: 1.31x slower                                                   |
| django_template            | 34.2 ms                                                                | 44.7 ms: 1.31x slower                                                  |
| coverage                   | 82.5 ms                                                                | 109 ms: 1.32x slower                                                   |
| typing_runtime_protocols   | 156 us                                                                 | 206 us: 1.33x slower                                                   |
| pickle_pure_python         | 292 us                                                                 | 388 us: 1.33x slower                                                   |
| unpickle_pure_python       | 208 us                                                                 | 277 us: 1.33x slower                                                   |
| logging_simple             | 6.14 us                                                                | 8.28 us: 1.35x slower                                                  |
| chaos                      | 56.3 ms                                                                | 75.9 ms: 1.35x slower                                                  |
| genshi_xml                 | 49.1 ms                                                                | 66.2 ms: 1.35x slower                                                  |
| generators                 | 28.5 ms                                                                | 38.7 ms: 1.36x slower                                                  |
| logging_format             | 6.92 us                                                                | 9.38 us: 1.36x slower                                                  |
| comprehensions             | 16.6 us                                                                | 22.7 us: 1.37x slower                                                  |
| meteor_contest             | 101 ms                                                                 | 139 ms: 1.37x slower                                                   |
| richards_super             | 50.4 ms                                                                | 69.2 ms: 1.37x slower                                                  |
| richards                   | 44.4 ms                                                                | 61.0 ms: 1.37x slower                                                  |
| crypto_pyaes               | 68.2 ms                                                                | 94.0 ms: 1.38x slower                                                  |
| hexiom                     | 5.95 ms                                                                | 8.21 ms: 1.38x slower                                                  |
| scimark_monte_carlo        | 65.8 ms                                                                | 91.4 ms: 1.39x slower                                                  |
| raytrace                   | 250 ms                                                                 | 352 ms: 1.41x slower                                                   |
| genshi_text                | 21.7 ms                                                                | 30.7 ms: 1.41x slower                                                  |
| fannkuch                   | 376 ms                                                                 | 533 ms: 1.42x slower                                                   |
| python_startup             | 11.0 ms                                                                | 15.8 ms: 1.44x slower                                                  |
| mako                       | 11.2 ms                                                                | 16.5 ms: 1.47x slower                                                  |
| deltablue                  | 3.10 ms                                                                | 4.58 ms: 1.48x slower                                                  |
| python_startup_no_site     | 7.41 ms                                                                | 11.2 ms: 1.50x slower                                                  |
| nbody                      | 85.3 ms                                                                | 153 ms: 1.79x slower                                                   |
| bench_thread_pool          | 924 us                                                                 | 3.19 ms: 3.45x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                                | 98.1 ms: 8.92x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.19x slower                                                           |

Benchmark hidden because not significant (2): asyncio_websockets, pylint
Ignored benchmarks (18) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250326-3.14.0a6+-151d1bf-NOGIL/bm-20250326-vultr-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.123x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.13x
- 95% likely to have a slowdown of 1.12x
- 99% likely to have a slowdown of 1.09x

# Memory
- memory change: 1.35x