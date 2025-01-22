# Results vs. 3.12.6

- fork: mpage
- ref: aa_test_6
- machine: linux-x86_64
- commit hash: 01bcf13
- commit date: 2025-01-21
- overall geometric mean: 1.087x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250121-vultr-x86_64-mpage-aa_test_6-3.14.0a4+-01bcf13 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 257 ms: 1.03x faster                                       |
| docutils       | 2.64 sec                                               | 2.58 sec: 1.02x faster                                     |
| Geometric mean | (ref)                                                  | 1.02x faster                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250121-vultr-x86_64-mpage-aa_test_6-3.14.0a4+-01bcf13 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 304 ms: 1.84x faster                                       |
| async_tree_io_tg           | 1.11 sec                                               | 612 ms: 1.81x faster                                       |
| async_tree_io              | 1.08 sec                                               | 606 ms: 1.79x faster                                       |
| async_tree_none            | 464 ms                                                 | 265 ms: 1.75x faster                                       |
| async_tree_none_tg         | 446 ms                                                 | 258 ms: 1.73x faster                                       |
| async_tree_memoization     | 555 ms                                                 | 323 ms: 1.72x faster                                       |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 480 ms: 1.50x faster                                       |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 493 ms: 1.45x faster                                       |
| async_generators           | 384 ms                                                 | 320 ms: 1.20x faster                                       |
| coroutines                 | 23.9 ms                                                | 22.3 ms: 1.07x faster                                      |
| asyncio_websockets         | 517 ms                                                 | 516 ms: 1.00x faster                                       |
| Geometric mean             | (ref)                                                  | 1.50x faster                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250121-vultr-x86_64-mpage-aa_test_6-3.14.0a4+-01bcf13 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| float          | 80.8 ms                                                | 70.2 ms: 1.15x faster                                      |
| nbody          | 89.3 ms                                                | 91.7 ms: 1.03x slower                                      |
| pidigits       | 184 ms                                                 | 206 ms: 1.12x slower                                       |
| Geometric mean | (ref)                                                  | 1.00x faster                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250121-vultr-x86_64-mpage-aa_test_6-3.14.0a4+-01bcf13 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.66 ms: 1.19x faster                                      |
| regex_compile  | 142 ms                                                 | 129 ms: 1.10x faster                                       |
| regex_dna      | 168 ms                                                 | 165 ms: 1.02x faster                                       |
| regex_v8       | 20.6 ms                                                | 24.3 ms: 1.18x slower                                      |
| Geometric mean | (ref)                                                  | 1.03x faster                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250121-vultr-x86_64-mpage-aa_test_6-3.14.0a4+-01bcf13 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 127 ms: 1.09x faster                                       |
| xml_etree_iterparse  | 96.7 ms                                                | 89.8 ms: 1.08x faster                                      |
| tomli_loads          | 2.11 sec                                               | 1.97 sec: 1.07x faster                                     |
| xml_etree_generate   | 85.2 ms                                                | 82.9 ms: 1.03x faster                                      |
| xml_etree_process    | 59.0 ms                                                | 60.0 ms: 1.02x slower                                      |
| unpickle_pure_python | 221 us                                                 | 226 us: 1.02x slower                                       |
| pickle_pure_python   | 308 us                                                 | 317 us: 1.03x slower                                       |
| json_loads           | 26.5 us                                                | 27.8 us: 1.05x slower                                      |
| json_dumps           | 10.4 ms                                                | 11.5 ms: 1.11x slower                                      |
| Geometric mean       | (ref)                                                  | 1.00x faster                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250121-vultr-x86_64-mpage-aa_test_6-3.14.0a4+-01bcf13 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.48 ms: 1.04x slower                                      |
| python_startup         | 9.93 ms                                                | 14.7 ms: 1.48x slower                                      |
| Geometric mean         | (ref)                                                  | 1.24x slower                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250121-vultr-x86_64-mpage-aa_test_6-3.14.0a4+-01bcf13 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 21.7 ms: 1.05x faster                                      |
| genshi_xml      | 50.2 ms                                                | 49.7 ms: 1.01x faster                                      |
| django_template | 34.7 ms                                                | 35.6 ms: 1.03x slower                                      |
| mako            | 11.0 ms                                                | 11.7 ms: 1.07x slower                                      |
| Geometric mean  | (ref)                                                  | 1.01x slower                                               |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250121-vultr-x86_64-mpage-aa_test_6-3.14.0a4+-01bcf13 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 304 ms: 1.84x faster                                       |
| async_tree_io_tg           | 1.11 sec                                               | 612 ms: 1.81x faster                                       |
| async_tree_io              | 1.08 sec                                               | 606 ms: 1.79x faster                                       |
| async_tree_none            | 464 ms                                                 | 265 ms: 1.75x faster                                       |
| async_tree_none_tg         | 446 ms                                                 | 258 ms: 1.73x faster                                       |
| async_tree_memoization     | 555 ms                                                 | 323 ms: 1.72x faster                                       |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 480 ms: 1.50x faster                                       |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 493 ms: 1.45x faster                                       |
| deepcopy                   | 352 us                                                 | 255 us: 1.38x faster                                       |
| deepcopy_memo              | 40.3 us                                                | 30.1 us: 1.34x faster                                      |
| go                         | 139 ms                                                 | 114 ms: 1.22x faster                                       |
| async_generators           | 384 ms                                                 | 320 ms: 1.20x faster                                       |
| deepcopy_reduce            | 3.08 us                                                | 2.57 us: 1.20x faster                                      |
| regex_effbot               | 3.17 ms                                                | 2.66 ms: 1.19x faster                                      |
| generators                 | 32.2 ms                                                | 27.2 ms: 1.19x faster                                      |
| comprehensions             | 19.8 us                                                | 16.8 us: 1.18x faster                                      |
| spectral_norm              | 110 ms                                                 | 93.6 ms: 1.18x faster                                      |
| pathlib                    | 21.5 ms                                                | 18.5 ms: 1.16x faster                                      |
| crypto_pyaes               | 76.6 ms                                                | 66.0 ms: 1.16x faster                                      |
| float                      | 80.8 ms                                                | 70.2 ms: 1.15x faster                                      |
| raytrace                   | 299 ms                                                 | 263 ms: 1.14x faster                                       |
| scimark_sor                | 130 ms                                                 | 114 ms: 1.13x faster                                       |
| pylint                     | 319 ms                                                 | 281 ms: 1.13x faster                                       |
| bpe_tokeniser              | 4.74 sec                                               | 4.24 sec: 1.12x faster                                     |
| richards                   | 45.9 ms                                                | 41.2 ms: 1.12x faster                                      |
| chaos                      | 62.8 ms                                                | 56.4 ms: 1.11x faster                                      |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.6 ms: 1.11x faster                                      |
| deltablue                  | 3.45 ms                                                | 3.10 ms: 1.11x faster                                      |
| regex_compile              | 142 ms                                                 | 129 ms: 1.10x faster                                       |
| sqlalchemy_declarative     | 143 ms                                                 | 130 ms: 1.10x faster                                       |
| richards_super             | 51.9 ms                                                | 47.4 ms: 1.09x faster                                      |
| scimark_fft                | 342 ms                                                 | 313 ms: 1.09x faster                                       |
| sqlglot_parse              | 1.36 ms                                                | 1.24 ms: 1.09x faster                                      |
| xml_etree_parse            | 139 ms                                                 | 127 ms: 1.09x faster                                       |
| pyflate                    | 448 ms                                                 | 412 ms: 1.09x faster                                       |
| sqlglot_transpile          | 1.67 ms                                                | 1.55 ms: 1.08x faster                                      |
| scimark_monte_carlo        | 68.4 ms                                                | 63.4 ms: 1.08x faster                                      |
| xml_etree_iterparse        | 96.7 ms                                                | 89.8 ms: 1.08x faster                                      |
| logging_silent             | 109 ns                                                 | 102 ns: 1.07x faster                                       |
| coroutines                 | 23.9 ms                                                | 22.3 ms: 1.07x faster                                      |
| sympy_sum                  | 166 ms                                                 | 155 ms: 1.07x faster                                       |
| tomli_loads                | 2.11 sec                                               | 1.97 sec: 1.07x faster                                     |
| hexiom                     | 6.17 ms                                                | 5.81 ms: 1.06x faster                                      |
| thrift                     | 791 us                                                 | 746 us: 1.06x faster                                       |
| sympy_str                  | 292 ms                                                 | 276 ms: 1.06x faster                                       |
| genshi_text                | 22.8 ms                                                | 21.7 ms: 1.05x faster                                      |
| mdp                        | 2.42 sec                                               | 2.30 sec: 1.05x faster                                     |
| pprint_pformat             | 1.52 sec                                               | 1.45 sec: 1.05x faster                                     |
| pprint_safe_repr           | 743 ms                                                 | 714 ms: 1.04x faster                                       |
| meteor_contest             | 104 ms                                                 | 99.6 ms: 1.04x faster                                      |
| sympy_integrate            | 20.5 ms                                                | 20.0 ms: 1.03x faster                                      |
| dulwich_log                | 78.9 ms                                                | 76.7 ms: 1.03x faster                                      |
| xml_etree_generate         | 85.2 ms                                                | 82.9 ms: 1.03x faster                                      |
| 2to3                       | 264 ms                                                 | 257 ms: 1.03x faster                                       |
| typing_runtime_protocols   | 163 us                                                 | 159 us: 1.03x faster                                       |
| pycparser                  | 1.17 sec                                               | 1.14 sec: 1.03x faster                                     |
| nqueens                    | 80.1 ms                                                | 78.3 ms: 1.02x faster                                      |
| docutils                   | 2.64 sec                                               | 2.58 sec: 1.02x faster                                     |
| scimark_lu                 | 114 ms                                                 | 112 ms: 1.02x faster                                       |
| regex_dna                  | 168 ms                                                 | 165 ms: 1.02x faster                                       |
| sqlglot_normalize          | 107 ms                                                 | 105 ms: 1.01x faster                                       |
| sqlglot_optimize           | 53.3 ms                                                | 52.7 ms: 1.01x faster                                      |
| json                       | 5.02 ms                                                | 4.97 ms: 1.01x faster                                      |
| genshi_xml                 | 50.2 ms                                                | 49.7 ms: 1.01x faster                                      |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.37 ms: 1.00x faster                                      |
| asyncio_websockets         | 517 ms                                                 | 516 ms: 1.00x faster                                       |
| fannkuch                   | 372 ms                                                 | 375 ms: 1.01x slower                                       |
| xml_etree_process          | 59.0 ms                                                | 60.0 ms: 1.02x slower                                      |
| unpickle_pure_python       | 221 us                                                 | 226 us: 1.02x slower                                       |
| django_template            | 34.7 ms                                                | 35.6 ms: 1.03x slower                                      |
| nbody                      | 89.3 ms                                                | 91.7 ms: 1.03x slower                                      |
| pickle_pure_python         | 308 us                                                 | 317 us: 1.03x slower                                       |
| python_startup_no_site     | 7.16 ms                                                | 7.48 ms: 1.04x slower                                      |
| json_loads                 | 26.5 us                                                | 27.8 us: 1.05x slower                                      |
| mako                       | 11.0 ms                                                | 11.7 ms: 1.07x slower                                      |
| telco                      | 6.53 ms                                                | 7.11 ms: 1.09x slower                                      |
| bench_thread_pool          | 941 us                                                 | 1.04 ms: 1.10x slower                                      |
| json_dumps                 | 10.4 ms                                                | 11.5 ms: 1.11x slower                                      |
| pidigits                   | 184 ms                                                 | 206 ms: 1.12x slower                                       |
| coverage                   | 71.4 ms                                                | 80.0 ms: 1.12x slower                                      |
| gc_traversal               | 3.46 ms                                                | 3.99 ms: 1.15x slower                                      |
| regex_v8                   | 20.6 ms                                                | 24.3 ms: 1.18x slower                                      |
| python_startup             | 9.93 ms                                                | 14.7 ms: 1.48x slower                                      |
| create_gc_cycles           | 1.09 ms                                                | 1.83 ms: 1.67x slower                                      |
| bench_mp_pool              | 10.8 ms                                                | 89.7 ms: 8.30x slower                                      |
| Geometric mean             | (ref)                                                  | 1.06x faster                                               |

Benchmark hidden because not significant (4): sympy_expand, logging_simple, logging_format, sqlite_synth
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250121-3.14.0a4+-01bcf13/bm-20250121-vultr-x86_64-mpage-aa_test_6-3.14.0a4+-01bcf13.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.087x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.11x