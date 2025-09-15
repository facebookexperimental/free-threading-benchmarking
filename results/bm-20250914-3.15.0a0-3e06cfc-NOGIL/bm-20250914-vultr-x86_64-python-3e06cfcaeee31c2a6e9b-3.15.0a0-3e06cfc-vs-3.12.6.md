# Results vs. 3.12.6

- fork: python
- ref: 3e06cfcaeee31c2a6e9b
- machine: linux-x86_64
- commit hash: 3e06cfc
- commit date: 2025-09-14
- overall geometric mean: 1.018x slower
- HPT reliability: 85.76%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.41x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250914-vultr-x86_64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 281 ms: 1.07x slower                                                  |
| docutils       | 2.64 sec                                               | 2.68 sec: 1.02x slower                                                |
| html5lib       | 63.6 ms                                                | 66.8 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                  | 1.04x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250914-vultr-x86_64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 517 ms: 2.15x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 223 ms: 2.00x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 280 ms: 2.00x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 543 ms: 1.99x faster                                                  |
| async_tree_none            | 464 ms                                                 | 257 ms: 1.81x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 308 ms: 1.80x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 487 ms: 1.48x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 515 ms: 1.39x faster                                                  |
| async_generators           | 384 ms                                                 | 368 ms: 1.05x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 512 ms: 1.01x faster                                                  |
| coroutines                 | 23.9 ms                                                | 24.2 ms: 1.01x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.55x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250914-vultr-x86_64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 70.1 ms: 1.15x faster                                                 |
| pidigits       | 184 ms                                                 | 194 ms: 1.05x slower                                                  |
| nbody          | 89.3 ms                                                | 124 ms: 1.38x slower                                                  |
| Geometric mean | (ref)                                                  | 1.08x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250914-vultr-x86_64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.51 ms: 1.26x faster                                                 |
| regex_dna      | 168 ms                                                 | 159 ms: 1.06x faster                                                  |
| regex_v8       | 20.6 ms                                                | 20.1 ms: 1.02x faster                                                 |
| regex_compile  | 142 ms                                                 | 143 ms: 1.00x slower                                                  |
| Geometric mean | (ref)                                                  | 1.08x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250914-vultr-x86_64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.0 ms: 1.11x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 2.01 sec: 1.05x faster                                                |
| unpickle_pure_python | 221 us                                                 | 232 us: 1.05x slower                                                  |
| json_dumps           | 10.4 ms                                                | 11.0 ms: 1.06x slower                                                 |
| pickle_pure_python   | 308 us                                                 | 347 us: 1.13x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 98.7 ms: 1.16x slower                                                 |
| json_loads           | 26.5 us                                                | 31.4 us: 1.18x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 70.9 ms: 1.20x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.06x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250914-vultr-x86_64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.57 ms: 1.34x slower                                                 |
| python_startup         | 9.93 ms                                                | 15.7 ms: 1.58x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.45x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250914-vultr-x86_64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 26.6 ms: 1.16x slower                                                 |
| genshi_xml      | 50.2 ms                                                | 59.0 ms: 1.18x slower                                                 |
| django_template | 34.7 ms                                                | 41.1 ms: 1.18x slower                                                 |
| mako            | 11.0 ms                                                | 15.7 ms: 1.43x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.23x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250914-vultr-x86_64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 517 ms: 2.15x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 223 ms: 2.00x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 280 ms: 2.00x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 543 ms: 1.99x faster                                                  |
| mdp                        | 2.42 sec                                               | 1.31 sec: 1.85x faster                                                |
| async_tree_none            | 464 ms                                                 | 257 ms: 1.81x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 308 ms: 1.80x faster                                                  |
| gc_traversal               | 3.46 ms                                                | 1.95 ms: 1.77x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 487 ms: 1.48x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 515 ms: 1.39x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 30.7 us: 1.31x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.51 ms: 1.26x faster                                                 |
| deepcopy                   | 352 us                                                 | 279 us: 1.26x faster                                                  |
| pathlib                    | 21.5 ms                                                | 18.1 ms: 1.19x faster                                                 |
| go                         | 139 ms                                                 | 121 ms: 1.15x faster                                                  |
| float                      | 80.8 ms                                                | 70.1 ms: 1.15x faster                                                 |
| comprehensions             | 19.8 us                                                | 17.6 us: 1.13x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 87.0 ms: 1.11x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 72.1 ms: 1.09x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.40 sec: 1.08x faster                                                |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                                  |
| logging_silent             | 109 ns                                                 | 103 ns: 1.06x faster                                                  |
| regex_dna                  | 168 ms                                                 | 159 ms: 1.06x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 2.09 us: 1.05x faster                                                 |
| tomli_loads                | 2.11 sec                                               | 2.01 sec: 1.05x faster                                                |
| async_generators           | 384 ms                                                 | 368 ms: 1.05x faster                                                  |
| generators                 | 32.2 ms                                                | 30.9 ms: 1.04x faster                                                 |
| scimark_sor                | 130 ms                                                 | 125 ms: 1.04x faster                                                  |
| pylint                     | 319 ms                                                 | 307 ms: 1.04x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.99 us: 1.03x faster                                                 |
| regex_v8                   | 20.6 ms                                                | 20.1 ms: 1.02x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 512 ms: 1.01x faster                                                  |
| regex_compile              | 142 ms                                                 | 143 ms: 1.00x slower                                                  |
| raytrace                   | 299 ms                                                 | 301 ms: 1.01x slower                                                  |
| chaos                      | 62.8 ms                                                | 63.5 ms: 1.01x slower                                                 |
| coroutines                 | 23.9 ms                                                | 24.2 ms: 1.01x slower                                                 |
| docutils                   | 2.64 sec                                               | 2.68 sec: 1.02x slower                                                |
| pyflate                    | 448 ms                                                 | 459 ms: 1.02x slower                                                  |
| deltablue                  | 3.45 ms                                                | 3.58 ms: 1.04x slower                                                 |
| spectral_norm              | 110 ms                                                 | 115 ms: 1.04x slower                                                  |
| logging_simple             | 6.63 us                                                | 6.93 us: 1.05x slower                                                 |
| html5lib                   | 63.6 ms                                                | 66.8 ms: 1.05x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 232 us: 1.05x slower                                                  |
| pidigits                   | 184 ms                                                 | 194 ms: 1.05x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 11.0 ms: 1.06x slower                                                 |
| hexiom                     | 6.17 ms                                                | 6.55 ms: 1.06x slower                                                 |
| 2to3                       | 264 ms                                                 | 281 ms: 1.07x slower                                                  |
| sympy_str                  | 292 ms                                                 | 312 ms: 1.07x slower                                                  |
| logging_format             | 7.35 us                                                | 7.87 us: 1.07x slower                                                 |
| sympy_integrate            | 20.5 ms                                                | 22.0 ms: 1.07x slower                                                 |
| sympy_sum                  | 166 ms                                                 | 178 ms: 1.07x slower                                                  |
| pprint_safe_repr           | 743 ms                                                 | 798 ms: 1.07x slower                                                  |
| json                       | 5.02 ms                                                | 5.40 ms: 1.08x slower                                                 |
| scimark_fft                | 342 ms                                                 | 369 ms: 1.08x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.65 sec: 1.08x slower                                                |
| nqueens                    | 80.1 ms                                                | 87.7 ms: 1.10x slower                                                 |
| sympy_expand               | 468 ms                                                 | 519 ms: 1.11x slower                                                  |
| thrift                     | 791 us                                                 | 885 us: 1.12x slower                                                  |
| richards                   | 45.9 ms                                                | 51.7 ms: 1.12x slower                                                 |
| pickle_pure_python         | 308 us                                                 | 347 us: 1.13x slower                                                  |
| meteor_contest             | 104 ms                                                 | 117 ms: 1.13x slower                                                  |
| crypto_pyaes               | 76.6 ms                                                | 86.8 ms: 1.13x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 130 ms: 1.14x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 78.6 ms: 1.15x slower                                                 |
| richards_super             | 51.9 ms                                                | 59.7 ms: 1.15x slower                                                 |
| xml_etree_generate         | 85.2 ms                                                | 98.7 ms: 1.16x slower                                                 |
| typing_runtime_protocols   | 163 us                                                 | 190 us: 1.16x slower                                                  |
| genshi_text                | 22.8 ms                                                | 26.6 ms: 1.16x slower                                                 |
| genshi_xml                 | 50.2 ms                                                | 59.0 ms: 1.18x slower                                                 |
| json_loads                 | 26.5 us                                                | 31.4 us: 1.18x slower                                                 |
| django_template            | 34.7 ms                                                | 41.1 ms: 1.18x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 70.9 ms: 1.20x slower                                                 |
| fannkuch                   | 372 ms                                                 | 459 ms: 1.23x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.48 ms: 1.25x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 9.57 ms: 1.34x slower                                                 |
| nbody                      | 89.3 ms                                                | 124 ms: 1.38x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.52 ms: 1.39x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 15.3 ms: 1.42x slower                                                 |
| mako                       | 11.0 ms                                                | 15.7 ms: 1.43x slower                                                 |
| coverage                   | 71.4 ms                                                | 110 ms: 1.55x slower                                                  |
| python_startup             | 9.93 ms                                                | 15.7 ms: 1.58x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.11 ms: 3.30x slower                                                 |
| telco                      | 6.53 ms                                                | 175 ms: 26.87x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.04x slower                                                          |

Benchmark hidden because not significant (1): pycparser
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250914-3.15.0a0-3e06cfc-NOGIL/bm-20250914-vultr-x86_64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.018x slower

# HPT report

- Reliability score: 85.76% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.41x