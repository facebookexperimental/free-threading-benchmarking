# Results vs. 3.12.6

- fork: python
- ref: a6bc60da02ea37f33d5a
- machine: linux-x86_64
- commit hash: a6bc60d
- commit date: 2026-01-12
- overall geometric mean: 1.033x slower
- HPT reliability: 87.61%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.41x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260112-vultr-x86_64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 277 ms: 1.05x slower                                                   |
| docutils       | 2.64 sec                                               | 2.74 sec: 1.04x slower                                                 |
| Geometric mean | (ref)                                                  | 1.03x slower                                                           |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260112-vultr-x86_64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 593 ms: 1.87x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 611 ms: 1.77x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 324 ms: 1.72x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 262 ms: 1.70x faster                                                   |
| async_tree_none            | 464 ms                                                 | 288 ms: 1.61x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 353 ms: 1.57x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 532 ms: 1.36x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 556 ms: 1.29x faster                                                   |
| async_generators           | 384 ms                                                 | 376 ms: 1.02x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 512 ms: 1.01x faster                                                   |
| coroutines                 | 23.9 ms                                                | 24.2 ms: 1.01x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.41x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260112-vultr-x86_64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 75.1 ms: 1.08x faster                                                  |
| pidigits       | 184 ms                                                 | 194 ms: 1.06x slower                                                   |
| nbody          | 89.3 ms                                                | 125 ms: 1.40x slower                                                   |
| Geometric mean | (ref)                                                  | 1.11x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260112-vultr-x86_64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.70 ms: 1.17x faster                                                  |
| regex_compile  | 142 ms                                                 | 141 ms: 1.01x faster                                                   |
| regex_dna      | 168 ms                                                 | 173 ms: 1.03x slower                                                   |
| regex_v8       | 20.6 ms                                                | 21.5 ms: 1.04x slower                                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260112-vultr-x86_64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.1 ms: 1.10x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                   |
| tomli_loads          | 2.11 sec                                               | 2.00 sec: 1.06x faster                                                 |
| json_dumps           | 10.4 ms                                                | 11.1 ms: 1.07x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 238 us: 1.08x slower                                                   |
| pickle_pure_python   | 308 us                                                 | 334 us: 1.09x slower                                                   |
| xml_etree_generate   | 85.2 ms                                                | 96.0 ms: 1.13x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 69.4 ms: 1.18x slower                                                  |
| json_loads           | 26.5 us                                                | 32.3 us: 1.22x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.06x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260112-vultr-x86_64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.67 ms: 1.35x slower                                                  |
| python_startup         | 9.93 ms                                                | 15.7 ms: 1.59x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.46x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260112-vultr-x86_64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 57.6 ms: 1.15x slower                                                  |
| django_template | 34.7 ms                                                | 39.9 ms: 1.15x slower                                                  |
| genshi_text     | 22.8 ms                                                | 27.2 ms: 1.19x slower                                                  |
| mako            | 11.0 ms                                                | 15.7 ms: 1.42x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.22x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260112-vultr-x86_64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 593 ms: 1.87x faster                                                   |
| mdp                        | 2.42 sec                                               | 1.31 sec: 1.84x faster                                                 |
| gc_traversal               | 3.46 ms                                                | 1.93 ms: 1.79x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 611 ms: 1.77x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 324 ms: 1.72x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 262 ms: 1.70x faster                                                   |
| async_tree_none            | 464 ms                                                 | 288 ms: 1.61x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 353 ms: 1.57x faster                                                   |
| bench_mp_pool              | 10.8 ms                                                | 7.04 ms: 1.53x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 532 ms: 1.36x faster                                                   |
| deepcopy                   | 352 us                                                 | 265 us: 1.33x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 30.8 us: 1.31x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 556 ms: 1.29x faster                                                   |
| pathlib                    | 21.5 ms                                                | 18.2 ms: 1.18x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.70 ms: 1.17x faster                                                  |
| go                         | 139 ms                                                 | 121 ms: 1.15x faster                                                   |
| dulwich_log                | 78.9 ms                                                | 70.9 ms: 1.11x faster                                                  |
| comprehensions             | 19.8 us                                                | 17.9 us: 1.11x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 88.1 ms: 1.10x faster                                                  |
| float                      | 80.8 ms                                                | 75.1 ms: 1.08x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 2.06 us: 1.07x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.44 sec: 1.07x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                   |
| pylint                     | 319 ms                                                 | 301 ms: 1.06x faster                                                   |
| deepcopy_reduce            | 3.08 us                                                | 2.91 us: 1.06x faster                                                  |
| tomli_loads                | 2.11 sec                                               | 2.00 sec: 1.06x faster                                                 |
| scimark_sor                | 130 ms                                                 | 123 ms: 1.05x faster                                                   |
| logging_silent             | 109 ns                                                 | 106 ns: 1.03x faster                                                   |
| pycparser                  | 1.17 sec                                               | 1.14 sec: 1.03x faster                                                 |
| async_generators           | 384 ms                                                 | 376 ms: 1.02x faster                                                   |
| regex_compile              | 142 ms                                                 | 141 ms: 1.01x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 512 ms: 1.01x faster                                                   |
| coroutines                 | 23.9 ms                                                | 24.2 ms: 1.01x slower                                                  |
| raytrace                   | 299 ms                                                 | 305 ms: 1.02x slower                                                   |
| chaos                      | 62.8 ms                                                | 64.3 ms: 1.02x slower                                                  |
| regex_dna                  | 168 ms                                                 | 173 ms: 1.03x slower                                                   |
| spectral_norm              | 110 ms                                                 | 113 ms: 1.03x slower                                                   |
| scimark_fft                | 342 ms                                                 | 353 ms: 1.03x slower                                                   |
| pprint_safe_repr           | 743 ms                                                 | 768 ms: 1.03x slower                                                   |
| hexiom                     | 6.17 ms                                                | 6.38 ms: 1.03x slower                                                  |
| logging_simple             | 6.63 us                                                | 6.87 us: 1.04x slower                                                  |
| docutils                   | 2.64 sec                                               | 2.74 sec: 1.04x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 21.5 ms: 1.04x slower                                                  |
| deltablue                  | 3.45 ms                                                | 3.61 ms: 1.05x slower                                                  |
| logging_format             | 7.35 us                                                | 7.71 us: 1.05x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.60 sec: 1.05x slower                                                 |
| pyflate                    | 448 ms                                                 | 471 ms: 1.05x slower                                                   |
| 2to3                       | 264 ms                                                 | 277 ms: 1.05x slower                                                   |
| pidigits                   | 184 ms                                                 | 194 ms: 1.06x slower                                                   |
| json_dumps                 | 10.4 ms                                                | 11.1 ms: 1.07x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 21.9 ms: 1.07x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 178 ms: 1.07x slower                                                   |
| sympy_str                  | 292 ms                                                 | 313 ms: 1.07x slower                                                   |
| unpickle_pure_python       | 221 us                                                 | 238 us: 1.08x slower                                                   |
| json                       | 5.02 ms                                                | 5.46 ms: 1.09x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 334 us: 1.09x slower                                                   |
| nqueens                    | 80.1 ms                                                | 88.8 ms: 1.11x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 96.0 ms: 1.13x slower                                                  |
| sympy_expand               | 468 ms                                                 | 528 ms: 1.13x slower                                                   |
| thrift                     | 791 us                                                 | 899 us: 1.14x slower                                                   |
| crypto_pyaes               | 76.6 ms                                                | 87.4 ms: 1.14x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 57.6 ms: 1.15x slower                                                  |
| richards                   | 45.9 ms                                                | 52.8 ms: 1.15x slower                                                  |
| django_template            | 34.7 ms                                                | 39.9 ms: 1.15x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 132 ms: 1.15x slower                                                   |
| richards_super             | 51.9 ms                                                | 60.1 ms: 1.16x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 79.5 ms: 1.16x slower                                                  |
| meteor_contest             | 104 ms                                                 | 121 ms: 1.17x slower                                                   |
| xml_etree_process          | 59.0 ms                                                | 69.4 ms: 1.18x slower                                                  |
| typing_runtime_protocols   | 163 us                                                 | 194 us: 1.19x slower                                                   |
| genshi_text                | 22.8 ms                                                | 27.2 ms: 1.19x slower                                                  |
| json_loads                 | 26.5 us                                                | 32.3 us: 1.22x slower                                                  |
| fannkuch                   | 372 ms                                                 | 464 ms: 1.25x slower                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.64 ms: 1.28x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 9.67 ms: 1.35x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.51 ms: 1.38x slower                                                  |
| nbody                      | 89.3 ms                                                | 125 ms: 1.40x slower                                                   |
| mako                       | 11.0 ms                                                | 15.7 ms: 1.42x slower                                                  |
| coverage                   | 71.4 ms                                                | 111 ms: 1.55x slower                                                   |
| bench_thread_pool          | 941 us                                                 | 1.47 ms: 1.57x slower                                                  |
| python_startup             | 9.93 ms                                                | 15.7 ms: 1.59x slower                                                  |
| telco                      | 6.53 ms                                                | 177 ms: 27.12x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.03x slower                                                           |

Benchmark hidden because not significant (2): generators, html5lib
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260112-3.15.0a3+-a6bc60d-NOGIL/bm-20260112-vultr-x86_64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.033x slower

# HPT report

- Reliability score: 87.61% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.41x