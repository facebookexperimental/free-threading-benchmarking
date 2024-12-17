# Results vs. 3.13.0rc2

- fork: nascheme
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: 4c484ab
- commit date: 2024-12-13
- overall geometric mean: 1.219x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.17x slower
- Memory change: 1.32x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-4c484ab |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 360 ms: 1.39x slower                                                     |
| docutils       | 2.62 sec                                                     | 3.05 sec: 1.17x slower                                                   |
| html5lib       | 67.0 ms                                                      | 95.0 ms: 1.42x slower                                                    |
| Geometric mean | (ref)                                                        | 1.32x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-4c484ab |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 740 ms: 1.23x faster                                                     |
| async_tree_io              | 876 ms                                                       | 761 ms: 1.15x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 598 ms: 1.11x faster                                                     |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 574 ms: 1.11x faster                                                     |
| async_tree_memoization     | 461 ms                                                       | 429 ms: 1.07x faster                                                     |
| async_tree_none_tg         | 336 ms                                                       | 322 ms: 1.05x faster                                                     |
| async_tree_memoization_tg  | 414 ms                                                       | 401 ms: 1.03x faster                                                     |
| coroutines                 | 23.6 ms                                                      | 24.1 ms: 1.02x slower                                                    |
| async_generators           | 377 ms                                                       | 444 ms: 1.18x slower                                                     |
| Geometric mean             | (ref)                                                        | 1.05x faster                                                             |

Benchmark hidden because not significant (2): asyncio_websockets, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-4c484ab |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 181 ms: 1.20x faster                                                     |
| float          | 77.5 ms                                                      | 111 ms: 1.43x slower                                                     |
| nbody          | 85.1 ms                                                      | 131 ms: 1.54x slower                                                     |
| Geometric mean | (ref)                                                        | 1.23x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-4c484ab |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.97 ms: 1.04x faster                                                    |
| regex_dna      | 180 ms                                                       | 192 ms: 1.07x slower                                                     |
| regex_v8       | 22.7 ms                                                      | 25.0 ms: 1.10x slower                                                    |
| regex_compile  | 132 ms                                                       | 170 ms: 1.29x slower                                                     |
| Geometric mean | (ref)                                                        | 1.10x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-4c484ab |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 90.4 ms: 1.05x faster                                                    |
| xml_etree_parse      | 136 ms                                                       | 131 ms: 1.04x faster                                                     |
| json_loads           | 27.0 us                                                      | 28.5 us: 1.05x slower                                                    |
| xml_etree_generate   | 85.4 ms                                                      | 97.6 ms: 1.14x slower                                                    |
| xml_etree_process    | 59.3 ms                                                      | 73.8 ms: 1.24x slower                                                    |
| tomli_loads          | 2.01 sec                                                     | 2.58 sec: 1.29x slower                                                   |
| json_dumps           | 10.5 ms                                                      | 14.2 ms: 1.34x slower                                                    |
| unpickle_pure_python | 210 us                                                       | 331 us: 1.58x slower                                                     |
| pickle_pure_python   | 294 us                                                       | 502 us: 1.71x slower                                                     |
| Geometric mean       | (ref)                                                        | 1.23x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-4c484ab |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                    |
| python_startup         | 11.0 ms                                                      | 17.1 ms: 1.56x slower                                                    |
| Geometric mean         | (ref)                                                        | 1.46x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-4c484ab |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 63.7 ms: 1.31x slower                                                    |
| genshi_text     | 21.5 ms                                                      | 30.9 ms: 1.43x slower                                                    |
| django_template | 34.1 ms                                                      | 50.2 ms: 1.47x slower                                                    |
| mako            | 11.3 ms                                                      | 17.2 ms: 1.51x slower                                                    |
| Geometric mean  | (ref)                                                        | 1.43x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-4c484ab |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 740 ms: 1.23x faster                                                     |
| pidigits                   | 217 ms                                                       | 181 ms: 1.20x faster                                                     |
| async_tree_io              | 876 ms                                                       | 761 ms: 1.15x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 598 ms: 1.11x faster                                                     |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 574 ms: 1.11x faster                                                     |
| deepcopy                   | 355 us                                                       | 323 us: 1.10x faster                                                     |
| async_tree_memoization     | 461 ms                                                       | 429 ms: 1.07x faster                                                     |
| xml_etree_iterparse        | 94.9 ms                                                      | 90.4 ms: 1.05x faster                                                    |
| async_tree_none_tg         | 336 ms                                                       | 322 ms: 1.05x faster                                                     |
| xml_etree_parse            | 136 ms                                                       | 131 ms: 1.04x faster                                                     |
| regex_effbot               | 3.08 ms                                                      | 2.97 ms: 1.04x faster                                                    |
| async_tree_memoization_tg  | 414 ms                                                       | 401 ms: 1.03x faster                                                     |
| sqlite_synth               | 2.21 us                                                      | 2.16 us: 1.02x faster                                                    |
| spectral_norm              | 111 ms                                                       | 110 ms: 1.01x faster                                                     |
| coroutines                 | 23.6 ms                                                      | 24.1 ms: 1.02x slower                                                    |
| json                       | 4.93 ms                                                      | 5.07 ms: 1.03x slower                                                    |
| pathlib                    | 19.2 ms                                                      | 19.9 ms: 1.04x slower                                                    |
| deepcopy_memo              | 39.1 us                                                      | 40.8 us: 1.04x slower                                                    |
| json_loads                 | 27.0 us                                                      | 28.5 us: 1.05x slower                                                    |
| regex_dna                  | 180 ms                                                       | 192 ms: 1.07x slower                                                     |
| deepcopy_reduce            | 3.11 us                                                      | 3.42 us: 1.10x slower                                                    |
| regex_v8                   | 22.7 ms                                                      | 25.0 ms: 1.10x slower                                                    |
| telco                      | 7.82 ms                                                      | 8.64 ms: 1.10x slower                                                    |
| scimark_fft                | 349 ms                                                       | 392 ms: 1.12x slower                                                     |
| bpe_tokeniser              | 4.45 sec                                                     | 5.03 sec: 1.13x slower                                                   |
| xml_etree_generate         | 85.4 ms                                                      | 97.6 ms: 1.14x slower                                                    |
| pylint                     | 317 ms                                                       | 364 ms: 1.15x slower                                                     |
| docutils                   | 2.62 sec                                                     | 3.05 sec: 1.17x slower                                                   |
| async_generators           | 377 ms                                                       | 444 ms: 1.18x slower                                                     |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.62 ms: 1.19x slower                                                    |
| coverage                   | 83.0 ms                                                      | 99.2 ms: 1.20x slower                                                    |
| dulwich_log                | 74.8 ms                                                      | 90.8 ms: 1.21x slower                                                    |
| mdp                        | 2.36 sec                                                     | 2.86 sec: 1.22x slower                                                   |
| nqueens                    | 78.6 ms                                                      | 97.6 ms: 1.24x slower                                                    |
| pycparser                  | 1.12 sec                                                     | 1.39 sec: 1.24x slower                                                   |
| xml_etree_process          | 59.3 ms                                                      | 73.8 ms: 1.24x slower                                                    |
| sqlglot_optimize           | 52.7 ms                                                      | 65.7 ms: 1.25x slower                                                    |
| sqlglot_normalize          | 106 ms                                                       | 133 ms: 1.26x slower                                                     |
| tomli_loads                | 2.01 sec                                                     | 2.58 sec: 1.29x slower                                                   |
| regex_compile              | 132 ms                                                       | 170 ms: 1.29x slower                                                     |
| thrift                     | 778 us                                                       | 1.00 ms: 1.29x slower                                                    |
| meteor_contest             | 102 ms                                                       | 131 ms: 1.29x slower                                                     |
| genshi_xml                 | 48.8 ms                                                      | 63.7 ms: 1.31x slower                                                    |
| pprint_safe_repr           | 738 ms                                                       | 965 ms: 1.31x slower                                                     |
| typing_runtime_protocols   | 155 us                                                       | 203 us: 1.31x slower                                                     |
| create_gc_cycles           | 1.34 ms                                                      | 1.78 ms: 1.33x slower                                                    |
| pprint_pformat             | 1.50 sec                                                     | 2.00 sec: 1.33x slower                                                   |
| generators                 | 28.8 ms                                                      | 38.5 ms: 1.34x slower                                                    |
| crypto_pyaes               | 67.9 ms                                                      | 90.7 ms: 1.34x slower                                                    |
| json_dumps                 | 10.5 ms                                                      | 14.2 ms: 1.34x slower                                                    |
| fannkuch                   | 370 ms                                                       | 498 ms: 1.35x slower                                                     |
| python_startup_no_site     | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                    |
| 2to3                       | 260 ms                                                       | 360 ms: 1.39x slower                                                     |
| html5lib                   | 67.0 ms                                                      | 95.0 ms: 1.42x slower                                                    |
| genshi_text                | 21.5 ms                                                      | 30.9 ms: 1.43x slower                                                    |
| float                      | 77.5 ms                                                      | 111 ms: 1.43x slower                                                     |
| django_template            | 34.1 ms                                                      | 50.2 ms: 1.47x slower                                                    |
| logging_simple             | 6.16 us                                                      | 9.06 us: 1.47x slower                                                    |
| pyflate                    | 449 ms                                                       | 662 ms: 1.48x slower                                                     |
| sympy_integrate            | 19.8 ms                                                      | 29.4 ms: 1.48x slower                                                    |
| logging_format             | 6.84 us                                                      | 10.1 us: 1.48x slower                                                    |
| richards_super             | 51.6 ms                                                      | 77.6 ms: 1.50x slower                                                    |
| mako                       | 11.3 ms                                                      | 17.2 ms: 1.51x slower                                                    |
| richards                   | 45.2 ms                                                      | 69.1 ms: 1.53x slower                                                    |
| nbody                      | 85.1 ms                                                      | 131 ms: 1.54x slower                                                     |
| python_startup             | 11.0 ms                                                      | 17.1 ms: 1.56x slower                                                    |
| unpickle_pure_python       | 210 us                                                       | 331 us: 1.58x slower                                                     |
| scimark_lu                 | 113 ms                                                       | 185 ms: 1.64x slower                                                     |
| scimark_monte_carlo        | 65.4 ms                                                      | 108 ms: 1.65x slower                                                     |
| hexiom                     | 5.99 ms                                                      | 9.87 ms: 1.65x slower                                                    |
| chaos                      | 57.3 ms                                                      | 95.9 ms: 1.67x slower                                                    |
| comprehensions             | 16.5 us                                                      | 27.7 us: 1.68x slower                                                    |
| pickle_pure_python         | 294 us                                                       | 502 us: 1.71x slower                                                     |
| sympy_str                  | 275 ms                                                       | 473 ms: 1.72x slower                                                     |
| sqlglot_transpile          | 1.56 ms                                                      | 2.69 ms: 1.72x slower                                                    |
| scimark_sor                | 134 ms                                                       | 232 ms: 1.73x slower                                                     |
| go                         | 141 ms                                                       | 244 ms: 1.73x slower                                                     |
| logging_silent             | 103 ns                                                       | 186 ns: 1.81x slower                                                     |
| sqlglot_parse              | 1.25 ms                                                      | 2.33 ms: 1.87x slower                                                    |
| raytrace                   | 253 ms                                                       | 495 ms: 1.96x slower                                                     |
| sympy_expand               | 457 ms                                                       | 953 ms: 2.09x slower                                                     |
| sympy_sum                  | 156 ms                                                       | 348 ms: 2.24x slower                                                     |
| deltablue                  | 3.12 ms                                                      | 7.65 ms: 2.45x slower                                                    |
| bench_thread_pool          | 919 us                                                       | 3.37 ms: 3.67x slower                                                    |
| bench_mp_pool              | 11.0 ms                                                      | 107 ms: 9.73x slower                                                     |
| Geometric mean             | (ref)                                                        | 1.33x slower                                                             |

Benchmark hidden because not significant (3): asyncio_websockets, async_tree_none, gc_traversal
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241213-3.14.0a2+-4c484ab-NOGIL/bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-4c484ab.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.219x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.21x
- 95% likely to have a slowdown of 1.19x
- 99% likely to have a slowdown of 1.17x

# Memory
- memory change: 1.32x