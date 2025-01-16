# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: 73aa5a2
- commit date: 2025-01-15
- overall geometric mean: 1.068x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-73aa5a2 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 250 ms: 1.04x faster                                                  |
| docutils       | 2.62 sec                                                     | 2.54 sec: 1.03x faster                                                |
| Geometric mean | (ref)                                                        | 1.03x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-73aa5a2 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 595 ms: 1.54x faster                                                  |
| async_tree_io              | 876 ms                                                       | 601 ms: 1.46x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 319 ms: 1.45x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 296 ms: 1.40x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 249 ms: 1.35x faster                                                  |
| async_tree_none            | 354 ms                                                       | 263 ms: 1.35x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 525 ms: 1.27x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 506 ms: 1.26x faster                                                  |
| async_generators           | 377 ms                                                       | 320 ms: 1.18x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 21.7 ms: 1.08x faster                                                 |
| asyncio_websockets         | 520 ms                                                       | 522 ms: 1.00x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.29x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-73aa5a2 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 70.9 ms: 1.09x faster                                                 |
| pidigits       | 217 ms                                                       | 207 ms: 1.05x faster                                                  |
| nbody          | 85.1 ms                                                      | 82.2 ms: 1.04x faster                                                 |
| Geometric mean | (ref)                                                        | 1.06x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-73aa5a2 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.62 ms: 1.18x faster                                                 |
| regex_dna      | 180 ms                                                       | 169 ms: 1.07x faster                                                  |
| regex_compile  | 132 ms                                                       | 124 ms: 1.06x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 22.9 ms: 1.01x slower                                                 |
| Geometric mean | (ref)                                                        | 1.07x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-73aa5a2 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                     | 1.86 sec: 1.08x faster                                                |
| xml_etree_iterparse  | 94.9 ms                                                      | 89.5 ms: 1.06x faster                                                 |
| xml_etree_parse      | 136 ms                                                       | 129 ms: 1.05x faster                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 82.4 ms: 1.04x faster                                                 |
| unpickle_pure_python | 210 us                                                       | 204 us: 1.03x faster                                                  |
| xml_etree_process    | 59.3 ms                                                      | 57.8 ms: 1.03x faster                                                 |
| json_loads           | 27.0 us                                                      | 27.7 us: 1.02x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 305 us: 1.04x slower                                                  |
| json_dumps           | 10.5 ms                                                      | 11.5 ms: 1.09x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.01x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-73aa5a2 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.43 ms: 1.00x slower                                                 |
| python_startup         | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.15x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-73aa5a2 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text    | 21.5 ms                                                      | 20.4 ms: 1.06x faster                                                 |
| genshi_xml     | 48.8 ms                                                      | 46.9 ms: 1.04x faster                                                 |
| mako           | 11.3 ms                                                      | 11.6 ms: 1.03x slower                                                 |
| Geometric mean | (ref)                                                        | 1.02x faster                                                          |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-73aa5a2 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 595 ms: 1.54x faster                                                  |
| async_tree_io              | 876 ms                                                       | 601 ms: 1.46x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 319 ms: 1.45x faster                                                  |
| deepcopy                   | 355 us                                                       | 253 us: 1.41x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 296 ms: 1.40x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 249 ms: 1.35x faster                                                  |
| async_tree_none            | 354 ms                                                       | 263 ms: 1.35x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 29.5 us: 1.33x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 525 ms: 1.27x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 506 ms: 1.26x faster                                                  |
| go                         | 141 ms                                                       | 112 ms: 1.25x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.55 us: 1.22x faster                                                 |
| async_generators           | 377 ms                                                       | 320 ms: 1.18x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.62 ms: 1.18x faster                                                 |
| scimark_sor                | 134 ms                                                       | 114 ms: 1.18x faster                                                  |
| pylint                     | 317 ms                                                       | 278 ms: 1.14x faster                                                  |
| spectral_norm              | 111 ms                                                       | 97.5 ms: 1.14x faster                                                 |
| pyflate                    | 449 ms                                                       | 400 ms: 1.12x faster                                                  |
| scimark_fft                | 349 ms                                                       | 313 ms: 1.12x faster                                                  |
| telco                      | 7.82 ms                                                      | 7.11 ms: 1.10x faster                                                 |
| richards_super             | 51.6 ms                                                      | 47.1 ms: 1.10x faster                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.30 ms: 1.09x faster                                                 |
| richards                   | 45.2 ms                                                      | 41.4 ms: 1.09x faster                                                 |
| float                      | 77.5 ms                                                      | 70.9 ms: 1.09x faster                                                 |
| pprint_safe_repr           | 738 ms                                                       | 678 ms: 1.09x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 21.7 ms: 1.08x faster                                                 |
| pprint_pformat             | 1.50 sec                                                     | 1.38 sec: 1.08x faster                                                |
| tomli_loads                | 2.01 sec                                                     | 1.86 sec: 1.08x faster                                                |
| regex_dna                  | 180 ms                                                       | 169 ms: 1.07x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.18 sec: 1.06x faster                                                |
| regex_compile              | 132 ms                                                       | 124 ms: 1.06x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 18.1 ms: 1.06x faster                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 89.5 ms: 1.06x faster                                                 |
| thrift                     | 778 us                                                       | 735 us: 1.06x faster                                                  |
| genshi_text                | 21.5 ms                                                      | 20.4 ms: 1.06x faster                                                 |
| generators                 | 28.8 ms                                                      | 27.2 ms: 1.06x faster                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 61.8 ms: 1.06x faster                                                 |
| xml_etree_parse            | 136 ms                                                       | 129 ms: 1.05x faster                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 64.8 ms: 1.05x faster                                                 |
| hexiom                     | 5.99 ms                                                      | 5.72 ms: 1.05x faster                                                 |
| pidigits                   | 217 ms                                                       | 207 ms: 1.05x faster                                                  |
| coverage                   | 83.0 ms                                                      | 79.4 ms: 1.05x faster                                                 |
| meteor_contest             | 102 ms                                                       | 97.5 ms: 1.04x faster                                                 |
| sqlglot_normalize          | 106 ms                                                       | 101 ms: 1.04x faster                                                  |
| logging_simple             | 6.16 us                                                      | 5.92 us: 1.04x faster                                                 |
| 2to3                       | 260 ms                                                       | 250 ms: 1.04x faster                                                  |
| genshi_xml                 | 48.8 ms                                                      | 46.9 ms: 1.04x faster                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 82.4 ms: 1.04x faster                                                 |
| nbody                      | 85.1 ms                                                      | 82.2 ms: 1.04x faster                                                 |
| logging_format             | 6.84 us                                                      | 6.63 us: 1.03x faster                                                 |
| docutils                   | 2.62 sec                                                     | 2.54 sec: 1.03x faster                                                |
| unpickle_pure_python       | 210 us                                                       | 204 us: 1.03x faster                                                  |
| sqlglot_optimize           | 52.7 ms                                                      | 51.4 ms: 1.03x faster                                                 |
| xml_etree_process          | 59.3 ms                                                      | 57.8 ms: 1.03x faster                                                 |
| mdp                        | 2.36 sec                                                     | 2.30 sec: 1.02x faster                                                |
| scimark_lu                 | 113 ms                                                       | 110 ms: 1.02x faster                                                  |
| sympy_sum                  | 156 ms                                                       | 152 ms: 1.02x faster                                                  |
| sqlglot_transpile          | 1.56 ms                                                      | 1.53 ms: 1.02x faster                                                 |
| pycparser                  | 1.12 sec                                                     | 1.09 sec: 1.02x faster                                                |
| nqueens                    | 78.6 ms                                                      | 77.0 ms: 1.02x faster                                                 |
| sympy_str                  | 275 ms                                                       | 269 ms: 1.02x faster                                                  |
| sqlglot_parse              | 1.25 ms                                                      | 1.23 ms: 1.02x faster                                                 |
| chaos                      | 57.3 ms                                                      | 56.4 ms: 1.02x faster                                                 |
| sympy_expand               | 457 ms                                                       | 450 ms: 1.01x faster                                                  |
| sympy_integrate            | 19.8 ms                                                      | 19.6 ms: 1.01x faster                                                 |
| deltablue                  | 3.12 ms                                                      | 3.10 ms: 1.01x faster                                                 |
| raytrace                   | 253 ms                                                       | 253 ms: 1.00x slower                                                  |
| asyncio_websockets         | 520 ms                                                       | 522 ms: 1.00x slower                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 7.43 ms: 1.00x slower                                                 |
| dulwich_log                | 74.8 ms                                                      | 75.2 ms: 1.00x slower                                                 |
| regex_v8                   | 22.7 ms                                                      | 22.9 ms: 1.01x slower                                                 |
| fannkuch                   | 370 ms                                                       | 376 ms: 1.02x slower                                                  |
| json_loads                 | 27.0 us                                                      | 27.7 us: 1.02x slower                                                 |
| mako                       | 11.3 ms                                                      | 11.6 ms: 1.03x slower                                                 |
| logging_silent             | 103 ns                                                       | 106 ns: 1.03x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 305 us: 1.04x slower                                                  |
| json_dumps                 | 10.5 ms                                                      | 11.5 ms: 1.09x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.03 ms: 1.12x slower                                                 |
| python_startup             | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 4.28 ms: 1.36x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.84 ms: 1.38x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 88.1 ms: 8.01x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.04x faster                                                          |

Benchmark hidden because not significant (5): sqlite_synth, comprehensions, django_template, typing_runtime_protocols, json
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250115-3.14.0a4+-73aa5a2/bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-73aa5a2.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.068x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.10x