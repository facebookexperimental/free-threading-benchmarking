# Results vs. 3.12.6

- fork: python
- ref: fb8d8d9c9f9cbc94fa58
- machine: linux-x86_64
- commit hash: fb8d8d9
- commit date: 2026-03-22
- overall geometric mean: 1.031x slower
- HPT reliability: 80.73%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.42x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260322-vultr-x86_64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 283 ms: 1.07x slower                                                   |
| html5lib       | 63.6 ms                                                | 65.3 ms: 1.03x slower                                                  |
| Geometric mean | (ref)                                                  | 1.03x slower                                                           |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260322-vultr-x86_64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 607 ms: 1.83x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 322 ms: 1.74x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 262 ms: 1.70x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 645 ms: 1.68x faster                                                   |
| async_tree_none            | 464 ms                                                 | 288 ms: 1.61x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 351 ms: 1.58x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 545 ms: 1.33x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 569 ms: 1.26x faster                                                   |
| async_generators           | 384 ms                                                 | 380 ms: 1.01x faster                                                   |
| coroutines                 | 23.9 ms                                                | 24.6 ms: 1.03x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.39x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260322-vultr-x86_64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 74.8 ms: 1.08x faster                                                  |
| pidigits       | 184 ms                                                 | 206 ms: 1.12x slower                                                   |
| nbody          | 89.3 ms                                                | 127 ms: 1.42x slower                                                   |
| Geometric mean | (ref)                                                  | 1.14x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260322-vultr-x86_64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.85 ms: 1.11x faster                                                  |
| regex_compile  | 142 ms                                                 | 141 ms: 1.01x faster                                                   |
| regex_v8       | 20.6 ms                                                | 21.8 ms: 1.06x slower                                                  |
| regex_dna      | 168 ms                                                 | 181 ms: 1.08x slower                                                   |
| Geometric mean | (ref)                                                  | 1.00x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260322-vultr-x86_64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.7 ms: 1.10x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 1.95 sec: 1.08x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 132 ms: 1.05x faster                                                   |
| json_dumps           | 10.4 ms                                                | 11.0 ms: 1.07x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 237 us: 1.08x slower                                                   |
| pickle_pure_python   | 308 us                                                 | 335 us: 1.09x slower                                                   |
| xml_etree_generate   | 85.2 ms                                                | 96.1 ms: 1.13x slower                                                  |
| json_loads           | 26.5 us                                                | 30.7 us: 1.16x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 68.4 ms: 1.16x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.05x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260322-vultr-x86_64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.77 ms: 1.36x slower                                                  |
| python_startup         | 9.93 ms                                                | 16.0 ms: 1.61x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.48x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260322-vultr-x86_64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 54.0 ms: 1.08x slower                                                  |
| genshi_text     | 22.8 ms                                                | 25.6 ms: 1.12x slower                                                  |
| django_template | 34.7 ms                                                | 39.7 ms: 1.15x slower                                                  |
| mako            | 11.0 ms                                                | 15.7 ms: 1.42x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.18x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260322-vultr-x86_64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.31 sec: 1.84x faster                                                 |
| async_tree_io_tg           | 1.11 sec                                               | 607 ms: 1.83x faster                                                   |
| gc_traversal               | 3.46 ms                                                | 1.93 ms: 1.80x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 322 ms: 1.74x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 262 ms: 1.70x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 645 ms: 1.68x faster                                                   |
| async_tree_none            | 464 ms                                                 | 288 ms: 1.61x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 351 ms: 1.58x faster                                                   |
| bench_mp_pool              | 10.8 ms                                                | 7.01 ms: 1.54x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 545 ms: 1.33x faster                                                   |
| deepcopy                   | 352 us                                                 | 266 us: 1.32x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 30.9 us: 1.30x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 569 ms: 1.26x faster                                                   |
| pathlib                    | 21.5 ms                                                | 17.6 ms: 1.23x faster                                                  |
| go                         | 139 ms                                                 | 121 ms: 1.15x faster                                                   |
| sqlite_synth               | 2.20 us                                                | 1.91 us: 1.15x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 70.6 ms: 1.12x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.85 ms: 1.11x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 87.7 ms: 1.10x faster                                                  |
| comprehensions             | 19.8 us                                                | 18.1 us: 1.10x faster                                                  |
| tomli_loads                | 2.11 sec                                               | 1.95 sec: 1.08x faster                                                 |
| float                      | 80.8 ms                                                | 74.8 ms: 1.08x faster                                                  |
| pylint                     | 319 ms                                                 | 296 ms: 1.07x faster                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 4.41 sec: 1.07x faster                                                 |
| scimark_sor                | 130 ms                                                 | 122 ms: 1.06x faster                                                   |
| xml_etree_parse            | 139 ms                                                 | 132 ms: 1.05x faster                                                   |
| deepcopy_reduce            | 3.08 us                                                | 2.94 us: 1.05x faster                                                  |
| logging_silent             | 109 ns                                                 | 104 ns: 1.04x faster                                                   |
| pycparser                  | 1.17 sec                                               | 1.12 sec: 1.04x faster                                                 |
| async_generators           | 384 ms                                                 | 380 ms: 1.01x faster                                                   |
| regex_compile              | 142 ms                                                 | 141 ms: 1.01x faster                                                   |
| chaos                      | 62.8 ms                                                | 62.5 ms: 1.01x faster                                                  |
| generators                 | 32.2 ms                                                | 32.5 ms: 1.01x slower                                                  |
| raytrace                   | 299 ms                                                 | 302 ms: 1.01x slower                                                   |
| deltablue                  | 3.45 ms                                                | 3.50 ms: 1.01x slower                                                  |
| pyflate                    | 448 ms                                                 | 459 ms: 1.02x slower                                                   |
| html5lib                   | 63.6 ms                                                | 65.3 ms: 1.03x slower                                                  |
| logging_simple             | 6.63 us                                                | 6.81 us: 1.03x slower                                                  |
| coroutines                 | 23.9 ms                                                | 24.6 ms: 1.03x slower                                                  |
| scimark_fft                | 342 ms                                                 | 355 ms: 1.04x slower                                                   |
| spectral_norm              | 110 ms                                                 | 115 ms: 1.05x slower                                                   |
| hexiom                     | 6.17 ms                                                | 6.48 ms: 1.05x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 21.6 ms: 1.05x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 21.8 ms: 1.06x slower                                                  |
| sympy_str                  | 292 ms                                                 | 309 ms: 1.06x slower                                                   |
| sympy_sum                  | 166 ms                                                 | 176 ms: 1.06x slower                                                   |
| logging_format             | 7.35 us                                                | 7.81 us: 1.06x slower                                                  |
| pprint_safe_repr           | 743 ms                                                 | 790 ms: 1.06x slower                                                   |
| json                       | 5.02 ms                                                | 5.35 ms: 1.06x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 11.0 ms: 1.07x slower                                                  |
| 2to3                       | 264 ms                                                 | 283 ms: 1.07x slower                                                   |
| unpickle_pure_python       | 221 us                                                 | 237 us: 1.08x slower                                                   |
| genshi_xml                 | 50.2 ms                                                | 54.0 ms: 1.08x slower                                                  |
| regex_dna                  | 168 ms                                                 | 181 ms: 1.08x slower                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.64 sec: 1.08x slower                                                 |
| pickle_pure_python         | 308 us                                                 | 335 us: 1.09x slower                                                   |
| scimark_lu                 | 114 ms                                                 | 125 ms: 1.10x slower                                                   |
| nqueens                    | 80.1 ms                                                | 88.0 ms: 1.10x slower                                                  |
| sympy_expand               | 468 ms                                                 | 520 ms: 1.11x slower                                                   |
| pidigits                   | 184 ms                                                 | 206 ms: 1.12x slower                                                   |
| genshi_text                | 22.8 ms                                                | 25.6 ms: 1.12x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 96.1 ms: 1.13x slower                                                  |
| crypto_pyaes               | 76.6 ms                                                | 87.6 ms: 1.14x slower                                                  |
| django_template            | 34.7 ms                                                | 39.7 ms: 1.15x slower                                                  |
| thrift                     | 791 us                                                 | 908 us: 1.15x slower                                                   |
| richards                   | 45.9 ms                                                | 53.0 ms: 1.15x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 79.1 ms: 1.16x slower                                                  |
| richards_super             | 51.9 ms                                                | 60.0 ms: 1.16x slower                                                  |
| json_loads                 | 26.5 us                                                | 30.7 us: 1.16x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 68.4 ms: 1.16x slower                                                  |
| meteor_contest             | 104 ms                                                 | 123 ms: 1.18x slower                                                   |
| typing_runtime_protocols   | 163 us                                                 | 196 us: 1.20x slower                                                   |
| fannkuch                   | 372 ms                                                 | 460 ms: 1.24x slower                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.47 ms: 1.24x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 9.77 ms: 1.36x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.51 ms: 1.38x slower                                                  |
| nbody                      | 89.3 ms                                                | 127 ms: 1.42x slower                                                   |
| mako                       | 11.0 ms                                                | 15.7 ms: 1.42x slower                                                  |
| coverage                   | 71.4 ms                                                | 112 ms: 1.57x slower                                                   |
| python_startup             | 9.93 ms                                                | 16.0 ms: 1.61x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.62 ms: 1.72x slower                                                  |
| telco                      | 6.53 ms                                                | 173 ms: 26.51x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.03x slower                                                           |

Benchmark hidden because not significant (2): asyncio_websockets, docutils
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260322-3.15.0a7+-fb8d8d9-NOGIL/bm-20260322-vultr-x86_64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7+-fb8d8d9.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.031x slower

# HPT report

- Reliability score: 80.73% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.42x