# Results vs. 3.13.0rc2

- fork: nascheme
- ref: gh_115999_load_super
- machine: linux-x86_64
- commit hash: ab3af14
- commit date: 2024-11-26
- overall geometric mean: 1.313x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.29x slower
- Memory change: 1.31x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241126-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-ab3af14 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 406 ms: 1.56x slower                                                     |
| docutils       | 2.62 sec                                                     | 3.29 sec: 1.26x slower                                                   |
| html5lib       | 67.0 ms                                                      | 105 ms: 1.57x slower                                                     |
| Geometric mean | (ref)                                                        | 1.46x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241126-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-ab3af14 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 893 ms: 1.02x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 684 ms: 1.03x slower                                                     |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 657 ms: 1.03x slower                                                     |
| async_tree_io              | 876 ms                                                       | 918 ms: 1.05x slower                                                     |
| async_tree_memoization     | 461 ms                                                       | 509 ms: 1.10x slower                                                     |
| async_tree_none_tg         | 336 ms                                                       | 385 ms: 1.14x slower                                                     |
| async_tree_memoization_tg  | 414 ms                                                       | 480 ms: 1.16x slower                                                     |
| async_tree_none            | 354 ms                                                       | 420 ms: 1.19x slower                                                     |
| coroutines                 | 23.6 ms                                                      | 29.2 ms: 1.24x slower                                                    |
| async_generators           | 377 ms                                                       | 482 ms: 1.28x slower                                                     |
| Geometric mean             | (ref)                                                        | 1.10x slower                                                             |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241126-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-ab3af14 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 183 ms: 1.18x faster                                                     |
| float          | 77.5 ms                                                      | 148 ms: 1.91x slower                                                     |
| nbody          | 85.1 ms                                                      | 197 ms: 2.32x slower                                                     |
| Geometric mean | (ref)                                                        | 1.55x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241126-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-ab3af14 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.86 ms: 1.08x faster                                                    |
| regex_dna      | 180 ms                                                       | 191 ms: 1.06x slower                                                     |
| regex_v8       | 22.7 ms                                                      | 25.6 ms: 1.13x slower                                                    |
| regex_compile  | 132 ms                                                       | 209 ms: 1.58x slower                                                     |
| Geometric mean | (ref)                                                        | 1.15x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241126-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-ab3af14 |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 131 ms: 1.04x faster                                                     |
| json_loads           | 27.0 us                                                      | 28.3 us: 1.05x slower                                                    |
| xml_etree_iterparse  | 94.9 ms                                                      | 102 ms: 1.08x slower                                                     |
| xml_etree_generate   | 85.4 ms                                                      | 106 ms: 1.25x slower                                                     |
| json_dumps           | 10.5 ms                                                      | 14.6 ms: 1.38x slower                                                    |
| xml_etree_process    | 59.3 ms                                                      | 86.5 ms: 1.46x slower                                                    |
| tomli_loads          | 2.01 sec                                                     | 3.05 sec: 1.52x slower                                                   |
| unpickle_pure_python | 210 us                                                       | 383 us: 1.83x slower                                                     |
| pickle_pure_python   | 294 us                                                       | 575 us: 1.95x slower                                                     |
| Geometric mean       | (ref)                                                        | 1.35x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241126-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-ab3af14 |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                                    |
| python_startup         | 11.0 ms                                                      | 17.5 ms: 1.59x slower                                                    |
| Geometric mean         | (ref)                                                        | 1.49x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241126-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-ab3af14 |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 75.0 ms: 1.54x slower                                                    |
| genshi_text     | 21.5 ms                                                      | 36.0 ms: 1.67x slower                                                    |
| django_template | 34.1 ms                                                      | 58.6 ms: 1.72x slower                                                    |
| mako            | 11.3 ms                                                      | 19.9 ms: 1.76x slower                                                    |
| Geometric mean  | (ref)                                                        | 1.67x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241126-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-ab3af14 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits                   | 217 ms                                                       | 183 ms: 1.18x faster                                                     |
| regex_effbot               | 3.08 ms                                                      | 2.86 ms: 1.08x faster                                                    |
| xml_etree_parse            | 136 ms                                                       | 131 ms: 1.04x faster                                                     |
| async_tree_io_tg           | 913 ms                                                       | 893 ms: 1.02x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 684 ms: 1.03x slower                                                     |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 657 ms: 1.03x slower                                                     |
| json_loads                 | 27.0 us                                                      | 28.3 us: 1.05x slower                                                    |
| async_tree_io              | 876 ms                                                       | 918 ms: 1.05x slower                                                     |
| json                       | 4.93 ms                                                      | 5.19 ms: 1.05x slower                                                    |
| regex_dna                  | 180 ms                                                       | 191 ms: 1.06x slower                                                     |
| deepcopy                   | 355 us                                                       | 379 us: 1.07x slower                                                     |
| xml_etree_iterparse        | 94.9 ms                                                      | 102 ms: 1.08x slower                                                     |
| sqlite_synth               | 2.21 us                                                      | 2.39 us: 1.08x slower                                                    |
| async_tree_memoization     | 461 ms                                                       | 509 ms: 1.10x slower                                                     |
| pathlib                    | 19.2 ms                                                      | 21.2 ms: 1.11x slower                                                    |
| gc_traversal               | 3.14 ms                                                      | 3.49 ms: 1.11x slower                                                    |
| regex_v8                   | 22.7 ms                                                      | 25.6 ms: 1.13x slower                                                    |
| async_tree_none_tg         | 336 ms                                                       | 385 ms: 1.14x slower                                                     |
| async_tree_memoization_tg  | 414 ms                                                       | 480 ms: 1.16x slower                                                     |
| telco                      | 7.82 ms                                                      | 9.11 ms: 1.16x slower                                                    |
| deepcopy_memo              | 39.1 us                                                      | 45.8 us: 1.17x slower                                                    |
| scimark_fft                | 349 ms                                                       | 410 ms: 1.17x slower                                                     |
| async_tree_none            | 354 ms                                                       | 420 ms: 1.19x slower                                                     |
| coroutines                 | 23.6 ms                                                      | 29.2 ms: 1.24x slower                                                    |
| coverage                   | 83.0 ms                                                      | 103 ms: 1.24x slower                                                     |
| xml_etree_generate         | 85.4 ms                                                      | 106 ms: 1.25x slower                                                     |
| docutils                   | 2.62 sec                                                     | 3.29 sec: 1.26x slower                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 3.94 us: 1.26x slower                                                    |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 6.00 ms: 1.28x slower                                                    |
| async_generators           | 377 ms                                                       | 482 ms: 1.28x slower                                                     |
| pylint                     | 317 ms                                                       | 407 ms: 1.28x slower                                                     |
| bpe_tokeniser              | 4.45 sec                                                     | 5.73 sec: 1.29x slower                                                   |
| meteor_contest             | 102 ms                                                       | 137 ms: 1.35x slower                                                     |
| mdp                        | 2.36 sec                                                     | 3.19 sec: 1.35x slower                                                   |
| create_gc_cycles           | 1.34 ms                                                      | 1.82 ms: 1.36x slower                                                    |
| dulwich_log                | 74.8 ms                                                      | 102 ms: 1.36x slower                                                     |
| spectral_norm              | 111 ms                                                       | 152 ms: 1.37x slower                                                     |
| json_dumps                 | 10.5 ms                                                      | 14.6 ms: 1.38x slower                                                    |
| python_startup_no_site     | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                                    |
| typing_runtime_protocols   | 155 us                                                       | 218 us: 1.41x slower                                                     |
| nqueens                    | 78.6 ms                                                      | 112 ms: 1.42x slower                                                     |
| generators                 | 28.8 ms                                                      | 41.2 ms: 1.43x slower                                                    |
| xml_etree_process          | 59.3 ms                                                      | 86.5 ms: 1.46x slower                                                    |
| pycparser                  | 1.12 sec                                                     | 1.66 sec: 1.49x slower                                                   |
| fannkuch                   | 370 ms                                                       | 555 ms: 1.50x slower                                                     |
| tomli_loads                | 2.01 sec                                                     | 3.05 sec: 1.52x slower                                                   |
| sqlglot_optimize           | 52.7 ms                                                      | 80.5 ms: 1.53x slower                                                    |
| genshi_xml                 | 48.8 ms                                                      | 75.0 ms: 1.54x slower                                                    |
| sqlglot_normalize          | 106 ms                                                       | 163 ms: 1.55x slower                                                     |
| pprint_safe_repr           | 738 ms                                                       | 1.15 sec: 1.55x slower                                                   |
| 2to3                       | 260 ms                                                       | 406 ms: 1.56x slower                                                     |
| html5lib                   | 67.0 ms                                                      | 105 ms: 1.57x slower                                                     |
| crypto_pyaes               | 67.9 ms                                                      | 107 ms: 1.57x slower                                                     |
| thrift                     | 778 us                                                       | 1.23 ms: 1.58x slower                                                    |
| regex_compile              | 132 ms                                                       | 209 ms: 1.58x slower                                                     |
| pprint_pformat             | 1.50 sec                                                     | 2.38 sec: 1.59x slower                                                   |
| python_startup             | 11.0 ms                                                      | 17.5 ms: 1.59x slower                                                    |
| sympy_integrate            | 19.8 ms                                                      | 32.0 ms: 1.61x slower                                                    |
| genshi_text                | 21.5 ms                                                      | 36.0 ms: 1.67x slower                                                    |
| pyflate                    | 449 ms                                                       | 770 ms: 1.72x slower                                                     |
| django_template            | 34.1 ms                                                      | 58.6 ms: 1.72x slower                                                    |
| mako                       | 11.3 ms                                                      | 19.9 ms: 1.76x slower                                                    |
| unpickle_pure_python       | 210 us                                                       | 383 us: 1.83x slower                                                     |
| comprehensions             | 16.5 us                                                      | 30.1 us: 1.83x slower                                                    |
| richards_super             | 51.6 ms                                                      | 94.8 ms: 1.84x slower                                                    |
| logging_simple             | 6.16 us                                                      | 11.5 us: 1.86x slower                                                    |
| scimark_lu                 | 113 ms                                                       | 212 ms: 1.89x slower                                                     |
| sympy_str                  | 275 ms                                                       | 519 ms: 1.89x slower                                                     |
| logging_format             | 6.84 us                                                      | 13.0 us: 1.89x slower                                                    |
| richards                   | 45.2 ms                                                      | 86.2 ms: 1.91x slower                                                    |
| float                      | 77.5 ms                                                      | 148 ms: 1.91x slower                                                     |
| scimark_monte_carlo        | 65.4 ms                                                      | 125 ms: 1.91x slower                                                     |
| hexiom                     | 5.99 ms                                                      | 11.7 ms: 1.95x slower                                                    |
| pickle_pure_python         | 294 us                                                       | 575 us: 1.95x slower                                                     |
| scimark_sor                | 134 ms                                                       | 271 ms: 2.02x slower                                                     |
| logging_silent             | 103 ns                                                       | 210 ns: 2.05x slower                                                     |
| go                         | 141 ms                                                       | 291 ms: 2.06x slower                                                     |
| sqlglot_transpile          | 1.56 ms                                                      | 3.23 ms: 2.07x slower                                                    |
| chaos                      | 57.3 ms                                                      | 119 ms: 2.07x slower                                                     |
| sympy_expand               | 457 ms                                                       | 1.02 sec: 2.23x slower                                                   |
| sqlglot_parse              | 1.25 ms                                                      | 2.80 ms: 2.24x slower                                                    |
| nbody                      | 85.1 ms                                                      | 197 ms: 2.32x slower                                                     |
| sympy_sum                  | 156 ms                                                       | 370 ms: 2.38x slower                                                     |
| raytrace                   | 253 ms                                                       | 630 ms: 2.49x slower                                                     |
| deltablue                  | 3.12 ms                                                      | 8.72 ms: 2.79x slower                                                    |
| bench_thread_pool          | 919 us                                                       | 3.47 ms: 3.78x slower                                                    |
| bench_mp_pool              | 11.0 ms                                                      | 110 ms: 9.99x slower                                                     |
| Geometric mean             | (ref)                                                        | 1.51x slower                                                             |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241126-3.14.0a2+-ab3af14-NOGIL/bm-20241126-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-ab3af14.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.313x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.35x
- 95% likely to have a slowdown of 1.34x
- 99% likely to have a slowdown of 1.29x

# Memory
- memory change: 1.31x