# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: eb8ce39
- commit date: 2024-12-05
- overall geometric mean: 1.212x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.16x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 361 ms: 1.37x slower                                                  |
| docutils       | 2.64 sec                                               | 3.07 sec: 1.16x slower                                                |
| html5lib       | 63.6 ms                                                | 98.7 ms: 1.55x slower                                                 |
| Geometric mean | (ref)                                                  | 1.35x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 786 ms: 1.41x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 811 ms: 1.33x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 432 ms: 1.29x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 345 ms: 1.29x faster                                                  |
| async_tree_none            | 464 ms                                                 | 374 ms: 1.24x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 453 ms: 1.23x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 610 ms: 1.18x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 626 ms: 1.14x faster                                                  |
| coroutines                 | 23.9 ms                                                | 25.1 ms: 1.05x slower                                                 |
| async_generators           | 384 ms                                                 | 453 ms: 1.18x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.16x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 184 ms: 1.00x faster                                                  |
| nbody          | 89.3 ms                                                | 125 ms: 1.39x slower                                                  |
| float          | 80.8 ms                                                | 137 ms: 1.70x slower                                                  |
| Geometric mean | (ref)                                                  | 1.33x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.81 ms: 1.13x faster                                                 |
| regex_dna      | 168 ms                                                 | 184 ms: 1.10x slower                                                  |
| regex_v8       | 20.6 ms                                                | 24.2 ms: 1.18x slower                                                 |
| regex_compile  | 142 ms                                                 | 179 ms: 1.26x slower                                                  |
| Geometric mean | (ref)                                                  | 1.10x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 91.5 ms: 1.06x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                  |
| json_loads           | 26.5 us                                                | 28.8 us: 1.09x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 97.4 ms: 1.14x slower                                                 |
| tomli_loads          | 2.11 sec                                               | 2.64 sec: 1.26x slower                                                |
| xml_etree_process    | 59.0 ms                                                | 78.5 ms: 1.33x slower                                                 |
| json_dumps           | 10.4 ms                                                | 14.3 ms: 1.38x slower                                                 |
| unpickle_pure_python | 221 us                                                 | 331 us: 1.50x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 518 us: 1.68x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.23x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.2 ms: 1.43x slower                                                 |
| python_startup         | 9.93 ms                                                | 17.1 ms: 1.73x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.57x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 62.7 ms: 1.25x slower                                                 |
| genshi_text     | 22.8 ms                                                | 30.4 ms: 1.33x slower                                                 |
| django_template | 34.7 ms                                                | 50.2 ms: 1.45x slower                                                 |
| mako            | 11.0 ms                                                | 16.8 ms: 1.53x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.39x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 786 ms: 1.41x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 811 ms: 1.33x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 432 ms: 1.29x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 345 ms: 1.29x faster                                                  |
| async_tree_none            | 464 ms                                                 | 374 ms: 1.24x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 453 ms: 1.23x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 610 ms: 1.18x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 626 ms: 1.14x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.81 ms: 1.13x faster                                                 |
| deepcopy                   | 352 us                                                 | 320 us: 1.10x faster                                                  |
| pathlib                    | 21.5 ms                                                | 20.1 ms: 1.07x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 91.5 ms: 1.06x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                  |
| gc_traversal               | 3.46 ms                                                | 3.29 ms: 1.05x faster                                                 |
| deepcopy_memo              | 40.3 us                                                | 39.5 us: 1.02x faster                                                 |
| pidigits                   | 184 ms                                                 | 184 ms: 1.00x faster                                                  |
| json                       | 5.02 ms                                                | 5.06 ms: 1.01x slower                                                 |
| sqlite_synth               | 2.20 us                                                | 2.22 us: 1.01x slower                                                 |
| coroutines                 | 23.9 ms                                                | 25.1 ms: 1.05x slower                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 5.00 sec: 1.06x slower                                                |
| spectral_norm              | 110 ms                                                 | 119 ms: 1.08x slower                                                  |
| json_loads                 | 26.5 us                                                | 28.8 us: 1.09x slower                                                 |
| regex_dna                  | 168 ms                                                 | 184 ms: 1.10x slower                                                  |
| deepcopy_reduce            | 3.08 us                                                | 3.44 us: 1.12x slower                                                 |
| mdp                        | 2.42 sec                                               | 2.74 sec: 1.13x slower                                                |
| xml_etree_generate         | 85.2 ms                                                | 97.4 ms: 1.14x slower                                                 |
| scimark_fft                | 342 ms                                                 | 391 ms: 1.15x slower                                                  |
| pylint                     | 319 ms                                                 | 370 ms: 1.16x slower                                                  |
| docutils                   | 2.64 sec                                               | 3.07 sec: 1.16x slower                                                |
| regex_v8                   | 20.6 ms                                                | 24.2 ms: 1.18x slower                                                 |
| async_generators           | 384 ms                                                 | 453 ms: 1.18x slower                                                  |
| generators                 | 32.2 ms                                                | 38.1 ms: 1.18x slower                                                 |
| crypto_pyaes               | 76.6 ms                                                | 91.6 ms: 1.20x slower                                                 |
| dulwich_log                | 78.9 ms                                                | 95.0 ms: 1.20x slower                                                 |
| nqueens                    | 80.1 ms                                                | 96.5 ms: 1.21x slower                                                 |
| meteor_contest             | 104 ms                                                 | 129 ms: 1.24x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 62.7 ms: 1.25x slower                                                 |
| typing_runtime_protocols   | 163 us                                                 | 204 us: 1.25x slower                                                  |
| sqlglot_optimize           | 53.3 ms                                                | 66.8 ms: 1.25x slower                                                 |
| tomli_loads                | 2.11 sec                                               | 2.64 sec: 1.26x slower                                                |
| regex_compile              | 142 ms                                                 | 179 ms: 1.26x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.57 ms: 1.27x slower                                                 |
| sqlglot_normalize          | 107 ms                                                 | 136 ms: 1.27x slower                                                  |
| pprint_safe_repr           | 743 ms                                                 | 959 ms: 1.29x slower                                                  |
| pycparser                  | 1.17 sec                                               | 1.53 sec: 1.31x slower                                                |
| pprint_pformat             | 1.52 sec                                               | 1.99 sec: 1.31x slower                                                |
| telco                      | 6.53 ms                                                | 8.59 ms: 1.32x slower                                                 |
| fannkuch                   | 372 ms                                                 | 491 ms: 1.32x slower                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 28.8 ms: 1.32x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 78.5 ms: 1.33x slower                                                 |
| genshi_text                | 22.8 ms                                                | 30.4 ms: 1.33x slower                                                 |
| 2to3                       | 264 ms                                                 | 361 ms: 1.37x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 14.3 ms: 1.38x slower                                                 |
| comprehensions             | 19.8 us                                                | 27.5 us: 1.39x slower                                                 |
| nbody                      | 89.3 ms                                                | 125 ms: 1.39x slower                                                  |
| thrift                     | 791 us                                                 | 1.11 ms: 1.41x slower                                                 |
| sqlalchemy_declarative     | 143 ms                                                 | 201 ms: 1.41x slower                                                  |
| coverage                   | 71.4 ms                                                | 101 ms: 1.42x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 29.3 ms: 1.43x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 10.2 ms: 1.43x slower                                                 |
| django_template            | 34.7 ms                                                | 50.2 ms: 1.45x slower                                                 |
| logging_simple             | 6.63 us                                                | 9.82 us: 1.48x slower                                                 |
| logging_format             | 7.35 us                                                | 10.9 us: 1.49x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 331 us: 1.50x slower                                                  |
| mako                       | 11.0 ms                                                | 16.8 ms: 1.53x slower                                                 |
| pyflate                    | 448 ms                                                 | 690 ms: 1.54x slower                                                  |
| html5lib                   | 63.6 ms                                                | 98.7 ms: 1.55x slower                                                 |
| hexiom                     | 6.17 ms                                                | 9.78 ms: 1.58x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 182 ms: 1.60x slower                                                  |
| sympy_str                  | 292 ms                                                 | 474 ms: 1.62x slower                                                  |
| chaos                      | 62.8 ms                                                | 103 ms: 1.63x slower                                                  |
| richards_super             | 51.9 ms                                                | 85.5 ms: 1.65x slower                                                 |
| richards                   | 45.9 ms                                                | 76.1 ms: 1.66x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.81 ms: 1.66x slower                                                 |
| pickle_pure_python         | 308 us                                                 | 518 us: 1.68x slower                                                  |
| logging_silent             | 109 ns                                                 | 184 ns: 1.69x slower                                                  |
| float                      | 80.8 ms                                                | 137 ms: 1.70x slower                                                  |
| python_startup             | 9.93 ms                                                | 17.1 ms: 1.73x slower                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 119 ms: 1.74x slower                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 2.93 ms: 1.75x slower                                                 |
| scimark_sor                | 130 ms                                                 | 233 ms: 1.79x slower                                                  |
| raytrace                   | 299 ms                                                 | 551 ms: 1.84x slower                                                  |
| sqlglot_parse              | 1.36 ms                                                | 2.54 ms: 1.88x slower                                                 |
| go                         | 139 ms                                                 | 266 ms: 1.91x slower                                                  |
| sympy_expand               | 468 ms                                                 | 952 ms: 2.03x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 348 ms: 2.10x slower                                                  |
| deltablue                  | 3.45 ms                                                | 8.08 ms: 2.35x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.32 ms: 3.52x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 108 ms: 10.00x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.32x slower                                                          |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241205-3.14.0a2+-eb8ce39-NOGIL/bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.212x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.19x
- 95% likely to have a slowdown of 1.18x
- 99% likely to have a slowdown of 1.16x

# Memory
- memory change: 1.33x