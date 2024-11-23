# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_tlbc_call
- machine: linux-x86_64
- commit hash: 4c7837f
- commit date: 2024-11-21
- overall geometric mean: 1.49x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.26x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241121-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-4c7837f |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 411 ms: 1.56x slower                                                 |
| docutils       | 2.64 sec                                               | 3.32 sec: 1.26x slower                                               |
| html5lib       | 63.6 ms                                                | 106 ms: 1.67x slower                                                 |
| Geometric mean | (ref)                                                  | 1.49x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241121-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-4c7837f |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 914 ms: 1.21x faster                                                 |
| async_tree_none_tg         | 446 ms                                                 | 382 ms: 1.17x faster                                                 |
| async_tree_memoization_tg  | 560 ms                                                 | 481 ms: 1.16x faster                                                 |
| async_tree_io              | 1.08 sec                                               | 941 ms: 1.15x faster                                                 |
| async_tree_none            | 464 ms                                                 | 421 ms: 1.10x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 657 ms: 1.10x faster                                                 |
| async_tree_memoization     | 555 ms                                                 | 512 ms: 1.08x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 687 ms: 1.04x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 521 ms: 1.01x slower                                                 |
| coroutines                 | 23.9 ms                                                | 29.2 ms: 1.22x slower                                                |
| async_generators           | 384 ms                                                 | 481 ms: 1.25x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.05x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241121-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-4c7837f |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 183 ms: 1.01x faster                                                 |
| float          | 80.8 ms                                                | 148 ms: 1.83x slower                                                 |
| nbody          | 89.3 ms                                                | 200 ms: 2.25x slower                                                 |
| Geometric mean | (ref)                                                  | 1.60x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241121-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-4c7837f |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.81 ms: 1.13x faster                                                |
| regex_dna      | 168 ms                                                 | 185 ms: 1.10x slower                                                 |
| regex_v8       | 20.6 ms                                                | 25.0 ms: 1.21x slower                                                |
| regex_compile  | 142 ms                                                 | 219 ms: 1.53x slower                                                 |
| Geometric mean | (ref)                                                  | 1.16x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241121-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-4c7837f |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 133 ms: 1.05x faster                                                 |
| json_loads           | 26.5 us                                                | 28.3 us: 1.07x slower                                                |
| xml_etree_iterparse  | 96.7 ms                                                | 105 ms: 1.09x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 110 ms: 1.29x slower                                                 |
| json_dumps           | 10.4 ms                                                | 15.5 ms: 1.49x slower                                                |
| tomli_loads          | 2.11 sec                                               | 3.16 sec: 1.50x slower                                               |
| xml_etree_process    | 59.0 ms                                                | 90.0 ms: 1.53x slower                                                |
| unpickle_pure_python | 221 us                                                 | 388 us: 1.76x slower                                                 |
| pickle_pure_python   | 308 us                                                 | 598 us: 1.95x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.37x slower                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241121-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-4c7837f |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.3 ms: 1.44x slower                                                |
| python_startup         | 9.93 ms                                                | 17.6 ms: 1.77x slower                                                |
| Geometric mean         | (ref)                                                  | 1.60x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241121-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-4c7837f |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 81.0 ms: 1.61x slower                                                |
| genshi_text     | 22.8 ms                                                | 39.2 ms: 1.72x slower                                                |
| mako            | 11.0 ms                                                | 19.2 ms: 1.74x slower                                                |
| django_template | 34.7 ms                                                | 62.3 ms: 1.80x slower                                                |
| Geometric mean  | (ref)                                                  | 1.72x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241121-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-4c7837f |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 914 ms: 1.21x faster                                                 |
| async_tree_none_tg         | 446 ms                                                 | 382 ms: 1.17x faster                                                 |
| async_tree_memoization_tg  | 560 ms                                                 | 481 ms: 1.16x faster                                                 |
| async_tree_io              | 1.08 sec                                               | 941 ms: 1.15x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.81 ms: 1.13x faster                                                |
| async_tree_none            | 464 ms                                                 | 421 ms: 1.10x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 657 ms: 1.10x faster                                                 |
| async_tree_memoization     | 555 ms                                                 | 512 ms: 1.08x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 133 ms: 1.05x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 687 ms: 1.04x faster                                                 |
| pidigits                   | 184 ms                                                 | 183 ms: 1.01x faster                                                 |
| pathlib                    | 21.5 ms                                                | 21.6 ms: 1.00x slower                                                |
| asyncio_websockets         | 517 ms                                                 | 521 ms: 1.01x slower                                                 |
| gc_traversal               | 3.46 ms                                                | 3.50 ms: 1.01x slower                                                |
| json                       | 5.02 ms                                                | 5.17 ms: 1.03x slower                                                |
| json_loads                 | 26.5 us                                                | 28.3 us: 1.07x slower                                                |
| xml_etree_iterparse        | 96.7 ms                                                | 105 ms: 1.09x slower                                                 |
| sqlite_synth               | 2.20 us                                                | 2.42 us: 1.10x slower                                                |
| regex_dna                  | 168 ms                                                 | 185 ms: 1.10x slower                                                 |
| deepcopy                   | 352 us                                                 | 413 us: 1.17x slower                                                 |
| deepcopy_memo              | 40.3 us                                                | 48.4 us: 1.20x slower                                                |
| bpe_tokeniser              | 4.74 sec                                               | 5.69 sec: 1.20x slower                                               |
| regex_v8                   | 20.6 ms                                                | 25.0 ms: 1.21x slower                                                |
| coroutines                 | 23.9 ms                                                | 29.2 ms: 1.22x slower                                                |
| scimark_fft                | 342 ms                                                 | 417 ms: 1.22x slower                                                 |
| async_generators           | 384 ms                                                 | 481 ms: 1.25x slower                                                 |
| mdp                        | 2.42 sec                                               | 3.03 sec: 1.25x slower                                               |
| docutils                   | 2.64 sec                                               | 3.32 sec: 1.26x slower                                               |
| generators                 | 32.2 ms                                                | 41.1 ms: 1.27x slower                                                |
| xml_etree_generate         | 85.2 ms                                                | 110 ms: 1.29x slower                                                 |
| pylint                     | 319 ms                                                 | 416 ms: 1.31x slower                                                 |
| dulwich_log                | 78.9 ms                                                | 103 ms: 1.31x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.92 ms: 1.35x slower                                                |
| meteor_contest             | 104 ms                                                 | 143 ms: 1.38x slower                                                 |
| deepcopy_reduce            | 3.08 us                                                | 4.33 us: 1.41x slower                                                |
| coverage                   | 71.4 ms                                                | 101 ms: 1.41x slower                                                 |
| crypto_pyaes               | 76.6 ms                                                | 108 ms: 1.41x slower                                                 |
| nqueens                    | 80.1 ms                                                | 113 ms: 1.42x slower                                                 |
| pycparser                  | 1.17 sec                                               | 1.67 sec: 1.43x slower                                               |
| spectral_norm              | 110 ms                                                 | 158 ms: 1.43x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 10.3 ms: 1.44x slower                                                |
| telco                      | 6.53 ms                                                | 9.46 ms: 1.45x slower                                                |
| fannkuch                   | 372 ms                                                 | 551 ms: 1.48x slower                                                 |
| typing_runtime_protocols   | 163 us                                                 | 243 us: 1.49x slower                                                 |
| comprehensions             | 19.8 us                                                | 29.5 us: 1.49x slower                                                |
| json_dumps                 | 10.4 ms                                                | 15.5 ms: 1.49x slower                                                |
| tomli_loads                | 2.11 sec                                               | 3.16 sec: 1.50x slower                                               |
| xml_etree_process          | 59.0 ms                                                | 90.0 ms: 1.53x slower                                                |
| regex_compile              | 142 ms                                                 | 219 ms: 1.53x slower                                                 |
| 2to3                       | 264 ms                                                 | 411 ms: 1.56x slower                                                 |
| sympy_integrate            | 20.5 ms                                                | 32.6 ms: 1.58x slower                                                |
| thrift                     | 791 us                                                 | 1.26 ms: 1.59x slower                                                |
| sqlglot_optimize           | 53.3 ms                                                | 85.9 ms: 1.61x slower                                                |
| genshi_xml                 | 50.2 ms                                                | 81.0 ms: 1.61x slower                                                |
| sqlglot_normalize          | 107 ms                                                 | 174 ms: 1.63x slower                                                 |
| html5lib                   | 63.6 ms                                                | 106 ms: 1.67x slower                                                 |
| pyflate                    | 448 ms                                                 | 752 ms: 1.68x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.83 ms: 1.68x slower                                                |
| pprint_safe_repr           | 743 ms                                                 | 1.25 sec: 1.68x slower                                               |
| pprint_pformat             | 1.52 sec                                               | 2.60 sec: 1.71x slower                                               |
| genshi_text                | 22.8 ms                                                | 39.2 ms: 1.72x slower                                                |
| mako                       | 11.0 ms                                                | 19.2 ms: 1.74x slower                                                |
| unpickle_pure_python       | 221 us                                                 | 388 us: 1.76x slower                                                 |
| python_startup             | 9.93 ms                                                | 17.6 ms: 1.77x slower                                                |
| logging_format             | 7.35 us                                                | 13.1 us: 1.79x slower                                                |
| django_template            | 34.7 ms                                                | 62.3 ms: 1.80x slower                                                |
| logging_simple             | 6.63 us                                                | 11.9 us: 1.80x slower                                                |
| sympy_str                  | 292 ms                                                 | 533 ms: 1.83x slower                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 125 ms: 1.83x slower                                                 |
| float                      | 80.8 ms                                                | 148 ms: 1.83x slower                                                 |
| chaos                      | 62.8 ms                                                | 117 ms: 1.87x slower                                                 |
| logging_silent             | 109 ns                                                 | 208 ns: 1.91x slower                                                 |
| hexiom                     | 6.17 ms                                                | 11.8 ms: 1.91x slower                                                |
| richards                   | 45.9 ms                                                | 88.1 ms: 1.92x slower                                                |
| pickle_pure_python         | 308 us                                                 | 598 us: 1.95x slower                                                 |
| sqlglot_transpile          | 1.67 ms                                                | 3.30 ms: 1.98x slower                                                |
| raytrace                   | 299 ms                                                 | 602 ms: 2.01x slower                                                 |
| richards_super             | 51.9 ms                                                | 106 ms: 2.04x slower                                                 |
| scimark_sor                | 130 ms                                                 | 267 ms: 2.05x slower                                                 |
| sqlglot_parse              | 1.36 ms                                                | 2.80 ms: 2.06x slower                                                |
| scimark_lu                 | 114 ms                                                 | 236 ms: 2.07x slower                                                 |
| go                         | 139 ms                                                 | 291 ms: 2.09x slower                                                 |
| sympy_expand               | 468 ms                                                 | 1.04 sec: 2.23x slower                                               |
| nbody                      | 89.3 ms                                                | 200 ms: 2.25x slower                                                 |
| sympy_sum                  | 166 ms                                                 | 379 ms: 2.28x slower                                                 |
| deltablue                  | 3.45 ms                                                | 8.79 ms: 2.55x slower                                                |
| bench_thread_pool          | 941 us                                                 | 3.50 ms: 3.72x slower                                                |
| bench_mp_pool              | 10.8 ms                                                | 111 ms: 10.31x slower                                                |
| Geometric mean             | (ref)                                                  | 1.49x slower                                                         |
Ignored benchmarks (17) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241121-3.14.0a2+-4c7837f-NOGIL/bm-20241121-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-4c7837f.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.34x
- 95% likely to have a slowdown of 1.31x
- 99% likely to have a slowdown of 1.26x

# Memory
- memory change: 1.33x