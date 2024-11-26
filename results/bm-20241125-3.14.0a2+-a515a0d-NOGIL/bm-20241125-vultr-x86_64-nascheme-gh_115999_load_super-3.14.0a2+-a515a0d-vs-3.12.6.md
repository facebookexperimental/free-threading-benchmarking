# Results vs. 3.12.6

- fork: nascheme
- ref: gh_115999_load_super
- machine: linux-x86_64
- commit hash: a515a0d
- commit date: 2024-11-25
- overall geometric mean: 1.411x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.43x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 455 ms: 1.73x slower                                                     |
| docutils       | 2.64 sec                                               | 3.33 sec: 1.26x slower                                                   |
| html5lib       | 63.6 ms                                                | 105 ms: 1.65x slower                                                     |
| Geometric mean | (ref)                                                  | 1.53x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_none_tg         | 446 ms                                                 | 384 ms: 1.16x faster                                                     |
| asyncio_websockets         | 517 ms                                                 | 523 ms: 1.01x slower                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 815 ms: 1.13x slower                                                     |
| coroutines                 | 23.9 ms                                                | 29.7 ms: 1.24x slower                                                    |
| async_generators           | 384 ms                                                 | 480 ms: 1.25x slower                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 725 ms: 1.30x slower                                                     |
| async_tree_none            | 464 ms                                                 | 664 ms: 1.43x slower                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 1.08 sec: 1.51x slower                                                   |
| async_tree_memoization     | 555 ms                                                 | 998 ms: 1.80x slower                                                     |
| async_tree_io_tg           | 1.11 sec                                               | 3.36 sec: 3.02x slower                                                   |
| async_tree_io              | 1.08 sec                                               | 3.62 sec: 3.35x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.49x slower                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 199 ms: 1.08x slower                                                     |
| float          | 80.8 ms                                                | 148 ms: 1.84x slower                                                     |
| nbody          | 89.3 ms                                                | 201 ms: 2.25x slower                                                     |
| Geometric mean | (ref)                                                  | 1.65x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.85 ms: 1.11x faster                                                    |
| regex_dna      | 168 ms                                                 | 188 ms: 1.12x slower                                                     |
| regex_v8       | 20.6 ms                                                | 25.1 ms: 1.22x slower                                                    |
| regex_compile  | 142 ms                                                 | 209 ms: 1.47x slower                                                     |
| Geometric mean | (ref)                                                  | 1.16x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 132 ms: 1.05x faster                                                     |
| xml_etree_iterparse  | 96.7 ms                                                | 102 ms: 1.05x slower                                                     |
| json_loads           | 26.5 us                                                | 28.6 us: 1.08x slower                                                    |
| xml_etree_generate   | 85.2 ms                                                | 107 ms: 1.25x slower                                                     |
| json_dumps           | 10.4 ms                                                | 14.8 ms: 1.43x slower                                                    |
| tomli_loads          | 2.11 sec                                               | 3.06 sec: 1.45x slower                                                   |
| xml_etree_process    | 59.0 ms                                                | 86.2 ms: 1.46x slower                                                    |
| unpickle_pure_python | 221 us                                                 | 381 us: 1.73x slower                                                     |
| pickle_pure_python   | 308 us                                                 | 576 us: 1.87x slower                                                     |
| Geometric mean       | (ref)                                                  | 1.33x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 11.3 ms: 1.58x slower                                                    |
| python_startup         | 9.93 ms                                                | 20.3 ms: 2.04x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.80x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 74.5 ms: 1.48x slower                                                    |
| genshi_text     | 22.8 ms                                                | 36.2 ms: 1.59x slower                                                    |
| django_template | 34.7 ms                                                | 61.8 ms: 1.78x slower                                                    |
| mako            | 11.0 ms                                                | 20.1 ms: 1.82x slower                                                    |
| Geometric mean  | (ref)                                                  | 1.66x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_none_tg         | 446 ms                                                 | 384 ms: 1.16x faster                                                     |
| regex_effbot               | 3.17 ms                                                | 2.85 ms: 1.11x faster                                                    |
| xml_etree_parse            | 139 ms                                                 | 132 ms: 1.05x faster                                                     |
| pathlib                    | 21.5 ms                                                | 21.1 ms: 1.02x faster                                                    |
| gc_traversal               | 3.46 ms                                                | 3.48 ms: 1.01x slower                                                    |
| asyncio_websockets         | 517 ms                                                 | 523 ms: 1.01x slower                                                     |
| json                       | 5.02 ms                                                | 5.22 ms: 1.04x slower                                                    |
| xml_etree_iterparse        | 96.7 ms                                                | 102 ms: 1.05x slower                                                     |
| json_loads                 | 26.5 us                                                | 28.6 us: 1.08x slower                                                    |
| pidigits                   | 184 ms                                                 | 199 ms: 1.08x slower                                                     |
| deepcopy                   | 352 us                                                 | 383 us: 1.09x slower                                                     |
| sqlite_synth               | 2.20 us                                                | 2.41 us: 1.09x slower                                                    |
| regex_dna                  | 168 ms                                                 | 188 ms: 1.12x slower                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 815 ms: 1.13x slower                                                     |
| deepcopy_memo              | 40.3 us                                                | 46.4 us: 1.15x slower                                                    |
| bpe_tokeniser              | 4.74 sec                                               | 5.74 sec: 1.21x slower                                                   |
| regex_v8                   | 20.6 ms                                                | 25.1 ms: 1.22x slower                                                    |
| coroutines                 | 23.9 ms                                                | 29.7 ms: 1.24x slower                                                    |
| async_generators           | 384 ms                                                 | 480 ms: 1.25x slower                                                     |
| scimark_fft                | 342 ms                                                 | 427 ms: 1.25x slower                                                     |
| xml_etree_generate         | 85.2 ms                                                | 107 ms: 1.25x slower                                                     |
| docutils                   | 2.64 sec                                               | 3.33 sec: 1.26x slower                                                   |
| generators                 | 32.2 ms                                                | 41.0 ms: 1.27x slower                                                    |
| deepcopy_reduce            | 3.08 us                                                | 3.98 us: 1.29x slower                                                    |
| async_tree_memoization_tg  | 560 ms                                                 | 725 ms: 1.30x slower                                                     |
| meteor_contest             | 104 ms                                                 | 139 ms: 1.34x slower                                                     |
| typing_runtime_protocols   | 163 us                                                 | 222 us: 1.36x slower                                                     |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 6.02 ms: 1.37x slower                                                    |
| nqueens                    | 80.1 ms                                                | 112 ms: 1.40x slower                                                     |
| crypto_pyaes               | 76.6 ms                                                | 108 ms: 1.41x slower                                                     |
| telco                      | 6.53 ms                                                | 9.20 ms: 1.41x slower                                                    |
| pycparser                  | 1.17 sec                                               | 1.66 sec: 1.42x slower                                                   |
| spectral_norm              | 110 ms                                                 | 157 ms: 1.42x slower                                                     |
| json_dumps                 | 10.4 ms                                                | 14.8 ms: 1.43x slower                                                    |
| async_tree_none            | 464 ms                                                 | 664 ms: 1.43x slower                                                     |
| coverage                   | 71.4 ms                                                | 102 ms: 1.43x slower                                                     |
| tomli_loads                | 2.11 sec                                               | 3.06 sec: 1.45x slower                                                   |
| xml_etree_process          | 59.0 ms                                                | 86.2 ms: 1.46x slower                                                    |
| regex_compile              | 142 ms                                                 | 209 ms: 1.47x slower                                                     |
| genshi_xml                 | 50.2 ms                                                | 74.5 ms: 1.48x slower                                                    |
| comprehensions             | 19.8 us                                                | 29.7 us: 1.50x slower                                                    |
| sqlglot_optimize           | 53.3 ms                                                | 80.2 ms: 1.51x slower                                                    |
| fannkuch                   | 372 ms                                                 | 561 ms: 1.51x slower                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 1.08 sec: 1.51x slower                                                   |
| sqlglot_normalize          | 107 ms                                                 | 162 ms: 1.52x slower                                                     |
| pprint_safe_repr           | 743 ms                                                 | 1.16 sec: 1.57x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 11.3 ms: 1.58x slower                                                    |
| genshi_text                | 22.8 ms                                                | 36.2 ms: 1.59x slower                                                    |
| pprint_pformat             | 1.52 sec                                               | 2.43 sec: 1.60x slower                                                   |
| html5lib                   | 63.6 ms                                                | 105 ms: 1.65x slower                                                     |
| create_gc_cycles           | 1.09 ms                                                | 1.81 ms: 1.66x slower                                                    |
| pyflate                    | 448 ms                                                 | 763 ms: 1.70x slower                                                     |
| unpickle_pure_python       | 221 us                                                 | 381 us: 1.73x slower                                                     |
| 2to3                       | 264 ms                                                 | 455 ms: 1.73x slower                                                     |
| logging_format             | 7.35 us                                                | 12.8 us: 1.74x slower                                                    |
| logging_simple             | 6.63 us                                                | 11.6 us: 1.76x slower                                                    |
| django_template            | 34.7 ms                                                | 61.8 ms: 1.78x slower                                                    |
| async_tree_memoization     | 555 ms                                                 | 998 ms: 1.80x slower                                                     |
| scimark_monte_carlo        | 68.4 ms                                                | 123 ms: 1.80x slower                                                     |
| mako                       | 11.0 ms                                                | 20.1 ms: 1.82x slower                                                    |
| float                      | 80.8 ms                                                | 148 ms: 1.84x slower                                                     |
| dulwich_log                | 78.9 ms                                                | 145 ms: 1.84x slower                                                     |
| scimark_lu                 | 114 ms                                                 | 213 ms: 1.87x slower                                                     |
| pickle_pure_python         | 308 us                                                 | 576 us: 1.87x slower                                                     |
| richards                   | 45.9 ms                                                | 86.1 ms: 1.87x slower                                                    |
| chaos                      | 62.8 ms                                                | 119 ms: 1.89x slower                                                     |
| hexiom                     | 6.17 ms                                                | 11.7 ms: 1.89x slower                                                    |
| sqlglot_transpile          | 1.67 ms                                                | 3.21 ms: 1.92x slower                                                    |
| logging_silent             | 109 ns                                                 | 209 ns: 1.92x slower                                                     |
| pylint                     | 319 ms                                                 | 642 ms: 2.01x slower                                                     |
| python_startup             | 9.93 ms                                                | 20.3 ms: 2.04x slower                                                    |
| sqlglot_parse              | 1.36 ms                                                | 2.78 ms: 2.05x slower                                                    |
| sympy_integrate            | 20.5 ms                                                | 42.2 ms: 2.06x slower                                                    |
| raytrace                   | 299 ms                                                 | 619 ms: 2.07x slower                                                     |
| go                         | 139 ms                                                 | 288 ms: 2.07x slower                                                     |
| scimark_sor                | 130 ms                                                 | 273 ms: 2.10x slower                                                     |
| nbody                      | 89.3 ms                                                | 201 ms: 2.25x slower                                                     |
| sympy_expand               | 468 ms                                                 | 1.25 sec: 2.68x slower                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 3.36 sec: 3.02x slower                                                   |
| sympy_sum                  | 166 ms                                                 | 535 ms: 3.22x slower                                                     |
| async_tree_io              | 1.08 sec                                               | 3.62 sec: 3.35x slower                                                   |
| sympy_str                  | 292 ms                                                 | 1.01 sec: 3.47x slower                                                   |
| bench_thread_pool          | 941 us                                                 | 4.32 ms: 4.59x slower                                                    |
| mdp                        | 2.42 sec                                               | 16.3 sec: 6.72x slower                                                   |
| thrift                     | 791 us                                                 | 6.57 ms: 8.31x slower                                                    |
| deltablue                  | 3.45 ms                                                | 43.9 ms: 12.75x slower                                                   |
| bench_mp_pool              | 10.8 ms                                                | 202 ms: 18.68x slower                                                    |
| richards_super             | 51.9 ms                                                | 1.82 sec: 35.01x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.76x slower                                                             |
Ignored benchmarks (17) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241125-3.14.0a2+-a515a0d-NOGIL/bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.411x slower
# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.47x
- 95% likely to have a slowdown of 1.45x
- 99% likely to have a slowdown of 1.43x

# Memory
- memory change: 1.33x