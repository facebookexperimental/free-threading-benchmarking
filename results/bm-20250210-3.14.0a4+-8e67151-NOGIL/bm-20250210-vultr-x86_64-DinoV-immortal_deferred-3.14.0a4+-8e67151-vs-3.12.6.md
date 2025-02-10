# Results vs. 3.12.6

- fork: DinoV
- ref: immortal_deferred
- machine: linux-x86_64
- commit hash: 8e67151
- commit date: 2025-02-10
- overall geometric mean: 1.045x slower
- HPT reliability: 99.95%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-vultr-x86_64-DinoV-immortal_deferred-3.14.0a4+-8e67151 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 302 ms: 1.15x slower                                               |
| docutils       | 2.64 sec                                               | 2.79 sec: 1.06x slower                                             |
| html5lib       | 63.6 ms                                                | 69.9 ms: 1.10x slower                                              |
| Geometric mean | (ref)                                                  | 1.10x slower                                                       |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-vultr-x86_64-DinoV-immortal_deferred-3.14.0a4+-8e67151 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 577 ms: 1.92x faster                                               |
| async_tree_io              | 1.08 sec                                               | 605 ms: 1.79x faster                                               |
| async_tree_none_tg         | 446 ms                                                 | 252 ms: 1.77x faster                                               |
| async_tree_memoization_tg  | 560 ms                                                 | 320 ms: 1.75x faster                                               |
| async_tree_none            | 464 ms                                                 | 291 ms: 1.59x faster                                               |
| async_tree_memoization     | 555 ms                                                 | 351 ms: 1.58x faster                                               |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 523 ms: 1.38x faster                                               |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 555 ms: 1.29x faster                                               |
| coroutines                 | 23.9 ms                                                | 23.2 ms: 1.03x faster                                              |
| async_generators           | 384 ms                                                 | 374 ms: 1.03x faster                                               |
| Geometric mean             | (ref)                                                  | 1.43x faster                                                       |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-vultr-x86_64-DinoV-immortal_deferred-3.14.0a4+-8e67151 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 75.1 ms: 1.08x faster                                              |
| pidigits       | 184 ms                                                 | 200 ms: 1.09x slower                                               |
| nbody          | 89.3 ms                                                | 135 ms: 1.51x slower                                               |
| Geometric mean | (ref)                                                  | 1.15x slower                                                       |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-vultr-x86_64-DinoV-immortal_deferred-3.14.0a4+-8e67151 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.92 ms: 1.08x faster                                              |
| regex_compile  | 142 ms                                                 | 148 ms: 1.04x slower                                               |
| regex_dna      | 168 ms                                                 | 186 ms: 1.11x slower                                               |
| regex_v8       | 20.6 ms                                                | 24.2 ms: 1.17x slower                                              |
| Geometric mean | (ref)                                                  | 1.06x slower                                                       |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-vultr-x86_64-DinoV-immortal_deferred-3.14.0a4+-8e67151 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.0 ms: 1.10x faster                                              |
| xml_etree_parse      | 139 ms                                                 | 127 ms: 1.10x faster                                               |
| tomli_loads          | 2.11 sec                                               | 2.30 sec: 1.09x slower                                             |
| xml_etree_generate   | 85.2 ms                                                | 95.8 ms: 1.12x slower                                              |
| unpickle_pure_python | 221 us                                                 | 250 us: 1.13x slower                                               |
| xml_etree_process    | 59.0 ms                                                | 68.8 ms: 1.17x slower                                              |
| json_loads           | 26.5 us                                                | 31.1 us: 1.17x slower                                              |
| pickle_pure_python   | 308 us                                                 | 374 us: 1.21x slower                                               |
| json_dumps           | 10.4 ms                                                | 12.7 ms: 1.22x slower                                              |
| Geometric mean       | (ref)                                                  | 1.10x slower                                                       |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-vultr-x86_64-DinoV-immortal_deferred-3.14.0a4+-8e67151 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.61 ms: 1.34x slower                                              |
| python_startup         | 9.93 ms                                                | 15.3 ms: 1.54x slower                                              |
| Geometric mean         | (ref)                                                  | 1.44x slower                                                       |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-vultr-x86_64-DinoV-immortal_deferred-3.14.0a4+-8e67151 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 60.4 ms: 1.20x slower                                              |
| django_template | 34.7 ms                                                | 42.6 ms: 1.23x slower                                              |
| genshi_text     | 22.8 ms                                                | 28.1 ms: 1.23x slower                                              |
| mako            | 11.0 ms                                                | 16.0 ms: 1.45x slower                                              |
| Geometric mean  | (ref)                                                  | 1.28x slower                                                       |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-vultr-x86_64-DinoV-immortal_deferred-3.14.0a4+-8e67151 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| gc_traversal               | 3.46 ms                                                | 1.73 ms: 1.99x faster                                              |
| async_tree_io_tg           | 1.11 sec                                               | 577 ms: 1.92x faster                                               |
| async_tree_io              | 1.08 sec                                               | 605 ms: 1.79x faster                                               |
| async_tree_none_tg         | 446 ms                                                 | 252 ms: 1.77x faster                                               |
| async_tree_memoization_tg  | 560 ms                                                 | 320 ms: 1.75x faster                                               |
| async_tree_none            | 464 ms                                                 | 291 ms: 1.59x faster                                               |
| async_tree_memoization     | 555 ms                                                 | 351 ms: 1.58x faster                                               |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 523 ms: 1.38x faster                                               |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 555 ms: 1.29x faster                                               |
| pathlib                    | 21.5 ms                                                | 18.7 ms: 1.15x faster                                              |
| deepcopy                   | 352 us                                                 | 310 us: 1.14x faster                                               |
| xml_etree_iterparse        | 96.7 ms                                                | 88.0 ms: 1.10x faster                                              |
| xml_etree_parse            | 139 ms                                                 | 127 ms: 1.10x faster                                               |
| sqlite_synth               | 2.20 us                                                | 2.02 us: 1.09x faster                                              |
| regex_effbot               | 3.17 ms                                                | 2.92 ms: 1.08x faster                                              |
| float                      | 80.8 ms                                                | 75.1 ms: 1.08x faster                                              |
| deepcopy_memo              | 40.3 us                                                | 38.4 us: 1.05x faster                                              |
| spectral_norm              | 110 ms                                                 | 105 ms: 1.05x faster                                               |
| coroutines                 | 23.9 ms                                                | 23.2 ms: 1.03x faster                                              |
| async_generators           | 384 ms                                                 | 374 ms: 1.03x faster                                               |
| bpe_tokeniser              | 4.74 sec                                               | 4.62 sec: 1.03x faster                                             |
| go                         | 139 ms                                                 | 137 ms: 1.02x faster                                               |
| pycparser                  | 1.17 sec                                               | 1.18 sec: 1.01x slower                                             |
| comprehensions             | 19.8 us                                                | 20.1 us: 1.01x slower                                              |
| dulwich_log                | 78.9 ms                                                | 81.9 ms: 1.04x slower                                              |
| deepcopy_reduce            | 3.08 us                                                | 3.20 us: 1.04x slower                                              |
| regex_compile              | 142 ms                                                 | 148 ms: 1.04x slower                                               |
| generators                 | 32.2 ms                                                | 34.0 ms: 1.06x slower                                              |
| docutils                   | 2.64 sec                                               | 2.79 sec: 1.06x slower                                             |
| json                       | 5.02 ms                                                | 5.36 ms: 1.07x slower                                              |
| logging_simple             | 6.63 us                                                | 7.18 us: 1.08x slower                                              |
| sqlalchemy_imperative      | 21.8 ms                                                | 23.6 ms: 1.08x slower                                              |
| pidigits                   | 184 ms                                                 | 200 ms: 1.09x slower                                               |
| pyflate                    | 448 ms                                                 | 487 ms: 1.09x slower                                               |
| pprint_safe_repr           | 743 ms                                                 | 811 ms: 1.09x slower                                               |
| tomli_loads                | 2.11 sec                                               | 2.30 sec: 1.09x slower                                             |
| raytrace                   | 299 ms                                                 | 328 ms: 1.09x slower                                               |
| chaos                      | 62.8 ms                                                | 68.9 ms: 1.10x slower                                              |
| html5lib                   | 63.6 ms                                                | 69.9 ms: 1.10x slower                                              |
| sqlalchemy_declarative     | 143 ms                                                 | 157 ms: 1.10x slower                                               |
| pprint_pformat             | 1.52 sec                                               | 1.67 sec: 1.10x slower                                             |
| sympy_sum                  | 166 ms                                                 | 184 ms: 1.11x slower                                               |
| regex_dna                  | 168 ms                                                 | 186 ms: 1.11x slower                                               |
| logging_format             | 7.35 us                                                | 8.20 us: 1.12x slower                                              |
| deltablue                  | 3.45 ms                                                | 3.86 ms: 1.12x slower                                              |
| mdp                        | 2.42 sec                                               | 2.72 sec: 1.12x slower                                             |
| xml_etree_generate         | 85.2 ms                                                | 95.8 ms: 1.12x slower                                              |
| sqlglot_normalize          | 107 ms                                                 | 120 ms: 1.13x slower                                               |
| thrift                     | 791 us                                                 | 894 us: 1.13x slower                                               |
| sqlglot_transpile          | 1.67 ms                                                | 1.89 ms: 1.13x slower                                              |
| unpickle_pure_python       | 221 us                                                 | 250 us: 1.13x slower                                               |
| scimark_fft                | 342 ms                                                 | 388 ms: 1.14x slower                                               |
| sqlglot_optimize           | 53.3 ms                                                | 61.0 ms: 1.15x slower                                              |
| sympy_str                  | 292 ms                                                 | 334 ms: 1.15x slower                                               |
| 2to3                       | 264 ms                                                 | 302 ms: 1.15x slower                                               |
| crypto_pyaes               | 76.6 ms                                                | 88.7 ms: 1.16x slower                                              |
| sqlglot_parse              | 1.36 ms                                                | 1.57 ms: 1.16x slower                                              |
| xml_etree_process          | 59.0 ms                                                | 68.8 ms: 1.17x slower                                              |
| sympy_integrate            | 20.5 ms                                                | 24.0 ms: 1.17x slower                                              |
| sympy_expand               | 468 ms                                                 | 547 ms: 1.17x slower                                               |
| json_loads                 | 26.5 us                                                | 31.1 us: 1.17x slower                                              |
| regex_v8                   | 20.6 ms                                                | 24.2 ms: 1.17x slower                                              |
| hexiom                     | 6.17 ms                                                | 7.32 ms: 1.19x slower                                              |
| scimark_lu                 | 114 ms                                                 | 136 ms: 1.19x slower                                               |
| genshi_xml                 | 50.2 ms                                                | 60.4 ms: 1.20x slower                                              |
| scimark_monte_carlo        | 68.4 ms                                                | 82.6 ms: 1.21x slower                                              |
| nqueens                    | 80.1 ms                                                | 96.9 ms: 1.21x slower                                              |
| typing_runtime_protocols   | 163 us                                                 | 198 us: 1.21x slower                                               |
| pickle_pure_python         | 308 us                                                 | 374 us: 1.21x slower                                               |
| json_dumps                 | 10.4 ms                                                | 12.7 ms: 1.22x slower                                              |
| richards                   | 45.9 ms                                                | 56.3 ms: 1.23x slower                                              |
| django_template            | 34.7 ms                                                | 42.6 ms: 1.23x slower                                              |
| genshi_text                | 22.8 ms                                                | 28.1 ms: 1.23x slower                                              |
| meteor_contest             | 104 ms                                                 | 130 ms: 1.26x slower                                               |
| create_gc_cycles           | 1.09 ms                                                | 1.37 ms: 1.26x slower                                              |
| richards_super             | 51.9 ms                                                | 66.9 ms: 1.29x slower                                              |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.70 ms: 1.30x slower                                              |
| fannkuch                   | 372 ms                                                 | 488 ms: 1.31x slower                                               |
| telco                      | 6.53 ms                                                | 8.66 ms: 1.33x slower                                              |
| python_startup_no_site     | 7.16 ms                                                | 9.61 ms: 1.34x slower                                              |
| coverage                   | 71.4 ms                                                | 97.5 ms: 1.37x slower                                              |
| mako                       | 11.0 ms                                                | 16.0 ms: 1.45x slower                                              |
| nbody                      | 89.3 ms                                                | 135 ms: 1.51x slower                                               |
| python_startup             | 9.93 ms                                                | 15.3 ms: 1.54x slower                                              |
| bench_thread_pool          | 941 us                                                 | 3.30 ms: 3.51x slower                                              |
| bench_mp_pool              | 10.8 ms                                                | 94.6 ms: 8.76x slower                                              |
| Geometric mean             | (ref)                                                  | 1.09x slower                                                       |

Benchmark hidden because not significant (4): pylint, logging_silent, asyncio_websockets, scimark_sor
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250210-3.14.0a4+-8e67151-NOGIL/bm-20250210-vultr-x86_64-DinoV-immortal_deferred-3.14.0a4+-8e67151.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.045x slower

# HPT report

- Reliability score: 99.95% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.36x