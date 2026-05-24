# Results vs. 3.12.6

- fork: python
- ref: a7d5a6cc179e2eabd780
- machine: linux-x86_64
- commit hash: a7d5a6c
- commit date: 2026-05-23
- overall geometric mean: 1.031x slower
- HPT reliability: 83.31%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.41x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260523-vultr-x86_64-python-a7d5a6cc179e2eabd780-3.16.0a0-a7d5a6c |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| docutils       | 2.64 sec                                               | 2.96 sec: 1.12x slower                                                |
| html5lib       | 63.6 ms                                                | 68.1 ms: 1.07x slower                                                 |
| Geometric mean | (ref)                                                  | 1.10x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260523-vultr-x86_64-python-a7d5a6cc179e2eabd780-3.16.0a0-a7d5a6c |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 691 ms: 1.61x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 708 ms: 1.53x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 396 ms: 1.41x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 328 ms: 1.36x faster                                                  |
| async_tree_none            | 464 ms                                                 | 348 ms: 1.34x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 423 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 576 ms: 1.25x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 592 ms: 1.21x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 510 ms: 1.01x faster                                                  |
| async_generators           | 384 ms                                                 | 388 ms: 1.01x slower                                                  |
| coroutines                 | 23.9 ms                                                | 24.7 ms: 1.03x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.26x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260523-vultr-x86_64-python-a7d5a6cc179e2eabd780-3.16.0a0-a7d5a6c |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 188 ms: 1.02x slower                                                  |
| float          | 80.8 ms                                                | 88.6 ms: 1.10x slower                                                 |
| nbody          | 89.3 ms                                                | 127 ms: 1.42x slower                                                  |
| Geometric mean | (ref)                                                  | 1.17x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260523-vultr-x86_64-python-a7d5a6cc179e2eabd780-3.16.0a0-a7d5a6c |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.94 ms: 1.08x faster                                                 |
| regex_v8       | 20.6 ms                                                | 20.3 ms: 1.01x faster                                                 |
| regex_compile  | 142 ms                                                 | 144 ms: 1.01x slower                                                  |
| regex_dna      | 168 ms                                                 | 175 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260523-vultr-x86_64-python-a7d5a6cc179e2eabd780-3.16.0a0-a7d5a6c |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.92 sec: 1.10x faster                                                |
| xml_etree_iterparse  | 96.7 ms                                                | 95.2 ms: 1.02x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 140 ms: 1.01x slower                                                  |
| json_dumps           | 10.4 ms                                                | 11.1 ms: 1.07x slower                                                 |
| unpickle_pure_python | 221 us                                                 | 243 us: 1.10x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 343 us: 1.12x slower                                                  |
| json_loads           | 26.5 us                                                | 31.1 us: 1.17x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 102 ms: 1.20x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 75.6 ms: 1.28x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.09x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260523-vultr-x86_64-python-a7d5a6cc179e2eabd780-3.16.0a0-a7d5a6c |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 40.6 ms: 1.17x slower                                                 |
| mako            | 11.0 ms                                                | 16.0 ms: 1.45x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.31x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260523-vultr-x86_64-python-a7d5a6cc179e2eabd780-3.16.0a0-a7d5a6c |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 319 ms                                                 | 132 ms: 2.40x faster                                                  |
| mdp                        | 2.42 sec                                               | 1.32 sec: 1.83x faster                                                |
| gc_traversal               | 3.46 ms                                                | 1.94 ms: 1.78x faster                                                 |
| async_tree_io_tg           | 1.11 sec                                               | 691 ms: 1.61x faster                                                  |
| bench_mp_pool              | 10.8 ms                                                | 6.98 ms: 1.55x faster                                                 |
| async_tree_io              | 1.08 sec                                               | 708 ms: 1.53x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 396 ms: 1.41x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 328 ms: 1.36x faster                                                  |
| async_tree_none            | 464 ms                                                 | 348 ms: 1.34x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 423 ms: 1.31x faster                                                  |
| deepcopy                   | 352 us                                                 | 271 us: 1.30x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 31.3 us: 1.29x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 576 ms: 1.25x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 592 ms: 1.21x faster                                                  |
| pathlib                    | 21.5 ms                                                | 18.1 ms: 1.19x faster                                                 |
| go                         | 139 ms                                                 | 122 ms: 1.14x faster                                                  |
| typing_runtime_protocols   | 163 us                                                 | 144 us: 1.14x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 1.95 us: 1.13x faster                                                 |
| comprehensions             | 19.8 us                                                | 17.6 us: 1.13x faster                                                 |
| tomli_loads                | 2.11 sec                                               | 1.92 sec: 1.10x faster                                                |
| dulwich_log                | 78.9 ms                                                | 72.0 ms: 1.09x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.39 sec: 1.08x faster                                                |
| regex_effbot               | 3.17 ms                                                | 2.94 ms: 1.08x faster                                                 |
| scimark_sor                | 130 ms                                                 | 121 ms: 1.07x faster                                                  |
| logging_silent             | 109 ns                                                 | 102 ns: 1.07x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.97 us: 1.04x faster                                                 |
| pycparser                  | 1.17 sec                                               | 1.14 sec: 1.03x faster                                                |
| spectral_norm              | 110 ms                                                 | 108 ms: 1.02x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 95.2 ms: 1.02x faster                                                 |
| chaos                      | 62.8 ms                                                | 61.9 ms: 1.02x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 510 ms: 1.01x faster                                                  |
| regex_v8                   | 20.6 ms                                                | 20.3 ms: 1.01x faster                                                 |
| scimark_fft                | 342 ms                                                 | 343 ms: 1.01x slower                                                  |
| xml_etree_parse            | 139 ms                                                 | 140 ms: 1.01x slower                                                  |
| generators                 | 32.2 ms                                                | 32.5 ms: 1.01x slower                                                 |
| async_generators           | 384 ms                                                 | 388 ms: 1.01x slower                                                  |
| regex_compile              | 142 ms                                                 | 144 ms: 1.01x slower                                                  |
| logging_simple             | 6.63 us                                                | 6.73 us: 1.02x slower                                                 |
| pidigits                   | 184 ms                                                 | 188 ms: 1.02x slower                                                  |
| coroutines                 | 23.9 ms                                                | 24.7 ms: 1.03x slower                                                 |
| pyflate                    | 448 ms                                                 | 464 ms: 1.04x slower                                                  |
| logging_format             | 7.35 us                                                | 7.66 us: 1.04x slower                                                 |
| regex_dna                  | 168 ms                                                 | 175 ms: 1.05x slower                                                  |
| hexiom                     | 6.17 ms                                                | 6.51 ms: 1.06x slower                                                 |
| json                       | 5.02 ms                                                | 5.36 ms: 1.07x slower                                                 |
| html5lib                   | 63.6 ms                                                | 68.1 ms: 1.07x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 11.1 ms: 1.07x slower                                                 |
| sympy_integrate            | 20.5 ms                                                | 22.0 ms: 1.07x slower                                                 |
| deltablue                  | 3.45 ms                                                | 3.73 ms: 1.08x slower                                                 |
| sympy_str                  | 292 ms                                                 | 317 ms: 1.09x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 180 ms: 1.09x slower                                                  |
| pprint_safe_repr           | 743 ms                                                 | 812 ms: 1.09x slower                                                  |
| nqueens                    | 80.1 ms                                                | 87.5 ms: 1.09x slower                                                 |
| float                      | 80.8 ms                                                | 88.6 ms: 1.10x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 243 us: 1.10x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.67 sec: 1.10x slower                                                |
| pickle_pure_python         | 308 us                                                 | 343 us: 1.12x slower                                                  |
| docutils                   | 2.64 sec                                               | 2.96 sec: 1.12x slower                                                |
| scimark_lu                 | 114 ms                                                 | 128 ms: 1.12x slower                                                  |
| sympy_expand               | 468 ms                                                 | 535 ms: 1.15x slower                                                  |
| richards                   | 45.9 ms                                                | 52.6 ms: 1.15x slower                                                 |
| thrift                     | 791 us                                                 | 911 us: 1.15x slower                                                  |
| richards_super             | 51.9 ms                                                | 60.2 ms: 1.16x slower                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 79.7 ms: 1.16x slower                                                 |
| json_loads                 | 26.5 us                                                | 31.1 us: 1.17x slower                                                 |
| django_template            | 34.7 ms                                                | 40.6 ms: 1.17x slower                                                 |
| crypto_pyaes               | 76.6 ms                                                | 89.9 ms: 1.17x slower                                                 |
| xml_etree_generate         | 85.2 ms                                                | 102 ms: 1.20x slower                                                  |
| meteor_contest             | 104 ms                                                 | 126 ms: 1.21x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.38 ms: 1.22x slower                                                 |
| fannkuch                   | 372 ms                                                 | 467 ms: 1.26x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 75.6 ms: 1.28x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.53 ms: 1.40x slower                                                 |
| nbody                      | 89.3 ms                                                | 127 ms: 1.42x slower                                                  |
| mako                       | 11.0 ms                                                | 16.0 ms: 1.45x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.48 ms: 1.57x slower                                                 |
| coverage                   | 71.4 ms                                                | 115 ms: 1.62x slower                                                  |
| telco                      | 6.53 ms                                                | 174 ms: 26.70x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.03x slower                                                          |

Benchmark hidden because not significant (1): raytrace
Ignored benchmarks (26) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260523-3.16.0a0-a7d5a6c-NOGIL/bm-20260523-vultr-x86_64-python-a7d5a6cc179e2eabd780-3.16.0a0-a7d5a6c.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.031x slower

# HPT report

- Reliability score: 83.31% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.41x