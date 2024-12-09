# Results vs. 3.12.6

- fork: python
- ref: a03efb533a58fd13fb0c
- machine: linux-x86_64
- commit hash: a03efb5
- commit date: 2024-12-08
- overall geometric mean: 1.069x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241208-vultr-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 257 ms: 1.02x faster                                                   |
| docutils       | 2.64 sec                                               | 2.56 sec: 1.03x faster                                                 |
| Geometric mean | (ref)                                                  | 1.03x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241208-vultr-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 619 ms: 1.79x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 606 ms: 1.79x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 332 ms: 1.69x faster                                                   |
| async_tree_none            | 464 ms                                                 | 276 ms: 1.68x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 339 ms: 1.64x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 274 ms: 1.63x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 498 ms: 1.45x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 506 ms: 1.41x faster                                                   |
| coroutines                 | 23.9 ms                                                | 22.2 ms: 1.08x faster                                                  |
| async_generators           | 384 ms                                                 | 359 ms: 1.07x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 523 ms: 1.01x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.44x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241208-vultr-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 79.6 ms: 1.01x faster                                                  |
| pidigits       | 184 ms                                                 | 185 ms: 1.00x slower                                                   |
| nbody          | 89.3 ms                                                | 94.8 ms: 1.06x slower                                                  |
| Geometric mean | (ref)                                                  | 1.02x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241208-vultr-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.77 ms: 1.14x faster                                                  |
| regex_compile  | 142 ms                                                 | 129 ms: 1.11x faster                                                   |
| regex_dna      | 168 ms                                                 | 171 ms: 1.02x slower                                                   |
| regex_v8       | 20.6 ms                                                | 24.2 ms: 1.18x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241208-vultr-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 126 ms: 1.10x faster                                                   |
| json_loads           | 26.5 us                                                | 25.0 us: 1.06x faster                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 91.3 ms: 1.06x faster                                                  |
| unpickle_pure_python | 221 us                                                 | 214 us: 1.03x faster                                                   |
| tomli_loads          | 2.11 sec                                               | 2.09 sec: 1.01x faster                                                 |
| xml_etree_process    | 59.0 ms                                                | 59.5 ms: 1.01x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 323 us: 1.05x slower                                                   |
| json_dumps           | 10.4 ms                                                | 11.5 ms: 1.11x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (1): xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241208-vultr-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.48 ms: 1.05x slower                                                  |
| python_startup         | 9.93 ms                                                | 14.6 ms: 1.47x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.24x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241208-vultr-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 22.2 ms: 1.03x faster                                                  |
| genshi_xml      | 50.2 ms                                                | 50.9 ms: 1.02x slower                                                  |
| django_template | 34.7 ms                                                | 36.3 ms: 1.05x slower                                                  |
| mako            | 11.0 ms                                                | 11.6 ms: 1.05x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.02x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241208-vultr-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 619 ms: 1.79x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 606 ms: 1.79x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 332 ms: 1.69x faster                                                   |
| async_tree_none            | 464 ms                                                 | 276 ms: 1.68x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 339 ms: 1.64x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 274 ms: 1.63x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 498 ms: 1.45x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 506 ms: 1.41x faster                                                   |
| deepcopy                   | 352 us                                                 | 262 us: 1.34x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 30.5 us: 1.32x faster                                                  |
| pathlib                    | 21.5 ms                                                | 18.2 ms: 1.19x faster                                                  |
| go                         | 139 ms                                                 | 118 ms: 1.18x faster                                                   |
| deepcopy_reduce            | 3.08 us                                                | 2.61 us: 1.18x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.77 ms: 1.14x faster                                                  |
| raytrace                   | 299 ms                                                 | 263 ms: 1.14x faster                                                   |
| pylint                     | 319 ms                                                 | 280 ms: 1.14x faster                                                   |
| crypto_pyaes               | 76.6 ms                                                | 67.6 ms: 1.13x faster                                                  |
| comprehensions             | 19.8 us                                                | 17.6 us: 1.13x faster                                                  |
| sqlalchemy_declarative     | 143 ms                                                 | 127 ms: 1.12x faster                                                   |
| generators                 | 32.2 ms                                                | 28.8 ms: 1.12x faster                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.5 ms: 1.12x faster                                                  |
| json                       | 5.02 ms                                                | 4.53 ms: 1.11x faster                                                  |
| regex_compile              | 142 ms                                                 | 129 ms: 1.11x faster                                                   |
| logging_simple             | 6.63 us                                                | 6.03 us: 1.10x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 126 ms: 1.10x faster                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 4.33 sec: 1.09x faster                                                 |
| coroutines                 | 23.9 ms                                                | 22.2 ms: 1.08x faster                                                  |
| chaos                      | 62.8 ms                                                | 58.4 ms: 1.08x faster                                                  |
| sympy_sum                  | 166 ms                                                 | 154 ms: 1.07x faster                                                   |
| async_generators           | 384 ms                                                 | 359 ms: 1.07x faster                                                   |
| deltablue                  | 3.45 ms                                                | 3.22 ms: 1.07x faster                                                  |
| logging_format             | 7.35 us                                                | 6.86 us: 1.07x faster                                                  |
| sympy_str                  | 292 ms                                                 | 274 ms: 1.06x faster                                                   |
| json_loads                 | 26.5 us                                                | 25.0 us: 1.06x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 91.3 ms: 1.06x faster                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 64.7 ms: 1.06x faster                                                  |
| logging_silent             | 109 ns                                                 | 103 ns: 1.06x faster                                                   |
| thrift                     | 791 us                                                 | 752 us: 1.05x faster                                                   |
| sqlglot_parse              | 1.36 ms                                                | 1.29 ms: 1.05x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.11 sec: 1.05x faster                                                 |
| hexiom                     | 6.17 ms                                                | 5.89 ms: 1.05x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 75.4 ms: 1.05x faster                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 1.60 ms: 1.04x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 214 us: 1.03x faster                                                   |
| sympy_integrate            | 20.5 ms                                                | 19.9 ms: 1.03x faster                                                  |
| meteor_contest             | 104 ms                                                 | 100 ms: 1.03x faster                                                   |
| docutils                   | 2.64 sec                                               | 2.56 sec: 1.03x faster                                                 |
| genshi_text                | 22.8 ms                                                | 22.2 ms: 1.03x faster                                                  |
| 2to3                       | 264 ms                                                 | 257 ms: 1.02x faster                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.49 sec: 1.02x faster                                                 |
| pprint_safe_repr           | 743 ms                                                 | 727 ms: 1.02x faster                                                   |
| typing_runtime_protocols   | 163 us                                                 | 160 us: 1.02x faster                                                   |
| sympy_expand               | 468 ms                                                 | 461 ms: 1.02x faster                                                   |
| float                      | 80.8 ms                                                | 79.6 ms: 1.01x faster                                                  |
| richards                   | 45.9 ms                                                | 45.4 ms: 1.01x faster                                                  |
| scimark_fft                | 342 ms                                                 | 338 ms: 1.01x faster                                                   |
| richards_super             | 51.9 ms                                                | 51.4 ms: 1.01x faster                                                  |
| nqueens                    | 80.1 ms                                                | 79.5 ms: 1.01x faster                                                  |
| tomli_loads                | 2.11 sec                                               | 2.09 sec: 1.01x faster                                                 |
| pyflate                    | 448 ms                                                 | 446 ms: 1.00x faster                                                   |
| pidigits                   | 184 ms                                                 | 185 ms: 1.00x slower                                                   |
| sqlglot_optimize           | 53.3 ms                                                | 53.7 ms: 1.01x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 59.5 ms: 1.01x slower                                                  |
| sqlite_synth               | 2.20 us                                                | 2.23 us: 1.01x slower                                                  |
| asyncio_websockets         | 517 ms                                                 | 523 ms: 1.01x slower                                                   |
| sqlglot_normalize          | 107 ms                                                 | 108 ms: 1.01x slower                                                   |
| genshi_xml                 | 50.2 ms                                                | 50.9 ms: 1.02x slower                                                  |
| fannkuch                   | 372 ms                                                 | 378 ms: 1.02x slower                                                   |
| regex_dna                  | 168 ms                                                 | 171 ms: 1.02x slower                                                   |
| scimark_sor                | 130 ms                                                 | 133 ms: 1.02x slower                                                   |
| mdp                        | 2.42 sec                                               | 2.48 sec: 1.03x slower                                                 |
| spectral_norm              | 110 ms                                                 | 113 ms: 1.03x slower                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.58 ms: 1.04x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 7.48 ms: 1.05x slower                                                  |
| django_template            | 34.7 ms                                                | 36.3 ms: 1.05x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 323 us: 1.05x slower                                                   |
| mako                       | 11.0 ms                                                | 11.6 ms: 1.05x slower                                                  |
| nbody                      | 89.3 ms                                                | 94.8 ms: 1.06x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.03 ms: 1.09x slower                                                  |
| telco                      | 6.53 ms                                                | 7.19 ms: 1.10x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 11.5 ms: 1.11x slower                                                  |
| coverage                   | 71.4 ms                                                | 79.8 ms: 1.12x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 24.2 ms: 1.18x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 4.07 ms: 1.18x slower                                                  |
| python_startup             | 9.93 ms                                                | 14.6 ms: 1.47x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.71 ms: 1.57x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 85.7 ms: 7.94x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                           |

Benchmark hidden because not significant (2): scimark_lu, xml_etree_generate
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241208-3.14.0a2+-a03efb5/bm-20241208-vultr-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.069x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.11x