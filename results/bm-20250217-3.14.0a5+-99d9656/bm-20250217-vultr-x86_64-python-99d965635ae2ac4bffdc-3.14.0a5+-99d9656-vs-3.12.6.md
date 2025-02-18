# Results vs. 3.12.6

- fork: python
- ref: 99d965635ae2ac4bffdc
- machine: linux-x86_64
- commit hash: 99d9656
- commit date: 2025-02-17
- overall geometric mean: 1.088x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250217-vultr-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 255 ms: 1.03x faster                                                   |
| docutils       | 2.64 sec                                               | 2.56 sec: 1.03x faster                                                 |
| Geometric mean | (ref)                                                  | 1.03x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250217-vultr-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 315 ms: 1.78x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 627 ms: 1.77x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 622 ms: 1.74x faster                                                   |
| async_tree_none            | 464 ms                                                 | 270 ms: 1.72x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 323 ms: 1.72x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 262 ms: 1.70x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 489 ms: 1.48x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 499 ms: 1.43x faster                                                   |
| async_generators           | 384 ms                                                 | 326 ms: 1.18x faster                                                   |
| coroutines                 | 23.9 ms                                                | 22.0 ms: 1.09x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.48x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250217-vultr-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 72.3 ms: 1.12x faster                                                  |
| nbody          | 89.3 ms                                                | 91.1 ms: 1.02x slower                                                  |
| pidigits       | 184 ms                                                 | 198 ms: 1.07x slower                                                   |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250217-vultr-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.69 ms: 1.18x faster                                                  |
| regex_compile  | 142 ms                                                 | 126 ms: 1.13x faster                                                   |
| regex_dna      | 168 ms                                                 | 169 ms: 1.01x slower                                                   |
| regex_v8       | 20.6 ms                                                | 24.1 ms: 1.17x slower                                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250217-vultr-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.91 sec: 1.10x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                                   |
| xml_etree_iterparse  | 96.7 ms                                                | 91.6 ms: 1.06x faster                                                  |
| xml_etree_generate   | 85.2 ms                                                | 83.0 ms: 1.03x faster                                                  |
| unpickle_pure_python | 221 us                                                 | 215 us: 1.03x faster                                                   |
| xml_etree_process    | 59.0 ms                                                | 58.4 ms: 1.01x faster                                                  |
| pickle_pure_python   | 308 us                                                 | 310 us: 1.01x slower                                                   |
| json_loads           | 26.5 us                                                | 28.2 us: 1.06x slower                                                  |
| json_dumps           | 10.4 ms                                                | 11.3 ms: 1.09x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250217-vultr-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.42 ms: 1.04x slower                                                  |
| python_startup         | 9.93 ms                                                | 14.6 ms: 1.47x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.23x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250217-vultr-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 21.3 ms: 1.07x faster                                                  |
| genshi_xml      | 50.2 ms                                                | 48.0 ms: 1.05x faster                                                  |
| django_template | 34.7 ms                                                | 34.9 ms: 1.01x slower                                                  |
| mako            | 11.0 ms                                                | 11.6 ms: 1.05x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.01x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250217-vultr-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 315 ms: 1.78x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 627 ms: 1.77x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 622 ms: 1.74x faster                                                   |
| async_tree_none            | 464 ms                                                 | 270 ms: 1.72x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 323 ms: 1.72x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 262 ms: 1.70x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 489 ms: 1.48x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 499 ms: 1.43x faster                                                   |
| deepcopy                   | 352 us                                                 | 254 us: 1.38x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 30.6 us: 1.32x faster                                                  |
| comprehensions             | 19.8 us                                                | 16.3 us: 1.21x faster                                                  |
| go                         | 139 ms                                                 | 115 ms: 1.21x faster                                                   |
| deepcopy_reduce            | 3.08 us                                                | 2.61 us: 1.18x faster                                                  |
| async_generators           | 384 ms                                                 | 326 ms: 1.18x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.69 ms: 1.18x faster                                                  |
| spectral_norm              | 110 ms                                                 | 93.6 ms: 1.18x faster                                                  |
| pylint                     | 319 ms                                                 | 277 ms: 1.15x faster                                                   |
| raytrace                   | 299 ms                                                 | 262 ms: 1.14x faster                                                   |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.1 ms: 1.14x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.18 sec: 1.13x faster                                                 |
| regex_compile              | 142 ms                                                 | 126 ms: 1.13x faster                                                   |
| sqlalchemy_declarative     | 143 ms                                                 | 127 ms: 1.13x faster                                                   |
| crypto_pyaes               | 76.6 ms                                                | 67.9 ms: 1.13x faster                                                  |
| scimark_sor                | 130 ms                                                 | 115 ms: 1.12x faster                                                   |
| logging_simple             | 6.63 us                                                | 5.90 us: 1.12x faster                                                  |
| float                      | 80.8 ms                                                | 72.3 ms: 1.12x faster                                                  |
| pathlib                    | 21.5 ms                                                | 19.3 ms: 1.12x faster                                                  |
| logging_format             | 7.35 us                                                | 6.60 us: 1.11x faster                                                  |
| tomli_loads                | 2.11 sec                                               | 1.91 sec: 1.10x faster                                                 |
| generators                 | 32.2 ms                                                | 29.3 ms: 1.10x faster                                                  |
| richards                   | 45.9 ms                                                | 41.9 ms: 1.10x faster                                                  |
| chaos                      | 62.8 ms                                                | 57.3 ms: 1.10x faster                                                  |
| sympy_sum                  | 166 ms                                                 | 152 ms: 1.09x faster                                                   |
| coroutines                 | 23.9 ms                                                | 22.0 ms: 1.09x faster                                                  |
| richards_super             | 51.9 ms                                                | 47.8 ms: 1.09x faster                                                  |
| deltablue                  | 3.45 ms                                                | 3.18 ms: 1.08x faster                                                  |
| pyflate                    | 448 ms                                                 | 413 ms: 1.08x faster                                                   |
| sympy_str                  | 292 ms                                                 | 269 ms: 1.08x faster                                                   |
| logging_silent             | 109 ns                                                 | 101 ns: 1.08x faster                                                   |
| sqlglot_parse              | 1.36 ms                                                | 1.26 ms: 1.07x faster                                                  |
| genshi_text                | 22.8 ms                                                | 21.3 ms: 1.07x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                                   |
| sqlglot_transpile          | 1.67 ms                                                | 1.57 ms: 1.07x faster                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.44 sec: 1.06x faster                                                 |
| scimark_fft                | 342 ms                                                 | 323 ms: 1.06x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 91.6 ms: 1.06x faster                                                  |
| pprint_safe_repr           | 743 ms                                                 | 705 ms: 1.05x faster                                                   |
| typing_runtime_protocols   | 163 us                                                 | 155 us: 1.05x faster                                                   |
| thrift                     | 791 us                                                 | 753 us: 1.05x faster                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 65.1 ms: 1.05x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 75.3 ms: 1.05x faster                                                  |
| genshi_xml                 | 50.2 ms                                                | 48.0 ms: 1.05x faster                                                  |
| sympy_integrate            | 20.5 ms                                                | 19.7 ms: 1.04x faster                                                  |
| sqlglot_normalize          | 107 ms                                                 | 103 ms: 1.04x faster                                                   |
| meteor_contest             | 104 ms                                                 | 99.7 ms: 1.04x faster                                                  |
| hexiom                     | 6.17 ms                                                | 5.94 ms: 1.04x faster                                                  |
| mdp                        | 2.42 sec                                               | 2.33 sec: 1.04x faster                                                 |
| sqlglot_optimize           | 53.3 ms                                                | 51.4 ms: 1.04x faster                                                  |
| 2to3                       | 264 ms                                                 | 255 ms: 1.03x faster                                                   |
| pycparser                  | 1.17 sec                                               | 1.13 sec: 1.03x faster                                                 |
| docutils                   | 2.64 sec                                               | 2.56 sec: 1.03x faster                                                 |
| sympy_expand               | 468 ms                                                 | 454 ms: 1.03x faster                                                   |
| xml_etree_generate         | 85.2 ms                                                | 83.0 ms: 1.03x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 215 us: 1.03x faster                                                   |
| nqueens                    | 80.1 ms                                                | 78.7 ms: 1.02x faster                                                  |
| xml_etree_process          | 59.0 ms                                                | 58.4 ms: 1.01x faster                                                  |
| django_template            | 34.7 ms                                                | 34.9 ms: 1.01x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 310 us: 1.01x slower                                                   |
| regex_dna                  | 168 ms                                                 | 169 ms: 1.01x slower                                                   |
| json                       | 5.02 ms                                                | 5.12 ms: 1.02x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.48 ms: 1.02x slower                                                  |
| nbody                      | 89.3 ms                                                | 91.1 ms: 1.02x slower                                                  |
| fannkuch                   | 372 ms                                                 | 382 ms: 1.03x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 7.42 ms: 1.04x slower                                                  |
| mako                       | 11.0 ms                                                | 11.6 ms: 1.05x slower                                                  |
| json_loads                 | 26.5 us                                                | 28.2 us: 1.06x slower                                                  |
| pidigits                   | 184 ms                                                 | 198 ms: 1.07x slower                                                   |
| bench_thread_pool          | 941 us                                                 | 1.03 ms: 1.09x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 11.3 ms: 1.09x slower                                                  |
| coverage                   | 71.4 ms                                                | 78.6 ms: 1.10x slower                                                  |
| telco                      | 6.53 ms                                                | 7.23 ms: 1.11x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 24.1 ms: 1.17x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 4.31 ms: 1.25x slower                                                  |
| python_startup             | 9.93 ms                                                | 14.6 ms: 1.47x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.84 ms: 1.68x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 87.5 ms: 8.10x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                           |

Benchmark hidden because not significant (3): sqlite_synth, asyncio_websockets, scimark_lu
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250217-3.14.0a5+-99d9656/bm-20250217-vultr-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5+-99d9656.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.088x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.12x