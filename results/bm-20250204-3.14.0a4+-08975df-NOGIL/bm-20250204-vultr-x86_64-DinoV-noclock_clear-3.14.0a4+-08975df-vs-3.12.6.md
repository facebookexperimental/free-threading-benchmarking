# Results vs. 3.12.6

- fork: DinoV
- ref: noclock_clear
- machine: linux-x86_64
- commit hash: 08975df
- commit date: 2025-02-04
- overall geometric mean: 1.054x slower
- HPT reliability: 99.93%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.46x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250204-vultr-x86_64-DinoV-noclock_clear-3.14.0a4+-08975df |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 303 ms: 1.15x slower                                           |
| docutils       | 2.64 sec                                               | 2.78 sec: 1.06x slower                                         |
| html5lib       | 63.6 ms                                                | 69.0 ms: 1.09x slower                                          |
| Geometric mean | (ref)                                                  | 1.10x slower                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250204-vultr-x86_64-DinoV-noclock_clear-3.14.0a4+-08975df |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 577 ms: 1.92x faster                                           |
| async_tree_none_tg         | 446 ms                                                 | 247 ms: 1.80x faster                                           |
| async_tree_io              | 1.08 sec                                               | 608 ms: 1.78x faster                                           |
| async_tree_memoization_tg  | 560 ms                                                 | 318 ms: 1.76x faster                                           |
| async_tree_none            | 464 ms                                                 | 286 ms: 1.63x faster                                           |
| async_tree_memoization     | 555 ms                                                 | 351 ms: 1.58x faster                                           |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 499 ms: 1.45x faster                                           |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 531 ms: 1.35x faster                                           |
| async_generators           | 384 ms                                                 | 373 ms: 1.03x faster                                           |
| coroutines                 | 23.9 ms                                                | 23.6 ms: 1.01x faster                                          |
| asyncio_websockets         | 517 ms                                                 | 516 ms: 1.00x faster                                           |
| Geometric mean             | (ref)                                                  | 1.44x faster                                                   |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250204-vultr-x86_64-DinoV-noclock_clear-3.14.0a4+-08975df |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------:|
| float          | 80.8 ms                                                | 76.7 ms: 1.05x faster                                          |
| pidigits       | 184 ms                                                 | 190 ms: 1.03x slower                                           |
| nbody          | 89.3 ms                                                | 132 ms: 1.48x slower                                           |
| Geometric mean | (ref)                                                  | 1.13x slower                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250204-vultr-x86_64-DinoV-noclock_clear-3.14.0a4+-08975df |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.82 ms: 1.12x faster                                          |
| regex_compile  | 142 ms                                                 | 148 ms: 1.04x slower                                           |
| regex_dna      | 168 ms                                                 | 185 ms: 1.10x slower                                           |
| regex_v8       | 20.6 ms                                                | 23.3 ms: 1.13x slower                                          |
| Geometric mean | (ref)                                                  | 1.04x slower                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250204-vultr-x86_64-DinoV-noclock_clear-3.14.0a4+-08975df |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.9 ms: 1.10x faster                                          |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                           |
| tomli_loads          | 2.11 sec                                               | 2.30 sec: 1.09x slower                                         |
| unpickle_pure_python | 221 us                                                 | 246 us: 1.11x slower                                           |
| xml_etree_generate   | 85.2 ms                                                | 96.5 ms: 1.13x slower                                          |
| xml_etree_process    | 59.0 ms                                                | 68.9 ms: 1.17x slower                                          |
| json_loads           | 26.5 us                                                | 31.6 us: 1.19x slower                                          |
| pickle_pure_python   | 308 us                                                 | 369 us: 1.20x slower                                           |
| json_dumps           | 10.4 ms                                                | 12.8 ms: 1.23x slower                                          |
| Geometric mean       | (ref)                                                  | 1.10x slower                                                   |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250204-vultr-x86_64-DinoV-noclock_clear-3.14.0a4+-08975df |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.62 ms: 1.34x slower                                          |
| python_startup         | 9.93 ms                                                | 15.3 ms: 1.54x slower                                          |
| Geometric mean         | (ref)                                                  | 1.44x slower                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250204-vultr-x86_64-DinoV-noclock_clear-3.14.0a4+-08975df |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 60.0 ms: 1.20x slower                                          |
| genshi_text     | 22.8 ms                                                | 27.5 ms: 1.21x slower                                          |
| django_template | 34.7 ms                                                | 42.6 ms: 1.23x slower                                          |
| mako            | 11.0 ms                                                | 16.0 ms: 1.45x slower                                          |
| Geometric mean  | (ref)                                                  | 1.27x slower                                                   |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250204-vultr-x86_64-DinoV-noclock_clear-3.14.0a4+-08975df |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------:|
| gc_traversal               | 3.46 ms                                                | 1.76 ms: 1.96x faster                                          |
| async_tree_io_tg           | 1.11 sec                                               | 577 ms: 1.92x faster                                           |
| async_tree_none_tg         | 446 ms                                                 | 247 ms: 1.80x faster                                           |
| async_tree_io              | 1.08 sec                                               | 608 ms: 1.78x faster                                           |
| async_tree_memoization_tg  | 560 ms                                                 | 318 ms: 1.76x faster                                           |
| async_tree_none            | 464 ms                                                 | 286 ms: 1.63x faster                                           |
| async_tree_memoization     | 555 ms                                                 | 351 ms: 1.58x faster                                           |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 499 ms: 1.45x faster                                           |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 531 ms: 1.35x faster                                           |
| pathlib                    | 21.5 ms                                                | 18.9 ms: 1.14x faster                                          |
| regex_effbot               | 3.17 ms                                                | 2.82 ms: 1.12x faster                                          |
| xml_etree_iterparse        | 96.7 ms                                                | 87.9 ms: 1.10x faster                                          |
| sqlite_synth               | 2.20 us                                                | 2.04 us: 1.08x faster                                          |
| deepcopy                   | 352 us                                                 | 328 us: 1.07x faster                                           |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                           |
| deepcopy_memo              | 40.3 us                                                | 37.8 us: 1.07x faster                                          |
| float                      | 80.8 ms                                                | 76.7 ms: 1.05x faster                                          |
| spectral_norm              | 110 ms                                                 | 106 ms: 1.04x faster                                           |
| async_generators           | 384 ms                                                 | 373 ms: 1.03x faster                                           |
| go                         | 139 ms                                                 | 136 ms: 1.02x faster                                           |
| coroutines                 | 23.9 ms                                                | 23.6 ms: 1.01x faster                                          |
| bpe_tokeniser              | 4.74 sec                                               | 4.68 sec: 1.01x faster                                         |
| asyncio_websockets         | 517 ms                                                 | 516 ms: 1.00x faster                                           |
| comprehensions             | 19.8 us                                                | 20.2 us: 1.02x slower                                          |
| generators                 | 32.2 ms                                                | 33.2 ms: 1.03x slower                                          |
| pidigits                   | 184 ms                                                 | 190 ms: 1.03x slower                                           |
| logging_silent             | 109 ns                                                 | 112 ns: 1.03x slower                                           |
| regex_compile              | 142 ms                                                 | 148 ms: 1.04x slower                                           |
| dulwich_log                | 78.9 ms                                                | 82.8 ms: 1.05x slower                                          |
| docutils                   | 2.64 sec                                               | 2.78 sec: 1.06x slower                                         |
| raytrace                   | 299 ms                                                 | 318 ms: 1.06x slower                                           |
| chaos                      | 62.8 ms                                                | 68.1 ms: 1.08x slower                                          |
| html5lib                   | 63.6 ms                                                | 69.0 ms: 1.09x slower                                          |
| json                       | 5.02 ms                                                | 5.45 ms: 1.09x slower                                          |
| scimark_fft                | 342 ms                                                 | 371 ms: 1.09x slower                                           |
| pprint_safe_repr           | 743 ms                                                 | 808 ms: 1.09x slower                                           |
| mdp                        | 2.42 sec                                               | 2.63 sec: 1.09x slower                                         |
| tomli_loads                | 2.11 sec                                               | 2.30 sec: 1.09x slower                                         |
| pyflate                    | 448 ms                                                 | 491 ms: 1.10x slower                                           |
| regex_dna                  | 168 ms                                                 | 185 ms: 1.10x slower                                           |
| pprint_pformat             | 1.52 sec                                               | 1.68 sec: 1.11x slower                                         |
| deepcopy_reduce            | 3.08 us                                                | 3.42 us: 1.11x slower                                          |
| unpickle_pure_python       | 221 us                                                 | 246 us: 1.11x slower                                           |
| sympy_sum                  | 166 ms                                                 | 186 ms: 1.12x slower                                           |
| sqlglot_normalize          | 107 ms                                                 | 120 ms: 1.13x slower                                           |
| regex_v8                   | 20.6 ms                                                | 23.3 ms: 1.13x slower                                          |
| thrift                     | 791 us                                                 | 896 us: 1.13x slower                                           |
| xml_etree_generate         | 85.2 ms                                                | 96.5 ms: 1.13x slower                                          |
| sqlglot_optimize           | 53.3 ms                                                | 60.9 ms: 1.14x slower                                          |
| sqlglot_transpile          | 1.67 ms                                                | 1.92 ms: 1.15x slower                                          |
| crypto_pyaes               | 76.6 ms                                                | 87.9 ms: 1.15x slower                                          |
| 2to3                       | 264 ms                                                 | 303 ms: 1.15x slower                                           |
| sympy_str                  | 292 ms                                                 | 337 ms: 1.16x slower                                           |
| xml_etree_process          | 59.0 ms                                                | 68.9 ms: 1.17x slower                                          |
| sympy_integrate            | 20.5 ms                                                | 24.1 ms: 1.17x slower                                          |
| sqlglot_parse              | 1.36 ms                                                | 1.59 ms: 1.17x slower                                          |
| scimark_monte_carlo        | 68.4 ms                                                | 80.5 ms: 1.18x slower                                          |
| scimark_lu                 | 114 ms                                                 | 135 ms: 1.18x slower                                           |
| sympy_expand               | 468 ms                                                 | 556 ms: 1.19x slower                                           |
| json_loads                 | 26.5 us                                                | 31.6 us: 1.19x slower                                          |
| genshi_xml                 | 50.2 ms                                                | 60.0 ms: 1.20x slower                                          |
| pickle_pure_python         | 308 us                                                 | 369 us: 1.20x slower                                           |
| logging_simple             | 6.63 us                                                | 7.96 us: 1.20x slower                                          |
| nqueens                    | 80.1 ms                                                | 96.2 ms: 1.20x slower                                          |
| hexiom                     | 6.17 ms                                                | 7.43 ms: 1.20x slower                                          |
| genshi_text                | 22.8 ms                                                | 27.5 ms: 1.21x slower                                          |
| richards                   | 45.9 ms                                                | 56.4 ms: 1.23x slower                                          |
| django_template            | 34.7 ms                                                | 42.6 ms: 1.23x slower                                          |
| create_gc_cycles           | 1.09 ms                                                | 1.35 ms: 1.23x slower                                          |
| typing_runtime_protocols   | 163 us                                                 | 201 us: 1.23x slower                                           |
| json_dumps                 | 10.4 ms                                                | 12.8 ms: 1.23x slower                                          |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.45 ms: 1.24x slower                                          |
| meteor_contest             | 104 ms                                                 | 129 ms: 1.25x slower                                           |
| richards_super             | 51.9 ms                                                | 66.3 ms: 1.28x slower                                          |
| telco                      | 6.53 ms                                                | 8.56 ms: 1.31x slower                                          |
| fannkuch                   | 372 ms                                                 | 490 ms: 1.32x slower                                           |
| python_startup_no_site     | 7.16 ms                                                | 9.62 ms: 1.34x slower                                          |
| deltablue                  | 3.45 ms                                                | 4.65 ms: 1.35x slower                                          |
| coverage                   | 71.4 ms                                                | 99.3 ms: 1.39x slower                                          |
| sqlalchemy_imperative      | 21.8 ms                                                | 30.3 ms: 1.39x slower                                          |
| logging_format             | 7.35 us                                                | 10.3 us: 1.40x slower                                          |
| mako                       | 11.0 ms                                                | 16.0 ms: 1.45x slower                                          |
| nbody                      | 89.3 ms                                                | 132 ms: 1.48x slower                                           |
| python_startup             | 9.93 ms                                                | 15.3 ms: 1.54x slower                                          |
| sqlalchemy_declarative     | 143 ms                                                 | 225 ms: 1.58x slower                                           |
| bench_thread_pool          | 941 us                                                 | 3.29 ms: 3.49x slower                                          |
| bench_mp_pool              | 10.8 ms                                                | 94.6 ms: 8.76x slower                                          |
| Geometric mean             | (ref)                                                  | 1.10x slower                                                   |

Benchmark hidden because not significant (3): pylint, pycparser, scimark_sor
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250204-3.14.0a4+-08975df-NOGIL/bm-20250204-vultr-x86_64-DinoV-noclock_clear-3.14.0a4+-08975df.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.054x slower

# HPT report

- Reliability score: 99.93% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.04x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.46x