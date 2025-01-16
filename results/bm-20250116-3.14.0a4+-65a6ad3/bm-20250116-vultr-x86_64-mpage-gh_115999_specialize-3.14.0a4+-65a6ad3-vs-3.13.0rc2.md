# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: 65a6ad3
- commit date: 2025-01-16
- overall geometric mean: 1.050x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 254 ms: 1.02x faster                                                  |
| docutils       | 2.62 sec                                                     | 2.58 sec: 1.01x faster                                                |
| Geometric mean | (ref)                                                        | 1.02x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 615 ms: 1.48x faster                                                  |
| async_tree_io              | 876 ms                                                       | 608 ms: 1.44x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 329 ms: 1.40x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 304 ms: 1.36x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 473 ms: 1.35x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 495 ms: 1.35x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 255 ms: 1.32x faster                                                  |
| async_tree_none            | 354 ms                                                       | 272 ms: 1.30x faster                                                  |
| async_generators           | 377 ms                                                       | 325 ms: 1.16x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 22.5 ms: 1.05x faster                                                 |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.01x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.28x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 191 ms: 1.13x faster                                                  |
| float          | 77.5 ms                                                      | 70.8 ms: 1.09x faster                                                 |
| nbody          | 85.1 ms                                                      | 87.3 ms: 1.03x slower                                                 |
| Geometric mean | (ref)                                                        | 1.07x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.71 ms: 1.14x faster                                                 |
| regex_compile  | 132 ms                                                       | 127 ms: 1.04x faster                                                  |
| regex_dna      | 180 ms                                                       | 177 ms: 1.02x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 23.4 ms: 1.03x slower                                                 |
| Geometric mean | (ref)                                                        | 1.04x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 128 ms: 1.07x faster                                                  |
| tomli_loads          | 2.01 sec                                                     | 1.90 sec: 1.05x faster                                                |
| xml_etree_iterparse  | 94.9 ms                                                      | 90.4 ms: 1.05x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 83.8 ms: 1.02x faster                                                 |
| json_loads           | 27.0 us                                                      | 27.6 us: 1.02x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 215 us: 1.02x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 313 us: 1.06x slower                                                  |
| json_dumps           | 10.5 ms                                                      | 11.5 ms: 1.09x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.00x slower                                                          |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.48 ms: 1.01x slower                                                 |
| python_startup         | 11.0 ms                                                      | 14.7 ms: 1.34x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.16x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 21.3 ms: 1.01x faster                                                 |
| mako            | 11.3 ms                                                      | 11.7 ms: 1.03x slower                                                 |
| django_template | 34.1 ms                                                      | 36.0 ms: 1.05x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.02x slower                                                          |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 615 ms: 1.48x faster                                                  |
| async_tree_io              | 876 ms                                                       | 608 ms: 1.44x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 329 ms: 1.40x faster                                                  |
| deepcopy                   | 355 us                                                       | 260 us: 1.37x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 304 ms: 1.36x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 473 ms: 1.35x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 495 ms: 1.35x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 255 ms: 1.32x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 29.9 us: 1.31x faster                                                 |
| async_tree_none            | 354 ms                                                       | 272 ms: 1.30x faster                                                  |
| go                         | 141 ms                                                       | 115 ms: 1.23x faster                                                  |
| scimark_sor                | 134 ms                                                       | 114 ms: 1.17x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.65 us: 1.17x faster                                                 |
| spectral_norm              | 111 ms                                                       | 95.4 ms: 1.16x faster                                                 |
| async_generators           | 377 ms                                                       | 325 ms: 1.16x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.71 ms: 1.14x faster                                                 |
| pidigits                   | 217 ms                                                       | 191 ms: 1.13x faster                                                  |
| pylint                     | 317 ms                                                       | 282 ms: 1.12x faster                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.20 ms: 1.12x faster                                                 |
| scimark_fft                | 349 ms                                                       | 314 ms: 1.11x faster                                                  |
| float                      | 77.5 ms                                                      | 70.8 ms: 1.09x faster                                                 |
| telco                      | 7.82 ms                                                      | 7.21 ms: 1.08x faster                                                 |
| pyflate                    | 449 ms                                                       | 415 ms: 1.08x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 128 ms: 1.07x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 18.1 ms: 1.06x faster                                                 |
| richards_super             | 51.6 ms                                                      | 48.9 ms: 1.06x faster                                                 |
| richards                   | 45.2 ms                                                      | 42.8 ms: 1.06x faster                                                 |
| tomli_loads                | 2.01 sec                                                     | 1.90 sec: 1.05x faster                                                |
| coverage                   | 83.0 ms                                                      | 78.8 ms: 1.05x faster                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.23 sec: 1.05x faster                                                |
| xml_etree_iterparse        | 94.9 ms                                                      | 90.4 ms: 1.05x faster                                                 |
| pprint_safe_repr           | 738 ms                                                       | 703 ms: 1.05x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 22.5 ms: 1.05x faster                                                 |
| pprint_pformat             | 1.50 sec                                                     | 1.43 sec: 1.04x faster                                                |
| chaos                      | 57.3 ms                                                      | 54.9 ms: 1.04x faster                                                 |
| thrift                     | 778 us                                                       | 750 us: 1.04x faster                                                  |
| regex_compile              | 132 ms                                                       | 127 ms: 1.04x faster                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 63.4 ms: 1.03x faster                                                 |
| meteor_contest             | 102 ms                                                       | 98.8 ms: 1.03x faster                                                 |
| hexiom                     | 5.99 ms                                                      | 5.85 ms: 1.02x faster                                                 |
| generators                 | 28.8 ms                                                      | 28.2 ms: 1.02x faster                                                 |
| 2to3                       | 260 ms                                                       | 254 ms: 1.02x faster                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 83.8 ms: 1.02x faster                                                 |
| crypto_pyaes               | 67.9 ms                                                      | 66.8 ms: 1.02x faster                                                 |
| regex_dna                  | 180 ms                                                       | 177 ms: 1.02x faster                                                  |
| docutils                   | 2.62 sec                                                     | 2.58 sec: 1.01x faster                                                |
| genshi_text                | 21.5 ms                                                      | 21.3 ms: 1.01x faster                                                 |
| sympy_sum                  | 156 ms                                                       | 154 ms: 1.01x faster                                                  |
| nqueens                    | 78.6 ms                                                      | 78.0 ms: 1.01x faster                                                 |
| sqlglot_normalize          | 106 ms                                                       | 105 ms: 1.01x faster                                                  |
| sqlglot_optimize           | 52.7 ms                                                      | 52.4 ms: 1.01x faster                                                 |
| scimark_lu                 | 113 ms                                                       | 112 ms: 1.01x faster                                                  |
| sqlglot_transpile          | 1.56 ms                                                      | 1.55 ms: 1.00x faster                                                 |
| sqlglot_parse              | 1.25 ms                                                      | 1.25 ms: 1.00x slower                                                 |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.01x slower                                                  |
| sympy_expand               | 457 ms                                                       | 460 ms: 1.01x slower                                                  |
| json                       | 4.93 ms                                                      | 4.98 ms: 1.01x slower                                                 |
| typing_runtime_protocols   | 155 us                                                       | 156 us: 1.01x slower                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 7.48 ms: 1.01x slower                                                 |
| logging_simple             | 6.16 us                                                      | 6.25 us: 1.02x slower                                                 |
| dulwich_log                | 74.8 ms                                                      | 76.0 ms: 1.02x slower                                                 |
| logging_silent             | 103 ns                                                       | 104 ns: 1.02x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 3.18 ms: 1.02x slower                                                 |
| fannkuch                   | 370 ms                                                       | 377 ms: 1.02x slower                                                  |
| logging_format             | 6.84 us                                                      | 6.97 us: 1.02x slower                                                 |
| comprehensions             | 16.5 us                                                      | 16.8 us: 1.02x slower                                                 |
| json_loads                 | 27.0 us                                                      | 27.6 us: 1.02x slower                                                 |
| unpickle_pure_python       | 210 us                                                       | 215 us: 1.02x slower                                                  |
| nbody                      | 85.1 ms                                                      | 87.3 ms: 1.03x slower                                                 |
| regex_v8                   | 22.7 ms                                                      | 23.4 ms: 1.03x slower                                                 |
| mako                       | 11.3 ms                                                      | 11.7 ms: 1.03x slower                                                 |
| raytrace                   | 253 ms                                                       | 262 ms: 1.04x slower                                                  |
| django_template            | 34.1 ms                                                      | 36.0 ms: 1.05x slower                                                 |
| mdp                        | 2.36 sec                                                     | 2.49 sec: 1.06x slower                                                |
| pickle_pure_python         | 294 us                                                       | 313 us: 1.06x slower                                                  |
| json_dumps                 | 10.5 ms                                                      | 11.5 ms: 1.09x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.04 ms: 1.13x slower                                                 |
| python_startup             | 11.0 ms                                                      | 14.7 ms: 1.34x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.83 ms: 1.37x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 4.38 ms: 1.39x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 88.9 ms: 8.08x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.02x faster                                                          |

Benchmark hidden because not significant (6): xml_etree_process, sqlite_synth, genshi_xml, sympy_integrate, sympy_str, pycparser
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250116-3.14.0a4+-65a6ad3/bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.050x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.10x