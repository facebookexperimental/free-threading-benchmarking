# Results vs. 3.12.6

- fork: python
- ref: 9ad0c7b0f14c5fcda6bf
- machine: linux-x86_64
- commit hash: 9ad0c7b
- commit date: 2025-05-13
- overall geometric mean: 1.015x faster
- HPT reliability: 90.96%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.42x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 285 ms: 1.08x slower                                                  |
| docutils       | 2.64 sec                                               | 2.70 sec: 1.02x slower                                                |
| html5lib       | 63.6 ms                                                | 65.4 ms: 1.03x slower                                                 |
| Geometric mean | (ref)                                                  | 1.04x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 517 ms: 2.15x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 282 ms: 1.99x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 545 ms: 1.99x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 225 ms: 1.98x faster                                                  |
| async_tree_none            | 464 ms                                                 | 257 ms: 1.81x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 308 ms: 1.80x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 481 ms: 1.50x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 508 ms: 1.41x faster                                                  |
| async_generators           | 384 ms                                                 | 367 ms: 1.05x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.0 ms: 1.04x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.55x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 69.4 ms: 1.16x faster                                                 |
| pidigits       | 184 ms                                                 | 190 ms: 1.03x slower                                                  |
| nbody          | 89.3 ms                                                | 117 ms: 1.31x slower                                                  |
| Geometric mean | (ref)                                                  | 1.05x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.82 ms: 1.12x faster                                                 |
| regex_v8       | 20.6 ms                                                | 20.8 ms: 1.01x slower                                                 |
| regex_compile  | 142 ms                                                 | 145 ms: 1.02x slower                                                  |
| regex_dna      | 168 ms                                                 | 181 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                  | 1.00x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 86.7 ms: 1.12x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 2.15 sec: 1.02x slower                                                |
| unpickle_pure_python | 221 us                                                 | 229 us: 1.04x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 334 us: 1.09x slower                                                  |
| json_dumps           | 10.4 ms                                                | 11.5 ms: 1.11x slower                                                 |
| json_loads           | 26.5 us                                                | 30.1 us: 1.13x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 97.0 ms: 1.14x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 69.6 ms: 1.18x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.06x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.60 ms: 1.34x slower                                                 |
| python_startup         | 9.93 ms                                                | 16.0 ms: 1.61x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.47x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 54.9 ms: 1.09x slower                                                 |
| genshi_text     | 22.8 ms                                                | 26.0 ms: 1.14x slower                                                 |
| django_template | 34.7 ms                                                | 39.6 ms: 1.14x slower                                                 |
| mako            | 11.0 ms                                                | 15.8 ms: 1.43x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.20x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 517 ms: 2.15x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 282 ms: 1.99x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 545 ms: 1.99x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 225 ms: 1.98x faster                                                  |
| mdp                        | 2.42 sec                                               | 1.33 sec: 1.82x faster                                                |
| gc_traversal               | 3.46 ms                                                | 1.91 ms: 1.81x faster                                                 |
| async_tree_none            | 464 ms                                                 | 257 ms: 1.81x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 308 ms: 1.80x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 481 ms: 1.50x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 508 ms: 1.41x faster                                                  |
| deepcopy                   | 352 us                                                 | 288 us: 1.22x faster                                                  |
| float                      | 80.8 ms                                                | 69.4 ms: 1.16x faster                                                 |
| deepcopy_memo              | 40.3 us                                                | 35.4 us: 1.14x faster                                                 |
| go                         | 139 ms                                                 | 123 ms: 1.13x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.82 ms: 1.12x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 86.7 ms: 1.12x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 72.0 ms: 1.10x faster                                                 |
| pathlib                    | 21.5 ms                                                | 19.7 ms: 1.09x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.44 sec: 1.07x faster                                                |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 2.07 us: 1.06x faster                                                 |
| deepcopy_reduce            | 3.08 us                                                | 2.92 us: 1.05x faster                                                 |
| scimark_sor                | 130 ms                                                 | 123 ms: 1.05x faster                                                  |
| async_generators           | 384 ms                                                 | 367 ms: 1.05x faster                                                  |
| generators                 | 32.2 ms                                                | 30.9 ms: 1.04x faster                                                 |
| pylint                     | 319 ms                                                 | 306 ms: 1.04x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.0 ms: 1.04x faster                                                 |
| pycparser                  | 1.17 sec                                               | 1.14 sec: 1.03x faster                                                |
| raytrace                   | 299 ms                                                 | 295 ms: 1.01x faster                                                  |
| comprehensions             | 19.8 us                                                | 19.6 us: 1.01x faster                                                 |
| regex_v8                   | 20.6 ms                                                | 20.8 ms: 1.01x slower                                                 |
| regex_compile              | 142 ms                                                 | 145 ms: 1.02x slower                                                  |
| tomli_loads                | 2.11 sec                                               | 2.15 sec: 1.02x slower                                                |
| docutils                   | 2.64 sec                                               | 2.70 sec: 1.02x slower                                                |
| html5lib                   | 63.6 ms                                                | 65.4 ms: 1.03x slower                                                 |
| deltablue                  | 3.45 ms                                                | 3.54 ms: 1.03x slower                                                 |
| pidigits                   | 184 ms                                                 | 190 ms: 1.03x slower                                                  |
| json                       | 5.02 ms                                                | 5.20 ms: 1.03x slower                                                 |
| spectral_norm              | 110 ms                                                 | 114 ms: 1.03x slower                                                  |
| unpickle_pure_python       | 221 us                                                 | 229 us: 1.04x slower                                                  |
| pprint_safe_repr           | 743 ms                                                 | 774 ms: 1.04x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.60 sec: 1.06x slower                                                |
| scimark_fft                | 342 ms                                                 | 362 ms: 1.06x slower                                                  |
| pyflate                    | 448 ms                                                 | 479 ms: 1.07x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 178 ms: 1.07x slower                                                  |
| regex_dna                  | 168 ms                                                 | 181 ms: 1.08x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 22.1 ms: 1.08x slower                                                 |
| sympy_str                  | 292 ms                                                 | 315 ms: 1.08x slower                                                  |
| 2to3                       | 264 ms                                                 | 285 ms: 1.08x slower                                                  |
| hexiom                     | 6.17 ms                                                | 6.69 ms: 1.08x slower                                                 |
| richards                   | 45.9 ms                                                | 49.9 ms: 1.09x slower                                                 |
| pickle_pure_python         | 308 us                                                 | 334 us: 1.09x slower                                                  |
| nqueens                    | 80.1 ms                                                | 87.6 ms: 1.09x slower                                                 |
| genshi_xml                 | 50.2 ms                                                | 54.9 ms: 1.09x slower                                                 |
| richards_super             | 51.9 ms                                                | 57.1 ms: 1.10x slower                                                 |
| thrift                     | 791 us                                                 | 873 us: 1.10x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 126 ms: 1.10x slower                                                  |
| crypto_pyaes               | 76.6 ms                                                | 84.7 ms: 1.11x slower                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 76.1 ms: 1.11x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 11.5 ms: 1.11x slower                                                 |
| sympy_expand               | 468 ms                                                 | 530 ms: 1.13x slower                                                  |
| json_loads                 | 26.5 us                                                | 30.1 us: 1.13x slower                                                 |
| xml_etree_generate         | 85.2 ms                                                | 97.0 ms: 1.14x slower                                                 |
| genshi_text                | 22.8 ms                                                | 26.0 ms: 1.14x slower                                                 |
| django_template            | 34.7 ms                                                | 39.6 ms: 1.14x slower                                                 |
| typing_runtime_protocols   | 163 us                                                 | 192 us: 1.18x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 69.6 ms: 1.18x slower                                                 |
| logging_simple             | 6.63 us                                                | 7.88 us: 1.19x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.26 ms: 1.20x slower                                                 |
| logging_format             | 7.35 us                                                | 8.81 us: 1.20x slower                                                 |
| meteor_contest             | 104 ms                                                 | 129 ms: 1.25x slower                                                  |
| fannkuch                   | 372 ms                                                 | 468 ms: 1.26x slower                                                  |
| nbody                      | 89.3 ms                                                | 117 ms: 1.31x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 9.60 ms: 1.34x slower                                                 |
| telco                      | 6.53 ms                                                | 8.77 ms: 1.34x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.49 ms: 1.36x slower                                                 |
| mako                       | 11.0 ms                                                | 15.8 ms: 1.43x slower                                                 |
| coverage                   | 71.4 ms                                                | 109 ms: 1.52x slower                                                  |
| python_startup             | 9.93 ms                                                | 16.0 ms: 1.61x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.13 ms: 3.32x slower                                                 |
| logging_silent             | 109 ns                                                 | 538 ns: 4.93x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 104 ms: 9.63x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.05x slower                                                          |

Benchmark hidden because not significant (2): chaos, asyncio_websockets
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250513-3.15.0a0-9ad0c7b-NOGIL/bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.015x faster

# HPT report

- Reliability score: 90.96% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.42x