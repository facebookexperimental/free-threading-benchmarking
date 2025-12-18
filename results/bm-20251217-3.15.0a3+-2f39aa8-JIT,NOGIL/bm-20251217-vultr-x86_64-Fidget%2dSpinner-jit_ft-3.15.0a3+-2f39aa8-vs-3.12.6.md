# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: jit_ft
- machine: linux-x86_64
- commit hash: 2f39aa8
- commit date: 2025-12-17
- overall geometric mean: 1.008x slower
- HPT reliability: 54.01%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.44x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251217-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-2f39aa8 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 278 ms: 1.06x slower                                               |
| docutils       | 2.64 sec                                               | 2.94 sec: 1.11x slower                                             |
| html5lib       | 63.6 ms                                                | 70.3 ms: 1.10x slower                                              |
| Geometric mean | (ref)                                                  | 1.09x slower                                                       |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251217-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-2f39aa8 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 607 ms: 1.83x faster                                               |
| async_tree_io              | 1.08 sec                                               | 633 ms: 1.71x faster                                               |
| async_tree_memoization_tg  | 560 ms                                                 | 329 ms: 1.70x faster                                               |
| async_tree_none_tg         | 446 ms                                                 | 264 ms: 1.69x faster                                               |
| async_tree_none            | 464 ms                                                 | 286 ms: 1.62x faster                                               |
| async_tree_memoization     | 555 ms                                                 | 352 ms: 1.58x faster                                               |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 533 ms: 1.36x faster                                               |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 556 ms: 1.29x faster                                               |
| asyncio_websockets         | 517 ms                                                 | 511 ms: 1.01x faster                                               |
| coroutines                 | 23.9 ms                                                | 24.2 ms: 1.01x slower                                              |
| async_generators           | 384 ms                                                 | 391 ms: 1.02x slower                                               |
| Geometric mean             | (ref)                                                  | 1.40x faster                                                       |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251217-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-2f39aa8 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 64.2 ms: 1.26x faster                                              |
| pidigits       | 184 ms                                                 | 192 ms: 1.04x slower                                               |
| nbody          | 89.3 ms                                                | 105 ms: 1.17x slower                                               |
| Geometric mean | (ref)                                                  | 1.01x faster                                                       |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251217-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-2f39aa8 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.92 ms: 1.08x faster                                              |
| regex_compile  | 142 ms                                                 | 146 ms: 1.03x slower                                               |
| regex_v8       | 20.6 ms                                                | 21.9 ms: 1.06x slower                                              |
| regex_dna      | 168 ms                                                 | 180 ms: 1.07x slower                                               |
| Geometric mean | (ref)                                                  | 1.02x slower                                                       |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251217-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-2f39aa8 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.7 ms: 1.10x faster                                              |
| unpickle_pure_python | 221 us                                                 | 204 us: 1.08x faster                                               |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.07x faster                                               |
| pickle_pure_python   | 308 us                                                 | 312 us: 1.01x slower                                               |
| tomli_loads          | 2.11 sec                                               | 2.15 sec: 1.02x slower                                             |
| json_dumps           | 10.4 ms                                                | 10.7 ms: 1.04x slower                                              |
| xml_etree_generate   | 85.2 ms                                                | 91.0 ms: 1.07x slower                                              |
| xml_etree_process    | 59.0 ms                                                | 63.6 ms: 1.08x slower                                              |
| json_loads           | 26.5 us                                                | 32.2 us: 1.21x slower                                              |
| Geometric mean       | (ref)                                                  | 1.02x slower                                                       |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251217-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-2f39aa8 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.56 ms: 1.34x slower                                              |
| python_startup         | 9.93 ms                                                | 15.9 ms: 1.60x slower                                              |
| Geometric mean         | (ref)                                                  | 1.46x slower                                                       |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251217-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-2f39aa8 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 41.1 ms: 1.19x slower                                              |
| genshi_text     | 22.8 ms                                                | 28.0 ms: 1.23x slower                                              |
| genshi_xml      | 50.2 ms                                                | 67.7 ms: 1.35x slower                                              |
| mako            | 11.0 ms                                                | 14.9 ms: 1.35x slower                                              |
| Geometric mean  | (ref)                                                  | 1.28x slower                                                       |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251217-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-2f39aa8 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| richards                   | 45.9 ms                                                | 22.7 ms: 2.02x faster                                              |
| richards_super             | 51.9 ms                                                | 27.8 ms: 1.86x faster                                              |
| gc_traversal               | 3.46 ms                                                | 1.89 ms: 1.83x faster                                              |
| async_tree_io_tg           | 1.11 sec                                               | 607 ms: 1.83x faster                                               |
| async_tree_io              | 1.08 sec                                               | 633 ms: 1.71x faster                                               |
| async_tree_memoization_tg  | 560 ms                                                 | 329 ms: 1.70x faster                                               |
| async_tree_none_tg         | 446 ms                                                 | 264 ms: 1.69x faster                                               |
| async_tree_none            | 464 ms                                                 | 286 ms: 1.62x faster                                               |
| async_tree_memoization     | 555 ms                                                 | 352 ms: 1.58x faster                                               |
| mdp                        | 2.42 sec                                               | 1.58 sec: 1.53x faster                                             |
| bench_mp_pool              | 10.8 ms                                                | 7.13 ms: 1.51x faster                                              |
| deepcopy_memo              | 40.3 us                                                | 29.3 us: 1.37x faster                                              |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 533 ms: 1.36x faster                                               |
| logging_silent             | 109 ns                                                 | 83.3 ns: 1.31x faster                                              |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 556 ms: 1.29x faster                                               |
| float                      | 80.8 ms                                                | 64.2 ms: 1.26x faster                                              |
| deepcopy                   | 352 us                                                 | 281 us: 1.25x faster                                               |
| go                         | 139 ms                                                 | 112 ms: 1.24x faster                                               |
| pathlib                    | 21.5 ms                                                | 18.0 ms: 1.19x faster                                              |
| scimark_fft                | 342 ms                                                 | 292 ms: 1.17x faster                                               |
| scimark_sor                | 130 ms                                                 | 114 ms: 1.14x faster                                               |
| bpe_tokeniser              | 4.74 sec                                               | 4.15 sec: 1.14x faster                                             |
| spectral_norm              | 110 ms                                                 | 99.9 ms: 1.10x faster                                              |
| xml_etree_iterparse        | 96.7 ms                                                | 87.7 ms: 1.10x faster                                              |
| sqlite_synth               | 2.20 us                                                | 2.02 us: 1.09x faster                                              |
| deltablue                  | 3.45 ms                                                | 3.17 ms: 1.09x faster                                              |
| regex_effbot               | 3.17 ms                                                | 2.92 ms: 1.08x faster                                              |
| unpickle_pure_python       | 221 us                                                 | 204 us: 1.08x faster                                               |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.07x faster                                               |
| dulwich_log                | 78.9 ms                                                | 74.6 ms: 1.06x faster                                              |
| deepcopy_reduce            | 3.08 us                                                | 2.92 us: 1.05x faster                                              |
| pyflate                    | 448 ms                                                 | 425 ms: 1.05x faster                                               |
| generators                 | 32.2 ms                                                | 31.0 ms: 1.04x faster                                              |
| pprint_safe_repr           | 743 ms                                                 | 721 ms: 1.03x faster                                               |
| chaos                      | 62.8 ms                                                | 61.2 ms: 1.03x faster                                              |
| comprehensions             | 19.8 us                                                | 19.4 us: 1.02x faster                                              |
| asyncio_websockets         | 517 ms                                                 | 511 ms: 1.01x faster                                               |
| pycparser                  | 1.17 sec                                               | 1.16 sec: 1.01x faster                                             |
| scimark_monte_carlo        | 68.4 ms                                                | 68.7 ms: 1.00x slower                                              |
| coroutines                 | 23.9 ms                                                | 24.2 ms: 1.01x slower                                              |
| pickle_pure_python         | 308 us                                                 | 312 us: 1.01x slower                                               |
| async_generators           | 384 ms                                                 | 391 ms: 1.02x slower                                               |
| pprint_pformat             | 1.52 sec                                               | 1.55 sec: 1.02x slower                                             |
| tomli_loads                | 2.11 sec                                               | 2.15 sec: 1.02x slower                                             |
| regex_compile              | 142 ms                                                 | 146 ms: 1.03x slower                                               |
| json_dumps                 | 10.4 ms                                                | 10.7 ms: 1.04x slower                                              |
| pylint                     | 319 ms                                                 | 331 ms: 1.04x slower                                               |
| raytrace                   | 299 ms                                                 | 311 ms: 1.04x slower                                               |
| pidigits                   | 184 ms                                                 | 192 ms: 1.04x slower                                               |
| logging_simple             | 6.63 us                                                | 6.94 us: 1.05x slower                                              |
| 2to3                       | 264 ms                                                 | 278 ms: 1.06x slower                                               |
| logging_format             | 7.35 us                                                | 7.79 us: 1.06x slower                                              |
| regex_v8                   | 20.6 ms                                                | 21.9 ms: 1.06x slower                                              |
| xml_etree_generate         | 85.2 ms                                                | 91.0 ms: 1.07x slower                                              |
| json                       | 5.02 ms                                                | 5.38 ms: 1.07x slower                                              |
| regex_dna                  | 168 ms                                                 | 180 ms: 1.07x slower                                               |
| xml_etree_process          | 59.0 ms                                                | 63.6 ms: 1.08x slower                                              |
| html5lib                   | 63.6 ms                                                | 70.3 ms: 1.10x slower                                              |
| scimark_lu                 | 114 ms                                                 | 126 ms: 1.11x slower                                               |
| thrift                     | 791 us                                                 | 877 us: 1.11x slower                                               |
| crypto_pyaes               | 76.6 ms                                                | 85.0 ms: 1.11x slower                                              |
| docutils                   | 2.64 sec                                               | 2.94 sec: 1.11x slower                                             |
| sympy_integrate            | 20.5 ms                                                | 23.2 ms: 1.13x slower                                              |
| fannkuch                   | 372 ms                                                 | 429 ms: 1.15x slower                                               |
| meteor_contest             | 104 ms                                                 | 121 ms: 1.16x slower                                               |
| hexiom                     | 6.17 ms                                                | 7.19 ms: 1.17x slower                                              |
| sympy_sum                  | 166 ms                                                 | 194 ms: 1.17x slower                                               |
| nbody                      | 89.3 ms                                                | 105 ms: 1.17x slower                                               |
| django_template            | 34.7 ms                                                | 41.1 ms: 1.19x slower                                              |
| sympy_str                  | 292 ms                                                 | 353 ms: 1.21x slower                                               |
| json_loads                 | 26.5 us                                                | 32.2 us: 1.21x slower                                              |
| typing_runtime_protocols   | 163 us                                                 | 200 us: 1.22x slower                                               |
| genshi_text                | 22.8 ms                                                | 28.0 ms: 1.23x slower                                              |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.44 ms: 1.24x slower                                              |
| sympy_expand               | 468 ms                                                 | 585 ms: 1.25x slower                                               |
| nqueens                    | 80.1 ms                                                | 100 ms: 1.25x slower                                               |
| python_startup_no_site     | 7.16 ms                                                | 9.56 ms: 1.34x slower                                              |
| create_gc_cycles           | 1.09 ms                                                | 1.46 ms: 1.34x slower                                              |
| genshi_xml                 | 50.2 ms                                                | 67.7 ms: 1.35x slower                                              |
| mako                       | 11.0 ms                                                | 14.9 ms: 1.35x slower                                              |
| coverage                   | 71.4 ms                                                | 111 ms: 1.56x slower                                               |
| bench_thread_pool          | 941 us                                                 | 1.48 ms: 1.57x slower                                              |
| python_startup             | 9.93 ms                                                | 15.9 ms: 1.60x slower                                              |
| telco                      | 6.53 ms                                                | 176 ms: 26.93x slower                                              |
| Geometric mean             | (ref)                                                  | 1.01x slower                                                       |
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251217-3.15.0a3+-2f39aa8-JIT,NOGIL/bm-20251217-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-2f39aa8.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.008x slower

# HPT report

- Reliability score: 54.01% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.44x