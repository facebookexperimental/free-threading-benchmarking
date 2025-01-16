# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: 65a6ad3
- commit date: 2025-01-16
- overall geometric mean: 1.059x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 306 ms: 1.16x slower                                                  |
| docutils       | 2.64 sec                                               | 2.83 sec: 1.07x slower                                                |
| html5lib       | 63.6 ms                                                | 70.9 ms: 1.12x slower                                                 |
| Geometric mean | (ref)                                                  | 1.11x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 583 ms: 1.90x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 240 ms: 1.86x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 310 ms: 1.80x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 610 ms: 1.78x faster                                                  |
| async_tree_none            | 464 ms                                                 | 286 ms: 1.62x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 350 ms: 1.59x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 499 ms: 1.45x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 540 ms: 1.32x faster                                                  |
| async_generators           | 384 ms                                                 | 367 ms: 1.05x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.7 ms: 1.01x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 513 ms: 1.01x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.45x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 78.5 ms: 1.03x faster                                                 |
| pidigits       | 184 ms                                                 | 209 ms: 1.14x slower                                                  |
| nbody          | 89.3 ms                                                | 135 ms: 1.51x slower                                                  |
| Geometric mean | (ref)                                                  | 1.19x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.82 ms: 1.12x faster                                                 |
| regex_compile  | 142 ms                                                 | 152 ms: 1.07x slower                                                  |
| regex_dna      | 168 ms                                                 | 183 ms: 1.09x slower                                                  |
| regex_v8       | 20.6 ms                                                | 23.4 ms: 1.14x slower                                                 |
| Geometric mean | (ref)                                                  | 1.04x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.0 ms: 1.11x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.08x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 2.35 sec: 1.12x slower                                                |
| xml_etree_generate   | 85.2 ms                                                | 96.4 ms: 1.13x slower                                                 |
| unpickle_pure_python | 221 us                                                 | 252 us: 1.14x slower                                                  |
| json_loads           | 26.5 us                                                | 30.7 us: 1.16x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 69.0 ms: 1.17x slower                                                 |
| pickle_pure_python   | 308 us                                                 | 377 us: 1.22x slower                                                  |
| json_dumps           | 10.4 ms                                                | 13.0 ms: 1.26x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.11x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.54 ms: 1.33x slower                                                 |
| python_startup         | 9.93 ms                                                | 15.2 ms: 1.53x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.43x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 60.4 ms: 1.20x slower                                                 |
| genshi_text     | 22.8 ms                                                | 28.2 ms: 1.24x slower                                                 |
| django_template | 34.7 ms                                                | 43.0 ms: 1.24x slower                                                 |
| mako            | 11.0 ms                                                | 15.6 ms: 1.42x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.27x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 583 ms: 1.90x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 240 ms: 1.86x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 310 ms: 1.80x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 610 ms: 1.78x faster                                                  |
| async_tree_none            | 464 ms                                                 | 286 ms: 1.62x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 350 ms: 1.59x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 499 ms: 1.45x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 540 ms: 1.32x faster                                                  |
| pathlib                    | 21.5 ms                                                | 18.7 ms: 1.15x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.82 ms: 1.12x faster                                                 |
| deepcopy                   | 352 us                                                 | 316 us: 1.11x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 87.0 ms: 1.11x faster                                                 |
| gc_traversal               | 3.46 ms                                                | 3.13 ms: 1.10x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 2.05 us: 1.08x faster                                                 |
| async_generators           | 384 ms                                                 | 367 ms: 1.05x faster                                                  |
| float                      | 80.8 ms                                                | 78.5 ms: 1.03x faster                                                 |
| deepcopy_memo              | 40.3 us                                                | 39.3 us: 1.02x faster                                                 |
| generators                 | 32.2 ms                                                | 31.5 ms: 1.02x faster                                                 |
| spectral_norm              | 110 ms                                                 | 108 ms: 1.02x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.7 ms: 1.01x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 513 ms: 1.01x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.74 sec: 1.00x slower                                                |
| pycparser                  | 1.17 sec                                               | 1.19 sec: 1.02x slower                                                |
| scimark_sor                | 130 ms                                                 | 133 ms: 1.02x slower                                                  |
| dulwich_log                | 78.9 ms                                                | 82.1 ms: 1.04x slower                                                 |
| comprehensions             | 19.8 us                                                | 20.9 us: 1.06x slower                                                 |
| json                       | 5.02 ms                                                | 5.33 ms: 1.06x slower                                                 |
| regex_compile              | 142 ms                                                 | 152 ms: 1.07x slower                                                  |
| docutils                   | 2.64 sec                                               | 2.83 sec: 1.07x slower                                                |
| logging_silent             | 109 ns                                                 | 118 ns: 1.08x slower                                                  |
| deepcopy_reduce            | 3.08 us                                                | 3.33 us: 1.08x slower                                                 |
| regex_dna                  | 168 ms                                                 | 183 ms: 1.09x slower                                                  |
| chaos                      | 62.8 ms                                                | 68.7 ms: 1.09x slower                                                 |
| raytrace                   | 299 ms                                                 | 330 ms: 1.10x slower                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.2 ms: 1.11x slower                                                 |
| logging_simple             | 6.63 us                                                | 7.37 us: 1.11x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 828 ms: 1.11x slower                                                  |
| html5lib                   | 63.6 ms                                                | 70.9 ms: 1.12x slower                                                 |
| tomli_loads                | 2.11 sec                                               | 2.35 sec: 1.12x slower                                                |
| pprint_pformat             | 1.52 sec                                               | 1.70 sec: 1.12x slower                                                |
| pyflate                    | 448 ms                                                 | 502 ms: 1.12x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 188 ms: 1.13x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 96.4 ms: 1.13x slower                                                 |
| scimark_fft                | 342 ms                                                 | 387 ms: 1.13x slower                                                  |
| pidigits                   | 184 ms                                                 | 209 ms: 1.14x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 23.4 ms: 1.14x slower                                                 |
| mdp                        | 2.42 sec                                               | 2.77 sec: 1.14x slower                                                |
| unpickle_pure_python       | 221 us                                                 | 252 us: 1.14x slower                                                  |
| sqlglot_normalize          | 107 ms                                                 | 122 ms: 1.15x slower                                                  |
| logging_format             | 7.35 us                                                | 8.43 us: 1.15x slower                                                 |
| sqlalchemy_declarative     | 143 ms                                                 | 164 ms: 1.15x slower                                                  |
| crypto_pyaes               | 76.6 ms                                                | 88.3 ms: 1.15x slower                                                 |
| sympy_str                  | 292 ms                                                 | 336 ms: 1.15x slower                                                  |
| thrift                     | 791 us                                                 | 914 us: 1.15x slower                                                  |
| json_loads                 | 26.5 us                                                | 30.7 us: 1.16x slower                                                 |
| 2to3                       | 264 ms                                                 | 306 ms: 1.16x slower                                                  |
| sqlglot_optimize           | 53.3 ms                                                | 62.1 ms: 1.17x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 69.0 ms: 1.17x slower                                                 |
| sqlglot_transpile          | 1.67 ms                                                | 1.96 ms: 1.17x slower                                                 |
| sympy_expand               | 468 ms                                                 | 552 ms: 1.18x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 24.3 ms: 1.18x slower                                                 |
| sqlglot_parse              | 1.36 ms                                                | 1.63 ms: 1.20x slower                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 82.2 ms: 1.20x slower                                                 |
| genshi_xml                 | 50.2 ms                                                | 60.4 ms: 1.20x slower                                                 |
| hexiom                     | 6.17 ms                                                | 7.44 ms: 1.21x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 138 ms: 1.21x slower                                                  |
| nqueens                    | 80.1 ms                                                | 96.9 ms: 1.21x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.32 ms: 1.21x slower                                                 |
| pickle_pure_python         | 308 us                                                 | 377 us: 1.22x slower                                                  |
| genshi_text                | 22.8 ms                                                | 28.2 ms: 1.24x slower                                                 |
| django_template            | 34.7 ms                                                | 43.0 ms: 1.24x slower                                                 |
| richards                   | 45.9 ms                                                | 57.3 ms: 1.25x slower                                                 |
| typing_runtime_protocols   | 163 us                                                 | 204 us: 1.25x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 13.0 ms: 1.26x slower                                                 |
| meteor_contest             | 104 ms                                                 | 131 ms: 1.27x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.63 ms: 1.28x slower                                                 |
| richards_super             | 51.9 ms                                                | 66.9 ms: 1.29x slower                                                 |
| fannkuch                   | 372 ms                                                 | 480 ms: 1.29x slower                                                  |
| telco                      | 6.53 ms                                                | 8.52 ms: 1.31x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 9.54 ms: 1.33x slower                                                 |
| deltablue                  | 3.45 ms                                                | 4.66 ms: 1.35x slower                                                 |
| coverage                   | 71.4 ms                                                | 97.9 ms: 1.37x slower                                                 |
| mako                       | 11.0 ms                                                | 15.6 ms: 1.42x slower                                                 |
| nbody                      | 89.3 ms                                                | 135 ms: 1.51x slower                                                  |
| python_startup             | 9.93 ms                                                | 15.2 ms: 1.53x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.33 ms: 3.53x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 94.7 ms: 8.77x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.10x slower                                                          |

Benchmark hidden because not significant (2): go, pylint
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250116-3.14.0a4+-65a6ad3-NOGIL/bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.059x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.35x