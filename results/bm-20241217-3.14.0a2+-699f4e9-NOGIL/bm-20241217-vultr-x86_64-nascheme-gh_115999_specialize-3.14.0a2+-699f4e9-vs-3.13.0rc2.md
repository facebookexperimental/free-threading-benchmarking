# Results vs. 3.13.0rc2

- fork: nascheme
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: 699f4e9
- commit date: 2024-12-17
- overall geometric mean: 1.227x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.17x slower
- Memory change: 1.32x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 367 ms: 1.42x slower                                                     |
| docutils       | 2.62 sec                                                     | 3.07 sec: 1.17x slower                                                   |
| html5lib       | 67.0 ms                                                      | 95.7 ms: 1.43x slower                                                    |
| Geometric mean | (ref)                                                        | 1.33x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 752 ms: 1.22x faster                                                     |
| async_tree_io              | 876 ms                                                       | 777 ms: 1.13x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 608 ms: 1.10x faster                                                     |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 583 ms: 1.09x faster                                                     |
| async_tree_memoization     | 461 ms                                                       | 442 ms: 1.04x faster                                                     |
| async_tree_none_tg         | 336 ms                                                       | 327 ms: 1.03x faster                                                     |
| async_tree_none            | 354 ms                                                       | 363 ms: 1.03x slower                                                     |
| coroutines                 | 23.6 ms                                                      | 25.1 ms: 1.06x slower                                                    |
| async_generators           | 377 ms                                                       | 446 ms: 1.18x slower                                                     |
| Geometric mean             | (ref)                                                        | 1.03x faster                                                             |

Benchmark hidden because not significant (2): asyncio_websockets, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 181 ms: 1.20x faster                                                     |
| float          | 77.5 ms                                                      | 111 ms: 1.44x slower                                                     |
| nbody          | 85.1 ms                                                      | 131 ms: 1.54x slower                                                     |
| Geometric mean | (ref)                                                        | 1.23x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.79 ms: 1.11x faster                                                    |
| regex_dna      | 180 ms                                                       | 188 ms: 1.04x slower                                                     |
| regex_v8       | 22.7 ms                                                      | 24.8 ms: 1.09x slower                                                    |
| regex_compile  | 132 ms                                                       | 172 ms: 1.30x slower                                                     |
| Geometric mean | (ref)                                                        | 1.08x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 89.9 ms: 1.06x faster                                                    |
| xml_etree_parse      | 136 ms                                                       | 131 ms: 1.04x faster                                                     |
| json_loads           | 27.0 us                                                      | 28.5 us: 1.05x slower                                                    |
| xml_etree_generate   | 85.4 ms                                                      | 98.3 ms: 1.15x slower                                                    |
| xml_etree_process    | 59.3 ms                                                      | 74.3 ms: 1.25x slower                                                    |
| tomli_loads          | 2.01 sec                                                     | 2.59 sec: 1.29x slower                                                   |
| json_dumps           | 10.5 ms                                                      | 14.2 ms: 1.35x slower                                                    |
| unpickle_pure_python | 210 us                                                       | 346 us: 1.65x slower                                                     |
| pickle_pure_python   | 294 us                                                       | 533 us: 1.81x slower                                                     |
| Geometric mean       | (ref)                                                        | 1.25x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                    |
| python_startup         | 11.0 ms                                                      | 17.1 ms: 1.56x slower                                                    |
| Geometric mean         | (ref)                                                        | 1.47x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 63.5 ms: 1.30x slower                                                    |
| genshi_text     | 21.5 ms                                                      | 30.6 ms: 1.42x slower                                                    |
| django_template | 34.1 ms                                                      | 51.2 ms: 1.50x slower                                                    |
| mako            | 11.3 ms                                                      | 17.2 ms: 1.51x slower                                                    |
| Geometric mean  | (ref)                                                        | 1.43x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 752 ms: 1.22x faster                                                     |
| pidigits                   | 217 ms                                                       | 181 ms: 1.20x faster                                                     |
| async_tree_io              | 876 ms                                                       | 777 ms: 1.13x faster                                                     |
| regex_effbot               | 3.08 ms                                                      | 2.79 ms: 1.11x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 608 ms: 1.10x faster                                                     |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 583 ms: 1.09x faster                                                     |
| deepcopy                   | 355 us                                                       | 327 us: 1.09x faster                                                     |
| xml_etree_iterparse        | 94.9 ms                                                      | 89.9 ms: 1.06x faster                                                    |
| async_tree_memoization     | 461 ms                                                       | 442 ms: 1.04x faster                                                     |
| xml_etree_parse            | 136 ms                                                       | 131 ms: 1.04x faster                                                     |
| spectral_norm              | 111 ms                                                       | 107 ms: 1.03x faster                                                     |
| sqlite_synth               | 2.21 us                                                      | 2.14 us: 1.03x faster                                                    |
| async_tree_none_tg         | 336 ms                                                       | 327 ms: 1.03x faster                                                     |
| pathlib                    | 19.2 ms                                                      | 19.6 ms: 1.02x slower                                                    |
| json                       | 4.93 ms                                                      | 5.05 ms: 1.03x slower                                                    |
| async_tree_none            | 354 ms                                                       | 363 ms: 1.03x slower                                                     |
| deepcopy_memo              | 39.1 us                                                      | 40.2 us: 1.03x slower                                                    |
| regex_dna                  | 180 ms                                                       | 188 ms: 1.04x slower                                                     |
| json_loads                 | 27.0 us                                                      | 28.5 us: 1.05x slower                                                    |
| scimark_fft                | 349 ms                                                       | 371 ms: 1.06x slower                                                     |
| coroutines                 | 23.6 ms                                                      | 25.1 ms: 1.06x slower                                                    |
| regex_v8                   | 22.7 ms                                                      | 24.8 ms: 1.09x slower                                                    |
| telco                      | 7.82 ms                                                      | 8.58 ms: 1.10x slower                                                    |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.20 ms: 1.11x slower                                                    |
| deepcopy_reduce            | 3.11 us                                                      | 3.46 us: 1.11x slower                                                    |
| bpe_tokeniser              | 4.45 sec                                                     | 4.99 sec: 1.12x slower                                                   |
| xml_etree_generate         | 85.4 ms                                                      | 98.3 ms: 1.15x slower                                                    |
| pylint                     | 317 ms                                                       | 367 ms: 1.16x slower                                                     |
| docutils                   | 2.62 sec                                                     | 3.07 sec: 1.17x slower                                                   |
| async_generators           | 377 ms                                                       | 446 ms: 1.18x slower                                                     |
| dulwich_log                | 74.8 ms                                                      | 91.2 ms: 1.22x slower                                                    |
| mdp                        | 2.36 sec                                                     | 2.88 sec: 1.22x slower                                                   |
| nqueens                    | 78.6 ms                                                      | 97.8 ms: 1.24x slower                                                    |
| xml_etree_process          | 59.3 ms                                                      | 74.3 ms: 1.25x slower                                                    |
| sqlglot_optimize           | 52.7 ms                                                      | 66.3 ms: 1.26x slower                                                    |
| coverage                   | 83.0 ms                                                      | 105 ms: 1.26x slower                                                     |
| sqlglot_normalize          | 106 ms                                                       | 133 ms: 1.26x slower                                                     |
| pycparser                  | 1.12 sec                                                     | 1.43 sec: 1.28x slower                                                   |
| meteor_contest             | 102 ms                                                       | 130 ms: 1.28x slower                                                     |
| thrift                     | 778 us                                                       | 998 us: 1.28x slower                                                     |
| tomli_loads                | 2.01 sec                                                     | 2.59 sec: 1.29x slower                                                   |
| regex_compile              | 132 ms                                                       | 172 ms: 1.30x slower                                                     |
| genshi_xml                 | 48.8 ms                                                      | 63.5 ms: 1.30x slower                                                    |
| typing_runtime_protocols   | 155 us                                                       | 202 us: 1.30x slower                                                     |
| fannkuch                   | 370 ms                                                       | 493 ms: 1.33x slower                                                     |
| create_gc_cycles           | 1.34 ms                                                      | 1.78 ms: 1.33x slower                                                    |
| pprint_safe_repr           | 738 ms                                                       | 984 ms: 1.33x slower                                                     |
| json_dumps                 | 10.5 ms                                                      | 14.2 ms: 1.35x slower                                                    |
| crypto_pyaes               | 67.9 ms                                                      | 92.7 ms: 1.37x slower                                                    |
| pprint_pformat             | 1.50 sec                                                     | 2.04 sec: 1.37x slower                                                   |
| generators                 | 28.8 ms                                                      | 39.5 ms: 1.37x slower                                                    |
| python_startup_no_site     | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                    |
| 2to3                       | 260 ms                                                       | 367 ms: 1.42x slower                                                     |
| genshi_text                | 21.5 ms                                                      | 30.6 ms: 1.42x slower                                                    |
| html5lib                   | 67.0 ms                                                      | 95.7 ms: 1.43x slower                                                    |
| float                      | 77.5 ms                                                      | 111 ms: 1.44x slower                                                     |
| sympy_integrate            | 19.8 ms                                                      | 29.5 ms: 1.49x slower                                                    |
| pyflate                    | 449 ms                                                       | 672 ms: 1.50x slower                                                     |
| django_template            | 34.1 ms                                                      | 51.2 ms: 1.50x slower                                                    |
| mako                       | 11.3 ms                                                      | 17.2 ms: 1.51x slower                                                    |
| logging_simple             | 6.16 us                                                      | 9.35 us: 1.52x slower                                                    |
| logging_format             | 6.84 us                                                      | 10.5 us: 1.53x slower                                                    |
| nbody                      | 85.1 ms                                                      | 131 ms: 1.54x slower                                                     |
| python_startup             | 11.0 ms                                                      | 17.1 ms: 1.56x slower                                                    |
| richards_super             | 51.6 ms                                                      | 81.6 ms: 1.58x slower                                                    |
| richards                   | 45.2 ms                                                      | 73.6 ms: 1.63x slower                                                    |
| unpickle_pure_python       | 210 us                                                       | 346 us: 1.65x slower                                                     |
| scimark_lu                 | 113 ms                                                       | 187 ms: 1.66x slower                                                     |
| hexiom                     | 5.99 ms                                                      | 10.2 ms: 1.70x slower                                                    |
| scimark_monte_carlo        | 65.4 ms                                                      | 111 ms: 1.70x slower                                                     |
| sympy_str                  | 275 ms                                                       | 473 ms: 1.72x slower                                                     |
| chaos                      | 57.3 ms                                                      | 99.0 ms: 1.73x slower                                                    |
| comprehensions             | 16.5 us                                                      | 28.5 us: 1.73x slower                                                    |
| sqlglot_transpile          | 1.56 ms                                                      | 2.71 ms: 1.74x slower                                                    |
| pickle_pure_python         | 294 us                                                       | 533 us: 1.81x slower                                                     |
| scimark_sor                | 134 ms                                                       | 245 ms: 1.82x slower                                                     |
| go                         | 141 ms                                                       | 261 ms: 1.86x slower                                                     |
| sqlglot_parse              | 1.25 ms                                                      | 2.35 ms: 1.88x slower                                                    |
| logging_silent             | 103 ns                                                       | 200 ns: 1.95x slower                                                     |
| raytrace                   | 253 ms                                                       | 523 ms: 2.07x slower                                                     |
| sympy_expand               | 457 ms                                                       | 953 ms: 2.09x slower                                                     |
| sympy_sum                  | 156 ms                                                       | 348 ms: 2.24x slower                                                     |
| deltablue                  | 3.12 ms                                                      | 8.05 ms: 2.58x slower                                                    |
| bench_thread_pool          | 919 us                                                       | 3.39 ms: 3.69x slower                                                    |
| bench_mp_pool              | 11.0 ms                                                      | 107 ms: 9.75x slower                                                     |
| Geometric mean             | (ref)                                                        | 1.34x slower                                                             |

Benchmark hidden because not significant (3): asyncio_websockets, async_tree_memoization_tg, gc_traversal
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241217-3.14.0a2+-699f4e9-NOGIL/bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.227x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.22x
- 95% likely to have a slowdown of 1.21x
- 99% likely to have a slowdown of 1.17x

# Memory
- memory change: 1.32x