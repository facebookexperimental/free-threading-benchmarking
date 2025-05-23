# Results vs. 3.12.6

- fork: corona10
- ref: gh_115999_binary_sub
- machine: linux-x86_64
- commit hash: 0637d48
- commit date: 2024-11-30
- overall geometric mean: 1.254x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.21x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241130-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-0637d48 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 377 ms: 1.43x slower                                                     |
| docutils       | 2.64 sec                                               | 3.20 sec: 1.21x slower                                                   |
| html5lib       | 63.6 ms                                                | 101 ms: 1.59x slower                                                     |
| Geometric mean | (ref)                                                  | 1.40x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241130-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-0637d48 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 865 ms: 1.28x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 886 ms: 1.22x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 368 ms: 1.21x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 463 ms: 1.21x faster                                                     |
| async_tree_none            | 464 ms                                                 | 399 ms: 1.16x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 628 ms: 1.15x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 490 ms: 1.13x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 658 ms: 1.09x faster                                                     |
| asyncio_websockets         | 517 ms                                                 | 519 ms: 1.00x slower                                                     |
| coroutines                 | 23.9 ms                                                | 28.1 ms: 1.18x slower                                                    |
| async_generators           | 384 ms                                                 | 471 ms: 1.22x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.09x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241130-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-0637d48 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 181 ms: 1.02x faster                                                     |
| nbody          | 89.3 ms                                                | 134 ms: 1.50x slower                                                     |
| float          | 80.8 ms                                                | 141 ms: 1.74x slower                                                     |
| Geometric mean | (ref)                                                  | 1.37x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241130-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-0637d48 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.87 ms: 1.10x faster                                                    |
| regex_dna      | 168 ms                                                 | 187 ms: 1.11x slower                                                     |
| regex_v8       | 20.6 ms                                                | 24.6 ms: 1.19x slower                                                    |
| regex_compile  | 142 ms                                                 | 193 ms: 1.36x slower                                                     |
| Geometric mean | (ref)                                                  | 1.13x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241130-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-0637d48 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 133 ms: 1.04x faster                                                     |
| xml_etree_iterparse  | 96.7 ms                                                | 94.7 ms: 1.02x faster                                                    |
| json_loads           | 26.5 us                                                | 28.3 us: 1.07x slower                                                    |
| xml_etree_generate   | 85.2 ms                                                | 102 ms: 1.20x slower                                                     |
| tomli_loads          | 2.11 sec                                               | 2.72 sec: 1.29x slower                                                   |
| json_dumps           | 10.4 ms                                                | 14.3 ms: 1.39x slower                                                    |
| xml_etree_process    | 59.0 ms                                                | 82.2 ms: 1.39x slower                                                    |
| unpickle_pure_python | 221 us                                                 | 372 us: 1.69x slower                                                     |
| pickle_pure_python   | 308 us                                                 | 547 us: 1.78x slower                                                     |
| Geometric mean       | (ref)                                                  | 1.28x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241130-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-0637d48 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.3 ms: 1.44x slower                                                    |
| python_startup         | 9.93 ms                                                | 17.5 ms: 1.77x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.60x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241130-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-0637d48 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 66.9 ms: 1.33x slower                                                    |
| genshi_text     | 22.8 ms                                                | 33.9 ms: 1.49x slower                                                    |
| django_template | 34.7 ms                                                | 55.7 ms: 1.61x slower                                                    |
| mako            | 11.0 ms                                                | 19.8 ms: 1.80x slower                                                    |
| Geometric mean  | (ref)                                                  | 1.55x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241130-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-0637d48 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 865 ms: 1.28x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 886 ms: 1.22x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 368 ms: 1.21x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 463 ms: 1.21x faster                                                     |
| async_tree_none            | 464 ms                                                 | 399 ms: 1.16x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 628 ms: 1.15x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 490 ms: 1.13x faster                                                     |
| regex_effbot               | 3.17 ms                                                | 2.87 ms: 1.10x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 658 ms: 1.09x faster                                                     |
| xml_etree_parse            | 139 ms                                                 | 133 ms: 1.04x faster                                                     |
| pathlib                    | 21.5 ms                                                | 20.9 ms: 1.03x faster                                                    |
| xml_etree_iterparse        | 96.7 ms                                                | 94.7 ms: 1.02x faster                                                    |
| pidigits                   | 184 ms                                                 | 181 ms: 1.02x faster                                                     |
| deepcopy                   | 352 us                                                 | 350 us: 1.00x faster                                                     |
| asyncio_websockets         | 517 ms                                                 | 519 ms: 1.00x slower                                                     |
| gc_traversal               | 3.46 ms                                                | 3.53 ms: 1.02x slower                                                    |
| sqlite_synth               | 2.20 us                                                | 2.32 us: 1.05x slower                                                    |
| json_loads                 | 26.5 us                                                | 28.3 us: 1.07x slower                                                    |
| regex_dna                  | 168 ms                                                 | 187 ms: 1.11x slower                                                     |
| deepcopy_memo              | 40.3 us                                                | 45.1 us: 1.12x slower                                                    |
| bpe_tokeniser              | 4.74 sec                                               | 5.45 sec: 1.15x slower                                                   |
| coroutines                 | 23.9 ms                                                | 28.1 ms: 1.18x slower                                                    |
| scimark_fft                | 342 ms                                                 | 404 ms: 1.18x slower                                                     |
| generators                 | 32.2 ms                                                | 38.4 ms: 1.19x slower                                                    |
| regex_v8                   | 20.6 ms                                                | 24.6 ms: 1.19x slower                                                    |
| xml_etree_generate         | 85.2 ms                                                | 102 ms: 1.20x slower                                                     |
| spectral_norm              | 110 ms                                                 | 132 ms: 1.20x slower                                                     |
| mdp                        | 2.42 sec                                               | 2.90 sec: 1.20x slower                                                   |
| deepcopy_reduce            | 3.08 us                                                | 3.73 us: 1.21x slower                                                    |
| docutils                   | 2.64 sec                                               | 3.20 sec: 1.21x slower                                                   |
| async_generators           | 384 ms                                                 | 471 ms: 1.22x slower                                                     |
| pylint                     | 319 ms                                                 | 394 ms: 1.24x slower                                                     |
| crypto_pyaes               | 76.6 ms                                                | 95.2 ms: 1.24x slower                                                    |
| dulwich_log                | 78.9 ms                                                | 98.9 ms: 1.25x slower                                                    |
| nqueens                    | 80.1 ms                                                | 101 ms: 1.27x slower                                                     |
| tomli_loads                | 2.11 sec                                               | 2.72 sec: 1.29x slower                                                   |
| meteor_contest             | 104 ms                                                 | 134 ms: 1.29x slower                                                     |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.69 ms: 1.29x slower                                                    |
| typing_runtime_protocols   | 163 us                                                 | 215 us: 1.32x slower                                                     |
| genshi_xml                 | 50.2 ms                                                | 66.9 ms: 1.33x slower                                                    |
| telco                      | 6.53 ms                                                | 8.84 ms: 1.35x slower                                                    |
| regex_compile              | 142 ms                                                 | 193 ms: 1.36x slower                                                     |
| fannkuch                   | 372 ms                                                 | 505 ms: 1.36x slower                                                     |
| pycparser                  | 1.17 sec                                               | 1.59 sec: 1.36x slower                                                   |
| json_dumps                 | 10.4 ms                                                | 14.3 ms: 1.39x slower                                                    |
| xml_etree_process          | 59.0 ms                                                | 82.2 ms: 1.39x slower                                                    |
| sqlglot_normalize          | 107 ms                                                 | 150 ms: 1.41x slower                                                     |
| sqlglot_optimize           | 53.3 ms                                                | 74.9 ms: 1.41x slower                                                    |
| coverage                   | 71.4 ms                                                | 102 ms: 1.43x slower                                                     |
| 2to3                       | 264 ms                                                 | 377 ms: 1.43x slower                                                     |
| python_startup_no_site     | 7.16 ms                                                | 10.3 ms: 1.44x slower                                                    |
| pprint_safe_repr           | 743 ms                                                 | 1.07 sec: 1.44x slower                                                   |
| pprint_pformat             | 1.52 sec                                               | 2.22 sec: 1.46x slower                                                   |
| comprehensions             | 19.8 us                                                | 29.0 us: 1.46x slower                                                    |
| genshi_text                | 22.8 ms                                                | 33.9 ms: 1.49x slower                                                    |
| sympy_integrate            | 20.5 ms                                                | 30.7 ms: 1.49x slower                                                    |
| nbody                      | 89.3 ms                                                | 134 ms: 1.50x slower                                                     |
| thrift                     | 791 us                                                 | 1.20 ms: 1.51x slower                                                    |
| html5lib                   | 63.6 ms                                                | 101 ms: 1.59x slower                                                     |
| pyflate                    | 448 ms                                                 | 713 ms: 1.59x slower                                                     |
| django_template            | 34.7 ms                                                | 55.7 ms: 1.61x slower                                                    |
| unpickle_pure_python       | 221 us                                                 | 372 us: 1.69x slower                                                     |
| sympy_str                  | 292 ms                                                 | 494 ms: 1.70x slower                                                     |
| scimark_lu                 | 114 ms                                                 | 194 ms: 1.70x slower                                                     |
| create_gc_cycles           | 1.09 ms                                                | 1.87 ms: 1.71x slower                                                    |
| logging_format             | 7.35 us                                                | 12.6 us: 1.71x slower                                                    |
| logging_simple             | 6.63 us                                                | 11.4 us: 1.71x slower                                                    |
| chaos                      | 62.8 ms                                                | 109 ms: 1.74x slower                                                     |
| float                      | 80.8 ms                                                | 141 ms: 1.74x slower                                                     |
| scimark_monte_carlo        | 68.4 ms                                                | 120 ms: 1.75x slower                                                     |
| hexiom                     | 6.17 ms                                                | 10.8 ms: 1.76x slower                                                    |
| python_startup             | 9.93 ms                                                | 17.5 ms: 1.77x slower                                                    |
| logging_silent             | 109 ns                                                 | 193 ns: 1.77x slower                                                     |
| pickle_pure_python         | 308 us                                                 | 547 us: 1.78x slower                                                     |
| mako                       | 11.0 ms                                                | 19.8 ms: 1.80x slower                                                    |
| richards                   | 45.9 ms                                                | 83.2 ms: 1.81x slower                                                    |
| sqlglot_transpile          | 1.67 ms                                                | 3.03 ms: 1.81x slower                                                    |
| scimark_sor                | 130 ms                                                 | 241 ms: 1.86x slower                                                     |
| richards_super             | 51.9 ms                                                | 98.4 ms: 1.90x slower                                                    |
| sqlglot_parse              | 1.36 ms                                                | 2.62 ms: 1.94x slower                                                    |
| go                         | 139 ms                                                 | 276 ms: 1.98x slower                                                     |
| raytrace                   | 299 ms                                                 | 601 ms: 2.01x slower                                                     |
| sympy_expand               | 468 ms                                                 | 985 ms: 2.11x slower                                                     |
| sympy_sum                  | 166 ms                                                 | 358 ms: 2.16x slower                                                     |
| deltablue                  | 3.45 ms                                                | 8.66 ms: 2.51x slower                                                    |
| bench_thread_pool          | 941 us                                                 | 3.40 ms: 3.61x slower                                                    |
| bench_mp_pool              | 10.8 ms                                                | 110 ms: 10.19x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.39x slower                                                             |

Benchmark hidden because not significant (1): json
Ignored benchmarks (17) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241130-3.14.0a2+-0637d48-NOGIL/bm-20241130-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-0637d48.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.254x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.25x
- 95% likely to have a slowdown of 1.23x
- 99% likely to have a slowdown of 1.21x

# Memory
- memory change: 1.33x