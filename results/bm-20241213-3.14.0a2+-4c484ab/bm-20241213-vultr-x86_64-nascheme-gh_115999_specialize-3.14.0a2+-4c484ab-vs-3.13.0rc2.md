# Results vs. 3.13.0rc2

- fork: nascheme
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: 4c484ab
- commit date: 2024-12-13
- overall geometric mean: 1.040x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-4c484ab |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 256 ms: 1.01x faster                                                     |
| docutils       | 2.62 sec                                                     | 2.54 sec: 1.03x faster                                                   |
| Geometric mean | (ref)                                                        | 1.02x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-4c484ab |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 619 ms: 1.48x faster                                                     |
| async_tree_io              | 876 ms                                                       | 627 ms: 1.40x faster                                                     |
| async_tree_memoization     | 461 ms                                                       | 337 ms: 1.37x faster                                                     |
| async_tree_memoization_tg  | 414 ms                                                       | 308 ms: 1.35x faster                                                     |
| async_tree_none_tg         | 336 ms                                                       | 256 ms: 1.31x faster                                                     |
| async_tree_none            | 354 ms                                                       | 281 ms: 1.26x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 572 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 550 ms: 1.16x faster                                                     |
| coroutines                 | 23.6 ms                                                      | 21.9 ms: 1.07x faster                                                    |
| async_generators           | 377 ms                                                       | 354 ms: 1.07x faster                                                     |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.01x slower                                                     |
| Geometric mean             | (ref)                                                        | 1.23x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-4c484ab |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 216 ms: 1.00x faster                                                     |
| nbody          | 85.1 ms                                                      | 89.2 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                        | 1.01x slower                                                             |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-4c484ab |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.74 ms: 1.12x faster                                                    |
| regex_dna      | 180 ms                                                       | 166 ms: 1.08x faster                                                     |
| regex_compile  | 132 ms                                                       | 127 ms: 1.04x faster                                                     |
| regex_v8       | 22.7 ms                                                      | 23.5 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                        | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-4c484ab |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 129 ms: 1.06x faster                                                     |
| xml_etree_iterparse  | 94.9 ms                                                      | 91.3 ms: 1.04x faster                                                    |
| json_loads           | 27.0 us                                                      | 26.1 us: 1.03x faster                                                    |
| xml_etree_generate   | 85.4 ms                                                      | 84.2 ms: 1.01x faster                                                    |
| tomli_loads          | 2.01 sec                                                     | 1.98 sec: 1.01x faster                                                   |
| xml_etree_process    | 59.3 ms                                                      | 58.5 ms: 1.01x faster                                                    |
| unpickle_pure_python | 210 us                                                       | 213 us: 1.02x slower                                                     |
| pickle_pure_python   | 294 us                                                       | 318 us: 1.08x slower                                                     |
| json_dumps           | 10.5 ms                                                      | 11.4 ms: 1.08x slower                                                    |
| Geometric mean       | (ref)                                                        | 1.00x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-4c484ab |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.52 ms: 1.02x slower                                                    |
| python_startup         | 11.0 ms                                                      | 14.7 ms: 1.34x slower                                                    |
| Geometric mean         | (ref)                                                        | 1.17x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-4c484ab |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| django_template | 34.1 ms                                                      | 35.0 ms: 1.03x slower                                                    |
| genshi_text     | 21.5 ms                                                      | 22.2 ms: 1.03x slower                                                    |
| mako            | 11.3 ms                                                      | 11.8 ms: 1.04x slower                                                    |
| genshi_xml      | 48.8 ms                                                      | 50.6 ms: 1.04x slower                                                    |
| Geometric mean  | (ref)                                                        | 1.03x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-4c484ab |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 619 ms: 1.48x faster                                                     |
| async_tree_io              | 876 ms                                                       | 627 ms: 1.40x faster                                                     |
| deepcopy                   | 355 us                                                       | 256 us: 1.39x faster                                                     |
| async_tree_memoization     | 461 ms                                                       | 337 ms: 1.37x faster                                                     |
| async_tree_memoization_tg  | 414 ms                                                       | 308 ms: 1.35x faster                                                     |
| async_tree_none_tg         | 336 ms                                                       | 256 ms: 1.31x faster                                                     |
| deepcopy_memo              | 39.1 us                                                      | 30.0 us: 1.30x faster                                                    |
| async_tree_none            | 354 ms                                                       | 281 ms: 1.26x faster                                                     |
| deepcopy_reduce            | 3.11 us                                                      | 2.59 us: 1.20x faster                                                    |
| go                         | 141 ms                                                       | 119 ms: 1.18x faster                                                     |
| spectral_norm              | 111 ms                                                       | 94.8 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 572 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 550 ms: 1.16x faster                                                     |
| scimark_fft                | 349 ms                                                       | 305 ms: 1.15x faster                                                     |
| regex_effbot               | 3.08 ms                                                      | 2.74 ms: 1.12x faster                                                    |
| pylint                     | 317 ms                                                       | 282 ms: 1.12x faster                                                     |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.20 ms: 1.12x faster                                                    |
| regex_dna                  | 180 ms                                                       | 166 ms: 1.08x faster                                                     |
| telco                      | 7.82 ms                                                      | 7.27 ms: 1.08x faster                                                    |
| coroutines                 | 23.6 ms                                                      | 21.9 ms: 1.07x faster                                                    |
| thrift                     | 778 us                                                       | 729 us: 1.07x faster                                                     |
| async_generators           | 377 ms                                                       | 354 ms: 1.07x faster                                                     |
| pathlib                    | 19.2 ms                                                      | 18.1 ms: 1.06x faster                                                    |
| generators                 | 28.8 ms                                                      | 27.1 ms: 1.06x faster                                                    |
| xml_etree_parse            | 136 ms                                                       | 129 ms: 1.06x faster                                                     |
| pyflate                    | 449 ms                                                       | 425 ms: 1.06x faster                                                     |
| coverage                   | 83.0 ms                                                      | 78.6 ms: 1.06x faster                                                    |
| scimark_sor                | 134 ms                                                       | 129 ms: 1.04x faster                                                     |
| bpe_tokeniser              | 4.45 sec                                                     | 4.26 sec: 1.04x faster                                                   |
| scimark_monte_carlo        | 65.4 ms                                                      | 62.7 ms: 1.04x faster                                                    |
| scimark_lu                 | 113 ms                                                       | 108 ms: 1.04x faster                                                     |
| xml_etree_iterparse        | 94.9 ms                                                      | 91.3 ms: 1.04x faster                                                    |
| regex_compile              | 132 ms                                                       | 127 ms: 1.04x faster                                                     |
| json                       | 4.93 ms                                                      | 4.76 ms: 1.04x faster                                                    |
| json_loads                 | 27.0 us                                                      | 26.1 us: 1.03x faster                                                    |
| docutils                   | 2.62 sec                                                     | 2.54 sec: 1.03x faster                                                   |
| meteor_contest             | 102 ms                                                       | 98.9 ms: 1.03x faster                                                    |
| sympy_sum                  | 156 ms                                                       | 152 ms: 1.03x faster                                                     |
| pprint_safe_repr           | 738 ms                                                       | 721 ms: 1.02x faster                                                     |
| crypto_pyaes               | 67.9 ms                                                      | 66.7 ms: 1.02x faster                                                    |
| sqlglot_normalize          | 106 ms                                                       | 104 ms: 1.02x faster                                                     |
| hexiom                     | 5.99 ms                                                      | 5.90 ms: 1.01x faster                                                    |
| xml_etree_generate         | 85.4 ms                                                      | 84.2 ms: 1.01x faster                                                    |
| tomli_loads                | 2.01 sec                                                     | 1.98 sec: 1.01x faster                                                   |
| pprint_pformat             | 1.50 sec                                                     | 1.48 sec: 1.01x faster                                                   |
| xml_etree_process          | 59.3 ms                                                      | 58.5 ms: 1.01x faster                                                    |
| 2to3                       | 260 ms                                                       | 256 ms: 1.01x faster                                                     |
| nqueens                    | 78.6 ms                                                      | 77.9 ms: 1.01x faster                                                    |
| sqlglot_optimize           | 52.7 ms                                                      | 52.3 ms: 1.01x faster                                                    |
| sympy_str                  | 275 ms                                                       | 273 ms: 1.01x faster                                                     |
| pidigits                   | 217 ms                                                       | 216 ms: 1.00x faster                                                     |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.01x slower                                                     |
| fannkuch                   | 370 ms                                                       | 372 ms: 1.01x slower                                                     |
| pycparser                  | 1.12 sec                                                     | 1.12 sec: 1.01x slower                                                   |
| dulwich_log                | 74.8 ms                                                      | 75.5 ms: 1.01x slower                                                    |
| sqlglot_transpile          | 1.56 ms                                                      | 1.58 ms: 1.01x slower                                                    |
| sqlglot_parse              | 1.25 ms                                                      | 1.26 ms: 1.01x slower                                                    |
| unpickle_pure_python       | 210 us                                                       | 213 us: 1.02x slower                                                     |
| python_startup_no_site     | 7.39 ms                                                      | 7.52 ms: 1.02x slower                                                    |
| typing_runtime_protocols   | 155 us                                                       | 158 us: 1.02x slower                                                     |
| deltablue                  | 3.12 ms                                                      | 3.20 ms: 1.02x slower                                                    |
| django_template            | 34.1 ms                                                      | 35.0 ms: 1.03x slower                                                    |
| genshi_text                | 21.5 ms                                                      | 22.2 ms: 1.03x slower                                                    |
| raytrace                   | 253 ms                                                       | 260 ms: 1.03x slower                                                     |
| regex_v8                   | 22.7 ms                                                      | 23.5 ms: 1.04x slower                                                    |
| mako                       | 11.3 ms                                                      | 11.8 ms: 1.04x slower                                                    |
| genshi_xml                 | 48.8 ms                                                      | 50.6 ms: 1.04x slower                                                    |
| logging_silent             | 103 ns                                                       | 107 ns: 1.04x slower                                                     |
| comprehensions             | 16.5 us                                                      | 17.2 us: 1.05x slower                                                    |
| nbody                      | 85.1 ms                                                      | 89.2 ms: 1.05x slower                                                    |
| mdp                        | 2.36 sec                                                     | 2.48 sec: 1.05x slower                                                   |
| pickle_pure_python         | 294 us                                                       | 318 us: 1.08x slower                                                     |
| json_dumps                 | 10.5 ms                                                      | 11.4 ms: 1.08x slower                                                    |
| bench_thread_pool          | 919 us                                                       | 1.03 ms: 1.12x slower                                                    |
| gc_traversal               | 3.14 ms                                                      | 4.04 ms: 1.28x slower                                                    |
| python_startup             | 11.0 ms                                                      | 14.7 ms: 1.34x slower                                                    |
| create_gc_cycles           | 1.34 ms                                                      | 1.85 ms: 1.38x slower                                                    |
| bench_mp_pool              | 11.0 ms                                                      | 89.3 ms: 8.12x slower                                                    |
| Geometric mean             | (ref)                                                        | 1.01x faster                                                             |

Benchmark hidden because not significant (9): float, richards_super, sympy_integrate, richards, logging_format, sqlite_synth, chaos, sympy_expand, logging_simple
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241213-3.14.0a2+-4c484ab/bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-4c484ab.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.040x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.09x