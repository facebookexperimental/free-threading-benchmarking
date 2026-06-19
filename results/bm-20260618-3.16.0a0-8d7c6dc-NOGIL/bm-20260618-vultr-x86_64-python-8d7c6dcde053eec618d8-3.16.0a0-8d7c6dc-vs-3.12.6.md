# Results vs. 3.12.6

- fork: python
- ref: 8d7c6dcde053eec618d8
- machine: linux-x86_64
- commit hash: 8d7c6dc
- commit date: 2026-06-18
- overall geometric mean: 1.035x slower
- HPT reliability: 89.84%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260618-vultr-x86_64-python-8d7c6dcde053eec618d8-3.16.0a0-8d7c6dc |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 295 ms: 1.12x slower                                                  |
| docutils       | 2.64 sec                                               | 2.94 sec: 1.11x slower                                                |
| html5lib       | 63.6 ms                                                | 68.8 ms: 1.08x slower                                                 |
| Geometric mean | (ref)                                                  | 1.11x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260618-vultr-x86_64-python-8d7c6dcde053eec618d8-3.16.0a0-8d7c6dc |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 679 ms: 1.63x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 701 ms: 1.54x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 388 ms: 1.44x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 320 ms: 1.39x faster                                                  |
| async_tree_none            | 464 ms                                                 | 339 ms: 1.37x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 415 ms: 1.34x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 605 ms: 1.19x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 633 ms: 1.13x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 514 ms: 1.01x faster                                                  |
| async_generators           | 384 ms                                                 | 391 ms: 1.02x slower                                                  |
| coroutines                 | 23.9 ms                                                | 24.5 ms: 1.02x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.25x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260618-vultr-x86_64-python-8d7c6dcde053eec618d8-3.16.0a0-8d7c6dc |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 86.1 ms: 1.07x slower                                                 |
| pidigits       | 184 ms                                                 | 198 ms: 1.08x slower                                                  |
| nbody          | 89.3 ms                                                | 124 ms: 1.38x slower                                                  |
| Geometric mean | (ref)                                                  | 1.17x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260618-vultr-x86_64-python-8d7c6dcde053eec618d8-3.16.0a0-8d7c6dc |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.97 ms: 1.06x faster                                                 |
| regex_v8       | 20.6 ms                                                | 20.1 ms: 1.02x faster                                                 |
| regex_compile  | 142 ms                                                 | 141 ms: 1.01x faster                                                  |
| regex_dna      | 168 ms                                                 | 177 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260618-vultr-x86_64-python-8d7c6dcde053eec618d8-3.16.0a0-8d7c6dc |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.96 sec: 1.07x faster                                                |
| xml_etree_iterparse  | 96.7 ms                                                | 94.0 ms: 1.03x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 140 ms: 1.01x slower                                                  |
| json_dumps           | 10.4 ms                                                | 10.5 ms: 1.02x slower                                                 |
| unpickle_pure_python | 221 us                                                 | 238 us: 1.08x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 338 us: 1.10x slower                                                  |
| json_loads           | 26.5 us                                                | 30.0 us: 1.13x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 101 ms: 1.19x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 75.0 ms: 1.27x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.07x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260618-vultr-x86_64-python-8d7c6dcde053eec618d8-3.16.0a0-8d7c6dc |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.17 ms: 1.28x slower                                                 |
| python_startup         | 9.93 ms                                                | 15.4 ms: 1.55x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.41x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260618-vultr-x86_64-python-8d7c6dcde053eec618d8-3.16.0a0-8d7c6dc |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 40.1 ms: 1.16x slower                                                 |
| mako            | 11.0 ms                                                | 16.1 ms: 1.46x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.30x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260618-vultr-x86_64-python-8d7c6dcde053eec618d8-3.16.0a0-8d7c6dc |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 319 ms                                                 | 132 ms: 2.42x faster                                                  |
| gc_traversal               | 3.46 ms                                                | 1.77 ms: 1.96x faster                                                 |
| mdp                        | 2.42 sec                                               | 1.31 sec: 1.84x faster                                                |
| async_tree_io_tg           | 1.11 sec                                               | 679 ms: 1.63x faster                                                  |
| bench_mp_pool              | 10.8 ms                                                | 6.79 ms: 1.59x faster                                                 |
| async_tree_io              | 1.08 sec                                               | 701 ms: 1.54x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 388 ms: 1.44x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 320 ms: 1.39x faster                                                  |
| async_tree_none            | 464 ms                                                 | 339 ms: 1.37x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 415 ms: 1.34x faster                                                  |
| deepcopy                   | 352 us                                                 | 270 us: 1.30x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 31.5 us: 1.28x faster                                                 |
| pathlib                    | 21.5 ms                                                | 17.9 ms: 1.20x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 605 ms: 1.19x faster                                                  |
| go                         | 139 ms                                                 | 121 ms: 1.15x faster                                                  |
| comprehensions             | 19.8 us                                                | 17.3 us: 1.15x faster                                                 |
| sqlite_synth               | 2.20 us                                                | 1.93 us: 1.14x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 633 ms: 1.13x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 70.2 ms: 1.12x faster                                                 |
| typing_runtime_protocols   | 163 us                                                 | 146 us: 1.12x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.40 sec: 1.08x faster                                                |
| tomli_loads                | 2.11 sec                                               | 1.96 sec: 1.07x faster                                                |
| scimark_sor                | 130 ms                                                 | 121 ms: 1.07x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.97 ms: 1.06x faster                                                 |
| logging_silent             | 109 ns                                                 | 104 ns: 1.04x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.96 us: 1.04x faster                                                 |
| spectral_norm              | 110 ms                                                 | 107 ms: 1.03x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 94.0 ms: 1.03x faster                                                 |
| regex_v8                   | 20.6 ms                                                | 20.1 ms: 1.02x faster                                                 |
| regex_compile              | 142 ms                                                 | 141 ms: 1.01x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.16 sec: 1.01x faster                                                |
| asyncio_websockets         | 517 ms                                                 | 514 ms: 1.01x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 140 ms: 1.01x slower                                                  |
| raytrace                   | 299 ms                                                 | 304 ms: 1.02x slower                                                  |
| async_generators           | 384 ms                                                 | 391 ms: 1.02x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 10.5 ms: 1.02x slower                                                 |
| scimark_fft                | 342 ms                                                 | 348 ms: 1.02x slower                                                  |
| coroutines                 | 23.9 ms                                                | 24.5 ms: 1.02x slower                                                 |
| pyflate                    | 448 ms                                                 | 459 ms: 1.03x slower                                                  |
| logging_simple             | 6.63 us                                                | 6.86 us: 1.03x slower                                                 |
| generators                 | 32.2 ms                                                | 33.4 ms: 1.04x slower                                                 |
| json                       | 5.02 ms                                                | 5.25 ms: 1.04x slower                                                 |
| logging_format             | 7.35 us                                                | 7.72 us: 1.05x slower                                                 |
| regex_dna                  | 168 ms                                                 | 177 ms: 1.05x slower                                                  |
| deltablue                  | 3.45 ms                                                | 3.66 ms: 1.06x slower                                                 |
| float                      | 80.8 ms                                                | 86.1 ms: 1.07x slower                                                 |
| sympy_integrate            | 20.5 ms                                                | 22.0 ms: 1.07x slower                                                 |
| hexiom                     | 6.17 ms                                                | 6.62 ms: 1.07x slower                                                 |
| pidigits                   | 184 ms                                                 | 198 ms: 1.08x slower                                                  |
| unpickle_pure_python       | 221 us                                                 | 238 us: 1.08x slower                                                  |
| sympy_str                  | 292 ms                                                 | 315 ms: 1.08x slower                                                  |
| html5lib                   | 63.6 ms                                                | 68.8 ms: 1.08x slower                                                 |
| sympy_sum                  | 166 ms                                                 | 180 ms: 1.09x slower                                                  |
| pprint_safe_repr           | 743 ms                                                 | 813 ms: 1.09x slower                                                  |
| nqueens                    | 80.1 ms                                                | 87.6 ms: 1.09x slower                                                 |
| pickle_pure_python         | 308 us                                                 | 338 us: 1.10x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.69 sec: 1.11x slower                                                |
| docutils                   | 2.64 sec                                               | 2.94 sec: 1.11x slower                                                |
| 2to3                       | 264 ms                                                 | 295 ms: 1.12x slower                                                  |
| sympy_expand               | 468 ms                                                 | 524 ms: 1.12x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 129 ms: 1.13x slower                                                  |
| json_loads                 | 26.5 us                                                | 30.0 us: 1.13x slower                                                 |
| richards                   | 45.9 ms                                                | 52.0 ms: 1.13x slower                                                 |
| richards_super             | 51.9 ms                                                | 59.0 ms: 1.14x slower                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 79.0 ms: 1.15x slower                                                 |
| django_template            | 34.7 ms                                                | 40.1 ms: 1.16x slower                                                 |
| crypto_pyaes               | 76.6 ms                                                | 89.8 ms: 1.17x slower                                                 |
| thrift                     | 791 us                                                 | 940 us: 1.19x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 101 ms: 1.19x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.27 ms: 1.20x slower                                                 |
| meteor_contest             | 104 ms                                                 | 127 ms: 1.23x slower                                                  |
| fannkuch                   | 372 ms                                                 | 470 ms: 1.26x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.38 ms: 1.26x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 75.0 ms: 1.27x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 9.17 ms: 1.28x slower                                                 |
| nbody                      | 89.3 ms                                                | 124 ms: 1.38x slower                                                  |
| mako                       | 11.0 ms                                                | 16.1 ms: 1.46x slower                                                 |
| python_startup             | 9.93 ms                                                | 15.4 ms: 1.55x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.47 ms: 1.57x slower                                                 |
| coverage                   | 71.4 ms                                                | 114 ms: 1.59x slower                                                  |
| telco                      | 6.53 ms                                                | 177 ms: 27.10x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.03x slower                                                          |

Benchmark hidden because not significant (1): chaos
Ignored benchmarks (23) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260618-3.16.0a0-8d7c6dc-NOGIL/bm-20260618-vultr-x86_64-python-8d7c6dcde053eec618d8-3.16.0a0-8d7c6dc.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.035x slower

# HPT report

- Reliability score: 89.84% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.36x