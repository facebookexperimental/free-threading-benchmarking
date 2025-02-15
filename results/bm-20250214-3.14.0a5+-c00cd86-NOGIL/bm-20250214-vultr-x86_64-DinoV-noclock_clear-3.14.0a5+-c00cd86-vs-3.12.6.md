# Results vs. 3.12.6

- fork: DinoV
- ref: noclock_clear
- machine: linux-x86_64
- commit hash: c00cd86
- commit date: 2025-02-14
- overall geometric mean: 1.047x slower
- HPT reliability: 99.98%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250214-vultr-x86_64-DinoV-noclock_clear-3.14.0a5+-c00cd86 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 304 ms: 1.15x slower                                           |
| docutils       | 2.64 sec                                               | 2.79 sec: 1.06x slower                                         |
| html5lib       | 63.6 ms                                                | 70.3 ms: 1.11x slower                                          |
| Geometric mean | (ref)                                                  | 1.11x slower                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250214-vultr-x86_64-DinoV-noclock_clear-3.14.0a5+-c00cd86 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 577 ms: 1.92x faster                                           |
| async_tree_io              | 1.08 sec                                               | 612 ms: 1.77x faster                                           |
| async_tree_memoization_tg  | 560 ms                                                 | 320 ms: 1.75x faster                                           |
| async_tree_none_tg         | 446 ms                                                 | 260 ms: 1.71x faster                                           |
| async_tree_none            | 464 ms                                                 | 292 ms: 1.59x faster                                           |
| async_tree_memoization     | 555 ms                                                 | 354 ms: 1.57x faster                                           |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 507 ms: 1.43x faster                                           |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 537 ms: 1.33x faster                                           |
| async_generators           | 384 ms                                                 | 374 ms: 1.03x faster                                           |
| asyncio_websockets         | 517 ms                                                 | 518 ms: 1.00x slower                                           |
| coroutines                 | 23.9 ms                                                | 24.2 ms: 1.01x slower                                          |
| Geometric mean             | (ref)                                                  | 1.42x faster                                                   |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250214-vultr-x86_64-DinoV-noclock_clear-3.14.0a5+-c00cd86 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------:|
| float          | 80.8 ms                                                | 76.2 ms: 1.06x faster                                          |
| pidigits       | 184 ms                                                 | 199 ms: 1.08x slower                                           |
| nbody          | 89.3 ms                                                | 130 ms: 1.46x slower                                           |
| Geometric mean | (ref)                                                  | 1.14x slower                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250214-vultr-x86_64-DinoV-noclock_clear-3.14.0a5+-c00cd86 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.83 ms: 1.12x faster                                          |
| regex_compile  | 142 ms                                                 | 152 ms: 1.07x slower                                           |
| regex_dna      | 168 ms                                                 | 182 ms: 1.08x slower                                           |
| regex_v8       | 20.6 ms                                                | 25.1 ms: 1.22x slower                                          |
| Geometric mean | (ref)                                                  | 1.06x slower                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250214-vultr-x86_64-DinoV-noclock_clear-3.14.0a5+-c00cd86 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.7 ms: 1.09x faster                                          |
| xml_etree_parse      | 139 ms                                                 | 127 ms: 1.09x faster                                           |
| tomli_loads          | 2.11 sec                                               | 2.34 sec: 1.11x slower                                         |
| unpickle_pure_python | 221 us                                                 | 250 us: 1.14x slower                                           |
| xml_etree_generate   | 85.2 ms                                                | 96.8 ms: 1.14x slower                                          |
| pickle_pure_python   | 308 us                                                 | 359 us: 1.17x slower                                           |
| json_loads           | 26.5 us                                                | 31.6 us: 1.19x slower                                          |
| xml_etree_process    | 59.0 ms                                                | 70.6 ms: 1.20x slower                                          |
| json_dumps           | 10.4 ms                                                | 13.0 ms: 1.26x slower                                          |
| Geometric mean       | (ref)                                                  | 1.11x slower                                                   |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250214-vultr-x86_64-DinoV-noclock_clear-3.14.0a5+-c00cd86 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.66 ms: 1.35x slower                                          |
| python_startup         | 9.93 ms                                                | 15.4 ms: 1.55x slower                                          |
| Geometric mean         | (ref)                                                  | 1.45x slower                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250214-vultr-x86_64-DinoV-noclock_clear-3.14.0a5+-c00cd86 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 59.8 ms: 1.19x slower                                          |
| django_template | 34.7 ms                                                | 42.0 ms: 1.21x slower                                          |
| genshi_text     | 22.8 ms                                                | 28.0 ms: 1.23x slower                                          |
| mako            | 11.0 ms                                                | 15.7 ms: 1.42x slower                                          |
| Geometric mean  | (ref)                                                  | 1.26x slower                                                   |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250214-vultr-x86_64-DinoV-noclock_clear-3.14.0a5+-c00cd86 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------:|
| gc_traversal               | 3.46 ms                                                | 1.76 ms: 1.96x faster                                          |
| async_tree_io_tg           | 1.11 sec                                               | 577 ms: 1.92x faster                                           |
| async_tree_io              | 1.08 sec                                               | 612 ms: 1.77x faster                                           |
| async_tree_memoization_tg  | 560 ms                                                 | 320 ms: 1.75x faster                                           |
| async_tree_none_tg         | 446 ms                                                 | 260 ms: 1.71x faster                                           |
| async_tree_none            | 464 ms                                                 | 292 ms: 1.59x faster                                           |
| async_tree_memoization     | 555 ms                                                 | 354 ms: 1.57x faster                                           |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 507 ms: 1.43x faster                                           |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 537 ms: 1.33x faster                                           |
| deepcopy                   | 352 us                                                 | 308 us: 1.14x faster                                           |
| pathlib                    | 21.5 ms                                                | 19.0 ms: 1.13x faster                                          |
| regex_effbot               | 3.17 ms                                                | 2.83 ms: 1.12x faster                                          |
| xml_etree_iterparse        | 96.7 ms                                                | 88.7 ms: 1.09x faster                                          |
| xml_etree_parse            | 139 ms                                                 | 127 ms: 1.09x faster                                           |
| sqlite_synth               | 2.20 us                                                | 2.04 us: 1.08x faster                                          |
| float                      | 80.8 ms                                                | 76.2 ms: 1.06x faster                                          |
| deepcopy_memo              | 40.3 us                                                | 38.7 us: 1.04x faster                                          |
| async_generators           | 384 ms                                                 | 374 ms: 1.03x faster                                           |
| spectral_norm              | 110 ms                                                 | 108 ms: 1.02x faster                                           |
| bpe_tokeniser              | 4.74 sec                                               | 4.68 sec: 1.01x faster                                         |
| asyncio_websockets         | 517 ms                                                 | 518 ms: 1.00x slower                                           |
| go                         | 139 ms                                                 | 140 ms: 1.01x slower                                           |
| coroutines                 | 23.9 ms                                                | 24.2 ms: 1.01x slower                                          |
| scimark_sor                | 130 ms                                                 | 132 ms: 1.01x slower                                           |
| pycparser                  | 1.17 sec                                               | 1.19 sec: 1.01x slower                                         |
| deepcopy_reduce            | 3.08 us                                                | 3.16 us: 1.03x slower                                          |
| dulwich_log                | 78.9 ms                                                | 82.4 ms: 1.04x slower                                          |
| docutils                   | 2.64 sec                                               | 2.79 sec: 1.06x slower                                         |
| regex_compile              | 142 ms                                                 | 152 ms: 1.07x slower                                           |
| logging_simple             | 6.63 us                                                | 7.10 us: 1.07x slower                                          |
| json                       | 5.02 ms                                                | 5.42 ms: 1.08x slower                                          |
| pidigits                   | 184 ms                                                 | 199 ms: 1.08x slower                                           |
| regex_dna                  | 168 ms                                                 | 182 ms: 1.08x slower                                           |
| raytrace                   | 299 ms                                                 | 325 ms: 1.08x slower                                           |
| sqlalchemy_declarative     | 143 ms                                                 | 156 ms: 1.09x slower                                           |
| pprint_safe_repr           | 743 ms                                                 | 817 ms: 1.10x slower                                           |
| logging_silent             | 109 ns                                                 | 120 ns: 1.10x slower                                           |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.0 ms: 1.10x slower                                          |
| logging_format             | 7.35 us                                                | 8.11 us: 1.10x slower                                          |
| pyflate                    | 448 ms                                                 | 495 ms: 1.10x slower                                           |
| chaos                      | 62.8 ms                                                | 69.4 ms: 1.10x slower                                          |
| html5lib                   | 63.6 ms                                                | 70.3 ms: 1.11x slower                                          |
| tomli_loads                | 2.11 sec                                               | 2.34 sec: 1.11x slower                                         |
| pprint_pformat             | 1.52 sec                                               | 1.69 sec: 1.11x slower                                         |
| sympy_sum                  | 166 ms                                                 | 185 ms: 1.11x slower                                           |
| mdp                        | 2.42 sec                                               | 2.71 sec: 1.12x slower                                         |
| sqlglot_normalize          | 107 ms                                                 | 120 ms: 1.12x slower                                           |
| thrift                     | 791 us                                                 | 890 us: 1.13x slower                                           |
| scimark_fft                | 342 ms                                                 | 388 ms: 1.13x slower                                           |
| unpickle_pure_python       | 221 us                                                 | 250 us: 1.14x slower                                           |
| xml_etree_generate         | 85.2 ms                                                | 96.8 ms: 1.14x slower                                          |
| deltablue                  | 3.45 ms                                                | 3.92 ms: 1.14x slower                                          |
| crypto_pyaes               | 76.6 ms                                                | 87.6 ms: 1.14x slower                                          |
| sympy_str                  | 292 ms                                                 | 333 ms: 1.14x slower                                           |
| sqlglot_transpile          | 1.67 ms                                                | 1.92 ms: 1.15x slower                                          |
| sqlglot_optimize           | 53.3 ms                                                | 61.1 ms: 1.15x slower                                          |
| 2to3                       | 264 ms                                                 | 304 ms: 1.15x slower                                           |
| pickle_pure_python         | 308 us                                                 | 359 us: 1.17x slower                                           |
| sympy_expand               | 468 ms                                                 | 547 ms: 1.17x slower                                           |
| sympy_integrate            | 20.5 ms                                                | 24.1 ms: 1.17x slower                                          |
| sqlglot_parse              | 1.36 ms                                                | 1.60 ms: 1.18x slower                                          |
| json_loads                 | 26.5 us                                                | 31.6 us: 1.19x slower                                          |
| genshi_xml                 | 50.2 ms                                                | 59.8 ms: 1.19x slower                                          |
| xml_etree_process          | 59.0 ms                                                | 70.6 ms: 1.20x slower                                          |
| hexiom                     | 6.17 ms                                                | 7.39 ms: 1.20x slower                                          |
| typing_runtime_protocols   | 163 us                                                 | 196 us: 1.20x slower                                           |
| scimark_monte_carlo        | 68.4 ms                                                | 82.4 ms: 1.20x slower                                          |
| nqueens                    | 80.1 ms                                                | 96.6 ms: 1.21x slower                                          |
| richards                   | 45.9 ms                                                | 55.5 ms: 1.21x slower                                          |
| django_template            | 34.7 ms                                                | 42.0 ms: 1.21x slower                                          |
| regex_v8                   | 20.6 ms                                                | 25.1 ms: 1.22x slower                                          |
| scimark_lu                 | 114 ms                                                 | 140 ms: 1.23x slower                                           |
| genshi_text                | 22.8 ms                                                | 28.0 ms: 1.23x slower                                          |
| create_gc_cycles           | 1.09 ms                                                | 1.35 ms: 1.24x slower                                          |
| richards_super             | 51.9 ms                                                | 64.7 ms: 1.25x slower                                          |
| json_dumps                 | 10.4 ms                                                | 13.0 ms: 1.26x slower                                          |
| meteor_contest             | 104 ms                                                 | 130 ms: 1.26x slower                                           |
| fannkuch                   | 372 ms                                                 | 487 ms: 1.31x slower                                           |
| telco                      | 6.53 ms                                                | 8.65 ms: 1.33x slower                                          |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.87 ms: 1.34x slower                                          |
| python_startup_no_site     | 7.16 ms                                                | 9.66 ms: 1.35x slower                                          |
| coverage                   | 71.4 ms                                                | 97.3 ms: 1.36x slower                                          |
| mako                       | 11.0 ms                                                | 15.7 ms: 1.42x slower                                          |
| nbody                      | 89.3 ms                                                | 130 ms: 1.46x slower                                           |
| python_startup             | 9.93 ms                                                | 15.4 ms: 1.55x slower                                          |
| bench_thread_pool          | 941 us                                                 | 3.32 ms: 3.52x slower                                          |
| bench_mp_pool              | 10.8 ms                                                | 95.1 ms: 8.81x slower                                          |
| Geometric mean             | (ref)                                                  | 1.09x slower                                                   |

Benchmark hidden because not significant (3): pylint, generators, comprehensions
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250214-3.14.0a5+-c00cd86-NOGIL/bm-20250214-vultr-x86_64-DinoV-noclock_clear-3.14.0a5+-c00cd86.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.047x slower

# HPT report

- Reliability score: 99.98% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.36x