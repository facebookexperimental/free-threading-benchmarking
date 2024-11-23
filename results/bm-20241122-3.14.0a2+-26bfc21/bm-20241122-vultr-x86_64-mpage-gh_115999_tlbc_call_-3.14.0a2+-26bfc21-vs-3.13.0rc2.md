# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_tlbc_call_
- machine: linux-x86_64
- commit hash: 26bfc21
- commit date: 2024-11-22
- overall geometric mean: 1.02x slower
- HPT reliability: 76.77%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 256 ms: 1.01x faster                                                  |
| docutils       | 2.62 sec                                                     | 2.64 sec: 1.01x slower                                                |
| Geometric mean | (ref)                                                        | 1.00x faster                                                          |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|---------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization    | 461 ms                                                       | 407 ms: 1.13x faster                                                  |
| async_tree_memoization_tg | 414 ms                                                       | 390 ms: 1.06x faster                                                  |
| async_tree_cpu_io_mixed   | 666 ms                                                       | 628 ms: 1.06x faster                                                  |
| async_tree_none           | 354 ms                                                       | 334 ms: 1.06x faster                                                  |
| coroutines                | 23.6 ms                                                      | 22.5 ms: 1.05x faster                                                 |
| async_tree_io             | 876 ms                                                       | 843 ms: 1.04x faster                                                  |
| async_tree_io_tg          | 913 ms                                                       | 888 ms: 1.03x faster                                                  |
| async_generators          | 377 ms                                                       | 373 ms: 1.01x faster                                                  |
| asyncio_websockets        | 520 ms                                                       | 523 ms: 1.01x slower                                                  |
| Geometric mean            | (ref)                                                        | 1.04x faster                                                          |

Benchmark hidden because not significant (2): async_tree_cpu_io_mixed_tg, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 216 ms: 1.00x faster                                                  |
| float          | 77.5 ms                                                      | 80.4 ms: 1.04x slower                                                 |
| nbody          | 85.1 ms                                                      | 94.9 ms: 1.11x slower                                                 |
| Geometric mean | (ref)                                                        | 1.05x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.93 ms: 1.05x faster                                                 |
| regex_compile  | 132 ms                                                       | 136 ms: 1.03x slower                                                  |
| regex_dna      | 180 ms                                                       | 186 ms: 1.03x slower                                                  |
| regex_v8       | 22.7 ms                                                      | 24.4 ms: 1.07x slower                                                 |
| Geometric mean | (ref)                                                        | 1.02x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_loads           | 27.0 us                                                      | 25.0 us: 1.08x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 86.7 ms: 1.02x slower                                                 |
| xml_etree_process    | 59.3 ms                                                      | 60.3 ms: 1.02x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 214 us: 1.02x slower                                                  |
| xml_etree_iterparse  | 94.9 ms                                                      | 98.9 ms: 1.04x slower                                                 |
| tomli_loads          | 2.01 sec                                                     | 2.09 sec: 1.04x slower                                                |
| pickle_pure_python   | 294 us                                                       | 318 us: 1.08x slower                                                  |
| json_dumps           | 10.5 ms                                                      | 11.4 ms: 1.08x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.02x slower                                                          |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup | 11.0 ms                                                      | 13.2 ms: 1.20x slower                                                 |
| Geometric mean | (ref)                                                        | 1.10x slower                                                          |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 21.9 ms: 1.01x slower                                                 |
| genshi_xml      | 48.8 ms                                                      | 49.8 ms: 1.02x slower                                                 |
| mako            | 11.3 ms                                                      | 11.7 ms: 1.03x slower                                                 |
| django_template | 34.1 ms                                                      | 35.5 ms: 1.04x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.03x slower                                                          |

All benchmarks:
===============

| Benchmark                 | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|---------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| deepcopy                  | 355 us                                                       | 258 us: 1.38x faster                                                  |
| deepcopy_memo             | 39.1 us                                                      | 29.6 us: 1.32x faster                                                 |
| deepcopy_reduce           | 3.11 us                                                      | 2.58 us: 1.21x faster                                                 |
| go                        | 141 ms                                                       | 119 ms: 1.19x faster                                                  |
| pylint                    | 317 ms                                                       | 270 ms: 1.17x faster                                                  |
| async_tree_memoization    | 461 ms                                                       | 407 ms: 1.13x faster                                                  |
| json                      | 4.93 ms                                                      | 4.51 ms: 1.09x faster                                                 |
| json_loads                | 27.0 us                                                      | 25.0 us: 1.08x faster                                                 |
| telco                     | 7.82 ms                                                      | 7.25 ms: 1.08x faster                                                 |
| async_tree_memoization_tg | 414 ms                                                       | 390 ms: 1.06x faster                                                  |
| async_tree_cpu_io_mixed   | 666 ms                                                       | 628 ms: 1.06x faster                                                  |
| async_tree_none           | 354 ms                                                       | 334 ms: 1.06x faster                                                  |
| regex_effbot              | 3.08 ms                                                      | 2.93 ms: 1.05x faster                                                 |
| coroutines                | 23.6 ms                                                      | 22.5 ms: 1.05x faster                                                 |
| scimark_sparse_mat_mult   | 4.71 ms                                                      | 4.51 ms: 1.04x faster                                                 |
| pathlib                   | 19.2 ms                                                      | 18.4 ms: 1.04x faster                                                 |
| async_tree_io             | 876 ms                                                       | 843 ms: 1.04x faster                                                  |
| scimark_fft               | 349 ms                                                       | 337 ms: 1.04x faster                                                  |
| pprint_safe_repr          | 738 ms                                                       | 713 ms: 1.03x faster                                                  |
| thrift                    | 778 us                                                       | 753 us: 1.03x faster                                                  |
| pprint_pformat            | 1.50 sec                                                     | 1.45 sec: 1.03x faster                                                |
| async_tree_io_tg          | 913 ms                                                       | 888 ms: 1.03x faster                                                  |
| coverage                  | 83.0 ms                                                      | 80.7 ms: 1.03x faster                                                 |
| spectral_norm             | 111 ms                                                       | 108 ms: 1.03x faster                                                  |
| 2to3                      | 260 ms                                                       | 256 ms: 1.01x faster                                                  |
| async_generators          | 377 ms                                                       | 373 ms: 1.01x faster                                                  |
| meteor_contest            | 102 ms                                                       | 100 ms: 1.01x faster                                                  |
| sympy_sum                 | 156 ms                                                       | 154 ms: 1.01x faster                                                  |
| bpe_tokeniser             | 4.45 sec                                                     | 4.41 sec: 1.01x faster                                                |
| scimark_monte_carlo       | 65.4 ms                                                      | 64.9 ms: 1.01x faster                                                 |
| scimark_lu                | 113 ms                                                       | 112 ms: 1.00x faster                                                  |
| pidigits                  | 217 ms                                                       | 216 ms: 1.00x faster                                                  |
| fannkuch                  | 370 ms                                                       | 371 ms: 1.00x slower                                                  |
| nqueens                   | 78.6 ms                                                      | 79.0 ms: 1.01x slower                                                 |
| asyncio_websockets        | 520 ms                                                       | 523 ms: 1.01x slower                                                  |
| pycparser                 | 1.12 sec                                                     | 1.13 sec: 1.01x slower                                                |
| docutils                  | 2.62 sec                                                     | 2.64 sec: 1.01x slower                                                |
| sqlglot_normalize         | 106 ms                                                       | 107 ms: 1.01x slower                                                  |
| sympy_expand              | 457 ms                                                       | 461 ms: 1.01x slower                                                  |
| sympy_integrate           | 19.8 ms                                                      | 20.0 ms: 1.01x slower                                                 |
| genshi_text               | 21.5 ms                                                      | 21.9 ms: 1.01x slower                                                 |
| logging_format            | 6.84 us                                                      | 6.94 us: 1.01x slower                                                 |
| xml_etree_generate        | 85.4 ms                                                      | 86.7 ms: 1.02x slower                                                 |
| xml_etree_process         | 59.3 ms                                                      | 60.3 ms: 1.02x slower                                                 |
| richards_super            | 51.6 ms                                                      | 52.5 ms: 1.02x slower                                                 |
| sqlglot_optimize          | 52.7 ms                                                      | 53.6 ms: 1.02x slower                                                 |
| chaos                     | 57.3 ms                                                      | 58.3 ms: 1.02x slower                                                 |
| generators                | 28.8 ms                                                      | 29.3 ms: 1.02x slower                                                 |
| unpickle_pure_python      | 210 us                                                       | 214 us: 1.02x slower                                                  |
| dulwich_log               | 74.8 ms                                                      | 76.4 ms: 1.02x slower                                                 |
| genshi_xml                | 48.8 ms                                                      | 49.8 ms: 1.02x slower                                                 |
| sqlglot_transpile         | 1.56 ms                                                      | 1.60 ms: 1.02x slower                                                 |
| typing_runtime_protocols  | 155 us                                                       | 159 us: 1.03x slower                                                  |
| regex_compile             | 132 ms                                                       | 136 ms: 1.03x slower                                                  |
| regex_dna                 | 180 ms                                                       | 186 ms: 1.03x slower                                                  |
| richards                  | 45.2 ms                                                      | 46.6 ms: 1.03x slower                                                 |
| mako                      | 11.3 ms                                                      | 11.7 ms: 1.03x slower                                                 |
| sqlglot_parse             | 1.25 ms                                                      | 1.29 ms: 1.03x slower                                                 |
| deltablue                 | 3.12 ms                                                      | 3.23 ms: 1.04x slower                                                 |
| logging_silent            | 103 ns                                                       | 106 ns: 1.04x slower                                                  |
| float                     | 77.5 ms                                                      | 80.4 ms: 1.04x slower                                                 |
| raytrace                  | 253 ms                                                       | 262 ms: 1.04x slower                                                  |
| django_template           | 34.1 ms                                                      | 35.5 ms: 1.04x slower                                                 |
| xml_etree_iterparse       | 94.9 ms                                                      | 98.9 ms: 1.04x slower                                                 |
| tomli_loads               | 2.01 sec                                                     | 2.09 sec: 1.04x slower                                                |
| comprehensions            | 16.5 us                                                      | 17.3 us: 1.05x slower                                                 |
| mdp                       | 2.36 sec                                                     | 2.49 sec: 1.06x slower                                                |
| regex_v8                  | 22.7 ms                                                      | 24.4 ms: 1.07x slower                                                 |
| pickle_pure_python        | 294 us                                                       | 318 us: 1.08x slower                                                  |
| json_dumps                | 10.5 ms                                                      | 11.4 ms: 1.08x slower                                                 |
| bench_thread_pool         | 919 us                                                       | 1.02 ms: 1.11x slower                                                 |
| nbody                     | 85.1 ms                                                      | 94.9 ms: 1.11x slower                                                 |
| python_startup            | 11.0 ms                                                      | 13.2 ms: 1.20x slower                                                 |
| gc_traversal              | 3.14 ms                                                      | 4.22 ms: 1.34x slower                                                 |
| create_gc_cycles          | 1.34 ms                                                      | 1.91 ms: 1.43x slower                                                 |
| bench_mp_pool             | 11.0 ms                                                      | 86.1 ms: 7.83x slower                                                 |
| Geometric mean            | (ref)                                                        | 1.02x slower                                                          |

Benchmark hidden because not significant (12): async_tree_cpu_io_mixed_tg, crypto_pyaes, hexiom, sympy_str, scimark_sor, html5lib, python_startup_no_site, sqlite_synth, pyflate, xml_etree_parse, logging_simple, async_tree_none_tg
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241122-3.14.0a2+-26bfc21/bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

# HPT report

- Reliability score: 76.77% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.09x