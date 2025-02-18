# Results vs. 3.13.0rc2

- fork: python
- ref: 99d965635ae2ac4bffdc
- machine: linux-x86_64
- commit hash: 99d9656
- commit date: 2025-02-17
- overall geometric mean: 1.048x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250217-vultr-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 255 ms: 1.02x faster                                                   |
| docutils       | 2.63 sec                                                               | 2.56 sec: 1.03x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250217-vultr-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 627 ms: 1.44x faster                                                   |
| async_tree_memoization     | 459 ms                                                                 | 323 ms: 1.42x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 622 ms: 1.42x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 499 ms: 1.34x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 270 ms: 1.31x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 315 ms: 1.30x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 489 ms: 1.30x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 262 ms: 1.27x faster                                                   |
| async_generators           | 375 ms                                                                 | 326 ms: 1.15x faster                                                   |
| coroutines                 | 23.3 ms                                                                | 22.0 ms: 1.06x faster                                                  |
| Geometric mean             | (ref)                                                                  | 1.26x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250217-vultr-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 198 ms: 1.10x faster                                                   |
| float          | 76.7 ms                                                                | 72.3 ms: 1.06x faster                                                  |
| nbody          | 85.3 ms                                                                | 91.1 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250217-vultr-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.69 ms: 1.19x faster                                                  |
| regex_dna      | 189 ms                                                                 | 169 ms: 1.11x faster                                                   |
| regex_compile  | 131 ms                                                                 | 126 ms: 1.04x faster                                                   |
| regex_v8       | 23.2 ms                                                                | 24.1 ms: 1.04x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.07x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250217-vultr-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                               | 1.91 sec: 1.05x faster                                                 |
| xml_etree_parse      | 136 ms                                                                 | 130 ms: 1.05x faster                                                   |
| xml_etree_iterparse  | 94.4 ms                                                                | 91.6 ms: 1.03x faster                                                  |
| xml_etree_generate   | 85.4 ms                                                                | 83.0 ms: 1.03x faster                                                  |
| xml_etree_process    | 59.2 ms                                                                | 58.4 ms: 1.01x faster                                                  |
| json_loads           | 27.3 us                                                                | 28.2 us: 1.03x slower                                                  |
| unpickle_pure_python | 208 us                                                                 | 215 us: 1.03x slower                                                   |
| pickle_pure_python   | 292 us                                                                 | 310 us: 1.06x slower                                                   |
| json_dumps           | 10.6 ms                                                                | 11.3 ms: 1.07x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250217-vultr-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup | 11.0 ms                                                                | 14.6 ms: 1.32x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.15x slower                                                           |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250217-vultr-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 48.0 ms: 1.02x faster                                                  |
| genshi_text     | 21.7 ms                                                                | 21.3 ms: 1.02x faster                                                  |
| django_template | 34.2 ms                                                                | 34.9 ms: 1.02x slower                                                  |
| mako            | 11.2 ms                                                                | 11.6 ms: 1.03x slower                                                  |
| Geometric mean  | (ref)                                                                  | 1.00x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250217-vultr-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 627 ms: 1.44x faster                                                   |
| async_tree_memoization     | 459 ms                                                                 | 323 ms: 1.42x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 622 ms: 1.42x faster                                                   |
| deepcopy                   | 357 us                                                                 | 254 us: 1.41x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 499 ms: 1.34x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 270 ms: 1.31x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 315 ms: 1.30x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 489 ms: 1.30x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 262 ms: 1.27x faster                                                   |
| deepcopy_memo              | 38.1 us                                                                | 30.6 us: 1.25x faster                                                  |
| go                         | 141 ms                                                                 | 115 ms: 1.22x faster                                                   |
| deepcopy_reduce            | 3.12 us                                                                | 2.61 us: 1.20x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.69 ms: 1.19x faster                                                  |
| scimark_sor                | 134 ms                                                                 | 115 ms: 1.16x faster                                                   |
| spectral_norm              | 108 ms                                                                 | 93.6 ms: 1.15x faster                                                  |
| async_generators           | 375 ms                                                                 | 326 ms: 1.15x faster                                                   |
| pylint                     | 317 ms                                                                 | 277 ms: 1.14x faster                                                   |
| regex_dna                  | 189 ms                                                                 | 169 ms: 1.11x faster                                                   |
| pidigits                   | 216 ms                                                                 | 198 ms: 1.10x faster                                                   |
| pyflate                    | 449 ms                                                                 | 413 ms: 1.09x faster                                                   |
| scimark_fft                | 348 ms                                                                 | 323 ms: 1.08x faster                                                   |
| telco                      | 7.77 ms                                                                | 7.23 ms: 1.08x faster                                                  |
| bpe_tokeniser              | 4.46 sec                                                               | 4.18 sec: 1.07x faster                                                 |
| float                      | 76.7 ms                                                                | 72.3 ms: 1.06x faster                                                  |
| richards                   | 44.4 ms                                                                | 41.9 ms: 1.06x faster                                                  |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.48 ms: 1.06x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 22.0 ms: 1.06x faster                                                  |
| richards_super             | 50.4 ms                                                                | 47.8 ms: 1.06x faster                                                  |
| tomli_loads                | 2.01 sec                                                               | 1.91 sec: 1.05x faster                                                 |
| coverage                   | 82.5 ms                                                                | 78.6 ms: 1.05x faster                                                  |
| xml_etree_parse            | 136 ms                                                                 | 130 ms: 1.05x faster                                                   |
| logging_format             | 6.92 us                                                                | 6.60 us: 1.05x faster                                                  |
| regex_compile              | 131 ms                                                                 | 126 ms: 1.04x faster                                                   |
| logging_simple             | 6.14 us                                                                | 5.90 us: 1.04x faster                                                  |
| xml_etree_iterparse        | 94.4 ms                                                                | 91.6 ms: 1.03x faster                                                  |
| sqlglot_normalize          | 106 ms                                                                 | 103 ms: 1.03x faster                                                   |
| xml_etree_generate         | 85.4 ms                                                                | 83.0 ms: 1.03x faster                                                  |
| docutils                   | 2.63 sec                                                               | 2.56 sec: 1.03x faster                                                 |
| thrift                     | 772 us                                                                 | 753 us: 1.03x faster                                                   |
| sqlite_synth               | 2.25 us                                                                | 2.19 us: 1.02x faster                                                  |
| sqlglot_optimize           | 52.7 ms                                                                | 51.4 ms: 1.02x faster                                                  |
| genshi_xml                 | 49.1 ms                                                                | 48.0 ms: 1.02x faster                                                  |
| genshi_text                | 21.7 ms                                                                | 21.3 ms: 1.02x faster                                                  |
| pprint_safe_repr           | 719 ms                                                                 | 705 ms: 1.02x faster                                                   |
| sympy_str                  | 274 ms                                                                 | 269 ms: 1.02x faster                                                   |
| 2to3                       | 259 ms                                                                 | 255 ms: 1.02x faster                                                   |
| meteor_contest             | 101 ms                                                                 | 99.7 ms: 1.02x faster                                                  |
| comprehensions             | 16.6 us                                                                | 16.3 us: 1.02x faster                                                  |
| sympy_sum                  | 154 ms                                                                 | 152 ms: 1.01x faster                                                   |
| xml_etree_process          | 59.2 ms                                                                | 58.4 ms: 1.01x faster                                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.44 sec: 1.01x faster                                                 |
| mdp                        | 2.34 sec                                                               | 2.33 sec: 1.00x faster                                                 |
| crypto_pyaes               | 68.2 ms                                                                | 67.9 ms: 1.00x faster                                                  |
| sqlglot_transpile          | 1.55 ms                                                                | 1.57 ms: 1.01x slower                                                  |
| pycparser                  | 1.12 sec                                                               | 1.13 sec: 1.01x slower                                                 |
| dulwich_log                | 74.5 ms                                                                | 75.3 ms: 1.01x slower                                                  |
| nqueens                    | 77.7 ms                                                                | 78.7 ms: 1.01x slower                                                  |
| sqlglot_parse              | 1.25 ms                                                                | 1.26 ms: 1.01x slower                                                  |
| fannkuch                   | 376 ms                                                                 | 382 ms: 1.02x slower                                                   |
| scimark_lu                 | 112 ms                                                                 | 114 ms: 1.02x slower                                                   |
| chaos                      | 56.3 ms                                                                | 57.3 ms: 1.02x slower                                                  |
| django_template            | 34.2 ms                                                                | 34.9 ms: 1.02x slower                                                  |
| generators                 | 28.5 ms                                                                | 29.3 ms: 1.03x slower                                                  |
| deltablue                  | 3.10 ms                                                                | 3.18 ms: 1.03x slower                                                  |
| json                       | 4.98 ms                                                                | 5.12 ms: 1.03x slower                                                  |
| logging_silent             | 98.2 ns                                                                | 101 ns: 1.03x slower                                                   |
| mako                       | 11.2 ms                                                                | 11.6 ms: 1.03x slower                                                  |
| json_loads                 | 27.3 us                                                                | 28.2 us: 1.03x slower                                                  |
| unpickle_pure_python       | 208 us                                                                 | 215 us: 1.03x slower                                                   |
| regex_v8                   | 23.2 ms                                                                | 24.1 ms: 1.04x slower                                                  |
| raytrace                   | 250 ms                                                                 | 262 ms: 1.05x slower                                                   |
| pickle_pure_python         | 292 us                                                                 | 310 us: 1.06x slower                                                   |
| json_dumps                 | 10.6 ms                                                                | 11.3 ms: 1.07x slower                                                  |
| nbody                      | 85.3 ms                                                                | 91.1 ms: 1.07x slower                                                  |
| bench_thread_pool          | 924 us                                                                 | 1.03 ms: 1.11x slower                                                  |
| gc_traversal               | 3.32 ms                                                                | 4.31 ms: 1.30x slower                                                  |
| python_startup             | 11.0 ms                                                                | 14.6 ms: 1.32x slower                                                  |
| create_gc_cycles           | 1.33 ms                                                                | 1.84 ms: 1.38x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                                | 87.5 ms: 7.95x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.02x faster                                                           |

Benchmark hidden because not significant (8): scimark_monte_carlo, typing_runtime_protocols, hexiom, asyncio_websockets, python_startup_no_site, sympy_integrate, sympy_expand, pathlib
Ignored benchmarks (15) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250217-3.14.0a5+-99d9656/bm-20250217-vultr-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.048x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.10x