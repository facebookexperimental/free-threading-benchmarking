# Results vs. 3.13.0rc2

- fork: nascheme
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: d6ea4f1
- commit date: 2024-12-13
- overall geometric mean: 1.035x faster
- HPT reliability: 99.98%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 255 ms: 1.02x faster                                                     |
| docutils       | 2.62 sec                                                     | 2.55 sec: 1.02x faster                                                   |
| Geometric mean | (ref)                                                        | 1.02x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 610 ms: 1.50x faster                                                     |
| async_tree_io              | 876 ms                                                       | 627 ms: 1.40x faster                                                     |
| async_tree_memoization     | 461 ms                                                       | 334 ms: 1.38x faster                                                     |
| async_tree_memoization_tg  | 414 ms                                                       | 308 ms: 1.35x faster                                                     |
| async_tree_none_tg         | 336 ms                                                       | 257 ms: 1.31x faster                                                     |
| async_tree_none            | 354 ms                                                       | 276 ms: 1.28x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 568 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 549 ms: 1.16x faster                                                     |
| coroutines                 | 23.6 ms                                                      | 21.3 ms: 1.10x faster                                                    |
| async_generators           | 377 ms                                                       | 363 ms: 1.04x faster                                                     |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.01x slower                                                     |
| Geometric mean             | (ref)                                                        | 1.23x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 217 ms: 1.00x slower                                                     |
| nbody          | 85.1 ms                                                      | 94.2 ms: 1.11x slower                                                    |
| Geometric mean | (ref)                                                        | 1.03x slower                                                             |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.73 ms: 1.13x faster                                                    |
| regex_dna      | 180 ms                                                       | 166 ms: 1.08x faster                                                     |
| regex_compile  | 132 ms                                                       | 130 ms: 1.02x faster                                                     |
| regex_v8       | 22.7 ms                                                      | 23.3 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                        | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 127 ms: 1.07x faster                                                     |
| xml_etree_iterparse  | 94.9 ms                                                      | 90.4 ms: 1.05x faster                                                    |
| xml_etree_generate   | 85.4 ms                                                      | 84.0 ms: 1.02x faster                                                    |
| xml_etree_process    | 59.3 ms                                                      | 58.7 ms: 1.01x faster                                                    |
| json_loads           | 27.0 us                                                      | 26.7 us: 1.01x faster                                                    |
| unpickle_pure_python | 210 us                                                       | 209 us: 1.01x faster                                                     |
| tomli_loads          | 2.01 sec                                                     | 2.06 sec: 1.03x slower                                                   |
| pickle_pure_python   | 294 us                                                       | 310 us: 1.05x slower                                                     |
| json_dumps           | 10.5 ms                                                      | 11.4 ms: 1.08x slower                                                    |
| Geometric mean       | (ref)                                                        | 1.00x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.49 ms: 1.01x slower                                                    |
| python_startup         | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                                    |
| Geometric mean         | (ref)                                                        | 1.16x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 21.8 ms: 1.01x slower                                                    |
| genshi_xml      | 48.8 ms                                                      | 49.8 ms: 1.02x slower                                                    |
| mako            | 11.3 ms                                                      | 11.7 ms: 1.03x slower                                                    |
| django_template | 34.1 ms                                                      | 35.3 ms: 1.04x slower                                                    |
| Geometric mean  | (ref)                                                        | 1.02x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 610 ms: 1.50x faster                                                     |
| async_tree_io              | 876 ms                                                       | 627 ms: 1.40x faster                                                     |
| deepcopy                   | 355 us                                                       | 254 us: 1.40x faster                                                     |
| async_tree_memoization     | 461 ms                                                       | 334 ms: 1.38x faster                                                     |
| async_tree_memoization_tg  | 414 ms                                                       | 308 ms: 1.35x faster                                                     |
| deepcopy_memo              | 39.1 us                                                      | 29.4 us: 1.33x faster                                                    |
| async_tree_none_tg         | 336 ms                                                       | 257 ms: 1.31x faster                                                     |
| async_tree_none            | 354 ms                                                       | 276 ms: 1.28x faster                                                     |
| go                         | 141 ms                                                       | 116 ms: 1.21x faster                                                     |
| deepcopy_reduce            | 3.11 us                                                      | 2.57 us: 1.21x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 568 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 549 ms: 1.16x faster                                                     |
| regex_effbot               | 3.08 ms                                                      | 2.73 ms: 1.13x faster                                                    |
| pylint                     | 317 ms                                                       | 282 ms: 1.12x faster                                                     |
| coroutines                 | 23.6 ms                                                      | 21.3 ms: 1.10x faster                                                    |
| regex_dna                  | 180 ms                                                       | 166 ms: 1.08x faster                                                     |
| telco                      | 7.82 ms                                                      | 7.25 ms: 1.08x faster                                                    |
| xml_etree_parse            | 136 ms                                                       | 127 ms: 1.07x faster                                                     |
| thrift                     | 778 us                                                       | 726 us: 1.07x faster                                                     |
| generators                 | 28.8 ms                                                      | 27.1 ms: 1.06x faster                                                    |
| pprint_safe_repr           | 738 ms                                                       | 699 ms: 1.06x faster                                                     |
| pathlib                    | 19.2 ms                                                      | 18.2 ms: 1.05x faster                                                    |
| coverage                   | 83.0 ms                                                      | 78.8 ms: 1.05x faster                                                    |
| pprint_pformat             | 1.50 sec                                                     | 1.42 sec: 1.05x faster                                                   |
| xml_etree_iterparse        | 94.9 ms                                                      | 90.4 ms: 1.05x faster                                                    |
| bpe_tokeniser              | 4.45 sec                                                     | 4.26 sec: 1.04x faster                                                   |
| async_generators           | 377 ms                                                       | 363 ms: 1.04x faster                                                     |
| hexiom                     | 5.99 ms                                                      | 5.78 ms: 1.04x faster                                                    |
| logging_simple             | 6.16 us                                                      | 5.99 us: 1.03x faster                                                    |
| meteor_contest             | 102 ms                                                       | 98.8 ms: 1.03x faster                                                    |
| docutils                   | 2.62 sec                                                     | 2.55 sec: 1.02x faster                                                   |
| scimark_sor                | 134 ms                                                       | 132 ms: 1.02x faster                                                     |
| logging_format             | 6.84 us                                                      | 6.70 us: 1.02x faster                                                    |
| spectral_norm              | 111 ms                                                       | 109 ms: 1.02x faster                                                     |
| pyflate                    | 449 ms                                                       | 440 ms: 1.02x faster                                                     |
| scimark_fft                | 349 ms                                                       | 343 ms: 1.02x faster                                                     |
| sympy_sum                  | 156 ms                                                       | 153 ms: 1.02x faster                                                     |
| regex_compile              | 132 ms                                                       | 130 ms: 1.02x faster                                                     |
| scimark_lu                 | 113 ms                                                       | 111 ms: 1.02x faster                                                     |
| xml_etree_generate         | 85.4 ms                                                      | 84.0 ms: 1.02x faster                                                    |
| sqlglot_normalize          | 106 ms                                                       | 104 ms: 1.02x faster                                                     |
| 2to3                       | 260 ms                                                       | 255 ms: 1.02x faster                                                     |
| scimark_monte_carlo        | 65.4 ms                                                      | 64.5 ms: 1.01x faster                                                    |
| json                       | 4.93 ms                                                      | 4.87 ms: 1.01x faster                                                    |
| xml_etree_process          | 59.3 ms                                                      | 58.7 ms: 1.01x faster                                                    |
| json_loads                 | 27.0 us                                                      | 26.7 us: 1.01x faster                                                    |
| sqlglot_optimize           | 52.7 ms                                                      | 52.2 ms: 1.01x faster                                                    |
| sympy_str                  | 275 ms                                                       | 273 ms: 1.01x faster                                                     |
| richards_super             | 51.6 ms                                                      | 51.3 ms: 1.01x faster                                                    |
| crypto_pyaes               | 67.9 ms                                                      | 67.4 ms: 1.01x faster                                                    |
| unpickle_pure_python       | 210 us                                                       | 209 us: 1.01x faster                                                     |
| pidigits                   | 217 ms                                                       | 217 ms: 1.00x slower                                                     |
| fannkuch                   | 370 ms                                                       | 371 ms: 1.00x slower                                                     |
| logging_silent             | 103 ns                                                       | 103 ns: 1.00x slower                                                     |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.01x slower                                                     |
| sympy_expand               | 457 ms                                                       | 461 ms: 1.01x slower                                                     |
| sympy_integrate            | 19.8 ms                                                      | 20.0 ms: 1.01x slower                                                    |
| genshi_text                | 21.5 ms                                                      | 21.8 ms: 1.01x slower                                                    |
| deltablue                  | 3.12 ms                                                      | 3.16 ms: 1.01x slower                                                    |
| python_startup_no_site     | 7.39 ms                                                      | 7.49 ms: 1.01x slower                                                    |
| dulwich_log                | 74.8 ms                                                      | 75.9 ms: 1.01x slower                                                    |
| typing_runtime_protocols   | 155 us                                                       | 158 us: 1.02x slower                                                     |
| genshi_xml                 | 48.8 ms                                                      | 49.8 ms: 1.02x slower                                                    |
| sqlglot_transpile          | 1.56 ms                                                      | 1.60 ms: 1.03x slower                                                    |
| sqlite_synth               | 2.21 us                                                      | 2.27 us: 1.03x slower                                                    |
| mako                       | 11.3 ms                                                      | 11.7 ms: 1.03x slower                                                    |
| regex_v8                   | 22.7 ms                                                      | 23.3 ms: 1.03x slower                                                    |
| tomli_loads                | 2.01 sec                                                     | 2.06 sec: 1.03x slower                                                   |
| sqlglot_parse              | 1.25 ms                                                      | 1.29 ms: 1.03x slower                                                    |
| raytrace                   | 253 ms                                                       | 261 ms: 1.03x slower                                                     |
| django_template            | 34.1 ms                                                      | 35.3 ms: 1.04x slower                                                    |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.89 ms: 1.04x slower                                                    |
| comprehensions             | 16.5 us                                                      | 17.2 us: 1.05x slower                                                    |
| mdp                        | 2.36 sec                                                     | 2.48 sec: 1.05x slower                                                   |
| pickle_pure_python         | 294 us                                                       | 310 us: 1.05x slower                                                     |
| json_dumps                 | 10.5 ms                                                      | 11.4 ms: 1.08x slower                                                    |
| nbody                      | 85.1 ms                                                      | 94.2 ms: 1.11x slower                                                    |
| bench_thread_pool          | 919 us                                                       | 1.02 ms: 1.11x slower                                                    |
| python_startup             | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                                    |
| gc_traversal               | 3.14 ms                                                      | 4.25 ms: 1.35x slower                                                    |
| create_gc_cycles           | 1.34 ms                                                      | 1.84 ms: 1.37x slower                                                    |
| bench_mp_pool              | 11.0 ms                                                      | 88.9 ms: 8.08x slower                                                    |
| Geometric mean             | (ref)                                                        | 1.01x faster                                                             |

Benchmark hidden because not significant (5): chaos, pycparser, nqueens, float, richards
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241213-3.14.0a2+-d6ea4f1/bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.035x faster

# HPT report

- Reliability score: 99.98% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.09x