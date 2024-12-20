# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: 1b787b3
- commit date: 2024-12-20
- overall geometric mean: 1.086x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-1b787b3 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 322 ms: 1.22x slower                                                  |
| docutils       | 2.64 sec                                               | 2.85 sec: 1.08x slower                                                |
| html5lib       | 63.6 ms                                                | 73.7 ms: 1.16x slower                                                 |
| Geometric mean | (ref)                                                  | 1.15x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-1b787b3 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 591 ms: 1.88x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 239 ms: 1.87x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 311 ms: 1.80x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 606 ms: 1.79x faster                                                  |
| async_tree_none            | 464 ms                                                 | 284 ms: 1.64x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 349 ms: 1.59x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 483 ms: 1.50x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 520 ms: 1.37x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 520 ms: 1.01x slower                                                  |
| coroutines                 | 23.9 ms                                                | 24.4 ms: 1.02x slower                                                 |
| async_generators           | 384 ms                                                 | 414 ms: 1.08x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.44x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-1b787b3 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 184 ms: 1.00x faster                                                  |
| float          | 80.8 ms                                                | 81.3 ms: 1.01x slower                                                 |
| nbody          | 89.3 ms                                                | 130 ms: 1.46x slower                                                  |
| Geometric mean | (ref)                                                  | 1.14x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-1b787b3 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.68 ms: 1.18x faster                                                 |
| regex_dna      | 168 ms                                                 | 172 ms: 1.03x slower                                                  |
| regex_compile  | 142 ms                                                 | 150 ms: 1.06x slower                                                  |
| regex_v8       | 20.6 ms                                                | 23.5 ms: 1.14x slower                                                 |
| Geometric mean | (ref)                                                  | 1.01x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-1b787b3 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.3 ms: 1.10x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.07x faster                                                  |
| json_loads           | 26.5 us                                                | 28.1 us: 1.06x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 96.0 ms: 1.13x slower                                                 |
| unpickle_pure_python | 221 us                                                 | 254 us: 1.15x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 68.2 ms: 1.16x slower                                                 |
| tomli_loads          | 2.11 sec                                               | 2.52 sec: 1.20x slower                                                |
| pickle_pure_python   | 308 us                                                 | 370 us: 1.20x slower                                                  |
| json_dumps           | 10.4 ms                                                | 13.1 ms: 1.26x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.11x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-1b787b3 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.2 ms: 1.42x slower                                                 |
| python_startup         | 9.93 ms                                                | 17.1 ms: 1.72x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.56x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-1b787b3 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 60.0 ms: 1.20x slower                                                 |
| django_template | 34.7 ms                                                | 42.4 ms: 1.22x slower                                                 |
| genshi_text     | 22.8 ms                                                | 28.3 ms: 1.24x slower                                                 |
| mako            | 11.0 ms                                                | 15.6 ms: 1.42x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.27x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-1b787b3 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 591 ms: 1.88x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 239 ms: 1.87x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 311 ms: 1.80x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 606 ms: 1.79x faster                                                  |
| async_tree_none            | 464 ms                                                 | 284 ms: 1.64x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 349 ms: 1.59x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 483 ms: 1.50x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 520 ms: 1.37x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.68 ms: 1.18x faster                                                 |
| pathlib                    | 21.5 ms                                                | 18.8 ms: 1.15x faster                                                 |
| deepcopy                   | 352 us                                                 | 311 us: 1.13x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 88.3 ms: 1.10x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.07x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 2.07 us: 1.06x faster                                                 |
| generators                 | 32.2 ms                                                | 30.5 ms: 1.06x faster                                                 |
| deepcopy_memo              | 40.3 us                                                | 38.4 us: 1.05x faster                                                 |
| json                       | 5.02 ms                                                | 4.96 ms: 1.01x faster                                                 |
| pidigits                   | 184 ms                                                 | 184 ms: 1.00x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.76 sec: 1.00x slower                                                |
| asyncio_websockets         | 517 ms                                                 | 520 ms: 1.01x slower                                                  |
| float                      | 80.8 ms                                                | 81.3 ms: 1.01x slower                                                 |
| gc_traversal               | 3.46 ms                                                | 3.49 ms: 1.01x slower                                                 |
| coroutines                 | 23.9 ms                                                | 24.4 ms: 1.02x slower                                                 |
| spectral_norm              | 110 ms                                                 | 113 ms: 1.02x slower                                                  |
| regex_dna                  | 168 ms                                                 | 172 ms: 1.03x slower                                                  |
| go                         | 139 ms                                                 | 143 ms: 1.03x slower                                                  |
| logging_silent             | 109 ns                                                 | 113 ns: 1.03x slower                                                  |
| pycparser                  | 1.17 sec                                               | 1.22 sec: 1.04x slower                                                |
| dulwich_log                | 78.9 ms                                                | 82.3 ms: 1.04x slower                                                 |
| deepcopy_reduce            | 3.08 us                                                | 3.23 us: 1.05x slower                                                 |
| regex_compile              | 142 ms                                                 | 150 ms: 1.06x slower                                                  |
| json_loads                 | 26.5 us                                                | 28.1 us: 1.06x slower                                                 |
| raytrace                   | 299 ms                                                 | 322 ms: 1.08x slower                                                  |
| async_generators           | 384 ms                                                 | 414 ms: 1.08x slower                                                  |
| docutils                   | 2.64 sec                                               | 2.85 sec: 1.08x slower                                                |
| comprehensions             | 19.8 us                                                | 21.4 us: 1.08x slower                                                 |
| pylint                     | 319 ms                                                 | 344 ms: 1.08x slower                                                  |
| logging_simple             | 6.63 us                                                | 7.21 us: 1.09x slower                                                 |
| scimark_fft                | 342 ms                                                 | 383 ms: 1.12x slower                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.5 ms: 1.12x slower                                                 |
| logging_format             | 7.35 us                                                | 8.27 us: 1.13x slower                                                 |
| xml_etree_generate         | 85.2 ms                                                | 96.0 ms: 1.13x slower                                                 |
| chaos                      | 62.8 ms                                                | 71.0 ms: 1.13x slower                                                 |
| sqlglot_normalize          | 107 ms                                                 | 121 ms: 1.14x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 23.5 ms: 1.14x slower                                                 |
| crypto_pyaes               | 76.6 ms                                                | 87.5 ms: 1.14x slower                                                 |
| thrift                     | 791 us                                                 | 905 us: 1.14x slower                                                  |
| pprint_safe_repr           | 743 ms                                                 | 850 ms: 1.14x slower                                                  |
| sqlglot_optimize           | 53.3 ms                                                | 60.9 ms: 1.14x slower                                                 |
| mdp                        | 2.42 sec                                               | 2.78 sec: 1.15x slower                                                |
| unpickle_pure_python       | 221 us                                                 | 254 us: 1.15x slower                                                  |
| pyflate                    | 448 ms                                                 | 516 ms: 1.15x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.75 sec: 1.15x slower                                                |
| sqlglot_transpile          | 1.67 ms                                                | 1.93 ms: 1.16x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 68.2 ms: 1.16x slower                                                 |
| html5lib                   | 63.6 ms                                                | 73.7 ms: 1.16x slower                                                 |
| sqlglot_parse              | 1.36 ms                                                | 1.60 ms: 1.18x slower                                                 |
| richards                   | 45.9 ms                                                | 54.8 ms: 1.19x slower                                                 |
| genshi_xml                 | 50.2 ms                                                | 60.0 ms: 1.20x slower                                                 |
| tomli_loads                | 2.11 sec                                               | 2.52 sec: 1.20x slower                                                |
| pickle_pure_python         | 308 us                                                 | 370 us: 1.20x slower                                                  |
| nqueens                    | 80.1 ms                                                | 97.1 ms: 1.21x slower                                                 |
| typing_runtime_protocols   | 163 us                                                 | 199 us: 1.22x slower                                                  |
| django_template            | 34.7 ms                                                | 42.4 ms: 1.22x slower                                                 |
| 2to3                       | 264 ms                                                 | 322 ms: 1.22x slower                                                  |
| richards_super             | 51.9 ms                                                | 63.8 ms: 1.23x slower                                                 |
| sqlalchemy_declarative     | 143 ms                                                 | 176 ms: 1.23x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 84.6 ms: 1.24x slower                                                 |
| genshi_text                | 22.8 ms                                                | 28.3 ms: 1.24x slower                                                 |
| hexiom                     | 6.17 ms                                                | 7.66 ms: 1.24x slower                                                 |
| scimark_sor                | 130 ms                                                 | 161 ms: 1.24x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 142 ms: 1.25x slower                                                  |
| meteor_contest             | 104 ms                                                 | 130 ms: 1.25x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 13.1 ms: 1.26x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.67 ms: 1.29x slower                                                 |
| telco                      | 6.53 ms                                                | 8.50 ms: 1.30x slower                                                 |
| fannkuch                   | 372 ms                                                 | 489 ms: 1.31x slower                                                  |
| deltablue                  | 3.45 ms                                                | 4.82 ms: 1.40x slower                                                 |
| sympy_integrate            | 20.5 ms                                                | 28.7 ms: 1.40x slower                                                 |
| coverage                   | 71.4 ms                                                | 100.0 ms: 1.40x slower                                                |
| python_startup_no_site     | 7.16 ms                                                | 10.2 ms: 1.42x slower                                                 |
| mako                       | 11.0 ms                                                | 15.6 ms: 1.42x slower                                                 |
| nbody                      | 89.3 ms                                                | 130 ms: 1.46x slower                                                  |
| sympy_str                  | 292 ms                                                 | 458 ms: 1.57x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.82 ms: 1.66x slower                                                 |
| python_startup             | 9.93 ms                                                | 17.1 ms: 1.72x slower                                                 |
| sympy_expand               | 468 ms                                                 | 926 ms: 1.98x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 341 ms: 2.06x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 3.33 ms: 3.54x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 105 ms: 9.76x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.13x slower                                                          |
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241220-3.14.0a3+-1b787b3-NOGIL/bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-1b787b3.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.086x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: 1.35x