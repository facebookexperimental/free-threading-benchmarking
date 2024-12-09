# Results vs. 3.12.6

- fork: colesbury
- ref: mro
- machine: linux-x86_64
- commit hash: 7f50611
- commit date: 2024-12-09
- overall geometric mean: 1.058x faster
- HPT reliability: 99.98%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241209-vultr-x86_64-colesbury-mro-3.14.0a2+-7f50611 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 259 ms: 1.02x faster                                     |
| docutils       | 2.64 sec                                               | 2.53 sec: 1.04x faster                                   |
| Geometric mean | (ref)                                                  | 1.03x faster                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241209-vultr-x86_64-colesbury-mro-3.14.0a2+-7f50611 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 621 ms: 1.79x faster                                     |
| async_tree_io              | 1.08 sec                                               | 606 ms: 1.79x faster                                     |
| async_tree_none            | 464 ms                                                 | 277 ms: 1.68x faster                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 333 ms: 1.68x faster                                     |
| async_tree_memoization     | 555 ms                                                 | 341 ms: 1.63x faster                                     |
| async_tree_none_tg         | 446 ms                                                 | 275 ms: 1.62x faster                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 600 ms: 1.20x faster                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 604 ms: 1.18x faster                                     |
| coroutines                 | 23.9 ms                                                | 22.6 ms: 1.06x faster                                    |
| async_generators           | 384 ms                                                 | 364 ms: 1.06x faster                                     |
| asyncio_websockets         | 517 ms                                                 | 523 ms: 1.01x slower                                     |
| Geometric mean             | (ref)                                                  | 1.39x faster                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241209-vultr-x86_64-colesbury-mro-3.14.0a2+-7f50611 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------:|
| float          | 80.8 ms                                                | 79.3 ms: 1.02x faster                                    |
| nbody          | 89.3 ms                                                | 93.0 ms: 1.04x slower                                    |
| pidigits       | 184 ms                                                 | 223 ms: 1.21x slower                                     |
| Geometric mean | (ref)                                                  | 1.07x slower                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241209-vultr-x86_64-colesbury-mro-3.14.0a2+-7f50611 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.76 ms: 1.15x faster                                    |
| regex_compile  | 142 ms                                                 | 130 ms: 1.10x faster                                     |
| regex_dna      | 168 ms                                                 | 172 ms: 1.02x slower                                     |
| regex_v8       | 20.6 ms                                                | 24.9 ms: 1.21x slower                                    |
| Geometric mean | (ref)                                                  | 1.00x faster                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241209-vultr-x86_64-colesbury-mro-3.14.0a2+-7f50611 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.08x faster                                     |
| json_loads           | 26.5 us                                                | 24.9 us: 1.06x faster                                    |
| xml_etree_iterparse  | 96.7 ms                                                | 91.5 ms: 1.06x faster                                    |
| unpickle_pure_python | 221 us                                                 | 216 us: 1.02x faster                                     |
| xml_etree_process    | 59.0 ms                                                | 59.4 ms: 1.01x slower                                    |
| pickle_pure_python   | 308 us                                                 | 317 us: 1.03x slower                                     |
| json_dumps           | 10.4 ms                                                | 11.5 ms: 1.11x slower                                    |
| Geometric mean       | (ref)                                                  | 1.01x faster                                             |

Benchmark hidden because not significant (2): tomli_loads, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241209-vultr-x86_64-colesbury-mro-3.14.0a2+-7f50611 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.58 ms: 1.06x slower                                    |
| python_startup         | 9.93 ms                                                | 14.8 ms: 1.49x slower                                    |
| Geometric mean         | (ref)                                                  | 1.26x slower                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241209-vultr-x86_64-colesbury-mro-3.14.0a2+-7f50611 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 21.9 ms: 1.04x faster                                    |
| django_template | 34.7 ms                                                | 35.9 ms: 1.03x slower                                    |
| mako            | 11.0 ms                                                | 11.7 ms: 1.06x slower                                    |
| Geometric mean  | (ref)                                                  | 1.01x slower                                             |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241209-vultr-x86_64-colesbury-mro-3.14.0a2+-7f50611 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 621 ms: 1.79x faster                                     |
| async_tree_io              | 1.08 sec                                               | 606 ms: 1.79x faster                                     |
| async_tree_none            | 464 ms                                                 | 277 ms: 1.68x faster                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 333 ms: 1.68x faster                                     |
| async_tree_memoization     | 555 ms                                                 | 341 ms: 1.63x faster                                     |
| async_tree_none_tg         | 446 ms                                                 | 275 ms: 1.62x faster                                     |
| deepcopy_memo              | 40.3 us                                                | 30.2 us: 1.33x faster                                    |
| deepcopy                   | 352 us                                                 | 264 us: 1.33x faster                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 600 ms: 1.20x faster                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 604 ms: 1.18x faster                                     |
| pathlib                    | 21.5 ms                                                | 18.4 ms: 1.17x faster                                    |
| deepcopy_reduce            | 3.08 us                                                | 2.64 us: 1.17x faster                                    |
| regex_effbot               | 3.17 ms                                                | 2.76 ms: 1.15x faster                                    |
| pylint                     | 319 ms                                                 | 278 ms: 1.14x faster                                     |
| comprehensions             | 19.8 us                                                | 17.3 us: 1.14x faster                                    |
| go                         | 139 ms                                                 | 122 ms: 1.14x faster                                     |
| crypto_pyaes               | 76.6 ms                                                | 67.5 ms: 1.13x faster                                    |
| raytrace                   | 299 ms                                                 | 266 ms: 1.13x faster                                     |
| json                       | 5.02 ms                                                | 4.58 ms: 1.10x faster                                    |
| regex_compile              | 142 ms                                                 | 130 ms: 1.10x faster                                     |
| generators                 | 32.2 ms                                                | 29.4 ms: 1.10x faster                                    |
| bpe_tokeniser              | 4.74 sec                                               | 4.33 sec: 1.09x faster                                   |
| sympy_sum                  | 166 ms                                                 | 153 ms: 1.09x faster                                     |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                     |
| logging_simple             | 6.63 us                                                | 6.16 us: 1.08x faster                                    |
| chaos                      | 62.8 ms                                                | 58.5 ms: 1.07x faster                                    |
| thrift                     | 791 us                                                 | 743 us: 1.07x faster                                     |
| json_loads                 | 26.5 us                                                | 24.9 us: 1.06x faster                                    |
| sympy_str                  | 292 ms                                                 | 274 ms: 1.06x faster                                     |
| coroutines                 | 23.9 ms                                                | 22.6 ms: 1.06x faster                                    |
| xml_etree_iterparse        | 96.7 ms                                                | 91.5 ms: 1.06x faster                                    |
| deltablue                  | 3.45 ms                                                | 3.26 ms: 1.06x faster                                    |
| async_generators           | 384 ms                                                 | 364 ms: 1.06x faster                                     |
| logging_format             | 7.35 us                                                | 6.97 us: 1.05x faster                                    |
| sqlglot_transpile          | 1.67 ms                                                | 1.60 ms: 1.05x faster                                    |
| sqlglot_parse              | 1.36 ms                                                | 1.30 ms: 1.05x faster                                    |
| docutils                   | 2.64 sec                                               | 2.53 sec: 1.04x faster                                   |
| genshi_text                | 22.8 ms                                                | 21.9 ms: 1.04x faster                                    |
| hexiom                     | 6.17 ms                                                | 5.93 ms: 1.04x faster                                    |
| meteor_contest             | 104 ms                                                 | 99.6 ms: 1.04x faster                                    |
| pycparser                  | 1.17 sec                                               | 1.13 sec: 1.04x faster                                   |
| sympy_integrate            | 20.5 ms                                                | 19.8 ms: 1.04x faster                                    |
| dulwich_log                | 78.9 ms                                                | 76.0 ms: 1.04x faster                                    |
| scimark_monte_carlo        | 68.4 ms                                                | 66.2 ms: 1.03x faster                                    |
| pprint_safe_repr           | 743 ms                                                 | 725 ms: 1.03x faster                                     |
| typing_runtime_protocols   | 163 us                                                 | 159 us: 1.02x faster                                     |
| pprint_pformat             | 1.52 sec                                               | 1.49 sec: 1.02x faster                                   |
| unpickle_pure_python       | 221 us                                                 | 216 us: 1.02x faster                                     |
| float                      | 80.8 ms                                                | 79.3 ms: 1.02x faster                                    |
| nqueens                    | 80.1 ms                                                | 78.6 ms: 1.02x faster                                    |
| 2to3                       | 264 ms                                                 | 259 ms: 1.02x faster                                     |
| logging_silent             | 109 ns                                                 | 108 ns: 1.01x faster                                     |
| scimark_fft                | 342 ms                                                 | 338 ms: 1.01x faster                                     |
| sympy_expand               | 468 ms                                                 | 465 ms: 1.01x faster                                     |
| sqlglot_normalize          | 107 ms                                                 | 106 ms: 1.01x faster                                     |
| scimark_lu                 | 114 ms                                                 | 115 ms: 1.01x slower                                     |
| pyflate                    | 448 ms                                                 | 451 ms: 1.01x slower                                     |
| xml_etree_process          | 59.0 ms                                                | 59.4 ms: 1.01x slower                                    |
| fannkuch                   | 372 ms                                                 | 376 ms: 1.01x slower                                     |
| asyncio_websockets         | 517 ms                                                 | 523 ms: 1.01x slower                                     |
| richards                   | 45.9 ms                                                | 46.6 ms: 1.01x slower                                    |
| regex_dna                  | 168 ms                                                 | 172 ms: 1.02x slower                                     |
| richards_super             | 51.9 ms                                                | 53.3 ms: 1.03x slower                                    |
| pickle_pure_python         | 308 us                                                 | 317 us: 1.03x slower                                     |
| django_template            | 34.7 ms                                                | 35.9 ms: 1.03x slower                                    |
| scimark_sor                | 130 ms                                                 | 135 ms: 1.04x slower                                     |
| nbody                      | 89.3 ms                                                | 93.0 ms: 1.04x slower                                    |
| mdp                        | 2.42 sec                                               | 2.52 sec: 1.04x slower                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.60 ms: 1.05x slower                                    |
| python_startup_no_site     | 7.16 ms                                                | 7.58 ms: 1.06x slower                                    |
| mako                       | 11.0 ms                                                | 11.7 ms: 1.06x slower                                    |
| bench_thread_pool          | 941 us                                                 | 1.03 ms: 1.10x slower                                    |
| json_dumps                 | 10.4 ms                                                | 11.5 ms: 1.11x slower                                    |
| telco                      | 6.53 ms                                                | 7.26 ms: 1.11x slower                                    |
| pidigits                   | 184 ms                                                 | 223 ms: 1.21x slower                                     |
| regex_v8                   | 20.6 ms                                                | 24.9 ms: 1.21x slower                                    |
| gc_traversal               | 3.46 ms                                                | 4.33 ms: 1.25x slower                                    |
| python_startup             | 9.93 ms                                                | 14.8 ms: 1.49x slower                                    |
| create_gc_cycles           | 1.09 ms                                                | 1.77 ms: 1.63x slower                                    |
| bench_mp_pool              | 10.8 ms                                                | 86.0 ms: 7.96x slower                                    |
| Geometric mean             | (ref)                                                  | 1.03x faster                                             |

Benchmark hidden because not significant (6): spectral_norm, tomli_loads, xml_etree_generate, sqlglot_optimize, genshi_xml, sqlite_synth
Ignored benchmarks (19) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, coverage, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241209-3.14.0a2+-7f50611/bm-20241209-vultr-x86_64-colesbury-mro-3.14.0a2+-7f50611.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.058x faster

# HPT report

- Reliability score: 99.98% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.12x