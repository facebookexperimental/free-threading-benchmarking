# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: 3cedaed
- commit date: 2025-01-15
- overall geometric mean: 1.063x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-3cedaed |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 249 ms: 1.04x faster                                                  |
| docutils       | 2.62 sec                                                     | 2.54 sec: 1.03x faster                                                |
| Geometric mean | (ref)                                                        | 1.04x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-3cedaed |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 593 ms: 1.54x faster                                                  |
| async_tree_io              | 876 ms                                                       | 601 ms: 1.46x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 319 ms: 1.45x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 299 ms: 1.39x faster                                                  |
| async_tree_none            | 354 ms                                                       | 265 ms: 1.34x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 252 ms: 1.34x faster                                                  |
| async_generators           | 377 ms                                                       | 317 ms: 1.19x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 560 ms: 1.19x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 545 ms: 1.17x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 20.8 ms: 1.13x faster                                                 |
| asyncio_websockets         | 520 ms                                                       | 522 ms: 1.00x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.28x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-3cedaed |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 72.5 ms: 1.07x faster                                                 |
| pidigits       | 217 ms                                                       | 211 ms: 1.03x faster                                                  |
| nbody          | 85.1 ms                                                      | 89.3 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                        | 1.01x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-3cedaed |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.69 ms: 1.14x faster                                                 |
| regex_compile  | 132 ms                                                       | 126 ms: 1.05x faster                                                  |
| regex_dna      | 180 ms                                                       | 172 ms: 1.05x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 23.1 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                        | 1.05x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-3cedaed |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 89.7 ms: 1.06x faster                                                 |
| xml_etree_parse      | 136 ms                                                       | 129 ms: 1.06x faster                                                  |
| tomli_loads          | 2.01 sec                                                     | 1.92 sec: 1.04x faster                                                |
| xml_etree_generate   | 85.4 ms                                                      | 83.6 ms: 1.02x faster                                                 |
| xml_etree_process    | 59.3 ms                                                      | 58.4 ms: 1.02x faster                                                 |
| unpickle_pure_python | 210 us                                                       | 209 us: 1.01x faster                                                  |
| json_loads           | 27.0 us                                                      | 27.3 us: 1.01x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 304 us: 1.03x slower                                                  |
| json_dumps           | 10.5 ms                                                      | 11.2 ms: 1.07x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.01x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-3cedaed |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.42 ms: 1.00x slower                                                 |
| python_startup         | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.15x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-3cedaed |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 20.4 ms: 1.06x faster                                                 |
| genshi_xml      | 48.8 ms                                                      | 46.9 ms: 1.04x faster                                                 |
| django_template | 34.1 ms                                                      | 33.7 ms: 1.01x faster                                                 |
| mako            | 11.3 ms                                                      | 11.7 ms: 1.03x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.02x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-3cedaed |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 593 ms: 1.54x faster                                                  |
| async_tree_io              | 876 ms                                                       | 601 ms: 1.46x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 319 ms: 1.45x faster                                                  |
| deepcopy                   | 355 us                                                       | 253 us: 1.40x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 299 ms: 1.39x faster                                                  |
| async_tree_none            | 354 ms                                                       | 265 ms: 1.34x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 252 ms: 1.34x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 30.3 us: 1.29x faster                                                 |
| go                         | 141 ms                                                       | 114 ms: 1.24x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.54 us: 1.22x faster                                                 |
| async_generators           | 377 ms                                                       | 317 ms: 1.19x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 560 ms: 1.19x faster                                                  |
| scimark_sor                | 134 ms                                                       | 114 ms: 1.18x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 545 ms: 1.17x faster                                                  |
| spectral_norm              | 111 ms                                                       | 95.9 ms: 1.16x faster                                                 |
| regex_effbot               | 3.08 ms                                                      | 2.69 ms: 1.14x faster                                                 |
| pylint                     | 317 ms                                                       | 278 ms: 1.14x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 20.8 ms: 1.13x faster                                                 |
| scimark_fft                | 349 ms                                                       | 311 ms: 1.12x faster                                                  |
| pyflate                    | 449 ms                                                       | 402 ms: 1.11x faster                                                  |
| telco                      | 7.82 ms                                                      | 7.09 ms: 1.10x faster                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.33 ms: 1.09x faster                                                 |
| pprint_safe_repr           | 738 ms                                                       | 681 ms: 1.08x faster                                                  |
| richards_super             | 51.6 ms                                                      | 47.7 ms: 1.08x faster                                                 |
| generators                 | 28.8 ms                                                      | 26.6 ms: 1.08x faster                                                 |
| pprint_pformat             | 1.50 sec                                                     | 1.39 sec: 1.08x faster                                                |
| richards                   | 45.2 ms                                                      | 42.0 ms: 1.08x faster                                                 |
| pathlib                    | 19.2 ms                                                      | 17.9 ms: 1.07x faster                                                 |
| thrift                     | 778 us                                                       | 727 us: 1.07x faster                                                  |
| float                      | 77.5 ms                                                      | 72.5 ms: 1.07x faster                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.17 sec: 1.07x faster                                                |
| xml_etree_iterparse        | 94.9 ms                                                      | 89.7 ms: 1.06x faster                                                 |
| genshi_text                | 21.5 ms                                                      | 20.4 ms: 1.06x faster                                                 |
| xml_etree_parse            | 136 ms                                                       | 129 ms: 1.06x faster                                                  |
| regex_compile              | 132 ms                                                       | 126 ms: 1.05x faster                                                  |
| meteor_contest             | 102 ms                                                       | 96.9 ms: 1.05x faster                                                 |
| hexiom                     | 5.99 ms                                                      | 5.72 ms: 1.05x faster                                                 |
| regex_dna                  | 180 ms                                                       | 172 ms: 1.05x faster                                                  |
| tomli_loads                | 2.01 sec                                                     | 1.92 sec: 1.04x faster                                                |
| coverage                   | 83.0 ms                                                      | 79.5 ms: 1.04x faster                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 62.6 ms: 1.04x faster                                                 |
| sqlglot_normalize          | 106 ms                                                       | 101 ms: 1.04x faster                                                  |
| 2to3                       | 260 ms                                                       | 249 ms: 1.04x faster                                                  |
| genshi_xml                 | 48.8 ms                                                      | 46.9 ms: 1.04x faster                                                 |
| logging_simple             | 6.16 us                                                      | 5.97 us: 1.03x faster                                                 |
| logging_format             | 6.84 us                                                      | 6.63 us: 1.03x faster                                                 |
| sympy_sum                  | 156 ms                                                       | 151 ms: 1.03x faster                                                  |
| docutils                   | 2.62 sec                                                     | 2.54 sec: 1.03x faster                                                |
| pidigits                   | 217 ms                                                       | 211 ms: 1.03x faster                                                  |
| sympy_str                  | 275 ms                                                       | 267 ms: 1.03x faster                                                  |
| sqlglot_optimize           | 52.7 ms                                                      | 51.4 ms: 1.03x faster                                                 |
| nqueens                    | 78.6 ms                                                      | 76.9 ms: 1.02x faster                                                 |
| deltablue                  | 3.12 ms                                                      | 3.06 ms: 1.02x faster                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 83.6 ms: 1.02x faster                                                 |
| sqlite_synth               | 2.21 us                                                      | 2.16 us: 1.02x faster                                                 |
| sympy_expand               | 457 ms                                                       | 448 ms: 1.02x faster                                                  |
| pycparser                  | 1.12 sec                                                     | 1.10 sec: 1.02x faster                                                |
| xml_etree_process          | 59.3 ms                                                      | 58.4 ms: 1.02x faster                                                 |
| sympy_integrate            | 19.8 ms                                                      | 19.5 ms: 1.02x faster                                                 |
| sqlglot_transpile          | 1.56 ms                                                      | 1.54 ms: 1.01x faster                                                 |
| crypto_pyaes               | 67.9 ms                                                      | 66.9 ms: 1.01x faster                                                 |
| mdp                        | 2.36 sec                                                     | 2.33 sec: 1.01x faster                                                |
| django_template            | 34.1 ms                                                      | 33.7 ms: 1.01x faster                                                 |
| chaos                      | 57.3 ms                                                      | 56.7 ms: 1.01x faster                                                 |
| unpickle_pure_python       | 210 us                                                       | 209 us: 1.01x faster                                                  |
| sqlglot_parse              | 1.25 ms                                                      | 1.24 ms: 1.01x faster                                                 |
| fannkuch                   | 370 ms                                                       | 368 ms: 1.01x faster                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 7.42 ms: 1.00x slower                                                 |
| asyncio_websockets         | 520 ms                                                       | 522 ms: 1.00x slower                                                  |
| dulwich_log                | 74.8 ms                                                      | 75.2 ms: 1.00x slower                                                 |
| comprehensions             | 16.5 us                                                      | 16.6 us: 1.01x slower                                                 |
| json_loads                 | 27.0 us                                                      | 27.3 us: 1.01x slower                                                 |
| raytrace                   | 253 ms                                                       | 256 ms: 1.01x slower                                                  |
| regex_v8                   | 22.7 ms                                                      | 23.1 ms: 1.02x slower                                                 |
| mako                       | 11.3 ms                                                      | 11.7 ms: 1.03x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 304 us: 1.03x slower                                                  |
| logging_silent             | 103 ns                                                       | 107 ns: 1.05x slower                                                  |
| nbody                      | 85.1 ms                                                      | 89.3 ms: 1.05x slower                                                 |
| json_dumps                 | 10.5 ms                                                      | 11.2 ms: 1.07x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.03 ms: 1.12x slower                                                 |
| python_startup             | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 4.28 ms: 1.36x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.83 ms: 1.37x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 88.2 ms: 8.02x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.04x faster                                                          |

Benchmark hidden because not significant (3): json, scimark_lu, typing_runtime_protocols
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250115-3.14.0a4+-3cedaed/bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-3cedaed.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.063x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.10x