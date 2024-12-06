# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_tlbc_call_
- machine: linux-x86_64
- commit hash: b22403e
- commit date: 2024-12-05
- overall geometric mean: 1.224x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.18x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 366 ms: 1.39x slower                                                  |
| docutils       | 2.64 sec                                               | 3.11 sec: 1.18x slower                                                |
| html5lib       | 63.6 ms                                                | 99.2 ms: 1.56x slower                                                 |
| Geometric mean | (ref)                                                  | 1.37x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 827 ms: 1.34x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 848 ms: 1.28x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 358 ms: 1.25x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 452 ms: 1.24x faster                                                  |
| async_tree_none            | 464 ms                                                 | 386 ms: 1.20x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 469 ms: 1.18x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 621 ms: 1.16x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 644 ms: 1.11x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 521 ms: 1.01x slower                                                  |
| async_generators           | 384 ms                                                 | 451 ms: 1.17x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.14x faster                                                          |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 184 ms: 1.00x faster                                                  |
| nbody          | 89.3 ms                                                | 131 ms: 1.47x slower                                                  |
| float          | 80.8 ms                                                | 140 ms: 1.73x slower                                                  |
| Geometric mean | (ref)                                                  | 1.36x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.90 ms: 1.09x faster                                                 |
| regex_dna      | 168 ms                                                 | 189 ms: 1.13x slower                                                  |
| regex_v8       | 20.6 ms                                                | 24.9 ms: 1.21x slower                                                 |
| regex_compile  | 142 ms                                                 | 180 ms: 1.26x slower                                                  |
| Geometric mean | (ref)                                                  | 1.12x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 91.6 ms: 1.06x faster                                                 |
| json_loads           | 26.5 us                                                | 28.7 us: 1.08x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 97.5 ms: 1.14x slower                                                 |
| tomli_loads          | 2.11 sec                                               | 2.66 sec: 1.26x slower                                                |
| xml_etree_process    | 59.0 ms                                                | 78.3 ms: 1.33x slower                                                 |
| json_dumps           | 10.4 ms                                                | 14.3 ms: 1.38x slower                                                 |
| unpickle_pure_python | 221 us                                                 | 334 us: 1.51x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 504 us: 1.64x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.23x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.3 ms: 1.43x slower                                                 |
| python_startup         | 9.93 ms                                                | 17.5 ms: 1.76x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.59x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 63.2 ms: 1.26x slower                                                 |
| genshi_text     | 22.8 ms                                                | 31.6 ms: 1.39x slower                                                 |
| django_template | 34.7 ms                                                | 50.7 ms: 1.46x slower                                                 |
| mako            | 11.0 ms                                                | 17.8 ms: 1.62x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.43x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 827 ms: 1.34x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 848 ms: 1.28x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 358 ms: 1.25x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 452 ms: 1.24x faster                                                  |
| async_tree_none            | 464 ms                                                 | 386 ms: 1.20x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 469 ms: 1.18x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 621 ms: 1.16x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 644 ms: 1.11x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.90 ms: 1.09x faster                                                 |
| deepcopy                   | 352 us                                                 | 328 us: 1.07x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                                  |
| pathlib                    | 21.5 ms                                                | 20.3 ms: 1.06x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 91.6 ms: 1.06x faster                                                 |
| gc_traversal               | 3.46 ms                                                | 3.29 ms: 1.05x faster                                                 |
| deepcopy_memo              | 40.3 us                                                | 39.7 us: 1.01x faster                                                 |
| pidigits                   | 184 ms                                                 | 184 ms: 1.00x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 521 ms: 1.01x slower                                                  |
| json                       | 5.02 ms                                                | 5.18 ms: 1.03x slower                                                 |
| sqlite_synth               | 2.20 us                                                | 2.30 us: 1.04x slower                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 5.01 sec: 1.06x slower                                                |
| spectral_norm              | 110 ms                                                 | 119 ms: 1.08x slower                                                  |
| json_loads                 | 26.5 us                                                | 28.7 us: 1.08x slower                                                 |
| regex_dna                  | 168 ms                                                 | 189 ms: 1.13x slower                                                  |
| deepcopy_reduce            | 3.08 us                                                | 3.51 us: 1.14x slower                                                 |
| xml_etree_generate         | 85.2 ms                                                | 97.5 ms: 1.14x slower                                                 |
| scimark_fft                | 342 ms                                                 | 395 ms: 1.16x slower                                                  |
| async_generators           | 384 ms                                                 | 451 ms: 1.17x slower                                                  |
| docutils                   | 2.64 sec                                               | 3.11 sec: 1.18x slower                                                |
| generators                 | 32.2 ms                                                | 38.4 ms: 1.19x slower                                                 |
| mdp                        | 2.42 sec                                               | 2.89 sec: 1.20x slower                                                |
| crypto_pyaes               | 76.6 ms                                                | 92.0 ms: 1.20x slower                                                 |
| pylint                     | 319 ms                                                 | 383 ms: 1.20x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 24.9 ms: 1.21x slower                                                 |
| nqueens                    | 80.1 ms                                                | 96.9 ms: 1.21x slower                                                 |
| dulwich_log                | 78.9 ms                                                | 96.5 ms: 1.22x slower                                                 |
| typing_runtime_protocols   | 163 us                                                 | 203 us: 1.25x slower                                                  |
| meteor_contest             | 104 ms                                                 | 130 ms: 1.26x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 63.2 ms: 1.26x slower                                                 |
| regex_compile              | 142 ms                                                 | 180 ms: 1.26x slower                                                  |
| tomli_loads                | 2.11 sec                                               | 2.66 sec: 1.26x slower                                                |
| sqlglot_normalize          | 107 ms                                                 | 136 ms: 1.28x slower                                                  |
| sqlglot_optimize           | 53.3 ms                                                | 69.0 ms: 1.30x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 965 ms: 1.30x slower                                                  |
| pycparser                  | 1.17 sec                                               | 1.52 sec: 1.30x slower                                                |
| pprint_pformat             | 1.52 sec                                               | 1.99 sec: 1.31x slower                                                |
| telco                      | 6.53 ms                                                | 8.63 ms: 1.32x slower                                                 |
| fannkuch                   | 372 ms                                                 | 494 ms: 1.33x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 78.3 ms: 1.33x slower                                                 |
| sqlalchemy_imperative      | 21.8 ms                                                | 29.1 ms: 1.34x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.97 ms: 1.36x slower                                                 |
| comprehensions             | 19.8 us                                                | 27.2 us: 1.37x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 14.3 ms: 1.38x slower                                                 |
| genshi_text                | 22.8 ms                                                | 31.6 ms: 1.39x slower                                                 |
| 2to3                       | 264 ms                                                 | 366 ms: 1.39x slower                                                  |
| coverage                   | 71.4 ms                                                | 101 ms: 1.41x slower                                                  |
| sqlalchemy_declarative     | 143 ms                                                 | 204 ms: 1.43x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 10.3 ms: 1.43x slower                                                 |
| sympy_integrate            | 20.5 ms                                                | 29.5 ms: 1.44x slower                                                 |
| thrift                     | 791 us                                                 | 1.16 ms: 1.46x slower                                                 |
| django_template            | 34.7 ms                                                | 50.7 ms: 1.46x slower                                                 |
| nbody                      | 89.3 ms                                                | 131 ms: 1.47x slower                                                  |
| unpickle_pure_python       | 221 us                                                 | 334 us: 1.51x slower                                                  |
| pyflate                    | 448 ms                                                 | 697 ms: 1.56x slower                                                  |
| html5lib                   | 63.6 ms                                                | 99.2 ms: 1.56x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 182 ms: 1.60x slower                                                  |
| hexiom                     | 6.17 ms                                                | 9.88 ms: 1.60x slower                                                 |
| mako                       | 11.0 ms                                                | 17.8 ms: 1.62x slower                                                 |
| sympy_str                  | 292 ms                                                 | 476 ms: 1.63x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 504 us: 1.64x slower                                                  |
| logging_simple             | 6.63 us                                                | 10.9 us: 1.64x slower                                                 |
| richards_super             | 51.9 ms                                                | 85.2 ms: 1.64x slower                                                 |
| chaos                      | 62.8 ms                                                | 104 ms: 1.65x slower                                                  |
| richards                   | 45.9 ms                                                | 76.0 ms: 1.65x slower                                                 |
| logging_format             | 7.35 us                                                | 12.2 us: 1.65x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.81 ms: 1.66x slower                                                 |
| logging_silent             | 109 ns                                                 | 186 ns: 1.71x slower                                                  |
| float                      | 80.8 ms                                                | 140 ms: 1.73x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 119 ms: 1.74x slower                                                  |
| python_startup             | 9.93 ms                                                | 17.5 ms: 1.76x slower                                                 |
| sqlglot_transpile          | 1.67 ms                                                | 3.00 ms: 1.79x slower                                                 |
| scimark_sor                | 130 ms                                                 | 235 ms: 1.81x slower                                                  |
| raytrace                   | 299 ms                                                 | 551 ms: 1.84x slower                                                  |
| go                         | 139 ms                                                 | 266 ms: 1.91x slower                                                  |
| sqlglot_parse              | 1.36 ms                                                | 2.60 ms: 1.92x slower                                                 |
| sympy_expand               | 468 ms                                                 | 953 ms: 2.04x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 350 ms: 2.11x slower                                                  |
| deltablue                  | 3.45 ms                                                | 7.94 ms: 2.31x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.35 ms: 3.56x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 109 ms: 10.08x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.34x slower                                                          |

Benchmark hidden because not significant (1): coroutines
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241205-3.14.0a2+-b22403e-NOGIL/bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.224x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.21x
- 95% likely to have a slowdown of 1.20x
- 99% likely to have a slowdown of 1.18x

# Memory
- memory change: 1.33x