# Results vs. 3.13.0rc2

- fork: nascheme
- ref: gh_127266_type_slots
- machine: linux-x86_64
- commit hash: 395a6d3
- commit date: 2025-04-01
- overall geometric mean: 1.116x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.07x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 314 ms: 1.21x slower                                                     |
| docutils       | 2.63 sec                                                               | 2.90 sec: 1.10x slower                                                   |
| html5lib       | 68.6 ms                                                                | 73.7 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.13x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 574 ms: 1.57x faster                                                     |
| async_tree_io              | 881 ms                                                                 | 604 ms: 1.46x faster                                                     |
| async_tree_memoization     | 459 ms                                                                 | 344 ms: 1.33x faster                                                     |
| async_tree_none_tg         | 333 ms                                                                 | 251 ms: 1.33x faster                                                     |
| async_tree_memoization_tg  | 410 ms                                                                 | 316 ms: 1.30x faster                                                     |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 491 ms: 1.29x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 521 ms: 1.28x faster                                                     |
| async_tree_none            | 353 ms                                                                 | 288 ms: 1.23x faster                                                     |
| async_generators           | 375 ms                                                                 | 388 ms: 1.04x slower                                                     |
| coroutines                 | 23.3 ms                                                                | 25.1 ms: 1.08x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.23x faster                                                             |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 195 ms: 1.11x faster                                                     |
| float          | 76.7 ms                                                                | 81.3 ms: 1.06x slower                                                    |
| nbody          | 85.3 ms                                                                | 148 ms: 1.74x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.18x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.77 ms: 1.16x faster                                                    |
| regex_dna      | 189 ms                                                                 | 173 ms: 1.09x faster                                                     |
| regex_v8       | 23.2 ms                                                                | 21.8 ms: 1.07x faster                                                    |
| regex_compile  | 131 ms                                                                 | 170 ms: 1.30x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                                 | 130 ms: 1.04x faster                                                     |
| xml_etree_iterparse  | 94.4 ms                                                                | 93.6 ms: 1.01x faster                                                    |
| json_loads           | 27.3 us                                                                | 30.7 us: 1.12x slower                                                    |
| xml_etree_generate   | 85.4 ms                                                                | 102 ms: 1.20x slower                                                     |
| json_dumps           | 10.6 ms                                                                | 13.1 ms: 1.23x slower                                                    |
| xml_etree_process    | 59.2 ms                                                                | 74.6 ms: 1.26x slower                                                    |
| tomli_loads          | 2.01 sec                                                               | 2.56 sec: 1.27x slower                                                   |
| unpickle_pure_python | 208 us                                                                 | 279 us: 1.34x slower                                                     |
| pickle_pure_python   | 292 us                                                                 | 393 us: 1.35x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.18x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 15.8 ms: 1.43x slower                                                    |
| python_startup_no_site | 7.41 ms                                                                | 11.1 ms: 1.50x slower                                                    |
| Geometric mean         | (ref)                                                                  | 1.47x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| django_template | 34.2 ms                                                                | 45.1 ms: 1.32x slower                                                    |
| genshi_xml      | 49.1 ms                                                                | 66.4 ms: 1.35x slower                                                    |
| genshi_text     | 21.7 ms                                                                | 31.0 ms: 1.43x slower                                                    |
| mako            | 11.2 ms                                                                | 16.5 ms: 1.47x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.39x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.80 ms: 1.85x faster                                                    |
| mdp                        | 2.34 sec                                                               | 1.47 sec: 1.60x faster                                                   |
| async_tree_io_tg           | 901 ms                                                                 | 574 ms: 1.57x faster                                                     |
| async_tree_io              | 881 ms                                                                 | 604 ms: 1.46x faster                                                     |
| async_tree_memoization     | 459 ms                                                                 | 344 ms: 1.33x faster                                                     |
| async_tree_none_tg         | 333 ms                                                                 | 251 ms: 1.33x faster                                                     |
| async_tree_memoization_tg  | 410 ms                                                                 | 316 ms: 1.30x faster                                                     |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 491 ms: 1.29x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 521 ms: 1.28x faster                                                     |
| async_tree_none            | 353 ms                                                                 | 288 ms: 1.23x faster                                                     |
| regex_effbot               | 3.21 ms                                                                | 2.77 ms: 1.16x faster                                                    |
| pidigits                   | 216 ms                                                                 | 195 ms: 1.11x faster                                                     |
| regex_dna                  | 189 ms                                                                 | 173 ms: 1.09x faster                                                     |
| sqlite_synth               | 2.25 us                                                                | 2.08 us: 1.08x faster                                                    |
| regex_v8                   | 23.2 ms                                                                | 21.8 ms: 1.07x faster                                                    |
| deepcopy                   | 357 us                                                                 | 338 us: 1.06x faster                                                     |
| xml_etree_parse            | 136 ms                                                                 | 130 ms: 1.04x faster                                                     |
| xml_etree_iterparse        | 94.4 ms                                                                | 93.6 ms: 1.01x faster                                                    |
| create_gc_cycles           | 1.33 ms                                                                | 1.36 ms: 1.02x slower                                                    |
| pathlib                    | 19.3 ms                                                                | 19.7 ms: 1.02x slower                                                    |
| async_generators           | 375 ms                                                                 | 388 ms: 1.04x slower                                                     |
| dulwich_log                | 74.5 ms                                                                | 77.3 ms: 1.04x slower                                                    |
| float                      | 76.7 ms                                                                | 81.3 ms: 1.06x slower                                                    |
| json                       | 4.98 ms                                                                | 5.34 ms: 1.07x slower                                                    |
| html5lib                   | 68.6 ms                                                                | 73.7 ms: 1.07x slower                                                    |
| coroutines                 | 23.3 ms                                                                | 25.1 ms: 1.08x slower                                                    |
| deepcopy_reduce            | 3.12 us                                                                | 3.37 us: 1.08x slower                                                    |
| docutils                   | 2.63 sec                                                               | 2.90 sec: 1.10x slower                                                   |
| spectral_norm              | 108 ms                                                                 | 120 ms: 1.11x slower                                                     |
| go                         | 141 ms                                                                 | 157 ms: 1.12x slower                                                     |
| deepcopy_memo              | 38.1 us                                                                | 42.7 us: 1.12x slower                                                    |
| json_loads                 | 27.3 us                                                                | 30.7 us: 1.12x slower                                                    |
| bpe_tokeniser              | 4.46 sec                                                               | 5.03 sec: 1.13x slower                                                   |
| pycparser                  | 1.12 sec                                                               | 1.27 sec: 1.13x slower                                                   |
| telco                      | 7.77 ms                                                                | 8.97 ms: 1.15x slower                                                    |
| scimark_fft                | 348 ms                                                                 | 411 ms: 1.18x slower                                                     |
| xml_etree_generate         | 85.4 ms                                                                | 102 ms: 1.20x slower                                                     |
| pyflate                    | 449 ms                                                                 | 541 ms: 1.21x slower                                                     |
| 2to3                       | 259 ms                                                                 | 314 ms: 1.21x slower                                                     |
| json_dumps                 | 10.6 ms                                                                | 13.1 ms: 1.23x slower                                                    |
| scimark_sor                | 134 ms                                                                 | 165 ms: 1.24x slower                                                     |
| sympy_integrate            | 19.7 ms                                                                | 24.5 ms: 1.24x slower                                                    |
| pprint_safe_repr           | 719 ms                                                                 | 896 ms: 1.25x slower                                                     |
| xml_etree_process          | 59.2 ms                                                                | 74.6 ms: 1.26x slower                                                    |
| sympy_sum                  | 154 ms                                                                 | 195 ms: 1.27x slower                                                     |
| tomli_loads                | 2.01 sec                                                               | 2.56 sec: 1.27x slower                                                   |
| pprint_pformat             | 1.46 sec                                                               | 1.86 sec: 1.28x slower                                                   |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 6.10 ms: 1.28x slower                                                    |
| logging_silent             | 98.2 ns                                                                | 126 ns: 1.28x slower                                                     |
| sympy_str                  | 274 ms                                                                 | 355 ms: 1.30x slower                                                     |
| regex_compile              | 131 ms                                                                 | 170 ms: 1.30x slower                                                     |
| sympy_expand               | 454 ms                                                                 | 595 ms: 1.31x slower                                                     |
| django_template            | 34.2 ms                                                                | 45.1 ms: 1.32x slower                                                    |
| nqueens                    | 77.7 ms                                                                | 103 ms: 1.32x slower                                                     |
| coverage                   | 82.5 ms                                                                | 110 ms: 1.33x slower                                                     |
| chaos                      | 56.3 ms                                                                | 75.2 ms: 1.34x slower                                                    |
| typing_runtime_protocols   | 156 us                                                                 | 208 us: 1.34x slower                                                     |
| unpickle_pure_python       | 208 us                                                                 | 279 us: 1.34x slower                                                     |
| generators                 | 28.5 ms                                                                | 38.4 ms: 1.35x slower                                                    |
| pickle_pure_python         | 292 us                                                                 | 393 us: 1.35x slower                                                     |
| logging_simple             | 6.14 us                                                                | 8.30 us: 1.35x slower                                                    |
| comprehensions             | 16.6 us                                                                | 22.4 us: 1.35x slower                                                    |
| genshi_xml                 | 49.1 ms                                                                | 66.4 ms: 1.35x slower                                                    |
| meteor_contest             | 101 ms                                                                 | 138 ms: 1.36x slower                                                     |
| scimark_lu                 | 112 ms                                                                 | 153 ms: 1.36x slower                                                     |
| logging_format             | 6.92 us                                                                | 9.41 us: 1.36x slower                                                    |
| richards_super             | 50.4 ms                                                                | 68.9 ms: 1.37x slower                                                    |
| hexiom                     | 5.95 ms                                                                | 8.14 ms: 1.37x slower                                                    |
| richards                   | 44.4 ms                                                                | 61.0 ms: 1.37x slower                                                    |
| scimark_monte_carlo        | 65.8 ms                                                                | 90.9 ms: 1.38x slower                                                    |
| crypto_pyaes               | 68.2 ms                                                                | 94.3 ms: 1.38x slower                                                    |
| raytrace                   | 250 ms                                                                 | 353 ms: 1.41x slower                                                     |
| fannkuch                   | 376 ms                                                                 | 536 ms: 1.43x slower                                                     |
| genshi_text                | 21.7 ms                                                                | 31.0 ms: 1.43x slower                                                    |
| python_startup             | 11.0 ms                                                                | 15.8 ms: 1.43x slower                                                    |
| deltablue                  | 3.10 ms                                                                | 4.55 ms: 1.47x slower                                                    |
| mako                       | 11.2 ms                                                                | 16.5 ms: 1.47x slower                                                    |
| python_startup_no_site     | 7.41 ms                                                                | 11.1 ms: 1.50x slower                                                    |
| nbody                      | 85.3 ms                                                                | 148 ms: 1.74x slower                                                     |
| bench_thread_pool          | 924 us                                                                 | 3.20 ms: 3.46x slower                                                    |
| bench_mp_pool              | 11.0 ms                                                                | 97.9 ms: 8.90x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.18x slower                                                             |

Benchmark hidden because not significant (2): asyncio_websockets, pylint
Ignored benchmarks (19) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250401-3.14.0a6+-395a6d3-NOGIL/bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.116x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.12x
- 95% likely to have a slowdown of 1.11x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 1.36x