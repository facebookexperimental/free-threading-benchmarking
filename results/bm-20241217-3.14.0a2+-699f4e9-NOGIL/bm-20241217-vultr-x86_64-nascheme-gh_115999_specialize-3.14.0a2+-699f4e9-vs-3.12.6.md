# Results vs. 3.12.6

- fork: nascheme
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: 699f4e9
- commit date: 2024-12-17
- overall geometric mean: 1.206x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.17x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 371 ms: 1.41x slower                                                     |
| docutils       | 2.64 sec                                               | 3.12 sec: 1.18x slower                                                   |
| html5lib       | 63.6 ms                                                | 98.4 ms: 1.55x slower                                                    |
| Geometric mean | (ref)                                                  | 1.37x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 759 ms: 1.46x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 789 ms: 1.37x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 417 ms: 1.34x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 334 ms: 1.34x faster                                                     |
| async_tree_none            | 464 ms                                                 | 368 ms: 1.26x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 446 ms: 1.25x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 587 ms: 1.23x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 613 ms: 1.17x faster                                                     |
| asyncio_websockets         | 517 ms                                                 | 521 ms: 1.01x slower                                                     |
| coroutines                 | 23.9 ms                                                | 25.3 ms: 1.06x slower                                                    |
| async_generators           | 384 ms                                                 | 450 ms: 1.17x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.19x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 184 ms: 1.00x faster                                                     |
| float          | 80.8 ms                                                | 112 ms: 1.39x slower                                                     |
| nbody          | 89.3 ms                                                | 130 ms: 1.46x slower                                                     |
| Geometric mean | (ref)                                                  | 1.26x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.92 ms: 1.08x faster                                                    |
| regex_dna      | 168 ms                                                 | 183 ms: 1.09x slower                                                     |
| regex_v8       | 20.6 ms                                                | 24.4 ms: 1.19x slower                                                    |
| regex_compile  | 142 ms                                                 | 174 ms: 1.22x slower                                                     |
| Geometric mean | (ref)                                                  | 1.10x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 90.5 ms: 1.07x faster                                                    |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.06x faster                                                     |
| json_loads           | 26.5 us                                                | 28.6 us: 1.08x slower                                                    |
| xml_etree_generate   | 85.2 ms                                                | 98.4 ms: 1.15x slower                                                    |
| tomli_loads          | 2.11 sec                                               | 2.56 sec: 1.21x slower                                                   |
| xml_etree_process    | 59.0 ms                                                | 74.3 ms: 1.26x slower                                                    |
| json_dumps           | 10.4 ms                                                | 14.4 ms: 1.39x slower                                                    |
| unpickle_pure_python | 221 us                                                 | 346 us: 1.57x slower                                                     |
| pickle_pure_python   | 308 us                                                 | 535 us: 1.74x slower                                                     |
| Geometric mean       | (ref)                                                  | 1.23x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.2 ms: 1.42x slower                                                    |
| python_startup         | 9.93 ms                                                | 17.1 ms: 1.73x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.57x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 64.0 ms: 1.28x slower                                                    |
| genshi_text     | 22.8 ms                                                | 30.7 ms: 1.34x slower                                                    |
| django_template | 34.7 ms                                                | 51.6 ms: 1.49x slower                                                    |
| mako            | 11.0 ms                                                | 17.1 ms: 1.55x slower                                                    |
| Geometric mean  | (ref)                                                  | 1.41x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 759 ms: 1.46x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 789 ms: 1.37x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 417 ms: 1.34x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 334 ms: 1.34x faster                                                     |
| async_tree_none            | 464 ms                                                 | 368 ms: 1.26x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 446 ms: 1.25x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 587 ms: 1.23x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 613 ms: 1.17x faster                                                     |
| pathlib                    | 21.5 ms                                                | 19.4 ms: 1.11x faster                                                    |
| deepcopy                   | 352 us                                                 | 321 us: 1.10x faster                                                     |
| regex_effbot               | 3.17 ms                                                | 2.92 ms: 1.08x faster                                                    |
| xml_etree_iterparse        | 96.7 ms                                                | 90.5 ms: 1.07x faster                                                    |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.06x faster                                                     |
| gc_traversal               | 3.46 ms                                                | 3.27 ms: 1.06x faster                                                    |
| sqlite_synth               | 2.20 us                                                | 2.14 us: 1.03x faster                                                    |
| spectral_norm              | 110 ms                                                 | 109 ms: 1.01x faster                                                     |
| pidigits                   | 184 ms                                                 | 184 ms: 1.00x faster                                                     |
| asyncio_websockets         | 517 ms                                                 | 521 ms: 1.01x slower                                                     |
| json                       | 5.02 ms                                                | 5.10 ms: 1.01x slower                                                    |
| bpe_tokeniser              | 4.74 sec                                               | 4.98 sec: 1.05x slower                                                   |
| coroutines                 | 23.9 ms                                                | 25.3 ms: 1.06x slower                                                    |
| json_loads                 | 26.5 us                                                | 28.6 us: 1.08x slower                                                    |
| regex_dna                  | 168 ms                                                 | 183 ms: 1.09x slower                                                     |
| scimark_fft                | 342 ms                                                 | 376 ms: 1.10x slower                                                     |
| deepcopy_reduce            | 3.08 us                                                | 3.45 us: 1.12x slower                                                    |
| xml_etree_generate         | 85.2 ms                                                | 98.4 ms: 1.15x slower                                                    |
| pylint                     | 319 ms                                                 | 369 ms: 1.16x slower                                                     |
| dulwich_log                | 78.9 ms                                                | 91.5 ms: 1.16x slower                                                    |
| async_generators           | 384 ms                                                 | 450 ms: 1.17x slower                                                     |
| docutils                   | 2.64 sec                                               | 3.12 sec: 1.18x slower                                                   |
| crypto_pyaes               | 76.6 ms                                                | 90.6 ms: 1.18x slower                                                    |
| mdp                        | 2.42 sec                                               | 2.87 sec: 1.19x slower                                                   |
| regex_v8                   | 20.6 ms                                                | 24.4 ms: 1.19x slower                                                    |
| tomli_loads                | 2.11 sec                                               | 2.56 sec: 1.21x slower                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.35 ms: 1.22x slower                                                    |
| regex_compile              | 142 ms                                                 | 174 ms: 1.22x slower                                                     |
| nqueens                    | 80.1 ms                                                | 97.9 ms: 1.22x slower                                                    |
| pycparser                  | 1.17 sec                                               | 1.44 sec: 1.23x slower                                                   |
| sqlglot_optimize           | 53.3 ms                                                | 66.1 ms: 1.24x slower                                                    |
| generators                 | 32.2 ms                                                | 40.1 ms: 1.24x slower                                                    |
| typing_runtime_protocols   | 163 us                                                 | 204 us: 1.25x slower                                                     |
| sqlglot_normalize          | 107 ms                                                 | 134 ms: 1.25x slower                                                     |
| meteor_contest             | 104 ms                                                 | 130 ms: 1.26x slower                                                     |
| xml_etree_process          | 59.0 ms                                                | 74.3 ms: 1.26x slower                                                    |
| thrift                     | 791 us                                                 | 1.00 ms: 1.27x slower                                                    |
| genshi_xml                 | 50.2 ms                                                | 64.0 ms: 1.28x slower                                                    |
| sqlalchemy_imperative      | 21.8 ms                                                | 28.2 ms: 1.29x slower                                                    |
| fannkuch                   | 372 ms                                                 | 487 ms: 1.31x slower                                                     |
| pprint_safe_repr           | 743 ms                                                 | 987 ms: 1.33x slower                                                     |
| pprint_pformat             | 1.52 sec                                               | 2.04 sec: 1.34x slower                                                   |
| genshi_text                | 22.8 ms                                                | 30.7 ms: 1.34x slower                                                    |
| telco                      | 6.53 ms                                                | 8.79 ms: 1.35x slower                                                    |
| json_dumps                 | 10.4 ms                                                | 14.4 ms: 1.39x slower                                                    |
| sqlalchemy_declarative     | 143 ms                                                 | 198 ms: 1.39x slower                                                     |
| float                      | 80.8 ms                                                | 112 ms: 1.39x slower                                                     |
| logging_format             | 7.35 us                                                | 10.3 us: 1.40x slower                                                    |
| logging_simple             | 6.63 us                                                | 9.28 us: 1.40x slower                                                    |
| coverage                   | 71.4 ms                                                | 100 ms: 1.41x slower                                                     |
| 2to3                       | 264 ms                                                 | 371 ms: 1.41x slower                                                     |
| python_startup_no_site     | 7.16 ms                                                | 10.2 ms: 1.42x slower                                                    |
| sympy_integrate            | 20.5 ms                                                | 29.7 ms: 1.44x slower                                                    |
| comprehensions             | 19.8 us                                                | 28.7 us: 1.45x slower                                                    |
| nbody                      | 89.3 ms                                                | 130 ms: 1.46x slower                                                     |
| django_template            | 34.7 ms                                                | 51.6 ms: 1.49x slower                                                    |
| pyflate                    | 448 ms                                                 | 681 ms: 1.52x slower                                                     |
| html5lib                   | 63.6 ms                                                | 98.4 ms: 1.55x slower                                                    |
| mako                       | 11.0 ms                                                | 17.1 ms: 1.55x slower                                                    |
| unpickle_pure_python       | 221 us                                                 | 346 us: 1.57x slower                                                     |
| richards_super             | 51.9 ms                                                | 83.0 ms: 1.60x slower                                                    |
| chaos                      | 62.8 ms                                                | 101 ms: 1.60x slower                                                     |
| sympy_str                  | 292 ms                                                 | 476 ms: 1.63x slower                                                     |
| sqlglot_transpile          | 1.67 ms                                                | 2.73 ms: 1.64x slower                                                    |
| richards                   | 45.9 ms                                                | 75.2 ms: 1.64x slower                                                    |
| create_gc_cycles           | 1.09 ms                                                | 1.79 ms: 1.64x slower                                                    |
| scimark_monte_carlo        | 68.4 ms                                                | 113 ms: 1.65x slower                                                     |
| scimark_lu                 | 114 ms                                                 | 189 ms: 1.66x slower                                                     |
| hexiom                     | 6.17 ms                                                | 10.2 ms: 1.66x slower                                                    |
| python_startup             | 9.93 ms                                                | 17.1 ms: 1.73x slower                                                    |
| pickle_pure_python         | 308 us                                                 | 535 us: 1.74x slower                                                     |
| sqlglot_parse              | 1.36 ms                                                | 2.37 ms: 1.75x slower                                                    |
| raytrace                   | 299 ms                                                 | 534 ms: 1.79x slower                                                     |
| logging_silent             | 109 ns                                                 | 201 ns: 1.85x slower                                                     |
| scimark_sor                | 130 ms                                                 | 245 ms: 1.89x slower                                                     |
| go                         | 139 ms                                                 | 267 ms: 1.92x slower                                                     |
| sympy_expand               | 468 ms                                                 | 954 ms: 2.04x slower                                                     |
| sympy_sum                  | 166 ms                                                 | 349 ms: 2.10x slower                                                     |
| deltablue                  | 3.45 ms                                                | 8.28 ms: 2.40x slower                                                    |
| bench_thread_pool          | 941 us                                                 | 3.40 ms: 3.61x slower                                                    |
| bench_mp_pool              | 10.8 ms                                                | 107 ms: 9.93x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.31x slower                                                             |

Benchmark hidden because not significant (1): deepcopy_memo
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241217-3.14.0a2+-699f4e9-NOGIL/bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.206x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.19x
- 95% likely to have a slowdown of 1.18x
- 99% likely to have a slowdown of 1.17x

# Memory
- memory change: 1.33x