# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_tlbc_call_
- machine: linux-x86_64
- commit hash: b22403e
- commit date: 2024-12-05
- overall geometric mean: 1.221x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.17x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 366 ms: 1.39x slower                                                  |
| docutils       | 2.64 sec                                               | 3.08 sec: 1.17x slower                                                |
| html5lib       | 63.6 ms                                                | 96.9 ms: 1.52x slower                                                 |
| Geometric mean | (ref)                                                  | 1.35x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 817 ms: 1.36x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 842 ms: 1.29x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 352 ms: 1.27x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 444 ms: 1.26x faster                                                  |
| async_tree_none            | 464 ms                                                 | 383 ms: 1.21x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 468 ms: 1.19x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 611 ms: 1.18x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 632 ms: 1.13x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 522 ms: 1.01x slower                                                  |
| coroutines                 | 23.9 ms                                                | 24.3 ms: 1.01x slower                                                 |
| async_generators           | 384 ms                                                 | 451 ms: 1.17x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.15x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 181 ms: 1.02x faster                                                  |
| nbody          | 89.3 ms                                                | 131 ms: 1.47x slower                                                  |
| float          | 80.8 ms                                                | 139 ms: 1.72x slower                                                  |
| Geometric mean | (ref)                                                  | 1.35x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.84 ms: 1.11x faster                                                 |
| regex_dna      | 168 ms                                                 | 181 ms: 1.08x slower                                                  |
| regex_v8       | 20.6 ms                                                | 25.0 ms: 1.21x slower                                                 |
| regex_compile  | 142 ms                                                 | 181 ms: 1.27x slower                                                  |
| Geometric mean | (ref)                                                  | 1.10x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 91.3 ms: 1.06x faster                                                 |
| json_loads           | 26.5 us                                                | 28.5 us: 1.07x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 97.9 ms: 1.15x slower                                                 |
| tomli_loads          | 2.11 sec                                               | 2.67 sec: 1.27x slower                                                |
| xml_etree_process    | 59.0 ms                                                | 78.0 ms: 1.32x slower                                                 |
| json_dumps           | 10.4 ms                                                | 14.4 ms: 1.39x slower                                                 |
| unpickle_pure_python | 221 us                                                 | 331 us: 1.50x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 504 us: 1.64x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.23x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.3 ms: 1.44x slower                                                 |
| python_startup         | 9.93 ms                                                | 17.5 ms: 1.76x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.59x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 63.4 ms: 1.26x slower                                                 |
| genshi_text     | 22.8 ms                                                | 31.5 ms: 1.38x slower                                                 |
| django_template | 34.7 ms                                                | 50.3 ms: 1.45x slower                                                 |
| mako            | 11.0 ms                                                | 17.7 ms: 1.61x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.42x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 817 ms: 1.36x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 842 ms: 1.29x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 352 ms: 1.27x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 444 ms: 1.26x faster                                                  |
| async_tree_none            | 464 ms                                                 | 383 ms: 1.21x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 468 ms: 1.19x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 611 ms: 1.18x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 632 ms: 1.13x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.84 ms: 1.11x faster                                                 |
| deepcopy                   | 352 us                                                 | 327 us: 1.07x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 91.3 ms: 1.06x faster                                                 |
| pathlib                    | 21.5 ms                                                | 20.5 ms: 1.05x faster                                                 |
| pidigits                   | 184 ms                                                 | 181 ms: 1.02x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 522 ms: 1.01x slower                                                  |
| coroutines                 | 23.9 ms                                                | 24.3 ms: 1.01x slower                                                 |
| gc_traversal               | 3.46 ms                                                | 3.51 ms: 1.02x slower                                                 |
| json                       | 5.02 ms                                                | 5.12 ms: 1.02x slower                                                 |
| sqlite_synth               | 2.20 us                                                | 2.29 us: 1.04x slower                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.97 sec: 1.05x slower                                                |
| json_loads                 | 26.5 us                                                | 28.5 us: 1.07x slower                                                 |
| regex_dna                  | 168 ms                                                 | 181 ms: 1.08x slower                                                  |
| spectral_norm              | 110 ms                                                 | 122 ms: 1.10x slower                                                  |
| mdp                        | 2.42 sec                                               | 2.77 sec: 1.14x slower                                                |
| xml_etree_generate         | 85.2 ms                                                | 97.9 ms: 1.15x slower                                                 |
| deepcopy_reduce            | 3.08 us                                                | 3.54 us: 1.15x slower                                                 |
| docutils                   | 2.64 sec                                               | 3.08 sec: 1.17x slower                                                |
| async_generators           | 384 ms                                                 | 451 ms: 1.17x slower                                                  |
| generators                 | 32.2 ms                                                | 37.9 ms: 1.17x slower                                                 |
| crypto_pyaes               | 76.6 ms                                                | 90.7 ms: 1.18x slower                                                 |
| scimark_fft                | 342 ms                                                 | 405 ms: 1.19x slower                                                  |
| pylint                     | 319 ms                                                 | 380 ms: 1.19x slower                                                  |
| nqueens                    | 80.1 ms                                                | 96.7 ms: 1.21x slower                                                 |
| dulwich_log                | 78.9 ms                                                | 95.4 ms: 1.21x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 25.0 ms: 1.21x slower                                                 |
| typing_runtime_protocols   | 163 us                                                 | 202 us: 1.24x slower                                                  |
| meteor_contest             | 104 ms                                                 | 130 ms: 1.26x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 63.4 ms: 1.26x slower                                                 |
| tomli_loads                | 2.11 sec                                               | 2.67 sec: 1.27x slower                                                |
| regex_compile              | 142 ms                                                 | 181 ms: 1.27x slower                                                  |
| sqlglot_normalize          | 107 ms                                                 | 136 ms: 1.28x slower                                                  |
| sqlglot_optimize           | 53.3 ms                                                | 68.8 ms: 1.29x slower                                                 |
| pycparser                  | 1.17 sec                                               | 1.53 sec: 1.31x slower                                                |
| pprint_safe_repr           | 743 ms                                                 | 971 ms: 1.31x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 2.01 sec: 1.32x slower                                                |
| xml_etree_process          | 59.0 ms                                                | 78.0 ms: 1.32x slower                                                 |
| telco                      | 6.53 ms                                                | 8.64 ms: 1.32x slower                                                 |
| fannkuch                   | 372 ms                                                 | 497 ms: 1.34x slower                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 29.4 ms: 1.35x slower                                                 |
| comprehensions             | 19.8 us                                                | 26.9 us: 1.36x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.96 ms: 1.36x slower                                                 |
| genshi_text                | 22.8 ms                                                | 31.5 ms: 1.38x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 14.4 ms: 1.39x slower                                                 |
| 2to3                       | 264 ms                                                 | 366 ms: 1.39x slower                                                  |
| coverage                   | 71.4 ms                                                | 101 ms: 1.41x slower                                                  |
| sqlalchemy_declarative     | 143 ms                                                 | 203 ms: 1.42x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 29.4 ms: 1.43x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 10.3 ms: 1.44x slower                                                 |
| django_template            | 34.7 ms                                                | 50.3 ms: 1.45x slower                                                 |
| nbody                      | 89.3 ms                                                | 131 ms: 1.47x slower                                                  |
| thrift                     | 791 us                                                 | 1.16 ms: 1.47x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 331 us: 1.50x slower                                                  |
| html5lib                   | 63.6 ms                                                | 96.9 ms: 1.52x slower                                                 |
| pyflate                    | 448 ms                                                 | 695 ms: 1.55x slower                                                  |
| logging_simple             | 6.63 us                                                | 10.5 us: 1.58x slower                                                 |
| hexiom                     | 6.17 ms                                                | 9.83 ms: 1.59x slower                                                 |
| logging_format             | 7.35 us                                                | 11.7 us: 1.60x slower                                                 |
| mako                       | 11.0 ms                                                | 17.7 ms: 1.61x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 184 ms: 1.61x slower                                                  |
| sympy_str                  | 292 ms                                                 | 475 ms: 1.63x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 504 us: 1.64x slower                                                  |
| chaos                      | 62.8 ms                                                | 104 ms: 1.65x slower                                                  |
| richards_super             | 51.9 ms                                                | 85.9 ms: 1.66x slower                                                 |
| logging_silent             | 109 ns                                                 | 181 ns: 1.66x slower                                                  |
| richards                   | 45.9 ms                                                | 76.6 ms: 1.67x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.84 ms: 1.68x slower                                                 |
| float                      | 80.8 ms                                                | 139 ms: 1.72x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 119 ms: 1.73x slower                                                  |
| python_startup             | 9.93 ms                                                | 17.5 ms: 1.76x slower                                                 |
| sqlglot_transpile          | 1.67 ms                                                | 2.99 ms: 1.79x slower                                                 |
| scimark_sor                | 130 ms                                                 | 234 ms: 1.80x slower                                                  |
| raytrace                   | 299 ms                                                 | 549 ms: 1.83x slower                                                  |
| go                         | 139 ms                                                 | 264 ms: 1.90x slower                                                  |
| sqlglot_parse              | 1.36 ms                                                | 2.58 ms: 1.90x slower                                                 |
| sympy_expand               | 468 ms                                                 | 949 ms: 2.03x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 348 ms: 2.10x slower                                                  |
| deltablue                  | 3.45 ms                                                | 7.86 ms: 2.28x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.36 ms: 3.56x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 109 ms: 10.10x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.33x slower                                                          |

Benchmark hidden because not significant (1): deepcopy_memo
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241205-3.14.0a2+-b22403e-NOGIL/bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.221x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.20x
- 95% likely to have a slowdown of 1.19x
- 99% likely to have a slowdown of 1.17x

# Memory
- memory change: 1.33x