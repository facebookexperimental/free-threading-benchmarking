# Results vs. 3.13.0rc2

- fork: python
- ref: 1b7470f8cbff4bb9e58e
- machine: linux-x86_64
- commit hash: 1b7470f
- commit date: 2025-04-28
- overall geometric mean: 1.007x slower
- HPT reliability: 85.78%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250428-vultr-x86_64-python-1b7470f8cbff4bb9e58e-3.14.0a7+-1b7470f |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 281 ms: 1.08x slower                                                   |
| docutils       | 2.63 sec                                                               | 2.72 sec: 1.04x slower                                                 |
| html5lib       | 68.6 ms                                                                | 65.6 ms: 1.05x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250428-vultr-x86_64-python-1b7470f8cbff4bb9e58e-3.14.0a7+-1b7470f |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 523 ms: 1.72x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 551 ms: 1.60x faster                                                   |
| async_tree_memoization     | 459 ms                                                                 | 310 ms: 1.48x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 228 ms: 1.46x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 284 ms: 1.44x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 258 ms: 1.37x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 482 ms: 1.31x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 508 ms: 1.31x faster                                                   |
| async_generators           | 375 ms                                                                 | 362 ms: 1.04x faster                                                   |
| coroutines                 | 23.3 ms                                                                | 22.9 ms: 1.02x faster                                                  |
| asyncio_websockets         | 517 ms                                                                 | 515 ms: 1.00x faster                                                   |
| Geometric mean             | (ref)                                                                  | 1.32x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250428-vultr-x86_64-python-1b7470f8cbff4bb9e58e-3.14.0a7+-1b7470f |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 190 ms: 1.14x faster                                                   |
| float          | 76.7 ms                                                                | 67.3 ms: 1.14x faster                                                  |
| nbody          | 85.3 ms                                                                | 108 ms: 1.27x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250428-vultr-x86_64-python-1b7470f8cbff4bb9e58e-3.14.0a7+-1b7470f |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.81 ms: 1.14x faster                                                  |
| regex_v8       | 23.2 ms                                                                | 20.7 ms: 1.12x faster                                                  |
| regex_dna      | 189 ms                                                                 | 179 ms: 1.06x faster                                                   |
| regex_compile  | 131 ms                                                                 | 144 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250428-vultr-x86_64-python-1b7470f8cbff4bb9e58e-3.14.0a7+-1b7470f |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 86.7 ms: 1.09x faster                                                  |
| xml_etree_parse      | 136 ms                                                                 | 129 ms: 1.05x faster                                                   |
| tomli_loads          | 2.01 sec                                                               | 2.10 sec: 1.04x slower                                                 |
| xml_etree_generate   | 85.4 ms                                                                | 93.1 ms: 1.09x slower                                                  |
| unpickle_pure_python | 208 us                                                                 | 228 us: 1.09x slower                                                   |
| json_loads           | 27.3 us                                                                | 30.2 us: 1.11x slower                                                  |
| pickle_pure_python   | 292 us                                                                 | 327 us: 1.12x slower                                                   |
| xml_etree_process    | 59.2 ms                                                                | 66.5 ms: 1.12x slower                                                  |
| json_dumps           | 10.6 ms                                                                | 12.8 ms: 1.21x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.07x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250428-vultr-x86_64-python-1b7470f8cbff4bb9e58e-3.14.0a7+-1b7470f |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 15.9 ms: 1.44x slower                                                  |
| python_startup_no_site | 7.41 ms                                                                | 11.2 ms: 1.51x slower                                                  |
| Geometric mean         | (ref)                                                                  | 1.47x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250428-vultr-x86_64-python-1b7470f8cbff4bb9e58e-3.14.0a7+-1b7470f |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 55.9 ms: 1.14x slower                                                  |
| django_template | 34.2 ms                                                                | 40.1 ms: 1.17x slower                                                  |
| genshi_text     | 21.7 ms                                                                | 25.8 ms: 1.19x slower                                                  |
| mako            | 11.2 ms                                                                | 15.3 ms: 1.36x slower                                                  |
| Geometric mean  | (ref)                                                                  | 1.21x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250428-vultr-x86_64-python-1b7470f8cbff4bb9e58e-3.14.0a7+-1b7470f |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.80 ms: 1.85x faster                                                  |
| mdp                        | 2.34 sec                                                               | 1.32 sec: 1.78x faster                                                 |
| async_tree_io_tg           | 901 ms                                                                 | 523 ms: 1.72x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 551 ms: 1.60x faster                                                   |
| async_tree_memoization     | 459 ms                                                                 | 310 ms: 1.48x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 228 ms: 1.46x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 284 ms: 1.44x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 258 ms: 1.37x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 482 ms: 1.31x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 508 ms: 1.31x faster                                                   |
| deepcopy                   | 357 us                                                                 | 290 us: 1.23x faster                                                   |
| pidigits                   | 216 ms                                                                 | 190 ms: 1.14x faster                                                   |
| float                      | 76.7 ms                                                                | 67.3 ms: 1.14x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.81 ms: 1.14x faster                                                  |
| go                         | 141 ms                                                                 | 124 ms: 1.13x faster                                                   |
| scimark_sor                | 134 ms                                                                 | 119 ms: 1.13x faster                                                   |
| regex_v8                   | 23.2 ms                                                                | 20.7 ms: 1.12x faster                                                  |
| sqlite_synth               | 2.25 us                                                                | 2.03 us: 1.11x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 34.8 us: 1.10x faster                                                  |
| xml_etree_iterparse        | 94.4 ms                                                                | 86.7 ms: 1.09x faster                                                  |
| regex_dna                  | 189 ms                                                                 | 179 ms: 1.06x faster                                                   |
| xml_etree_parse            | 136 ms                                                                 | 129 ms: 1.05x faster                                                   |
| spectral_norm              | 108 ms                                                                 | 102 ms: 1.05x faster                                                   |
| html5lib                   | 68.6 ms                                                                | 65.6 ms: 1.05x faster                                                  |
| dulwich_log                | 74.5 ms                                                                | 71.5 ms: 1.04x faster                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 3.00 us: 1.04x faster                                                  |
| async_generators           | 375 ms                                                                 | 362 ms: 1.04x faster                                                   |
| bpe_tokeniser              | 4.46 sec                                                               | 4.36 sec: 1.02x faster                                                 |
| scimark_fft                | 348 ms                                                                 | 341 ms: 1.02x faster                                                   |
| coroutines                 | 23.3 ms                                                                | 22.9 ms: 1.02x faster                                                  |
| asyncio_websockets         | 517 ms                                                                 | 515 ms: 1.00x faster                                                   |
| pathlib                    | 19.3 ms                                                                | 19.3 ms: 1.00x slower                                                  |
| json                       | 4.98 ms                                                                | 5.05 ms: 1.01x slower                                                  |
| create_gc_cycles           | 1.33 ms                                                                | 1.37 ms: 1.03x slower                                                  |
| pyflate                    | 449 ms                                                                 | 462 ms: 1.03x slower                                                   |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.90 ms: 1.03x slower                                                  |
| docutils                   | 2.63 sec                                                               | 2.72 sec: 1.04x slower                                                 |
| pycparser                  | 1.12 sec                                                               | 1.17 sec: 1.04x slower                                                 |
| tomli_loads                | 2.01 sec                                                               | 2.10 sec: 1.04x slower                                                 |
| logging_silent             | 98.2 ns                                                                | 104 ns: 1.06x slower                                                   |
| pprint_safe_repr           | 719 ms                                                                 | 775 ms: 1.08x slower                                                   |
| telco                      | 7.77 ms                                                                | 8.39 ms: 1.08x slower                                                  |
| chaos                      | 56.3 ms                                                                | 60.9 ms: 1.08x slower                                                  |
| 2to3                       | 259 ms                                                                 | 281 ms: 1.08x slower                                                   |
| pprint_pformat             | 1.46 sec                                                               | 1.58 sec: 1.09x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                                | 93.1 ms: 1.09x slower                                                  |
| regex_compile              | 131 ms                                                                 | 144 ms: 1.09x slower                                                   |
| unpickle_pure_python       | 208 us                                                                 | 228 us: 1.09x slower                                                   |
| nqueens                    | 77.7 ms                                                                | 85.8 ms: 1.10x slower                                                  |
| json_loads                 | 27.3 us                                                                | 30.2 us: 1.11x slower                                                  |
| generators                 | 28.5 ms                                                                | 31.6 ms: 1.11x slower                                                  |
| scimark_monte_carlo        | 65.8 ms                                                                | 73.2 ms: 1.11x slower                                                  |
| sympy_integrate            | 19.7 ms                                                                | 22.0 ms: 1.11x slower                                                  |
| pickle_pure_python         | 292 us                                                                 | 327 us: 1.12x slower                                                   |
| xml_etree_process          | 59.2 ms                                                                | 66.5 ms: 1.12x slower                                                  |
| hexiom                     | 5.95 ms                                                                | 6.71 ms: 1.13x slower                                                  |
| richards                   | 44.4 ms                                                                | 50.4 ms: 1.13x slower                                                  |
| logging_simple             | 6.14 us                                                                | 6.97 us: 1.13x slower                                                  |
| genshi_xml                 | 49.1 ms                                                                | 55.9 ms: 1.14x slower                                                  |
| sympy_str                  | 274 ms                                                                 | 312 ms: 1.14x slower                                                   |
| logging_format             | 6.92 us                                                                | 7.89 us: 1.14x slower                                                  |
| scimark_lu                 | 112 ms                                                                 | 128 ms: 1.14x slower                                                   |
| deltablue                  | 3.10 ms                                                                | 3.54 ms: 1.14x slower                                                  |
| sympy_sum                  | 154 ms                                                                 | 177 ms: 1.15x slower                                                   |
| richards_super             | 50.4 ms                                                                | 58.0 ms: 1.15x slower                                                  |
| sympy_expand               | 454 ms                                                                 | 525 ms: 1.16x slower                                                   |
| raytrace                   | 250 ms                                                                 | 290 ms: 1.16x slower                                                   |
| comprehensions             | 16.6 us                                                                | 19.3 us: 1.17x slower                                                  |
| django_template            | 34.2 ms                                                                | 40.1 ms: 1.17x slower                                                  |
| genshi_text                | 21.7 ms                                                                | 25.8 ms: 1.19x slower                                                  |
| json_dumps                 | 10.6 ms                                                                | 12.8 ms: 1.21x slower                                                  |
| fannkuch                   | 376 ms                                                                 | 455 ms: 1.21x slower                                                   |
| typing_runtime_protocols   | 156 us                                                                 | 189 us: 1.22x slower                                                   |
| crypto_pyaes               | 68.2 ms                                                                | 83.3 ms: 1.22x slower                                                  |
| meteor_contest             | 101 ms                                                                 | 128 ms: 1.26x slower                                                   |
| nbody                      | 85.3 ms                                                                | 108 ms: 1.27x slower                                                   |
| coverage                   | 82.5 ms                                                                | 109 ms: 1.32x slower                                                   |
| mako                       | 11.2 ms                                                                | 15.3 ms: 1.36x slower                                                  |
| python_startup             | 11.0 ms                                                                | 15.9 ms: 1.44x slower                                                  |
| python_startup_no_site     | 7.41 ms                                                                | 11.2 ms: 1.51x slower                                                  |
| bench_thread_pool          | 924 us                                                                 | 3.12 ms: 3.38x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                                | 96.2 ms: 8.75x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.05x slower                                                           |

Benchmark hidden because not significant (1): pylint
Ignored benchmarks (19) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250428-3.14.0a7+-1b7470f-NOGIL/bm-20250428-vultr-x86_64-python-1b7470f8cbff4bb9e58e-3.14.0a7+-1b7470f.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.007x slower

# HPT report

- Reliability score: 85.78% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.36x