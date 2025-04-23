# Results vs. 3.13.0rc2

- fork: nascheme
- ref: gh_127266_type_slots
- machine: linux-x86_64
- commit hash: 986f23a
- commit date: 2025-04-22
- overall geometric mean: 1.003x slower
- HPT reliability: 84.06%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250422-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-986f23a |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 281 ms: 1.08x slower                                                     |
| docutils       | 2.63 sec                                                               | 2.70 sec: 1.03x slower                                                   |
| html5lib       | 68.6 ms                                                                | 67.0 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250422-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-986f23a |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 519 ms: 1.74x faster                                                     |
| async_tree_io              | 881 ms                                                                 | 551 ms: 1.60x faster                                                     |
| async_tree_memoization     | 459 ms                                                                 | 311 ms: 1.47x faster                                                     |
| async_tree_none_tg         | 333 ms                                                                 | 227 ms: 1.46x faster                                                     |
| async_tree_memoization_tg  | 410 ms                                                                 | 284 ms: 1.44x faster                                                     |
| async_tree_none            | 353 ms                                                                 | 259 ms: 1.37x faster                                                     |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 468 ms: 1.35x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 494 ms: 1.35x faster                                                     |
| async_generators           | 375 ms                                                                 | 358 ms: 1.05x faster                                                     |
| coroutines                 | 23.3 ms                                                                | 22.8 ms: 1.02x faster                                                    |
| asyncio_websockets         | 517 ms                                                                 | 516 ms: 1.00x faster                                                     |
| Geometric mean             | (ref)                                                                  | 1.33x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250422-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-986f23a |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 186 ms: 1.17x faster                                                     |
| float          | 76.7 ms                                                                | 67.2 ms: 1.14x faster                                                    |
| nbody          | 85.3 ms                                                                | 110 ms: 1.28x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250422-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-986f23a |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.78 ms: 1.16x faster                                                    |
| regex_v8       | 23.2 ms                                                                | 21.0 ms: 1.11x faster                                                    |
| regex_dna      | 189 ms                                                                 | 180 ms: 1.05x faster                                                     |
| regex_compile  | 131 ms                                                                 | 143 ms: 1.09x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250422-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-986f23a |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 86.8 ms: 1.09x faster                                                    |
| xml_etree_parse      | 136 ms                                                                 | 129 ms: 1.05x faster                                                     |
| tomli_loads          | 2.01 sec                                                               | 2.07 sec: 1.03x slower                                                   |
| json_loads           | 27.3 us                                                                | 29.4 us: 1.08x slower                                                    |
| xml_etree_generate   | 85.4 ms                                                                | 93.3 ms: 1.09x slower                                                    |
| unpickle_pure_python | 208 us                                                                 | 228 us: 1.10x slower                                                     |
| pickle_pure_python   | 292 us                                                                 | 326 us: 1.12x slower                                                     |
| xml_etree_process    | 59.2 ms                                                                | 66.6 ms: 1.12x slower                                                    |
| json_dumps           | 10.6 ms                                                                | 12.6 ms: 1.18x slower                                                    |
| Geometric mean       | (ref)                                                                  | 1.06x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250422-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-986f23a |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 15.8 ms: 1.43x slower                                                    |
| python_startup_no_site | 7.41 ms                                                                | 11.1 ms: 1.50x slower                                                    |
| Geometric mean         | (ref)                                                                  | 1.47x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250422-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-986f23a |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 55.4 ms: 1.13x slower                                                    |
| django_template | 34.2 ms                                                                | 40.4 ms: 1.18x slower                                                    |
| genshi_text     | 21.7 ms                                                                | 25.8 ms: 1.18x slower                                                    |
| mako            | 11.2 ms                                                                | 15.2 ms: 1.36x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.21x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250422-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-986f23a |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.79 ms: 1.85x faster                                                    |
| mdp                        | 2.34 sec                                                               | 1.31 sec: 1.79x faster                                                   |
| async_tree_io_tg           | 901 ms                                                                 | 519 ms: 1.74x faster                                                     |
| async_tree_io              | 881 ms                                                                 | 551 ms: 1.60x faster                                                     |
| async_tree_memoization     | 459 ms                                                                 | 311 ms: 1.47x faster                                                     |
| async_tree_none_tg         | 333 ms                                                                 | 227 ms: 1.46x faster                                                     |
| async_tree_memoization_tg  | 410 ms                                                                 | 284 ms: 1.44x faster                                                     |
| async_tree_none            | 353 ms                                                                 | 259 ms: 1.37x faster                                                     |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 468 ms: 1.35x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 494 ms: 1.35x faster                                                     |
| deepcopy                   | 357 us                                                                 | 290 us: 1.23x faster                                                     |
| pidigits                   | 216 ms                                                                 | 186 ms: 1.17x faster                                                     |
| regex_effbot               | 3.21 ms                                                                | 2.78 ms: 1.16x faster                                                    |
| float                      | 76.7 ms                                                                | 67.2 ms: 1.14x faster                                                    |
| sqlite_synth               | 2.25 us                                                                | 1.99 us: 1.13x faster                                                    |
| go                         | 141 ms                                                                 | 124 ms: 1.13x faster                                                     |
| scimark_sor                | 134 ms                                                                 | 119 ms: 1.13x faster                                                     |
| regex_v8                   | 23.2 ms                                                                | 21.0 ms: 1.11x faster                                                    |
| deepcopy_memo              | 38.1 us                                                                | 34.8 us: 1.10x faster                                                    |
| xml_etree_iterparse        | 94.4 ms                                                                | 86.8 ms: 1.09x faster                                                    |
| dulwich_log                | 74.5 ms                                                                | 70.6 ms: 1.05x faster                                                    |
| xml_etree_parse            | 136 ms                                                                 | 129 ms: 1.05x faster                                                     |
| spectral_norm              | 108 ms                                                                 | 102 ms: 1.05x faster                                                     |
| async_generators           | 375 ms                                                                 | 358 ms: 1.05x faster                                                     |
| regex_dna                  | 189 ms                                                                 | 180 ms: 1.05x faster                                                     |
| scimark_fft                | 348 ms                                                                 | 335 ms: 1.04x faster                                                     |
| deepcopy_reduce            | 3.12 us                                                                | 3.02 us: 1.03x faster                                                    |
| bpe_tokeniser              | 4.46 sec                                                               | 4.34 sec: 1.03x faster                                                   |
| html5lib                   | 68.6 ms                                                                | 67.0 ms: 1.02x faster                                                    |
| coroutines                 | 23.3 ms                                                                | 22.8 ms: 1.02x faster                                                    |
| asyncio_websockets         | 517 ms                                                                 | 516 ms: 1.00x faster                                                     |
| pathlib                    | 19.3 ms                                                                | 19.4 ms: 1.01x slower                                                    |
| pycparser                  | 1.12 sec                                                               | 1.13 sec: 1.01x slower                                                   |
| pyflate                    | 449 ms                                                                 | 459 ms: 1.02x slower                                                     |
| create_gc_cycles           | 1.33 ms                                                                | 1.37 ms: 1.03x slower                                                    |
| docutils                   | 2.63 sec                                                               | 2.70 sec: 1.03x slower                                                   |
| tomli_loads                | 2.01 sec                                                               | 2.07 sec: 1.03x slower                                                   |
| logging_silent             | 98.2 ns                                                                | 102 ns: 1.04x slower                                                     |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.01 ms: 1.05x slower                                                    |
| generators                 | 28.5 ms                                                                | 30.1 ms: 1.06x slower                                                    |
| pprint_safe_repr           | 719 ms                                                                 | 764 ms: 1.06x slower                                                     |
| json_loads                 | 27.3 us                                                                | 29.4 us: 1.08x slower                                                    |
| 2to3                       | 259 ms                                                                 | 281 ms: 1.08x slower                                                     |
| chaos                      | 56.3 ms                                                                | 61.0 ms: 1.08x slower                                                    |
| regex_compile              | 131 ms                                                                 | 143 ms: 1.09x slower                                                     |
| xml_etree_generate         | 85.4 ms                                                                | 93.3 ms: 1.09x slower                                                    |
| telco                      | 7.77 ms                                                                | 8.49 ms: 1.09x slower                                                    |
| pprint_pformat             | 1.46 sec                                                               | 1.59 sec: 1.09x slower                                                   |
| unpickle_pure_python       | 208 us                                                                 | 228 us: 1.10x slower                                                     |
| hexiom                     | 5.95 ms                                                                | 6.55 ms: 1.10x slower                                                    |
| scimark_monte_carlo        | 65.8 ms                                                                | 73.4 ms: 1.12x slower                                                    |
| pickle_pure_python         | 292 us                                                                 | 326 us: 1.12x slower                                                     |
| sympy_integrate            | 19.7 ms                                                                | 22.1 ms: 1.12x slower                                                    |
| richards                   | 44.4 ms                                                                | 49.7 ms: 1.12x slower                                                    |
| nqueens                    | 77.7 ms                                                                | 87.2 ms: 1.12x slower                                                    |
| xml_etree_process          | 59.2 ms                                                                | 66.6 ms: 1.12x slower                                                    |
| logging_format             | 6.92 us                                                                | 7.78 us: 1.12x slower                                                    |
| genshi_xml                 | 49.1 ms                                                                | 55.4 ms: 1.13x slower                                                    |
| logging_simple             | 6.14 us                                                                | 6.96 us: 1.13x slower                                                    |
| richards_super             | 50.4 ms                                                                | 57.3 ms: 1.14x slower                                                    |
| deltablue                  | 3.10 ms                                                                | 3.52 ms: 1.14x slower                                                    |
| sympy_str                  | 274 ms                                                                 | 313 ms: 1.14x slower                                                     |
| sympy_sum                  | 154 ms                                                                 | 177 ms: 1.15x slower                                                     |
| scimark_lu                 | 112 ms                                                                 | 130 ms: 1.15x slower                                                     |
| raytrace                   | 250 ms                                                                 | 288 ms: 1.15x slower                                                     |
| sympy_expand               | 454 ms                                                                 | 525 ms: 1.16x slower                                                     |
| comprehensions             | 16.6 us                                                                | 19.3 us: 1.17x slower                                                    |
| json_dumps                 | 10.6 ms                                                                | 12.6 ms: 1.18x slower                                                    |
| django_template            | 34.2 ms                                                                | 40.4 ms: 1.18x slower                                                    |
| genshi_text                | 21.7 ms                                                                | 25.8 ms: 1.18x slower                                                    |
| crypto_pyaes               | 68.2 ms                                                                | 81.8 ms: 1.20x slower                                                    |
| fannkuch                   | 376 ms                                                                 | 452 ms: 1.20x slower                                                     |
| typing_runtime_protocols   | 156 us                                                                 | 188 us: 1.21x slower                                                     |
| meteor_contest             | 101 ms                                                                 | 126 ms: 1.25x slower                                                     |
| nbody                      | 85.3 ms                                                                | 110 ms: 1.28x slower                                                     |
| coverage                   | 82.5 ms                                                                | 110 ms: 1.33x slower                                                     |
| mako                       | 11.2 ms                                                                | 15.2 ms: 1.36x slower                                                    |
| python_startup             | 11.0 ms                                                                | 15.8 ms: 1.43x slower                                                    |
| python_startup_no_site     | 7.41 ms                                                                | 11.1 ms: 1.50x slower                                                    |
| bench_thread_pool          | 924 us                                                                 | 3.13 ms: 3.39x slower                                                    |
| bench_mp_pool              | 11.0 ms                                                                | 96.0 ms: 8.72x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.04x slower                                                             |

Benchmark hidden because not significant (2): pylint, json
Ignored benchmarks (19) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250422-3.14.0a7+-986f23a-NOGIL/bm-20250422-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-986f23a.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.003x slower

# HPT report

- Reliability score: 84.06% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.36x