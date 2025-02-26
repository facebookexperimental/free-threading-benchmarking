# Results vs. 3.12.6

- fork: python
- ref: 0ef4ffeefd1737c18dc9
- machine: linux-x86_64
- commit hash: 0ef4ffe
- commit date: 2025-02-25
- overall geometric mean: 1.097x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 250 ms: 1.05x faster                                                   |
| docutils       | 2.64 sec                                               | 2.54 sec: 1.04x faster                                                 |
| Geometric mean | (ref)                                                  | 1.05x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 597 ms: 1.86x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 307 ms: 1.82x faster                                                   |
| async_tree_none            | 464 ms                                                 | 258 ms: 1.80x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 603 ms: 1.80x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 312 ms: 1.78x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 253 ms: 1.76x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 472 ms: 1.53x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 482 ms: 1.48x faster                                                   |
| async_generators           | 384 ms                                                 | 318 ms: 1.21x faster                                                   |
| coroutines                 | 23.9 ms                                                | 21.4 ms: 1.12x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.53x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 70.3 ms: 1.15x faster                                                  |
| nbody          | 89.3 ms                                                | 86.9 ms: 1.03x faster                                                  |
| pidigits       | 184 ms                                                 | 208 ms: 1.13x slower                                                   |
| Geometric mean | (ref)                                                  | 1.02x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.65 ms: 1.19x faster                                                  |
| regex_compile  | 142 ms                                                 | 124 ms: 1.14x faster                                                   |
| regex_dna      | 168 ms                                                 | 171 ms: 1.02x slower                                                   |
| regex_v8       | 20.6 ms                                                | 24.7 ms: 1.20x slower                                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.89 sec: 1.11x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.08x faster                                                   |
| xml_etree_iterparse  | 96.7 ms                                                | 90.4 ms: 1.07x faster                                                  |
| unpickle_pure_python | 221 us                                                 | 211 us: 1.05x faster                                                   |
| xml_etree_generate   | 85.2 ms                                                | 82.0 ms: 1.04x faster                                                  |
| xml_etree_process    | 59.0 ms                                                | 57.0 ms: 1.03x faster                                                  |
| json_loads           | 26.5 us                                                | 28.0 us: 1.06x slower                                                  |
| json_dumps           | 10.4 ms                                                | 11.1 ms: 1.07x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.51 ms: 1.05x slower                                                  |
| python_startup         | 9.93 ms                                                | 14.7 ms: 1.49x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.25x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.4 ms: 1.12x faster                                                  |
| django_template | 34.7 ms                                                | 32.4 ms: 1.07x faster                                                  |
| genshi_xml      | 50.2 ms                                                | 47.7 ms: 1.05x faster                                                  |
| mako            | 11.0 ms                                                | 11.6 ms: 1.05x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.05x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 597 ms: 1.86x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 307 ms: 1.82x faster                                                   |
| async_tree_none            | 464 ms                                                 | 258 ms: 1.80x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 603 ms: 1.80x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 312 ms: 1.78x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 253 ms: 1.76x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 472 ms: 1.53x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 482 ms: 1.48x faster                                                   |
| deepcopy                   | 352 us                                                 | 245 us: 1.44x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 29.1 us: 1.39x faster                                                  |
| go                         | 139 ms                                                 | 111 ms: 1.25x faster                                                   |
| comprehensions             | 19.8 us                                                | 15.9 us: 1.25x faster                                                  |
| spectral_norm              | 110 ms                                                 | 90.5 ms: 1.22x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.53 us: 1.22x faster                                                  |
| async_generators           | 384 ms                                                 | 318 ms: 1.21x faster                                                   |
| generators                 | 32.2 ms                                                | 26.7 ms: 1.21x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.65 ms: 1.19x faster                                                  |
| raytrace                   | 299 ms                                                 | 257 ms: 1.16x faster                                                   |
| pylint                     | 319 ms                                                 | 274 ms: 1.16x faster                                                   |
| scimark_sor                | 130 ms                                                 | 112 ms: 1.16x faster                                                   |
| float                      | 80.8 ms                                                | 70.3 ms: 1.15x faster                                                  |
| chaos                      | 62.8 ms                                                | 54.8 ms: 1.15x faster                                                  |
| regex_compile              | 142 ms                                                 | 124 ms: 1.14x faster                                                   |
| crypto_pyaes               | 76.6 ms                                                | 67.0 ms: 1.14x faster                                                  |
| deltablue                  | 3.45 ms                                                | 3.02 ms: 1.14x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.15 sec: 1.14x faster                                                 |
| logging_simple             | 6.63 us                                                | 5.82 us: 1.14x faster                                                  |
| sqlalchemy_declarative     | 143 ms                                                 | 126 ms: 1.14x faster                                                   |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.2 ms: 1.13x faster                                                  |
| pathlib                    | 21.5 ms                                                | 19.1 ms: 1.13x faster                                                  |
| genshi_text                | 22.8 ms                                                | 20.4 ms: 1.12x faster                                                  |
| coroutines                 | 23.9 ms                                                | 21.4 ms: 1.12x faster                                                  |
| pyflate                    | 448 ms                                                 | 402 ms: 1.11x faster                                                   |
| tomli_loads                | 2.11 sec                                               | 1.89 sec: 1.11x faster                                                 |
| logging_format             | 7.35 us                                                | 6.63 us: 1.11x faster                                                  |
| logging_silent             | 109 ns                                                 | 98.4 ns: 1.11x faster                                                  |
| scimark_fft                | 342 ms                                                 | 309 ms: 1.11x faster                                                   |
| sympy_sum                  | 166 ms                                                 | 151 ms: 1.10x faster                                                   |
| sqlglot_parse              | 1.36 ms                                                | 1.23 ms: 1.10x faster                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 62.3 ms: 1.10x faster                                                  |
| pprint_safe_repr           | 743 ms                                                 | 677 ms: 1.10x faster                                                   |
| richards                   | 45.9 ms                                                | 41.9 ms: 1.10x faster                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.39 sec: 1.09x faster                                                 |
| sqlglot_transpile          | 1.67 ms                                                | 1.53 ms: 1.09x faster                                                  |
| richards_super             | 51.9 ms                                                | 47.4 ms: 1.09x faster                                                  |
| thrift                     | 791 us                                                 | 726 us: 1.09x faster                                                   |
| sympy_str                  | 292 ms                                                 | 267 ms: 1.09x faster                                                   |
| hexiom                     | 6.17 ms                                                | 5.67 ms: 1.09x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.08x faster                                                   |
| typing_runtime_protocols   | 163 us                                                 | 152 us: 1.08x faster                                                   |
| nqueens                    | 80.1 ms                                                | 74.7 ms: 1.07x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 90.4 ms: 1.07x faster                                                  |
| django_template            | 34.7 ms                                                | 32.4 ms: 1.07x faster                                                  |
| sympy_integrate            | 20.5 ms                                                | 19.3 ms: 1.07x faster                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.15 ms: 1.06x faster                                                  |
| 2to3                       | 264 ms                                                 | 250 ms: 1.05x faster                                                   |
| genshi_xml                 | 50.2 ms                                                | 47.7 ms: 1.05x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 75.0 ms: 1.05x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.12 sec: 1.05x faster                                                 |
| unpickle_pure_python       | 221 us                                                 | 211 us: 1.05x faster                                                   |
| sqlglot_optimize           | 53.3 ms                                                | 51.0 ms: 1.04x faster                                                  |
| meteor_contest             | 104 ms                                                 | 99.2 ms: 1.04x faster                                                  |
| xml_etree_generate         | 85.2 ms                                                | 82.0 ms: 1.04x faster                                                  |
| docutils                   | 2.64 sec                                               | 2.54 sec: 1.04x faster                                                 |
| xml_etree_process          | 59.0 ms                                                | 57.0 ms: 1.03x faster                                                  |
| sympy_expand               | 468 ms                                                 | 453 ms: 1.03x faster                                                   |
| scimark_lu                 | 114 ms                                                 | 111 ms: 1.03x faster                                                   |
| nbody                      | 89.3 ms                                                | 86.9 ms: 1.03x faster                                                  |
| fannkuch                   | 372 ms                                                 | 366 ms: 1.02x faster                                                   |
| regex_dna                  | 168 ms                                                 | 171 ms: 1.02x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 7.51 ms: 1.05x slower                                                  |
| mako                       | 11.0 ms                                                | 11.6 ms: 1.05x slower                                                  |
| json_loads                 | 26.5 us                                                | 28.0 us: 1.06x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 11.1 ms: 1.07x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.03 ms: 1.10x slower                                                  |
| telco                      | 6.53 ms                                                | 7.19 ms: 1.10x slower                                                  |
| coverage                   | 71.4 ms                                                | 79.5 ms: 1.11x slower                                                  |
| pidigits                   | 184 ms                                                 | 208 ms: 1.13x slower                                                   |
| regex_v8                   | 20.6 ms                                                | 24.7 ms: 1.20x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 4.21 ms: 1.22x slower                                                  |
| python_startup             | 9.93 ms                                                | 14.7 ms: 1.49x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.81 ms: 1.66x slower                                                  |
| sqlglot_normalize          | 107 ms                                                 | 280 ms: 2.62x slower                                                   |
| bench_mp_pool              | 10.8 ms                                                | 88.3 ms: 8.18x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                           |

Benchmark hidden because not significant (5): json, sqlite_synth, pickle_pure_python, mdp, asyncio_websockets
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250225-3.14.0a5+-0ef4ffe/bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.097x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.12x