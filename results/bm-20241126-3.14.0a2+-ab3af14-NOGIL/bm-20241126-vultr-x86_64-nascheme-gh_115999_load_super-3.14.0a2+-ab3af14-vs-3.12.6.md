# Results vs. 3.12.6

- fork: nascheme
- ref: gh_115999_load_super
- machine: linux-x86_64
- commit hash: ab3af14
- commit date: 2024-11-26
- overall geometric mean: 1.289x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.26x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241126-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-ab3af14 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 406 ms: 1.54x slower                                                     |
| docutils       | 2.64 sec                                               | 3.29 sec: 1.25x slower                                                   |
| html5lib       | 63.6 ms                                                | 105 ms: 1.66x slower                                                     |
| Geometric mean | (ref)                                                  | 1.47x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241126-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-ab3af14 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 893 ms: 1.24x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 918 ms: 1.18x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 480 ms: 1.17x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 385 ms: 1.16x faster                                                     |
| async_tree_none            | 464 ms                                                 | 420 ms: 1.11x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 657 ms: 1.10x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 509 ms: 1.09x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 684 ms: 1.05x faster                                                     |
| asyncio_websockets         | 517 ms                                                 | 521 ms: 1.01x slower                                                     |
| coroutines                 | 23.9 ms                                                | 29.2 ms: 1.22x slower                                                    |
| async_generators           | 384 ms                                                 | 482 ms: 1.25x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.05x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241126-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-ab3af14 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 183 ms: 1.01x faster                                                     |
| float          | 80.8 ms                                                | 148 ms: 1.83x slower                                                     |
| nbody          | 89.3 ms                                                | 197 ms: 2.21x slower                                                     |
| Geometric mean | (ref)                                                  | 1.59x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241126-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-ab3af14 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.86 ms: 1.11x faster                                                    |
| regex_dna      | 168 ms                                                 | 191 ms: 1.14x slower                                                     |
| regex_v8       | 20.6 ms                                                | 25.6 ms: 1.25x slower                                                    |
| regex_compile  | 142 ms                                                 | 209 ms: 1.47x slower                                                     |
| Geometric mean | (ref)                                                  | 1.17x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241126-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-ab3af14 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                     |
| xml_etree_iterparse  | 96.7 ms                                                | 102 ms: 1.06x slower                                                     |
| json_loads           | 26.5 us                                                | 28.3 us: 1.07x slower                                                    |
| xml_etree_generate   | 85.2 ms                                                | 106 ms: 1.25x slower                                                     |
| json_dumps           | 10.4 ms                                                | 14.6 ms: 1.41x slower                                                    |
| tomli_loads          | 2.11 sec                                               | 3.05 sec: 1.45x slower                                                   |
| xml_etree_process    | 59.0 ms                                                | 86.5 ms: 1.47x slower                                                    |
| unpickle_pure_python | 221 us                                                 | 383 us: 1.74x slower                                                     |
| pickle_pure_python   | 308 us                                                 | 575 us: 1.87x slower                                                     |
| Geometric mean       | (ref)                                                  | 1.33x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241126-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-ab3af14 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.3 ms: 1.43x slower                                                    |
| python_startup         | 9.93 ms                                                | 17.5 ms: 1.76x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.59x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241126-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-ab3af14 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 75.0 ms: 1.49x slower                                                    |
| genshi_text     | 22.8 ms                                                | 36.0 ms: 1.58x slower                                                    |
| django_template | 34.7 ms                                                | 58.6 ms: 1.69x slower                                                    |
| mako            | 11.0 ms                                                | 19.9 ms: 1.81x slower                                                    |
| Geometric mean  | (ref)                                                  | 1.64x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241126-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-ab3af14 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 893 ms: 1.24x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 918 ms: 1.18x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 480 ms: 1.17x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 385 ms: 1.16x faster                                                     |
| regex_effbot               | 3.17 ms                                                | 2.86 ms: 1.11x faster                                                    |
| async_tree_none            | 464 ms                                                 | 420 ms: 1.11x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 657 ms: 1.10x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 509 ms: 1.09x faster                                                     |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 684 ms: 1.05x faster                                                     |
| pathlib                    | 21.5 ms                                                | 21.2 ms: 1.01x faster                                                    |
| pidigits                   | 184 ms                                                 | 183 ms: 1.01x faster                                                     |
| asyncio_websockets         | 517 ms                                                 | 521 ms: 1.01x slower                                                     |
| gc_traversal               | 3.46 ms                                                | 3.49 ms: 1.01x slower                                                    |
| json                       | 5.02 ms                                                | 5.19 ms: 1.03x slower                                                    |
| xml_etree_iterparse        | 96.7 ms                                                | 102 ms: 1.06x slower                                                     |
| json_loads                 | 26.5 us                                                | 28.3 us: 1.07x slower                                                    |
| deepcopy                   | 352 us                                                 | 379 us: 1.08x slower                                                     |
| sqlite_synth               | 2.20 us                                                | 2.39 us: 1.09x slower                                                    |
| deepcopy_memo              | 40.3 us                                                | 45.8 us: 1.14x slower                                                    |
| regex_dna                  | 168 ms                                                 | 191 ms: 1.14x slower                                                     |
| scimark_fft                | 342 ms                                                 | 410 ms: 1.20x slower                                                     |
| bpe_tokeniser              | 4.74 sec                                               | 5.73 sec: 1.21x slower                                                   |
| coroutines                 | 23.9 ms                                                | 29.2 ms: 1.22x slower                                                    |
| regex_v8                   | 20.6 ms                                                | 25.6 ms: 1.25x slower                                                    |
| docutils                   | 2.64 sec                                               | 3.29 sec: 1.25x slower                                                   |
| xml_etree_generate         | 85.2 ms                                                | 106 ms: 1.25x slower                                                     |
| async_generators           | 384 ms                                                 | 482 ms: 1.25x slower                                                     |
| pylint                     | 319 ms                                                 | 407 ms: 1.28x slower                                                     |
| generators                 | 32.2 ms                                                | 41.2 ms: 1.28x slower                                                    |
| deepcopy_reduce            | 3.08 us                                                | 3.94 us: 1.28x slower                                                    |
| dulwich_log                | 78.9 ms                                                | 102 ms: 1.29x slower                                                     |
| mdp                        | 2.42 sec                                               | 3.19 sec: 1.32x slower                                                   |
| meteor_contest             | 104 ms                                                 | 137 ms: 1.32x slower                                                     |
| typing_runtime_protocols   | 163 us                                                 | 218 us: 1.34x slower                                                     |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 6.00 ms: 1.37x slower                                                    |
| spectral_norm              | 110 ms                                                 | 152 ms: 1.38x slower                                                     |
| crypto_pyaes               | 76.6 ms                                                | 107 ms: 1.39x slower                                                     |
| nqueens                    | 80.1 ms                                                | 112 ms: 1.40x slower                                                     |
| telco                      | 6.53 ms                                                | 9.11 ms: 1.40x slower                                                    |
| json_dumps                 | 10.4 ms                                                | 14.6 ms: 1.41x slower                                                    |
| pycparser                  | 1.17 sec                                               | 1.66 sec: 1.42x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 10.3 ms: 1.43x slower                                                    |
| coverage                   | 71.4 ms                                                | 103 ms: 1.45x slower                                                     |
| tomli_loads                | 2.11 sec                                               | 3.05 sec: 1.45x slower                                                   |
| xml_etree_process          | 59.0 ms                                                | 86.5 ms: 1.47x slower                                                    |
| regex_compile              | 142 ms                                                 | 209 ms: 1.47x slower                                                     |
| fannkuch                   | 372 ms                                                 | 555 ms: 1.49x slower                                                     |
| genshi_xml                 | 50.2 ms                                                | 75.0 ms: 1.49x slower                                                    |
| sqlglot_optimize           | 53.3 ms                                                | 80.5 ms: 1.51x slower                                                    |
| comprehensions             | 19.8 us                                                | 30.1 us: 1.52x slower                                                    |
| sqlglot_normalize          | 107 ms                                                 | 163 ms: 1.53x slower                                                     |
| 2to3                       | 264 ms                                                 | 406 ms: 1.54x slower                                                     |
| pprint_safe_repr           | 743 ms                                                 | 1.15 sec: 1.54x slower                                                   |
| thrift                     | 791 us                                                 | 1.23 ms: 1.55x slower                                                    |
| sympy_integrate            | 20.5 ms                                                | 32.0 ms: 1.56x slower                                                    |
| pprint_pformat             | 1.52 sec                                               | 2.38 sec: 1.56x slower                                                   |
| genshi_text                | 22.8 ms                                                | 36.0 ms: 1.58x slower                                                    |
| html5lib                   | 63.6 ms                                                | 105 ms: 1.66x slower                                                     |
| create_gc_cycles           | 1.09 ms                                                | 1.82 ms: 1.67x slower                                                    |
| django_template            | 34.7 ms                                                | 58.6 ms: 1.69x slower                                                    |
| pyflate                    | 448 ms                                                 | 770 ms: 1.72x slower                                                     |
| logging_simple             | 6.63 us                                                | 11.5 us: 1.73x slower                                                    |
| unpickle_pure_python       | 221 us                                                 | 383 us: 1.74x slower                                                     |
| python_startup             | 9.93 ms                                                | 17.5 ms: 1.76x slower                                                    |
| logging_format             | 7.35 us                                                | 13.0 us: 1.76x slower                                                    |
| sympy_str                  | 292 ms                                                 | 519 ms: 1.78x slower                                                     |
| mako                       | 11.0 ms                                                | 19.9 ms: 1.81x slower                                                    |
| scimark_monte_carlo        | 68.4 ms                                                | 125 ms: 1.82x slower                                                     |
| float                      | 80.8 ms                                                | 148 ms: 1.83x slower                                                     |
| richards_super             | 51.9 ms                                                | 94.8 ms: 1.83x slower                                                    |
| scimark_lu                 | 114 ms                                                 | 212 ms: 1.86x slower                                                     |
| pickle_pure_python         | 308 us                                                 | 575 us: 1.87x slower                                                     |
| richards                   | 45.9 ms                                                | 86.2 ms: 1.88x slower                                                    |
| chaos                      | 62.8 ms                                                | 119 ms: 1.89x slower                                                     |
| hexiom                     | 6.17 ms                                                | 11.7 ms: 1.89x slower                                                    |
| logging_silent             | 109 ns                                                 | 210 ns: 1.93x slower                                                     |
| sqlglot_transpile          | 1.67 ms                                                | 3.23 ms: 1.93x slower                                                    |
| sqlglot_parse              | 1.36 ms                                                | 2.80 ms: 2.06x slower                                                    |
| go                         | 139 ms                                                 | 291 ms: 2.09x slower                                                     |
| scimark_sor                | 130 ms                                                 | 271 ms: 2.09x slower                                                     |
| raytrace                   | 299 ms                                                 | 630 ms: 2.10x slower                                                     |
| sympy_expand               | 468 ms                                                 | 1.02 sec: 2.18x slower                                                   |
| nbody                      | 89.3 ms                                                | 197 ms: 2.21x slower                                                     |
| sympy_sum                  | 166 ms                                                 | 370 ms: 2.23x slower                                                     |
| deltablue                  | 3.45 ms                                                | 8.72 ms: 2.53x slower                                                    |
| bench_thread_pool          | 941 us                                                 | 3.47 ms: 3.69x slower                                                    |
| bench_mp_pool              | 10.8 ms                                                | 110 ms: 10.17x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.46x slower                                                             |
Ignored benchmarks (17) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241126-3.14.0a2+-ab3af14-NOGIL/bm-20241126-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-ab3af14.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.289x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.32x
- 95% likely to have a slowdown of 1.31x
- 99% likely to have a slowdown of 1.26x

# Memory
- memory change: 1.33x