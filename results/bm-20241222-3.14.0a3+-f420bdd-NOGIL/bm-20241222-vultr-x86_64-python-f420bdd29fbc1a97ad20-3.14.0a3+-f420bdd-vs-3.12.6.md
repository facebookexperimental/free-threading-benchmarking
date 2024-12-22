# Results vs. 3.12.6

- fork: python
- ref: f420bdd29fbc1a97ad20
- machine: linux-x86_64
- commit hash: f420bdd
- commit date: 2024-12-22
- overall geometric mean: 1.187x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.14x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241222-vultr-x86_64-python-f420bdd29fbc1a97ad20-3.14.0a3+-f420bdd |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 360 ms: 1.37x slower                                                   |
| docutils       | 2.64 sec                                               | 3.03 sec: 1.15x slower                                                 |
| html5lib       | 63.6 ms                                                | 94.6 ms: 1.49x slower                                                  |
| Geometric mean | (ref)                                                  | 1.33x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241222-vultr-x86_64-python-f420bdd29fbc1a97ad20-3.14.0a3+-f420bdd |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 734 ms: 1.51x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 754 ms: 1.44x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 317 ms: 1.41x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 401 ms: 1.39x faster                                                   |
| async_tree_none            | 464 ms                                                 | 350 ms: 1.33x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 426 ms: 1.30x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 569 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 593 ms: 1.21x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 522 ms: 1.01x slower                                                   |
| coroutines                 | 23.9 ms                                                | 24.4 ms: 1.02x slower                                                  |
| async_generators           | 384 ms                                                 | 450 ms: 1.17x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.23x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241222-vultr-x86_64-python-f420bdd29fbc1a97ad20-3.14.0a3+-f420bdd |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 184 ms: 1.00x faster                                                   |
| float          | 80.8 ms                                                | 113 ms: 1.40x slower                                                   |
| nbody          | 89.3 ms                                                | 128 ms: 1.44x slower                                                   |
| Geometric mean | (ref)                                                  | 1.26x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241222-vultr-x86_64-python-f420bdd29fbc1a97ad20-3.14.0a3+-f420bdd |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.76 ms: 1.15x faster                                                  |
| regex_dna      | 168 ms                                                 | 186 ms: 1.11x slower                                                   |
| regex_compile  | 142 ms                                                 | 169 ms: 1.19x slower                                                   |
| regex_v8       | 20.6 ms                                                | 24.7 ms: 1.20x slower                                                  |
| Geometric mean | (ref)                                                  | 1.08x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241222-vultr-x86_64-python-f420bdd29fbc1a97ad20-3.14.0a3+-f420bdd |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 90.4 ms: 1.07x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                                   |
| json_loads           | 26.5 us                                                | 28.2 us: 1.06x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 98.1 ms: 1.15x slower                                                  |
| tomli_loads          | 2.11 sec                                               | 2.56 sec: 1.22x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 73.8 ms: 1.25x slower                                                  |
| json_dumps           | 10.4 ms                                                | 14.1 ms: 1.36x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 326 us: 1.48x slower                                                   |
| pickle_pure_python   | 308 us                                                 | 503 us: 1.63x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.20x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241222-vultr-x86_64-python-f420bdd29fbc1a97ad20-3.14.0a3+-f420bdd |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.2 ms: 1.43x slower                                                  |
| python_startup         | 9.93 ms                                                | 17.2 ms: 1.73x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.57x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241222-vultr-x86_64-python-f420bdd29fbc1a97ad20-3.14.0a3+-f420bdd |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 63.4 ms: 1.26x slower                                                  |
| genshi_text     | 22.8 ms                                                | 30.6 ms: 1.34x slower                                                  |
| django_template | 34.7 ms                                                | 49.9 ms: 1.44x slower                                                  |
| mako            | 11.0 ms                                                | 16.9 ms: 1.54x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.39x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241222-vultr-x86_64-python-f420bdd29fbc1a97ad20-3.14.0a3+-f420bdd |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 734 ms: 1.51x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 754 ms: 1.44x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 317 ms: 1.41x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 401 ms: 1.39x faster                                                   |
| async_tree_none            | 464 ms                                                 | 350 ms: 1.33x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 426 ms: 1.30x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 569 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 593 ms: 1.21x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.76 ms: 1.15x faster                                                  |
| pathlib                    | 21.5 ms                                                | 19.6 ms: 1.10x faster                                                  |
| deepcopy                   | 352 us                                                 | 329 us: 1.07x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 90.4 ms: 1.07x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                                   |
| gc_traversal               | 3.46 ms                                                | 3.28 ms: 1.05x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 2.15 us: 1.02x faster                                                  |
| pidigits                   | 184 ms                                                 | 184 ms: 1.00x faster                                                   |
| json                       | 5.02 ms                                                | 5.06 ms: 1.01x slower                                                  |
| asyncio_websockets         | 517 ms                                                 | 522 ms: 1.01x slower                                                   |
| deepcopy_memo              | 40.3 us                                                | 41.0 us: 1.02x slower                                                  |
| coroutines                 | 23.9 ms                                                | 24.4 ms: 1.02x slower                                                  |
| spectral_norm              | 110 ms                                                 | 113 ms: 1.03x slower                                                   |
| json_loads                 | 26.5 us                                                | 28.2 us: 1.06x slower                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 5.03 sec: 1.06x slower                                                 |
| regex_dna                  | 168 ms                                                 | 186 ms: 1.11x slower                                                   |
| mdp                        | 2.42 sec                                               | 2.69 sec: 1.11x slower                                                 |
| scimark_fft                | 342 ms                                                 | 381 ms: 1.12x slower                                                   |
| deepcopy_reduce            | 3.08 us                                                | 3.47 us: 1.13x slower                                                  |
| pylint                     | 319 ms                                                 | 364 ms: 1.14x slower                                                   |
| docutils                   | 2.64 sec                                               | 3.03 sec: 1.15x slower                                                 |
| xml_etree_generate         | 85.2 ms                                                | 98.1 ms: 1.15x slower                                                  |
| dulwich_log                | 78.9 ms                                                | 91.2 ms: 1.16x slower                                                  |
| async_generators           | 384 ms                                                 | 450 ms: 1.17x slower                                                   |
| crypto_pyaes               | 76.6 ms                                                | 90.4 ms: 1.18x slower                                                  |
| regex_compile              | 142 ms                                                 | 169 ms: 1.19x slower                                                   |
| generators                 | 32.2 ms                                                | 38.3 ms: 1.19x slower                                                  |
| pycparser                  | 1.17 sec                                               | 1.40 sec: 1.20x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 24.7 ms: 1.20x slower                                                  |
| tomli_loads                | 2.11 sec                                               | 2.56 sec: 1.22x slower                                                 |
| sqlglot_optimize           | 53.3 ms                                                | 65.8 ms: 1.24x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.45 ms: 1.24x slower                                                  |
| sqlglot_normalize          | 107 ms                                                 | 133 ms: 1.24x slower                                                   |
| nqueens                    | 80.1 ms                                                | 99.9 ms: 1.25x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 73.8 ms: 1.25x slower                                                  |
| typing_runtime_protocols   | 163 us                                                 | 205 us: 1.25x slower                                                   |
| thrift                     | 791 us                                                 | 999 us: 1.26x slower                                                   |
| genshi_xml                 | 50.2 ms                                                | 63.4 ms: 1.26x slower                                                  |
| meteor_contest             | 104 ms                                                 | 132 ms: 1.27x slower                                                   |
| sqlalchemy_imperative      | 21.8 ms                                                | 28.0 ms: 1.28x slower                                                  |
| pprint_safe_repr           | 743 ms                                                 | 961 ms: 1.29x slower                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.99 sec: 1.31x slower                                                 |
| fannkuch                   | 372 ms                                                 | 492 ms: 1.32x slower                                                   |
| telco                      | 6.53 ms                                                | 8.72 ms: 1.34x slower                                                  |
| genshi_text                | 22.8 ms                                                | 30.6 ms: 1.34x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 14.1 ms: 1.36x slower                                                  |
| comprehensions             | 19.8 us                                                | 27.1 us: 1.37x slower                                                  |
| 2to3                       | 264 ms                                                 | 360 ms: 1.37x slower                                                   |
| sqlalchemy_declarative     | 143 ms                                                 | 197 ms: 1.38x slower                                                   |
| scimark_lu                 | 114 ms                                                 | 158 ms: 1.39x slower                                                   |
| logging_simple             | 6.63 us                                                | 9.23 us: 1.39x slower                                                  |
| logging_format             | 7.35 us                                                | 10.2 us: 1.40x slower                                                  |
| float                      | 80.8 ms                                                | 113 ms: 1.40x slower                                                   |
| coverage                   | 71.4 ms                                                | 100.0 ms: 1.40x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 10.2 ms: 1.43x slower                                                  |
| richards_super             | 51.9 ms                                                | 74.4 ms: 1.43x slower                                                  |
| nbody                      | 89.3 ms                                                | 128 ms: 1.44x slower                                                   |
| richards                   | 45.9 ms                                                | 66.1 ms: 1.44x slower                                                  |
| django_template            | 34.7 ms                                                | 49.9 ms: 1.44x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 29.8 ms: 1.45x slower                                                  |
| pyflate                    | 448 ms                                                 | 653 ms: 1.46x slower                                                   |
| unpickle_pure_python       | 221 us                                                 | 326 us: 1.48x slower                                                   |
| html5lib                   | 63.6 ms                                                | 94.6 ms: 1.49x slower                                                  |
| chaos                      | 62.8 ms                                                | 96.4 ms: 1.53x slower                                                  |
| mako                       | 11.0 ms                                                | 16.9 ms: 1.54x slower                                                  |
| hexiom                     | 6.17 ms                                                | 9.52 ms: 1.54x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 106 ms: 1.55x slower                                                   |
| logging_silent             | 109 ns                                                 | 177 ns: 1.63x slower                                                   |
| sqlglot_transpile          | 1.67 ms                                                | 2.72 ms: 1.63x slower                                                  |
| raytrace                   | 299 ms                                                 | 489 ms: 1.63x slower                                                   |
| pickle_pure_python         | 308 us                                                 | 503 us: 1.63x slower                                                   |
| sympy_str                  | 292 ms                                                 | 478 ms: 1.64x slower                                                   |
| create_gc_cycles           | 1.09 ms                                                | 1.81 ms: 1.65x slower                                                  |
| scimark_sor                | 130 ms                                                 | 217 ms: 1.67x slower                                                   |
| go                         | 139 ms                                                 | 239 ms: 1.72x slower                                                   |
| sqlglot_parse              | 1.36 ms                                                | 2.34 ms: 1.72x slower                                                  |
| python_startup             | 9.93 ms                                                | 17.2 ms: 1.73x slower                                                  |
| sympy_expand               | 468 ms                                                 | 961 ms: 2.05x slower                                                   |
| sympy_sum                  | 166 ms                                                 | 351 ms: 2.12x slower                                                   |
| deltablue                  | 3.45 ms                                                | 7.31 ms: 2.12x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 3.39 ms: 3.60x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 108 ms: 10.00x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.28x slower                                                           |
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241222-3.14.0a3+-f420bdd-NOGIL/bm-20241222-vultr-x86_64-python-f420bdd29fbc1a97ad20-3.14.0a3+-f420bdd.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.187x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.18x
- 95% likely to have a slowdown of 1.17x
- 99% likely to have a slowdown of 1.14x

# Memory
- memory change: 1.34x