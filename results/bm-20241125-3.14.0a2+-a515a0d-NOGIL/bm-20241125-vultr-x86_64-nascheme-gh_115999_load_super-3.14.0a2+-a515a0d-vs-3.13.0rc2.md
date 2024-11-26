# Results vs. 3.13.0rc2

- fork: nascheme
- ref: gh_115999_load_super
- machine: linux-x86_64
- commit hash: a515a0d
- commit date: 2024-11-25
- overall geometric mean: 1.431x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.48x slower
- Memory change: 1.31x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 455 ms: 1.75x slower                                                     |
| docutils       | 2.62 sec                                                     | 3.33 sec: 1.27x slower                                                   |
| html5lib       | 67.0 ms                                                      | 105 ms: 1.57x slower                                                     |
| Geometric mean | (ref)                                                        | 1.52x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.00x slower                                                     |
| async_tree_none_tg         | 336 ms                                                       | 384 ms: 1.14x slower                                                     |
| coroutines                 | 23.6 ms                                                      | 29.7 ms: 1.26x slower                                                    |
| async_generators           | 377 ms                                                       | 480 ms: 1.27x slower                                                     |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 815 ms: 1.28x slower                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 1.08 sec: 1.63x slower                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 725 ms: 1.75x slower                                                     |
| async_tree_none            | 354 ms                                                       | 664 ms: 1.88x slower                                                     |
| async_tree_memoization     | 461 ms                                                       | 998 ms: 2.16x slower                                                     |
| async_tree_io_tg           | 913 ms                                                       | 3.36 sec: 3.67x slower                                                   |
| async_tree_io              | 876 ms                                                       | 3.62 sec: 4.14x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.73x slower                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 199 ms: 1.09x faster                                                     |
| float          | 77.5 ms                                                      | 148 ms: 1.91x slower                                                     |
| nbody          | 85.1 ms                                                      | 201 ms: 2.37x slower                                                     |
| Geometric mean | (ref)                                                        | 1.61x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.85 ms: 1.08x faster                                                    |
| regex_dna      | 180 ms                                                       | 188 ms: 1.05x slower                                                     |
| regex_v8       | 22.7 ms                                                      | 25.1 ms: 1.11x slower                                                    |
| regex_compile  | 132 ms                                                       | 209 ms: 1.58x slower                                                     |
| Geometric mean | (ref)                                                        | 1.14x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 132 ms: 1.03x faster                                                     |
| json_loads           | 27.0 us                                                      | 28.6 us: 1.06x slower                                                    |
| xml_etree_iterparse  | 94.9 ms                                                      | 102 ms: 1.07x slower                                                     |
| xml_etree_generate   | 85.4 ms                                                      | 107 ms: 1.25x slower                                                     |
| json_dumps           | 10.5 ms                                                      | 14.8 ms: 1.41x slower                                                    |
| xml_etree_process    | 59.3 ms                                                      | 86.2 ms: 1.45x slower                                                    |
| tomli_loads          | 2.01 sec                                                     | 3.06 sec: 1.53x slower                                                   |
| unpickle_pure_python | 210 us                                                       | 381 us: 1.81x slower                                                     |
| pickle_pure_python   | 294 us                                                       | 576 us: 1.96x slower                                                     |
| Geometric mean       | (ref)                                                        | 1.35x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 11.3 ms: 1.53x slower                                                    |
| python_startup         | 11.0 ms                                                      | 20.3 ms: 1.85x slower                                                    |
| Geometric mean         | (ref)                                                        | 1.68x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 74.5 ms: 1.53x slower                                                    |
| genshi_text     | 21.5 ms                                                      | 36.2 ms: 1.68x slower                                                    |
| mako            | 11.3 ms                                                      | 20.1 ms: 1.77x slower                                                    |
| django_template | 34.1 ms                                                      | 61.8 ms: 1.81x slower                                                    |
| Geometric mean  | (ref)                                                        | 1.69x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits                   | 217 ms                                                       | 199 ms: 1.09x faster                                                     |
| regex_effbot               | 3.08 ms                                                      | 2.85 ms: 1.08x faster                                                    |
| xml_etree_parse            | 136 ms                                                       | 132 ms: 1.03x faster                                                     |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.00x slower                                                     |
| regex_dna                  | 180 ms                                                       | 188 ms: 1.05x slower                                                     |
| json_loads                 | 27.0 us                                                      | 28.6 us: 1.06x slower                                                    |
| json                       | 4.93 ms                                                      | 5.22 ms: 1.06x slower                                                    |
| xml_etree_iterparse        | 94.9 ms                                                      | 102 ms: 1.07x slower                                                     |
| deepcopy                   | 355 us                                                       | 383 us: 1.08x slower                                                     |
| sqlite_synth               | 2.21 us                                                      | 2.41 us: 1.09x slower                                                    |
| pathlib                    | 19.2 ms                                                      | 21.1 ms: 1.10x slower                                                    |
| regex_v8                   | 22.7 ms                                                      | 25.1 ms: 1.11x slower                                                    |
| gc_traversal               | 3.14 ms                                                      | 3.48 ms: 1.11x slower                                                    |
| async_tree_none_tg         | 336 ms                                                       | 384 ms: 1.14x slower                                                     |
| telco                      | 7.82 ms                                                      | 9.20 ms: 1.18x slower                                                    |
| deepcopy_memo              | 39.1 us                                                      | 46.4 us: 1.19x slower                                                    |
| scimark_fft                | 349 ms                                                       | 427 ms: 1.22x slower                                                     |
| coverage                   | 83.0 ms                                                      | 102 ms: 1.23x slower                                                     |
| xml_etree_generate         | 85.4 ms                                                      | 107 ms: 1.25x slower                                                     |
| coroutines                 | 23.6 ms                                                      | 29.7 ms: 1.26x slower                                                    |
| async_generators           | 377 ms                                                       | 480 ms: 1.27x slower                                                     |
| docutils                   | 2.62 sec                                                     | 3.33 sec: 1.27x slower                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 3.98 us: 1.28x slower                                                    |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 815 ms: 1.28x slower                                                     |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 6.02 ms: 1.28x slower                                                    |
| bpe_tokeniser              | 4.45 sec                                                     | 5.74 sec: 1.29x slower                                                   |
| create_gc_cycles           | 1.34 ms                                                      | 1.81 ms: 1.35x slower                                                    |
| meteor_contest             | 102 ms                                                       | 139 ms: 1.36x slower                                                     |
| json_dumps                 | 10.5 ms                                                      | 14.8 ms: 1.41x slower                                                    |
| spectral_norm              | 111 ms                                                       | 157 ms: 1.41x slower                                                     |
| generators                 | 28.8 ms                                                      | 41.0 ms: 1.42x slower                                                    |
| nqueens                    | 78.6 ms                                                      | 112 ms: 1.43x slower                                                     |
| typing_runtime_protocols   | 155 us                                                       | 222 us: 1.44x slower                                                     |
| xml_etree_process          | 59.3 ms                                                      | 86.2 ms: 1.45x slower                                                    |
| pycparser                  | 1.12 sec                                                     | 1.66 sec: 1.48x slower                                                   |
| fannkuch                   | 370 ms                                                       | 561 ms: 1.52x slower                                                     |
| sqlglot_optimize           | 52.7 ms                                                      | 80.2 ms: 1.52x slower                                                    |
| tomli_loads                | 2.01 sec                                                     | 3.06 sec: 1.53x slower                                                   |
| python_startup_no_site     | 7.39 ms                                                      | 11.3 ms: 1.53x slower                                                    |
| genshi_xml                 | 48.8 ms                                                      | 74.5 ms: 1.53x slower                                                    |
| sqlglot_normalize          | 106 ms                                                       | 162 ms: 1.53x slower                                                     |
| html5lib                   | 67.0 ms                                                      | 105 ms: 1.57x slower                                                     |
| pprint_safe_repr           | 738 ms                                                       | 1.16 sec: 1.58x slower                                                   |
| regex_compile              | 132 ms                                                       | 209 ms: 1.58x slower                                                     |
| crypto_pyaes               | 67.9 ms                                                      | 108 ms: 1.59x slower                                                     |
| pprint_pformat             | 1.50 sec                                                     | 2.43 sec: 1.62x slower                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 1.08 sec: 1.63x slower                                                   |
| genshi_text                | 21.5 ms                                                      | 36.2 ms: 1.68x slower                                                    |
| pyflate                    | 449 ms                                                       | 763 ms: 1.70x slower                                                     |
| async_tree_memoization_tg  | 414 ms                                                       | 725 ms: 1.75x slower                                                     |
| 2to3                       | 260 ms                                                       | 455 ms: 1.75x slower                                                     |
| mako                       | 11.3 ms                                                      | 20.1 ms: 1.77x slower                                                    |
| comprehensions             | 16.5 us                                                      | 29.7 us: 1.81x slower                                                    |
| django_template            | 34.1 ms                                                      | 61.8 ms: 1.81x slower                                                    |
| unpickle_pure_python       | 210 us                                                       | 381 us: 1.81x slower                                                     |
| python_startup             | 11.0 ms                                                      | 20.3 ms: 1.85x slower                                                    |
| logging_format             | 6.84 us                                                      | 12.8 us: 1.87x slower                                                    |
| async_tree_none            | 354 ms                                                       | 664 ms: 1.88x slower                                                     |
| scimark_monte_carlo        | 65.4 ms                                                      | 123 ms: 1.89x slower                                                     |
| scimark_lu                 | 113 ms                                                       | 213 ms: 1.89x slower                                                     |
| logging_simple             | 6.16 us                                                      | 11.6 us: 1.89x slower                                                    |
| richards                   | 45.2 ms                                                      | 86.1 ms: 1.90x slower                                                    |
| float                      | 77.5 ms                                                      | 148 ms: 1.91x slower                                                     |
| dulwich_log                | 74.8 ms                                                      | 145 ms: 1.94x slower                                                     |
| hexiom                     | 5.99 ms                                                      | 11.7 ms: 1.95x slower                                                    |
| pickle_pure_python         | 294 us                                                       | 576 us: 1.96x slower                                                     |
| pylint                     | 317 ms                                                       | 642 ms: 2.02x slower                                                     |
| scimark_sor                | 134 ms                                                       | 273 ms: 2.03x slower                                                     |
| logging_silent             | 103 ns                                                       | 209 ns: 2.04x slower                                                     |
| go                         | 141 ms                                                       | 288 ms: 2.05x slower                                                     |
| sqlglot_transpile          | 1.56 ms                                                      | 3.21 ms: 2.06x slower                                                    |
| chaos                      | 57.3 ms                                                      | 119 ms: 2.07x slower                                                     |
| sympy_integrate            | 19.8 ms                                                      | 42.2 ms: 2.13x slower                                                    |
| async_tree_memoization     | 461 ms                                                       | 998 ms: 2.16x slower                                                     |
| sqlglot_parse              | 1.25 ms                                                      | 2.78 ms: 2.22x slower                                                    |
| nbody                      | 85.1 ms                                                      | 201 ms: 2.37x slower                                                     |
| raytrace                   | 253 ms                                                       | 619 ms: 2.45x slower                                                     |
| sympy_expand               | 457 ms                                                       | 1.25 sec: 2.74x slower                                                   |
| sympy_sum                  | 156 ms                                                       | 535 ms: 3.44x slower                                                     |
| async_tree_io_tg           | 913 ms                                                       | 3.36 sec: 3.67x slower                                                   |
| sympy_str                  | 275 ms                                                       | 1.01 sec: 3.68x slower                                                   |
| async_tree_io              | 876 ms                                                       | 3.62 sec: 4.14x slower                                                   |
| bench_thread_pool          | 919 us                                                       | 4.32 ms: 4.70x slower                                                    |
| mdp                        | 2.36 sec                                                     | 16.3 sec: 6.91x slower                                                   |
| thrift                     | 778 us                                                       | 6.57 ms: 8.45x slower                                                    |
| deltablue                  | 3.12 ms                                                      | 43.9 ms: 14.06x slower                                                   |
| bench_mp_pool              | 11.0 ms                                                      | 202 ms: 18.35x slower                                                    |
| richards_super             | 51.6 ms                                                      | 1.82 sec: 35.17x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.82x slower                                                             |
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241125-3.14.0a2+-a515a0d-NOGIL/bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.431x slower
# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.53x
- 95% likely to have a slowdown of 1.52x
- 99% likely to have a slowdown of 1.48x

# Memory
- memory change: 1.31x