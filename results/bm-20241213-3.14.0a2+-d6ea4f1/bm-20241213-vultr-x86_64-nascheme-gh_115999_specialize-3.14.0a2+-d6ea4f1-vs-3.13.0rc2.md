# Results vs. 3.13.0rc2

- fork: nascheme
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: d6ea4f1
- commit date: 2024-12-13
- overall geometric mean: 1.044x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 255 ms: 1.02x faster                                                     |
| docutils       | 2.62 sec                                                     | 2.55 sec: 1.03x faster                                                   |
| Geometric mean | (ref)                                                        | 1.02x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 610 ms: 1.50x faster                                                     |
| async_tree_io              | 876 ms                                                       | 618 ms: 1.42x faster                                                     |
| async_tree_memoization     | 461 ms                                                       | 331 ms: 1.39x faster                                                     |
| async_tree_memoization_tg  | 414 ms                                                       | 305 ms: 1.36x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 498 ms: 1.34x faster                                                     |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 481 ms: 1.33x faster                                                     |
| async_tree_none_tg         | 336 ms                                                       | 255 ms: 1.32x faster                                                     |
| async_tree_none            | 354 ms                                                       | 275 ms: 1.29x faster                                                     |
| async_generators           | 377 ms                                                       | 362 ms: 1.04x faster                                                     |
| coroutines                 | 23.6 ms                                                      | 23.2 ms: 1.02x faster                                                    |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.01x slower                                                     |
| Geometric mean             | (ref)                                                        | 1.26x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 185 ms: 1.17x faster                                                     |
| float          | 77.5 ms                                                      | 76.1 ms: 1.02x faster                                                    |
| nbody          | 85.1 ms                                                      | 91.8 ms: 1.08x slower                                                    |
| Geometric mean | (ref)                                                        | 1.03x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.72 ms: 1.13x faster                                                    |
| regex_dna      | 180 ms                                                       | 174 ms: 1.04x faster                                                     |
| regex_compile  | 132 ms                                                       | 129 ms: 1.03x faster                                                     |
| regex_v8       | 22.7 ms                                                      | 24.7 ms: 1.09x slower                                                    |
| Geometric mean | (ref)                                                        | 1.03x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 127 ms: 1.07x faster                                                     |
| xml_etree_iterparse  | 94.9 ms                                                      | 90.5 ms: 1.05x faster                                                    |
| json_loads           | 27.0 us                                                      | 26.1 us: 1.04x faster                                                    |
| xml_etree_generate   | 85.4 ms                                                      | 83.7 ms: 1.02x faster                                                    |
| xml_etree_process    | 59.3 ms                                                      | 58.4 ms: 1.02x faster                                                    |
| unpickle_pure_python | 210 us                                                       | 212 us: 1.01x slower                                                     |
| tomli_loads          | 2.01 sec                                                     | 2.06 sec: 1.02x slower                                                   |
| pickle_pure_python   | 294 us                                                       | 310 us: 1.05x slower                                                     |
| json_dumps           | 10.5 ms                                                      | 11.4 ms: 1.08x slower                                                    |
| Geometric mean       | (ref)                                                        | 1.00x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.48 ms: 1.01x slower                                                    |
| python_startup         | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                                    |
| Geometric mean         | (ref)                                                        | 1.16x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 21.4 ms: 1.01x faster                                                    |
| genshi_xml      | 48.8 ms                                                      | 49.7 ms: 1.02x slower                                                    |
| django_template | 34.1 ms                                                      | 35.0 ms: 1.03x slower                                                    |
| mako            | 11.3 ms                                                      | 11.7 ms: 1.03x slower                                                    |
| Geometric mean  | (ref)                                                        | 1.02x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 610 ms: 1.50x faster                                                     |
| async_tree_io              | 876 ms                                                       | 618 ms: 1.42x faster                                                     |
| deepcopy                   | 355 us                                                       | 255 us: 1.40x faster                                                     |
| async_tree_memoization     | 461 ms                                                       | 331 ms: 1.39x faster                                                     |
| async_tree_memoization_tg  | 414 ms                                                       | 305 ms: 1.36x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 498 ms: 1.34x faster                                                     |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 481 ms: 1.33x faster                                                     |
| async_tree_none_tg         | 336 ms                                                       | 255 ms: 1.32x faster                                                     |
| deepcopy_memo              | 39.1 us                                                      | 29.7 us: 1.31x faster                                                    |
| async_tree_none            | 354 ms                                                       | 275 ms: 1.29x faster                                                     |
| deepcopy_reduce            | 3.11 us                                                      | 2.56 us: 1.22x faster                                                    |
| go                         | 141 ms                                                       | 119 ms: 1.19x faster                                                     |
| pidigits                   | 217 ms                                                       | 185 ms: 1.17x faster                                                     |
| regex_effbot               | 3.08 ms                                                      | 2.72 ms: 1.13x faster                                                    |
| pylint                     | 317 ms                                                       | 282 ms: 1.12x faster                                                     |
| telco                      | 7.82 ms                                                      | 7.11 ms: 1.10x faster                                                    |
| xml_etree_parse            | 136 ms                                                       | 127 ms: 1.07x faster                                                     |
| thrift                     | 778 us                                                       | 728 us: 1.07x faster                                                     |
| generators                 | 28.8 ms                                                      | 27.0 ms: 1.07x faster                                                    |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.42 ms: 1.07x faster                                                    |
| scimark_fft                | 349 ms                                                       | 330 ms: 1.06x faster                                                     |
| xml_etree_iterparse        | 94.9 ms                                                      | 90.5 ms: 1.05x faster                                                    |
| pprint_safe_repr           | 738 ms                                                       | 703 ms: 1.05x faster                                                     |
| pathlib                    | 19.2 ms                                                      | 18.3 ms: 1.05x faster                                                    |
| logging_simple             | 6.16 us                                                      | 5.91 us: 1.04x faster                                                    |
| async_generators           | 377 ms                                                       | 362 ms: 1.04x faster                                                     |
| pprint_pformat             | 1.50 sec                                                     | 1.44 sec: 1.04x faster                                                   |
| hexiom                     | 5.99 ms                                                      | 5.77 ms: 1.04x faster                                                    |
| regex_dna                  | 180 ms                                                       | 174 ms: 1.04x faster                                                     |
| logging_format             | 6.84 us                                                      | 6.61 us: 1.04x faster                                                    |
| json_loads                 | 27.0 us                                                      | 26.1 us: 1.04x faster                                                    |
| crypto_pyaes               | 67.9 ms                                                      | 65.6 ms: 1.04x faster                                                    |
| coverage                   | 83.0 ms                                                      | 80.3 ms: 1.03x faster                                                    |
| pyflate                    | 449 ms                                                       | 435 ms: 1.03x faster                                                     |
| bpe_tokeniser              | 4.45 sec                                                     | 4.31 sec: 1.03x faster                                                   |
| spectral_norm              | 111 ms                                                       | 108 ms: 1.03x faster                                                     |
| json                       | 4.93 ms                                                      | 4.79 ms: 1.03x faster                                                    |
| regex_compile              | 132 ms                                                       | 129 ms: 1.03x faster                                                     |
| docutils                   | 2.62 sec                                                     | 2.55 sec: 1.03x faster                                                   |
| scimark_sor                | 134 ms                                                       | 131 ms: 1.03x faster                                                     |
| scimark_monte_carlo        | 65.4 ms                                                      | 63.7 ms: 1.03x faster                                                    |
| sympy_sum                  | 156 ms                                                       | 152 ms: 1.02x faster                                                     |
| scimark_lu                 | 113 ms                                                       | 110 ms: 1.02x faster                                                     |
| xml_etree_generate         | 85.4 ms                                                      | 83.7 ms: 1.02x faster                                                    |
| sympy_str                  | 275 ms                                                       | 269 ms: 1.02x faster                                                     |
| sqlglot_normalize          | 106 ms                                                       | 104 ms: 1.02x faster                                                     |
| float                      | 77.5 ms                                                      | 76.1 ms: 1.02x faster                                                    |
| 2to3                       | 260 ms                                                       | 255 ms: 1.02x faster                                                     |
| coroutines                 | 23.6 ms                                                      | 23.2 ms: 1.02x faster                                                    |
| meteor_contest             | 102 ms                                                       | 100 ms: 1.02x faster                                                     |
| xml_etree_process          | 59.3 ms                                                      | 58.4 ms: 1.02x faster                                                    |
| richards_super             | 51.6 ms                                                      | 50.9 ms: 1.01x faster                                                    |
| nqueens                    | 78.6 ms                                                      | 77.7 ms: 1.01x faster                                                    |
| richards                   | 45.2 ms                                                      | 44.7 ms: 1.01x faster                                                    |
| genshi_text                | 21.5 ms                                                      | 21.4 ms: 1.01x faster                                                    |
| sqlglot_optimize           | 52.7 ms                                                      | 52.4 ms: 1.01x faster                                                    |
| sympy_integrate            | 19.8 ms                                                      | 19.7 ms: 1.00x faster                                                    |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.01x slower                                                     |
| dulwich_log                | 74.8 ms                                                      | 75.3 ms: 1.01x slower                                                    |
| sqlite_synth               | 2.21 us                                                      | 2.23 us: 1.01x slower                                                    |
| chaos                      | 57.3 ms                                                      | 57.8 ms: 1.01x slower                                                    |
| unpickle_pure_python       | 210 us                                                       | 212 us: 1.01x slower                                                     |
| deltablue                  | 3.12 ms                                                      | 3.15 ms: 1.01x slower                                                    |
| sqlglot_transpile          | 1.56 ms                                                      | 1.58 ms: 1.01x slower                                                    |
| sqlglot_parse              | 1.25 ms                                                      | 1.26 ms: 1.01x slower                                                    |
| python_startup_no_site     | 7.39 ms                                                      | 7.48 ms: 1.01x slower                                                    |
| pycparser                  | 1.12 sec                                                     | 1.13 sec: 1.01x slower                                                   |
| fannkuch                   | 370 ms                                                       | 376 ms: 1.02x slower                                                     |
| genshi_xml                 | 48.8 ms                                                      | 49.7 ms: 1.02x slower                                                    |
| comprehensions             | 16.5 us                                                      | 16.8 us: 1.02x slower                                                    |
| tomli_loads                | 2.01 sec                                                     | 2.06 sec: 1.02x slower                                                   |
| django_template            | 34.1 ms                                                      | 35.0 ms: 1.03x slower                                                    |
| logging_silent             | 103 ns                                                       | 105 ns: 1.03x slower                                                     |
| raytrace                   | 253 ms                                                       | 260 ms: 1.03x slower                                                     |
| mako                       | 11.3 ms                                                      | 11.7 ms: 1.03x slower                                                    |
| mdp                        | 2.36 sec                                                     | 2.47 sec: 1.05x slower                                                   |
| pickle_pure_python         | 294 us                                                       | 310 us: 1.05x slower                                                     |
| nbody                      | 85.1 ms                                                      | 91.8 ms: 1.08x slower                                                    |
| json_dumps                 | 10.5 ms                                                      | 11.4 ms: 1.08x slower                                                    |
| regex_v8                   | 22.7 ms                                                      | 24.7 ms: 1.09x slower                                                    |
| bench_thread_pool          | 919 us                                                       | 1.03 ms: 1.12x slower                                                    |
| python_startup             | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                                    |
| gc_traversal               | 3.14 ms                                                      | 4.18 ms: 1.33x slower                                                    |
| create_gc_cycles           | 1.34 ms                                                      | 1.84 ms: 1.38x slower                                                    |
| bench_mp_pool              | 11.0 ms                                                      | 88.7 ms: 8.06x slower                                                    |
| Geometric mean             | (ref)                                                        | 1.02x faster                                                             |

Benchmark hidden because not significant (2): sympy_expand, typing_runtime_protocols
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241213-3.14.0a2+-d6ea4f1/bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.044x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.09x