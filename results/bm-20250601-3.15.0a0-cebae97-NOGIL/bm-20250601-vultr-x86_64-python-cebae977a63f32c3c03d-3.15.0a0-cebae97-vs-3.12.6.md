# Results vs. 3.12.6

- fork: python
- ref: cebae977a63f32c3c03d
- machine: linux-x86_64
- commit hash: cebae97
- commit date: 2025-06-01
- overall geometric mean: 1.013x faster
- HPT reliability: 84.76%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.42x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 284 ms: 1.08x slower                                                  |
| docutils       | 2.64 sec                                               | 2.70 sec: 1.02x slower                                                |
| html5lib       | 63.6 ms                                                | 67.0 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                  | 1.05x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 528 ms: 2.10x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 287 ms: 1.95x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 229 ms: 1.95x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 559 ms: 1.94x faster                                                  |
| async_tree_none            | 464 ms                                                 | 261 ms: 1.78x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 316 ms: 1.75x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 475 ms: 1.52x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 503 ms: 1.42x faster                                                  |
| coroutines                 | 23.9 ms                                                | 22.8 ms: 1.05x faster                                                 |
| async_generators           | 384 ms                                                 | 370 ms: 1.04x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 516 ms: 1.00x faster                                                  |
| asyncio_tcp                | 519 ms                                                 | 535 ms: 1.03x slower                                                  |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.79 sec: 1.19x slower                                                |
| Geometric mean             | (ref)                                                  | 1.42x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 69.4 ms: 1.16x faster                                                 |
| pidigits       | 184 ms                                                 | 195 ms: 1.06x slower                                                  |
| nbody          | 89.3 ms                                                | 118 ms: 1.33x slower                                                  |
| Geometric mean | (ref)                                                  | 1.06x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.68 ms: 1.18x faster                                                 |
| regex_v8       | 20.6 ms                                                | 20.2 ms: 1.02x faster                                                 |
| regex_compile  | 142 ms                                                 | 144 ms: 1.01x slower                                                  |
| regex_dna      | 168 ms                                                 | 175 ms: 1.04x slower                                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.2 ms: 1.11x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 2.13 sec: 1.01x slower                                                |
| pickle_list          | 4.77 us                                                | 4.95 us: 1.04x slower                                                 |
| unpickle_pure_python | 221 us                                                 | 230 us: 1.04x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 335 us: 1.09x slower                                                  |
| unpickle             | 14.1 us                                                | 15.3 us: 1.09x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 94.9 ms: 1.11x slower                                                 |
| pickle               | 10.9 us                                                | 12.3 us: 1.12x slower                                                 |
| unpickle_list        | 4.67 us                                                | 5.38 us: 1.15x slower                                                 |
| json_dumps           | 10.4 ms                                                | 12.0 ms: 1.16x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 68.7 ms: 1.16x slower                                                 |
| json_loads           | 26.5 us                                                | 31.5 us: 1.19x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.07x slower                                                          |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.62 ms: 1.34x slower                                                 |
| python_startup         | 9.93 ms                                                | 16.0 ms: 1.62x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.47x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 39.8 ms: 1.15x slower                                                 |
| genshi_xml      | 50.2 ms                                                | 57.8 ms: 1.15x slower                                                 |
| genshi_text     | 22.8 ms                                                | 26.6 ms: 1.16x slower                                                 |
| mako            | 11.0 ms                                                | 15.7 ms: 1.42x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.22x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 528 ms: 2.10x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 287 ms: 1.95x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 229 ms: 1.95x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 559 ms: 1.94x faster                                                  |
| mdp                        | 2.42 sec                                               | 1.32 sec: 1.83x faster                                                |
| gc_traversal               | 3.46 ms                                                | 1.93 ms: 1.79x faster                                                 |
| async_tree_none            | 464 ms                                                 | 261 ms: 1.78x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 316 ms: 1.75x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 475 ms: 1.52x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 503 ms: 1.42x faster                                                  |
| deepcopy                   | 352 us                                                 | 291 us: 1.21x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.68 ms: 1.18x faster                                                 |
| deepcopy_memo              | 40.3 us                                                | 34.5 us: 1.17x faster                                                 |
| float                      | 80.8 ms                                                | 69.4 ms: 1.16x faster                                                 |
| go                         | 139 ms                                                 | 121 ms: 1.15x faster                                                  |
| comprehensions             | 19.8 us                                                | 17.6 us: 1.13x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 87.2 ms: 1.11x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 71.4 ms: 1.11x faster                                                 |
| pathlib                    | 21.5 ms                                                | 19.5 ms: 1.10x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.33 sec: 1.09x faster                                                |
| generators                 | 32.2 ms                                                | 29.7 ms: 1.08x faster                                                 |
| sqlite_synth               | 2.20 us                                                | 2.04 us: 1.08x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                                  |
| scimark_sor                | 130 ms                                                 | 122 ms: 1.06x faster                                                  |
| coroutines                 | 23.9 ms                                                | 22.8 ms: 1.05x faster                                                 |
| pycparser                  | 1.17 sec                                               | 1.12 sec: 1.04x faster                                                |
| async_generators           | 384 ms                                                 | 370 ms: 1.04x faster                                                  |
| pylint                     | 319 ms                                                 | 309 ms: 1.03x faster                                                  |
| regex_v8                   | 20.6 ms                                                | 20.2 ms: 1.02x faster                                                 |
| chaos                      | 62.8 ms                                                | 61.9 ms: 1.01x faster                                                 |
| raytrace                   | 299 ms                                                 | 296 ms: 1.01x faster                                                  |
| spectral_norm              | 110 ms                                                 | 109 ms: 1.01x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 3.06 us: 1.01x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 516 ms: 1.00x faster                                                  |
| regex_compile              | 142 ms                                                 | 144 ms: 1.01x slower                                                  |
| tomli_loads                | 2.11 sec                                               | 2.13 sec: 1.01x slower                                                |
| unpack_sequence            | 52.1 ns                                                | 52.9 ns: 1.02x slower                                                 |
| docutils                   | 2.64 sec                                               | 2.70 sec: 1.02x slower                                                |
| hexiom                     | 6.17 ms                                                | 6.33 ms: 1.03x slower                                                 |
| asyncio_tcp                | 519 ms                                                 | 535 ms: 1.03x slower                                                  |
| pickle_list                | 4.77 us                                                | 4.95 us: 1.04x slower                                                 |
| pyflate                    | 448 ms                                                 | 465 ms: 1.04x slower                                                  |
| regex_dna                  | 168 ms                                                 | 175 ms: 1.04x slower                                                  |
| unpickle_pure_python       | 221 us                                                 | 230 us: 1.04x slower                                                  |
| html5lib                   | 63.6 ms                                                | 67.0 ms: 1.05x slower                                                 |
| deltablue                  | 3.45 ms                                                | 3.63 ms: 1.05x slower                                                 |
| pidigits                   | 184 ms                                                 | 195 ms: 1.06x slower                                                  |
| nqueens                    | 80.1 ms                                                | 85.4 ms: 1.07x slower                                                 |
| scimark_fft                | 342 ms                                                 | 365 ms: 1.07x slower                                                  |
| json                       | 5.02 ms                                                | 5.37 ms: 1.07x slower                                                 |
| sympy_integrate            | 20.5 ms                                                | 22.0 ms: 1.07x slower                                                 |
| 2to3                       | 264 ms                                                 | 284 ms: 1.08x slower                                                  |
| sympy_str                  | 292 ms                                                 | 315 ms: 1.08x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 181 ms: 1.09x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 335 us: 1.09x slower                                                  |
| unpickle                   | 14.1 us                                                | 15.3 us: 1.09x slower                                                 |
| crypto_pyaes               | 76.6 ms                                                | 85.1 ms: 1.11x slower                                                 |
| xml_etree_generate         | 85.2 ms                                                | 94.9 ms: 1.11x slower                                                 |
| richards                   | 45.9 ms                                                | 51.5 ms: 1.12x slower                                                 |
| pickle                     | 10.9 us                                                | 12.3 us: 1.12x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 128 ms: 1.12x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 77.1 ms: 1.13x slower                                                 |
| thrift                     | 791 us                                                 | 893 us: 1.13x slower                                                  |
| sympy_expand               | 468 ms                                                 | 528 ms: 1.13x slower                                                  |
| richards_super             | 51.9 ms                                                | 58.7 ms: 1.13x slower                                                 |
| django_template            | 34.7 ms                                                | 39.8 ms: 1.15x slower                                                 |
| unpickle_list              | 4.67 us                                                | 5.38 us: 1.15x slower                                                 |
| genshi_xml                 | 50.2 ms                                                | 57.8 ms: 1.15x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 12.0 ms: 1.16x slower                                                 |
| meteor_contest             | 104 ms                                                 | 120 ms: 1.16x slower                                                  |
| genshi_text                | 22.8 ms                                                | 26.6 ms: 1.16x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 68.7 ms: 1.16x slower                                                 |
| typing_runtime_protocols   | 163 us                                                 | 191 us: 1.17x slower                                                  |
| logging_simple             | 6.63 us                                                | 7.79 us: 1.18x slower                                                 |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.79 sec: 1.19x slower                                                |
| json_loads                 | 26.5 us                                                | 31.5 us: 1.19x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 883 ms: 1.19x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.83 sec: 1.20x slower                                                |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.33 ms: 1.21x slower                                                 |
| logging_format             | 7.35 us                                                | 9.01 us: 1.23x slower                                                 |
| fannkuch                   | 372 ms                                                 | 459 ms: 1.23x slower                                                  |
| nbody                      | 89.3 ms                                                | 118 ms: 1.33x slower                                                  |
| telco                      | 6.53 ms                                                | 8.73 ms: 1.34x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 9.62 ms: 1.34x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.50 ms: 1.38x slower                                                 |
| mako                       | 11.0 ms                                                | 15.7 ms: 1.42x slower                                                 |
| coverage                   | 71.4 ms                                                | 111 ms: 1.56x slower                                                  |
| python_startup             | 9.93 ms                                                | 16.0 ms: 1.62x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.12 ms: 3.31x slower                                                 |
| logging_silent             | 109 ns                                                 | 533 ns: 4.89x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 103 ms: 9.49x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.05x slower                                                          |

Benchmark hidden because not significant (1): pickle_dict
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20250601-3.15.0a0-cebae97-NOGIL/bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.013x faster

# HPT report

- Reliability score: 84.76% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.42x