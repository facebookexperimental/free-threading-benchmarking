# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_tlbc_call_
- machine: linux-x86_64
- commit hash: c0d3c19
- commit date: 2024-12-04
- overall geometric mean: 1.247x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.19x slower
- Memory change: 1.31x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 366 ms: 1.41x slower                                                  |
| docutils       | 2.62 sec                                                     | 3.10 sec: 1.19x slower                                                |
| html5lib       | 67.0 ms                                                      | 99.4 ms: 1.48x slower                                                 |
| Geometric mean | (ref)                                                        | 1.35x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 819 ms: 1.12x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 617 ms: 1.03x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 645 ms: 1.03x faster                                                  |
| async_tree_io              | 876 ms                                                       | 850 ms: 1.03x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 24.8 ms: 1.05x slower                                                 |
| async_tree_none_tg         | 336 ms                                                       | 355 ms: 1.06x slower                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 447 ms: 1.08x slower                                                  |
| async_tree_none            | 354 ms                                                       | 388 ms: 1.10x slower                                                  |
| async_generators           | 377 ms                                                       | 457 ms: 1.21x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.03x slower                                                          |

Benchmark hidden because not significant (2): asyncio_websockets, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 181 ms: 1.20x faster                                                  |
| nbody          | 85.1 ms                                                      | 128 ms: 1.50x slower                                                  |
| float          | 77.5 ms                                                      | 138 ms: 1.78x slower                                                  |
| Geometric mean | (ref)                                                        | 1.31x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.82 ms: 1.09x faster                                                 |
| regex_dna      | 180 ms                                                       | 178 ms: 1.01x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 24.1 ms: 1.06x slower                                                 |
| regex_compile  | 132 ms                                                       | 179 ms: 1.35x slower                                                  |
| Geometric mean | (ref)                                                        | 1.07x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 130 ms: 1.05x faster                                                  |
| xml_etree_iterparse  | 94.9 ms                                                      | 91.2 ms: 1.04x faster                                                 |
| json_loads           | 27.0 us                                                      | 29.0 us: 1.07x slower                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 96.9 ms: 1.13x slower                                                 |
| xml_etree_process    | 59.3 ms                                                      | 77.3 ms: 1.30x slower                                                 |
| tomli_loads          | 2.01 sec                                                     | 2.68 sec: 1.33x slower                                                |
| json_dumps           | 10.5 ms                                                      | 14.1 ms: 1.34x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 331 us: 1.58x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 508 us: 1.72x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.24x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                                 |
| python_startup         | 11.0 ms                                                      | 17.5 ms: 1.60x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.49x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 62.9 ms: 1.29x slower                                                 |
| genshi_text     | 21.5 ms                                                      | 31.4 ms: 1.46x slower                                                 |
| django_template | 34.1 ms                                                      | 50.8 ms: 1.49x slower                                                 |
| mako            | 11.3 ms                                                      | 17.6 ms: 1.55x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.44x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits                   | 217 ms                                                       | 181 ms: 1.20x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 819 ms: 1.12x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.82 ms: 1.09x faster                                                 |
| deepcopy                   | 355 us                                                       | 327 us: 1.09x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 130 ms: 1.05x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 91.2 ms: 1.04x faster                                                 |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 617 ms: 1.03x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 645 ms: 1.03x faster                                                  |
| async_tree_io              | 876 ms                                                       | 850 ms: 1.03x faster                                                  |
| regex_dna                  | 180 ms                                                       | 178 ms: 1.01x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 39.5 us: 1.01x slower                                                 |
| sqlite_synth               | 2.21 us                                                      | 2.28 us: 1.03x slower                                                 |
| json                       | 4.93 ms                                                      | 5.10 ms: 1.03x slower                                                 |
| coroutines                 | 23.6 ms                                                      | 24.8 ms: 1.05x slower                                                 |
| pathlib                    | 19.2 ms                                                      | 20.2 ms: 1.06x slower                                                 |
| async_tree_none_tg         | 336 ms                                                       | 355 ms: 1.06x slower                                                  |
| regex_v8                   | 22.7 ms                                                      | 24.1 ms: 1.06x slower                                                 |
| json_loads                 | 27.0 us                                                      | 29.0 us: 1.07x slower                                                 |
| async_tree_memoization_tg  | 414 ms                                                       | 447 ms: 1.08x slower                                                  |
| async_tree_none            | 354 ms                                                       | 388 ms: 1.10x slower                                                  |
| spectral_norm              | 111 ms                                                       | 124 ms: 1.11x slower                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.97 sec: 1.12x slower                                                |
| telco                      | 7.82 ms                                                      | 8.75 ms: 1.12x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 3.52 ms: 1.12x slower                                                 |
| deepcopy_reduce            | 3.11 us                                                      | 3.50 us: 1.12x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 96.9 ms: 1.13x slower                                                 |
| scimark_fft                | 349 ms                                                       | 401 ms: 1.15x slower                                                  |
| mdp                        | 2.36 sec                                                     | 2.77 sec: 1.18x slower                                                |
| docutils                   | 2.62 sec                                                     | 3.10 sec: 1.19x slower                                                |
| pylint                     | 317 ms                                                       | 383 ms: 1.21x slower                                                  |
| async_generators           | 377 ms                                                       | 457 ms: 1.21x slower                                                  |
| coverage                   | 83.0 ms                                                      | 104 ms: 1.25x slower                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.95 ms: 1.26x slower                                                 |
| nqueens                    | 78.6 ms                                                      | 99.4 ms: 1.27x slower                                                 |
| dulwich_log                | 74.8 ms                                                      | 95.8 ms: 1.28x slower                                                 |
| meteor_contest             | 102 ms                                                       | 131 ms: 1.29x slower                                                  |
| genshi_xml                 | 48.8 ms                                                      | 62.9 ms: 1.29x slower                                                 |
| typing_runtime_protocols   | 155 us                                                       | 201 us: 1.30x slower                                                  |
| sqlglot_normalize          | 106 ms                                                       | 137 ms: 1.30x slower                                                  |
| xml_etree_process          | 59.3 ms                                                      | 77.3 ms: 1.30x slower                                                 |
| pprint_safe_repr           | 738 ms                                                       | 963 ms: 1.31x slower                                                  |
| sqlglot_optimize           | 52.7 ms                                                      | 68.9 ms: 1.31x slower                                                 |
| generators                 | 28.8 ms                                                      | 38.2 ms: 1.32x slower                                                 |
| pprint_pformat             | 1.50 sec                                                     | 2.00 sec: 1.33x slower                                                |
| tomli_loads                | 2.01 sec                                                     | 2.68 sec: 1.33x slower                                                |
| json_dumps                 | 10.5 ms                                                      | 14.1 ms: 1.34x slower                                                 |
| fannkuch                   | 370 ms                                                       | 496 ms: 1.34x slower                                                  |
| regex_compile              | 132 ms                                                       | 179 ms: 1.35x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 91.9 ms: 1.35x slower                                                 |
| pycparser                  | 1.12 sec                                                     | 1.55 sec: 1.39x slower                                                |
| create_gc_cycles           | 1.34 ms                                                      | 1.86 ms: 1.39x slower                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                                 |
| 2to3                       | 260 ms                                                       | 366 ms: 1.41x slower                                                  |
| genshi_text                | 21.5 ms                                                      | 31.4 ms: 1.46x slower                                                 |
| html5lib                   | 67.0 ms                                                      | 99.4 ms: 1.48x slower                                                 |
| thrift                     | 778 us                                                       | 1.15 ms: 1.48x slower                                                 |
| sympy_integrate            | 19.8 ms                                                      | 29.5 ms: 1.49x slower                                                 |
| django_template            | 34.1 ms                                                      | 50.8 ms: 1.49x slower                                                 |
| nbody                      | 85.1 ms                                                      | 128 ms: 1.50x slower                                                  |
| pyflate                    | 449 ms                                                       | 684 ms: 1.52x slower                                                  |
| mako                       | 11.3 ms                                                      | 17.6 ms: 1.55x slower                                                 |
| unpickle_pure_python       | 210 us                                                       | 331 us: 1.58x slower                                                  |
| python_startup             | 11.0 ms                                                      | 17.5 ms: 1.60x slower                                                 |
| scimark_lu                 | 113 ms                                                       | 181 ms: 1.61x slower                                                  |
| hexiom                     | 5.99 ms                                                      | 9.80 ms: 1.64x slower                                                 |
| richards_super             | 51.6 ms                                                      | 85.5 ms: 1.66x slower                                                 |
| comprehensions             | 16.5 us                                                      | 27.3 us: 1.66x slower                                                 |
| richards                   | 45.2 ms                                                      | 76.1 ms: 1.68x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 508 us: 1.72x slower                                                  |
| scimark_sor                | 134 ms                                                       | 233 ms: 1.73x slower                                                  |
| sympy_str                  | 275 ms                                                       | 477 ms: 1.74x slower                                                  |
| logging_silent             | 103 ns                                                       | 179 ns: 1.74x slower                                                  |
| logging_simple             | 6.16 us                                                      | 10.9 us: 1.76x slower                                                 |
| logging_format             | 6.84 us                                                      | 12.2 us: 1.78x slower                                                 |
| float                      | 77.5 ms                                                      | 138 ms: 1.78x slower                                                  |
| chaos                      | 57.3 ms                                                      | 103 ms: 1.79x slower                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 119 ms: 1.82x slower                                                  |
| go                         | 141 ms                                                       | 265 ms: 1.88x slower                                                  |
| sqlglot_transpile          | 1.56 ms                                                      | 2.94 ms: 1.89x slower                                                 |
| sqlglot_parse              | 1.25 ms                                                      | 2.56 ms: 2.05x slower                                                 |
| sympy_expand               | 457 ms                                                       | 956 ms: 2.09x slower                                                  |
| raytrace                   | 253 ms                                                       | 543 ms: 2.15x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 351 ms: 2.26x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 7.92 ms: 2.53x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 3.37 ms: 3.67x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 109 ms: 9.93x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.38x slower                                                          |

Benchmark hidden because not significant (2): asyncio_websockets, async_tree_memoization
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241204-3.14.0a2+-c0d3c19-NOGIL/bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.247x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.24x
- 95% likely to have a slowdown of 1.22x
- 99% likely to have a slowdown of 1.19x

# Memory
- memory change: 1.31x