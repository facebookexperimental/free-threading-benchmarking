# Results vs. 3.12.6

- fork: python
- ref: bcff99cb3f3b887a08c4
- machine: linux-x86_64
- commit hash: bcff99c
- commit date: 2026-03-23
- overall geometric mean: 1.067x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260323-vultr-x86_64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 252 ms: 1.05x faster                                                   |
| docutils       | 2.64 sec                                               | 2.46 sec: 1.07x faster                                                 |
| html5lib       | 63.6 ms                                                | 60.0 ms: 1.06x faster                                                  |
| Geometric mean | (ref)                                                  | 1.06x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260323-vultr-x86_64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 571 ms: 1.94x faster                                                   |
| async_tree_none            | 464 ms                                                 | 250 ms: 1.86x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 591 ms: 1.83x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 307 ms: 1.82x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 246 ms: 1.82x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 315 ms: 1.76x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 510 ms: 1.40x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 522 ms: 1.38x faster                                                   |
| async_generators           | 384 ms                                                 | 344 ms: 1.12x faster                                                   |
| coroutines                 | 23.9 ms                                                | 23.5 ms: 1.02x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 545 ms: 1.05x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.49x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260323-vultr-x86_64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 69.8 ms: 1.16x faster                                                  |
| nbody          | 89.3 ms                                                | 94.9 ms: 1.06x slower                                                  |
| pidigits       | 184 ms                                                 | 204 ms: 1.11x slower                                                   |
| Geometric mean | (ref)                                                  | 1.01x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260323-vultr-x86_64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.68 ms: 1.18x faster                                                  |
| regex_compile  | 142 ms                                                 | 125 ms: 1.14x faster                                                   |
| regex_dna      | 168 ms                                                 | 165 ms: 1.02x faster                                                   |
| regex_v8       | 20.6 ms                                                | 21.1 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                  | 1.08x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260323-vultr-x86_64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.84 sec: 1.14x faster                                                 |
| xml_etree_iterparse  | 96.7 ms                                                | 85.2 ms: 1.13x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 132 ms: 1.05x faster                                                   |
| unpickle_pure_python | 221 us                                                 | 215 us: 1.03x faster                                                   |
| json_dumps           | 10.4 ms                                                | 10.1 ms: 1.02x faster                                                  |
| xml_etree_process    | 59.0 ms                                                | 59.6 ms: 1.01x slower                                                  |
| json_loads           | 26.5 us                                                | 27.8 us: 1.05x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (2): xml_etree_generate, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260323-vultr-x86_64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.42 ms: 1.04x slower                                                  |
| python_startup         | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.15x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260323-vultr-x86_64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 21.4 ms: 1.06x faster                                                  |
| genshi_xml      | 50.2 ms                                                | 51.2 ms: 1.02x slower                                                  |
| django_template | 34.7 ms                                                | 35.5 ms: 1.02x slower                                                  |
| mako            | 11.0 ms                                                | 12.0 ms: 1.09x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.02x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260323-vultr-x86_64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.15 sec: 2.09x faster                                                 |
| async_tree_io_tg           | 1.11 sec                                               | 571 ms: 1.94x faster                                                   |
| async_tree_none            | 464 ms                                                 | 250 ms: 1.86x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 591 ms: 1.83x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 307 ms: 1.82x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 246 ms: 1.82x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 315 ms: 1.76x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 26.5 us: 1.52x faster                                                  |
| deepcopy                   | 352 us                                                 | 234 us: 1.51x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 510 ms: 1.40x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 522 ms: 1.38x faster                                                   |
| go                         | 139 ms                                                 | 104 ms: 1.34x faster                                                   |
| pathlib                    | 21.5 ms                                                | 17.8 ms: 1.21x faster                                                  |
| comprehensions             | 19.8 us                                                | 16.5 us: 1.20x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.57 us: 1.20x faster                                                  |
| spectral_norm              | 110 ms                                                 | 93.1 ms: 1.18x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.68 ms: 1.18x faster                                                  |
| scimark_sor                | 130 ms                                                 | 110 ms: 1.18x faster                                                   |
| raytrace                   | 299 ms                                                 | 254 ms: 1.18x faster                                                   |
| float                      | 80.8 ms                                                | 69.8 ms: 1.16x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 68.5 ms: 1.15x faster                                                  |
| logging_simple             | 6.63 us                                                | 5.78 us: 1.15x faster                                                  |
| chaos                      | 62.8 ms                                                | 54.9 ms: 1.14x faster                                                  |
| tomli_loads                | 2.11 sec                                               | 1.84 sec: 1.14x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.16 sec: 1.14x faster                                                 |
| regex_compile              | 142 ms                                                 | 125 ms: 1.14x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 85.2 ms: 1.13x faster                                                  |
| pylint                     | 319 ms                                                 | 283 ms: 1.12x faster                                                   |
| logging_silent             | 109 ns                                                 | 97.1 ns: 1.12x faster                                                  |
| async_generators           | 384 ms                                                 | 344 ms: 1.12x faster                                                   |
| pyflate                    | 448 ms                                                 | 407 ms: 1.10x faster                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 62.2 ms: 1.10x faster                                                  |
| logging_format             | 7.35 us                                                | 6.71 us: 1.10x faster                                                  |
| crypto_pyaes               | 76.6 ms                                                | 70.0 ms: 1.09x faster                                                  |
| generators                 | 32.2 ms                                                | 29.5 ms: 1.09x faster                                                  |
| richards                   | 45.9 ms                                                | 42.3 ms: 1.09x faster                                                  |
| scimark_fft                | 342 ms                                                 | 316 ms: 1.08x faster                                                   |
| hexiom                     | 6.17 ms                                                | 5.75 ms: 1.07x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.09 sec: 1.07x faster                                                 |
| docutils                   | 2.64 sec                                               | 2.46 sec: 1.07x faster                                                 |
| richards_super             | 51.9 ms                                                | 48.5 ms: 1.07x faster                                                  |
| genshi_text                | 22.8 ms                                                | 21.4 ms: 1.06x faster                                                  |
| sympy_integrate            | 20.5 ms                                                | 19.3 ms: 1.06x faster                                                  |
| html5lib                   | 63.6 ms                                                | 60.0 ms: 1.06x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 132 ms: 1.05x faster                                                   |
| scimark_lu                 | 114 ms                                                 | 109 ms: 1.05x faster                                                   |
| nqueens                    | 80.1 ms                                                | 76.3 ms: 1.05x faster                                                  |
| 2to3                       | 264 ms                                                 | 252 ms: 1.05x faster                                                   |
| sympy_sum                  | 166 ms                                                 | 159 ms: 1.04x faster                                                   |
| deltablue                  | 3.45 ms                                                | 3.31 ms: 1.04x faster                                                  |
| sympy_str                  | 292 ms                                                 | 282 ms: 1.03x faster                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.48 sec: 1.03x faster                                                 |
| meteor_contest             | 104 ms                                                 | 101 ms: 1.03x faster                                                   |
| pprint_safe_repr           | 743 ms                                                 | 723 ms: 1.03x faster                                                   |
| unpickle_pure_python       | 221 us                                                 | 215 us: 1.03x faster                                                   |
| json_dumps                 | 10.4 ms                                                | 10.1 ms: 1.02x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.5 ms: 1.02x faster                                                  |
| typing_runtime_protocols   | 163 us                                                 | 160 us: 1.02x faster                                                   |
| regex_dna                  | 168 ms                                                 | 165 ms: 1.02x faster                                                   |
| thrift                     | 791 us                                                 | 780 us: 1.01x faster                                                   |
| xml_etree_process          | 59.0 ms                                                | 59.6 ms: 1.01x slower                                                  |
| json                       | 5.02 ms                                                | 5.11 ms: 1.02x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 51.2 ms: 1.02x slower                                                  |
| django_template            | 34.7 ms                                                | 35.5 ms: 1.02x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 21.1 ms: 1.02x slower                                                  |
| fannkuch                   | 372 ms                                                 | 382 ms: 1.03x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 7.42 ms: 1.04x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.60 ms: 1.05x slower                                                  |
| json_loads                 | 26.5 us                                                | 27.8 us: 1.05x slower                                                  |
| asyncio_websockets         | 517 ms                                                 | 545 ms: 1.05x slower                                                   |
| sympy_expand               | 468 ms                                                 | 495 ms: 1.06x slower                                                   |
| nbody                      | 89.3 ms                                                | 94.9 ms: 1.06x slower                                                  |
| mako                       | 11.0 ms                                                | 12.0 ms: 1.09x slower                                                  |
| pidigits                   | 184 ms                                                 | 204 ms: 1.11x slower                                                   |
| coverage                   | 71.4 ms                                                | 83.3 ms: 1.17x slower                                                  |
| python_startup             | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 4.46 ms: 1.29x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.33 ms: 1.41x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.83 ms: 1.68x slower                                                  |
| telco                      | 6.53 ms                                                | 161 ms: 24.71x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 298 ms: 27.64x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.02x faster                                                           |

Benchmark hidden because not significant (3): xml_etree_generate, pickle_pure_python, sqlite_synth
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260323-3.15.0a7+-bcff99c/bm-20260323-vultr-x86_64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.067x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.17x