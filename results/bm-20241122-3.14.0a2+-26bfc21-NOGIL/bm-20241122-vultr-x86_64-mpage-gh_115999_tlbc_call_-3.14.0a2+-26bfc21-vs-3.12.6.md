# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_tlbc_call_
- machine: linux-x86_64
- commit hash: 26bfc21
- commit date: 2024-11-22
- overall geometric mean: 1.41x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.22x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 381 ms: 1.44x slower                                                  |
| docutils       | 2.64 sec                                               | 3.21 sec: 1.22x slower                                                |
| html5lib       | 63.6 ms                                                | 99.7 ms: 1.57x slower                                                 |
| Geometric mean | (ref)                                                  | 1.40x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 887 ms: 1.25x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 912 ms: 1.19x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 472 ms: 1.18x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 377 ms: 1.18x faster                                                  |
| async_tree_none            | 464 ms                                                 | 412 ms: 1.13x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 642 ms: 1.13x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 500 ms: 1.11x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 667 ms: 1.07x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 520 ms: 1.01x slower                                                  |
| coroutines                 | 23.9 ms                                                | 27.5 ms: 1.15x slower                                                 |
| async_generators           | 384 ms                                                 | 473 ms: 1.23x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 184 ms: 1.00x faster                                                  |
| nbody          | 89.3 ms                                                | 158 ms: 1.77x slower                                                  |
| float          | 80.8 ms                                                | 146 ms: 1.80x slower                                                  |
| Geometric mean | (ref)                                                  | 1.47x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.80 ms: 1.13x faster                                                 |
| regex_dna      | 168 ms                                                 | 181 ms: 1.08x slower                                                  |
| regex_v8       | 20.6 ms                                                | 25.3 ms: 1.23x slower                                                 |
| regex_compile  | 142 ms                                                 | 196 ms: 1.38x slower                                                  |
| Geometric mean | (ref)                                                  | 1.13x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 95.6 ms: 1.01x faster                                                 |
| json_loads           | 26.5 us                                                | 27.9 us: 1.05x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 103 ms: 1.21x slower                                                  |
| tomli_loads          | 2.11 sec                                               | 2.88 sec: 1.37x slower                                                |
| xml_etree_process    | 59.0 ms                                                | 82.6 ms: 1.40x slower                                                 |
| json_dumps           | 10.4 ms                                                | 14.5 ms: 1.40x slower                                                 |
| unpickle_pure_python | 221 us                                                 | 371 us: 1.68x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 545 us: 1.77x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.28x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.3 ms: 1.44x slower                                                 |
| python_startup         | 9.93 ms                                                | 17.5 ms: 1.76x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.59x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 68.1 ms: 1.36x slower                                                 |
| genshi_text     | 22.8 ms                                                | 34.2 ms: 1.50x slower                                                 |
| django_template | 34.7 ms                                                | 55.5 ms: 1.60x slower                                                 |
| mako            | 11.0 ms                                                | 19.7 ms: 1.79x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.55x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 887 ms: 1.25x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 912 ms: 1.19x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 472 ms: 1.18x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 377 ms: 1.18x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.80 ms: 1.13x faster                                                 |
| async_tree_none            | 464 ms                                                 | 412 ms: 1.13x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 642 ms: 1.13x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 500 ms: 1.11x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 667 ms: 1.07x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                  |
| pathlib                    | 21.5 ms                                                | 20.7 ms: 1.04x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 95.6 ms: 1.01x faster                                                 |
| pidigits                   | 184 ms                                                 | 184 ms: 1.00x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 520 ms: 1.01x slower                                                  |
| deepcopy                   | 352 us                                                 | 356 us: 1.01x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 3.51 ms: 1.02x slower                                                 |
| json_loads                 | 26.5 us                                                | 27.9 us: 1.05x slower                                                 |
| sqlite_synth               | 2.20 us                                                | 2.31 us: 1.05x slower                                                 |
| regex_dna                  | 168 ms                                                 | 181 ms: 1.08x slower                                                  |
| deepcopy_memo              | 40.3 us                                                | 45.2 us: 1.12x slower                                                 |
| coroutines                 | 23.9 ms                                                | 27.5 ms: 1.15x slower                                                 |
| spectral_norm              | 110 ms                                                 | 127 ms: 1.15x slower                                                  |
| scimark_fft                | 342 ms                                                 | 401 ms: 1.17x slower                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 5.64 sec: 1.19x slower                                                |
| xml_etree_generate         | 85.2 ms                                                | 103 ms: 1.21x slower                                                  |
| generators                 | 32.2 ms                                                | 39.0 ms: 1.21x slower                                                 |
| docutils                   | 2.64 sec                                               | 3.21 sec: 1.22x slower                                                |
| regex_v8                   | 20.6 ms                                                | 25.3 ms: 1.23x slower                                                 |
| deepcopy_reduce            | 3.08 us                                                | 3.79 us: 1.23x slower                                                 |
| async_generators           | 384 ms                                                 | 473 ms: 1.23x slower                                                  |
| pylint                     | 319 ms                                                 | 396 ms: 1.24x slower                                                  |
| mdp                        | 2.42 sec                                               | 3.02 sec: 1.25x slower                                                |
| dulwich_log                | 78.9 ms                                                | 98.7 ms: 1.25x slower                                                 |
| typing_runtime_protocols   | 163 us                                                 | 211 us: 1.29x slower                                                  |
| meteor_contest             | 104 ms                                                 | 136 ms: 1.31x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.80 ms: 1.32x slower                                                 |
| nqueens                    | 80.1 ms                                                | 108 ms: 1.34x slower                                                  |
| crypto_pyaes               | 76.6 ms                                                | 103 ms: 1.35x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 68.1 ms: 1.36x slower                                                 |
| tomli_loads                | 2.11 sec                                               | 2.88 sec: 1.37x slower                                                |
| pycparser                  | 1.17 sec                                               | 1.61 sec: 1.38x slower                                                |
| regex_compile              | 142 ms                                                 | 196 ms: 1.38x slower                                                  |
| telco                      | 6.53 ms                                                | 9.12 ms: 1.40x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 82.6 ms: 1.40x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 14.5 ms: 1.40x slower                                                 |
| sqlglot_normalize          | 107 ms                                                 | 149 ms: 1.40x slower                                                  |
| coverage                   | 71.4 ms                                                | 101 ms: 1.41x slower                                                  |
| sqlglot_optimize           | 53.3 ms                                                | 75.5 ms: 1.42x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 10.3 ms: 1.44x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 1.07 sec: 1.44x slower                                                |
| 2to3                       | 264 ms                                                 | 381 ms: 1.44x slower                                                  |
| comprehensions             | 19.8 us                                                | 28.9 us: 1.46x slower                                                 |
| pprint_pformat             | 1.52 sec                                               | 2.23 sec: 1.47x slower                                                |
| fannkuch                   | 372 ms                                                 | 550 ms: 1.48x slower                                                  |
| genshi_text                | 22.8 ms                                                | 34.2 ms: 1.50x slower                                                 |
| sympy_integrate            | 20.5 ms                                                | 31.3 ms: 1.52x slower                                                 |
| thrift                     | 791 us                                                 | 1.21 ms: 1.52x slower                                                 |
| html5lib                   | 63.6 ms                                                | 99.7 ms: 1.57x slower                                                 |
| django_template            | 34.7 ms                                                | 55.5 ms: 1.60x slower                                                 |
| pyflate                    | 448 ms                                                 | 738 ms: 1.65x slower                                                  |
| logging_simple             | 6.63 us                                                | 11.1 us: 1.67x slower                                                 |
| logging_format             | 7.35 us                                                | 12.3 us: 1.68x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 371 us: 1.68x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.85 ms: 1.69x slower                                                 |
| sympy_str                  | 292 ms                                                 | 497 ms: 1.70x slower                                                  |
| python_startup             | 9.93 ms                                                | 17.5 ms: 1.76x slower                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 121 ms: 1.77x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 545 us: 1.77x slower                                                  |
| nbody                      | 89.3 ms                                                | 158 ms: 1.77x slower                                                  |
| logging_silent             | 109 ns                                                 | 195 ns: 1.79x slower                                                  |
| mako                       | 11.0 ms                                                | 19.7 ms: 1.79x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 205 ms: 1.80x slower                                                  |
| float                      | 80.8 ms                                                | 146 ms: 1.80x slower                                                  |
| richards                   | 45.9 ms                                                | 83.6 ms: 1.82x slower                                                 |
| chaos                      | 62.8 ms                                                | 115 ms: 1.84x slower                                                  |
| hexiom                     | 6.17 ms                                                | 11.4 ms: 1.84x slower                                                 |
| sqlglot_transpile          | 1.67 ms                                                | 3.09 ms: 1.85x slower                                                 |
| scimark_sor                | 130 ms                                                 | 243 ms: 1.87x slower                                                  |
| richards_super             | 51.9 ms                                                | 99.7 ms: 1.92x slower                                                 |
| sqlglot_parse              | 1.36 ms                                                | 2.68 ms: 1.98x slower                                                 |
| raytrace                   | 299 ms                                                 | 601 ms: 2.01x slower                                                  |
| go                         | 139 ms                                                 | 284 ms: 2.04x slower                                                  |
| sympy_expand               | 468 ms                                                 | 991 ms: 2.12x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 358 ms: 2.15x slower                                                  |
| deltablue                  | 3.45 ms                                                | 8.65 ms: 2.51x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.42 ms: 3.64x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 110 ms: 10.18x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.41x slower                                                          |

Benchmark hidden because not significant (1): json
Ignored benchmarks (17) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241122-3.14.0a2+-26bfc21-NOGIL/bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.26x
- 95% likely to have a slowdown of 1.25x
- 99% likely to have a slowdown of 1.22x

# Memory
- memory change: 1.33x