# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: 8b96368
- commit date: 2025-01-02
- overall geometric mean: 1.098x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 254 ms: 1.04x faster                                                  |
| docutils       | 2.64 sec                                               | 2.55 sec: 1.04x faster                                                |
| Geometric mean | (ref)                                                  | 1.04x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 295 ms: 1.90x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 604 ms: 1.84x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 248 ms: 1.80x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 608 ms: 1.78x faster                                                  |
| async_tree_none            | 464 ms                                                 | 267 ms: 1.74x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 321 ms: 1.73x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 464 ms: 1.56x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 483 ms: 1.48x faster                                                  |
| coroutines                 | 23.9 ms                                                | 21.0 ms: 1.14x faster                                                 |
| async_generators           | 384 ms                                                 | 352 ms: 1.09x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 523 ms: 1.01x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.51x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 72.4 ms: 1.12x faster                                                 |
| pidigits       | 184 ms                                                 | 184 ms: 1.00x faster                                                  |
| nbody          | 89.3 ms                                                | 91.4 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                  | 1.03x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.74 ms: 1.16x faster                                                 |
| regex_compile  | 142 ms                                                 | 128 ms: 1.12x faster                                                  |
| regex_dna      | 168 ms                                                 | 169 ms: 1.01x slower                                                  |
| regex_v8       | 20.6 ms                                                | 23.9 ms: 1.16x slower                                                 |
| Geometric mean | (ref)                                                  | 1.02x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.93 sec: 1.09x faster                                                |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.08x faster                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 90.6 ms: 1.07x faster                                                 |
| unpickle_pure_python | 221 us                                                 | 209 us: 1.05x faster                                                  |
| xml_etree_generate   | 85.2 ms                                                | 83.2 ms: 1.02x faster                                                 |
| xml_etree_process    | 59.0 ms                                                | 57.6 ms: 1.02x faster                                                 |
| json_loads           | 26.5 us                                                | 26.0 us: 1.02x faster                                                 |
| pickle_pure_python   | 308 us                                                 | 310 us: 1.01x slower                                                  |
| json_dumps           | 10.4 ms                                                | 11.2 ms: 1.08x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.48 ms: 1.04x slower                                                 |
| python_startup         | 9.93 ms                                                | 14.7 ms: 1.48x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.24x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text    | 22.8 ms                                                | 21.0 ms: 1.09x faster                                                 |
| genshi_xml     | 50.2 ms                                                | 48.0 ms: 1.04x faster                                                 |
| mako           | 11.0 ms                                                | 11.8 ms: 1.07x slower                                                 |
| Geometric mean | (ref)                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 295 ms: 1.90x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 604 ms: 1.84x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 248 ms: 1.80x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 608 ms: 1.78x faster                                                  |
| async_tree_none            | 464 ms                                                 | 267 ms: 1.74x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 321 ms: 1.73x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 464 ms: 1.56x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 483 ms: 1.48x faster                                                  |
| deepcopy                   | 352 us                                                 | 250 us: 1.41x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 29.8 us: 1.35x faster                                                 |
| deepcopy_reduce            | 3.08 us                                                | 2.56 us: 1.20x faster                                                 |
| pathlib                    | 21.5 ms                                                | 18.1 ms: 1.19x faster                                                 |
| go                         | 139 ms                                                 | 118 ms: 1.18x faster                                                  |
| generators                 | 32.2 ms                                                | 27.4 ms: 1.17x faster                                                 |
| comprehensions             | 19.8 us                                                | 17.0 us: 1.17x faster                                                 |
| raytrace                   | 299 ms                                                 | 258 ms: 1.16x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.74 ms: 1.16x faster                                                 |
| spectral_norm              | 110 ms                                                 | 96.0 ms: 1.15x faster                                                 |
| crypto_pyaes               | 76.6 ms                                                | 66.9 ms: 1.14x faster                                                 |
| pylint                     | 319 ms                                                 | 279 ms: 1.14x faster                                                  |
| coroutines                 | 23.9 ms                                                | 21.0 ms: 1.14x faster                                                 |
| scimark_sor                | 130 ms                                                 | 114 ms: 1.14x faster                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.3 ms: 1.13x faster                                                 |
| sqlalchemy_declarative     | 143 ms                                                 | 128 ms: 1.12x faster                                                  |
| regex_compile              | 142 ms                                                 | 128 ms: 1.12x faster                                                  |
| float                      | 80.8 ms                                                | 72.4 ms: 1.12x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.26 sec: 1.11x faster                                                |
| logging_simple             | 6.63 us                                                | 6.02 us: 1.10x faster                                                 |
| sqlglot_parse              | 1.36 ms                                                | 1.23 ms: 1.10x faster                                                 |
| deltablue                  | 3.45 ms                                                | 3.14 ms: 1.10x faster                                                 |
| thrift                     | 791 us                                                 | 723 us: 1.09x faster                                                  |
| logging_format             | 7.35 us                                                | 6.72 us: 1.09x faster                                                 |
| async_generators           | 384 ms                                                 | 352 ms: 1.09x faster                                                  |
| tomli_loads                | 2.11 sec                                               | 1.93 sec: 1.09x faster                                                |
| richards                   | 45.9 ms                                                | 42.2 ms: 1.09x faster                                                 |
| sqlglot_transpile          | 1.67 ms                                                | 1.54 ms: 1.09x faster                                                 |
| genshi_text                | 22.8 ms                                                | 21.0 ms: 1.09x faster                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 63.0 ms: 1.09x faster                                                 |
| scimark_fft                | 342 ms                                                 | 315 ms: 1.08x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                                  |
| pyflate                    | 448 ms                                                 | 414 ms: 1.08x faster                                                  |
| chaos                      | 62.8 ms                                                | 58.1 ms: 1.08x faster                                                 |
| sympy_sum                  | 166 ms                                                 | 154 ms: 1.08x faster                                                  |
| pprint_safe_repr           | 743 ms                                                 | 689 ms: 1.08x faster                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.41 sec: 1.08x faster                                                |
| sympy_str                  | 292 ms                                                 | 272 ms: 1.07x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 90.6 ms: 1.07x faster                                                 |
| richards_super             | 51.9 ms                                                | 48.6 ms: 1.07x faster                                                 |
| logging_silent             | 109 ns                                                 | 102 ns: 1.06x faster                                                  |
| json                       | 5.02 ms                                                | 4.73 ms: 1.06x faster                                                 |
| pycparser                  | 1.17 sec                                               | 1.11 sec: 1.06x faster                                                |
| hexiom                     | 6.17 ms                                                | 5.84 ms: 1.06x faster                                                 |
| unpickle_pure_python       | 221 us                                                 | 209 us: 1.05x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 75.1 ms: 1.05x faster                                                 |
| typing_runtime_protocols   | 163 us                                                 | 156 us: 1.05x faster                                                  |
| genshi_xml                 | 50.2 ms                                                | 48.0 ms: 1.04x faster                                                 |
| mdp                        | 2.42 sec                                               | 2.32 sec: 1.04x faster                                                |
| sqlglot_normalize          | 107 ms                                                 | 102 ms: 1.04x faster                                                  |
| sympy_integrate            | 20.5 ms                                                | 19.8 ms: 1.04x faster                                                 |
| 2to3                       | 264 ms                                                 | 254 ms: 1.04x faster                                                  |
| meteor_contest             | 104 ms                                                 | 100.0 ms: 1.04x faster                                                |
| docutils                   | 2.64 sec                                               | 2.55 sec: 1.04x faster                                                |
| nqueens                    | 80.1 ms                                                | 77.8 ms: 1.03x faster                                                 |
| sqlglot_optimize           | 53.3 ms                                                | 51.9 ms: 1.03x faster                                                 |
| xml_etree_generate         | 85.2 ms                                                | 83.2 ms: 1.02x faster                                                 |
| xml_etree_process          | 59.0 ms                                                | 57.6 ms: 1.02x faster                                                 |
| json_loads                 | 26.5 us                                                | 26.0 us: 1.02x faster                                                 |
| fannkuch                   | 372 ms                                                 | 366 ms: 1.02x faster                                                  |
| sympy_expand               | 468 ms                                                 | 460 ms: 1.02x faster                                                  |
| scimark_lu                 | 114 ms                                                 | 112 ms: 1.02x faster                                                  |
| pidigits                   | 184 ms                                                 | 184 ms: 1.00x faster                                                  |
| pickle_pure_python         | 308 us                                                 | 310 us: 1.01x slower                                                  |
| regex_dna                  | 168 ms                                                 | 169 ms: 1.01x slower                                                  |
| asyncio_websockets         | 517 ms                                                 | 523 ms: 1.01x slower                                                  |
| nbody                      | 89.3 ms                                                | 91.4 ms: 1.02x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 7.48 ms: 1.04x slower                                                 |
| mako                       | 11.0 ms                                                | 11.8 ms: 1.07x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 11.2 ms: 1.08x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.04 ms: 1.10x slower                                                 |
| coverage                   | 71.4 ms                                                | 78.6 ms: 1.10x slower                                                 |
| telco                      | 6.53 ms                                                | 7.30 ms: 1.12x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 23.9 ms: 1.16x slower                                                 |
| gc_traversal               | 3.46 ms                                                | 4.19 ms: 1.21x slower                                                 |
| python_startup             | 9.93 ms                                                | 14.7 ms: 1.48x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.83 ms: 1.68x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 89.0 ms: 8.24x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                          |

Benchmark hidden because not significant (3): django_template, scimark_sparse_mat_mult, sqlite_synth
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250102-3.14.0a3+-8b96368/bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.098x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.11x