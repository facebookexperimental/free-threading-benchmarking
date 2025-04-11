# Results vs. 3.13.0rc2

- fork: nascheme
- ref: gh_127266_type_slots
- machine: linux-x86_64
- commit hash: 57c2a44
- commit date: 2025-04-10
- overall geometric mean: 1.124x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.09x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250410-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-57c2a44 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 316 ms: 1.22x slower                                                     |
| docutils       | 2.63 sec                                                               | 2.91 sec: 1.11x slower                                                   |
| html5lib       | 68.6 ms                                                                | 76.9 ms: 1.12x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.15x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250410-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-57c2a44 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 580 ms: 1.55x faster                                                     |
| async_tree_io              | 881 ms                                                                 | 613 ms: 1.44x faster                                                     |
| async_tree_memoization     | 459 ms                                                                 | 349 ms: 1.32x faster                                                     |
| async_tree_none_tg         | 333 ms                                                                 | 255 ms: 1.30x faster                                                     |
| async_tree_memoization_tg  | 410 ms                                                                 | 320 ms: 1.28x faster                                                     |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 520 ms: 1.22x faster                                                     |
| async_tree_none            | 353 ms                                                                 | 290 ms: 1.22x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 551 ms: 1.21x faster                                                     |
| async_generators           | 375 ms                                                                 | 389 ms: 1.04x slower                                                     |
| coroutines                 | 23.3 ms                                                                | 25.6 ms: 1.10x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.20x faster                                                             |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250410-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-57c2a44 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 202 ms: 1.07x faster                                                     |
| float          | 76.7 ms                                                                | 84.0 ms: 1.09x slower                                                    |
| nbody          | 85.3 ms                                                                | 152 ms: 1.78x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.22x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250410-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-57c2a44 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.77 ms: 1.16x faster                                                    |
| regex_v8       | 23.2 ms                                                                | 21.1 ms: 1.10x faster                                                    |
| regex_dna      | 189 ms                                                                 | 181 ms: 1.04x faster                                                     |
| regex_compile  | 131 ms                                                                 | 173 ms: 1.32x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250410-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-57c2a44 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                                 | 130 ms: 1.04x faster                                                     |
| xml_etree_iterparse  | 94.4 ms                                                                | 92.9 ms: 1.02x faster                                                    |
| json_loads           | 27.3 us                                                                | 30.9 us: 1.13x slower                                                    |
| xml_etree_generate   | 85.4 ms                                                                | 102 ms: 1.19x slower                                                     |
| json_dumps           | 10.6 ms                                                                | 13.1 ms: 1.23x slower                                                    |
| xml_etree_process    | 59.2 ms                                                                | 74.4 ms: 1.26x slower                                                    |
| tomli_loads          | 2.01 sec                                                               | 2.62 sec: 1.30x slower                                                   |
| unpickle_pure_python | 208 us                                                                 | 282 us: 1.36x slower                                                     |
| pickle_pure_python   | 292 us                                                                 | 399 us: 1.37x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.19x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250410-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-57c2a44 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 15.9 ms: 1.44x slower                                                    |
| python_startup_no_site | 7.41 ms                                                                | 11.2 ms: 1.51x slower                                                    |
| Geometric mean         | (ref)                                                                  | 1.47x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250410-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-57c2a44 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| django_template | 34.2 ms                                                                | 45.4 ms: 1.33x slower                                                    |
| genshi_xml      | 49.1 ms                                                                | 67.4 ms: 1.37x slower                                                    |
| genshi_text     | 21.7 ms                                                                | 31.6 ms: 1.45x slower                                                    |
| mako            | 11.2 ms                                                                | 16.6 ms: 1.48x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.41x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250410-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-57c2a44 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.81 ms: 1.83x faster                                                    |
| mdp                        | 2.34 sec                                                               | 1.46 sec: 1.61x faster                                                   |
| async_tree_io_tg           | 901 ms                                                                 | 580 ms: 1.55x faster                                                     |
| async_tree_io              | 881 ms                                                                 | 613 ms: 1.44x faster                                                     |
| async_tree_memoization     | 459 ms                                                                 | 349 ms: 1.32x faster                                                     |
| async_tree_none_tg         | 333 ms                                                                 | 255 ms: 1.30x faster                                                     |
| async_tree_memoization_tg  | 410 ms                                                                 | 320 ms: 1.28x faster                                                     |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 520 ms: 1.22x faster                                                     |
| async_tree_none            | 353 ms                                                                 | 290 ms: 1.22x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 551 ms: 1.21x faster                                                     |
| regex_effbot               | 3.21 ms                                                                | 2.77 ms: 1.16x faster                                                    |
| regex_v8                   | 23.2 ms                                                                | 21.1 ms: 1.10x faster                                                    |
| sqlite_synth               | 2.25 us                                                                | 2.07 us: 1.09x faster                                                    |
| pidigits                   | 216 ms                                                                 | 202 ms: 1.07x faster                                                     |
| deepcopy                   | 357 us                                                                 | 339 us: 1.06x faster                                                     |
| xml_etree_parse            | 136 ms                                                                 | 130 ms: 1.04x faster                                                     |
| regex_dna                  | 189 ms                                                                 | 181 ms: 1.04x faster                                                     |
| xml_etree_iterparse        | 94.4 ms                                                                | 92.9 ms: 1.02x faster                                                    |
| pathlib                    | 19.3 ms                                                                | 19.8 ms: 1.03x slower                                                    |
| async_generators           | 375 ms                                                                 | 389 ms: 1.04x slower                                                     |
| create_gc_cycles           | 1.33 ms                                                                | 1.39 ms: 1.04x slower                                                    |
| dulwich_log                | 74.5 ms                                                                | 77.7 ms: 1.04x slower                                                    |
| json                       | 4.98 ms                                                                | 5.32 ms: 1.07x slower                                                    |
| float                      | 76.7 ms                                                                | 84.0 ms: 1.09x slower                                                    |
| coroutines                 | 23.3 ms                                                                | 25.6 ms: 1.10x slower                                                    |
| deepcopy_reduce            | 3.12 us                                                                | 3.45 us: 1.11x slower                                                    |
| docutils                   | 2.63 sec                                                               | 2.91 sec: 1.11x slower                                                   |
| html5lib                   | 68.6 ms                                                                | 76.9 ms: 1.12x slower                                                    |
| deepcopy_memo              | 38.1 us                                                                | 42.8 us: 1.13x slower                                                    |
| bpe_tokeniser              | 4.46 sec                                                               | 5.02 sec: 1.13x slower                                                   |
| pycparser                  | 1.12 sec                                                               | 1.26 sec: 1.13x slower                                                   |
| json_loads                 | 27.3 us                                                                | 30.9 us: 1.13x slower                                                    |
| spectral_norm              | 108 ms                                                                 | 122 ms: 1.13x slower                                                     |
| go                         | 141 ms                                                                 | 161 ms: 1.14x slower                                                     |
| telco                      | 7.77 ms                                                                | 9.00 ms: 1.16x slower                                                    |
| scimark_fft                | 348 ms                                                                 | 412 ms: 1.18x slower                                                     |
| xml_etree_generate         | 85.4 ms                                                                | 102 ms: 1.19x slower                                                     |
| 2to3                       | 259 ms                                                                 | 316 ms: 1.22x slower                                                     |
| pyflate                    | 449 ms                                                                 | 553 ms: 1.23x slower                                                     |
| json_dumps                 | 10.6 ms                                                                | 13.1 ms: 1.23x slower                                                    |
| scimark_sor                | 134 ms                                                                 | 165 ms: 1.24x slower                                                     |
| sympy_integrate            | 19.7 ms                                                                | 24.6 ms: 1.25x slower                                                    |
| pprint_safe_repr           | 719 ms                                                                 | 901 ms: 1.25x slower                                                     |
| xml_etree_process          | 59.2 ms                                                                | 74.4 ms: 1.26x slower                                                    |
| sympy_sum                  | 154 ms                                                                 | 196 ms: 1.27x slower                                                     |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 6.04 ms: 1.27x slower                                                    |
| pprint_pformat             | 1.46 sec                                                               | 1.87 sec: 1.28x slower                                                   |
| sympy_str                  | 274 ms                                                                 | 352 ms: 1.29x slower                                                     |
| sympy_expand               | 454 ms                                                                 | 590 ms: 1.30x slower                                                     |
| tomli_loads                | 2.01 sec                                                               | 2.62 sec: 1.30x slower                                                   |
| nqueens                    | 77.7 ms                                                                | 102 ms: 1.31x slower                                                     |
| regex_compile              | 131 ms                                                                 | 173 ms: 1.32x slower                                                     |
| typing_runtime_protocols   | 156 us                                                                 | 206 us: 1.33x slower                                                     |
| django_template            | 34.2 ms                                                                | 45.4 ms: 1.33x slower                                                    |
| logging_silent             | 98.2 ns                                                                | 131 ns: 1.33x slower                                                     |
| coverage                   | 82.5 ms                                                                | 111 ms: 1.34x slower                                                     |
| generators                 | 28.5 ms                                                                | 38.4 ms: 1.35x slower                                                    |
| unpickle_pure_python       | 208 us                                                                 | 282 us: 1.36x slower                                                     |
| comprehensions             | 16.6 us                                                                | 22.5 us: 1.36x slower                                                    |
| scimark_lu                 | 112 ms                                                                 | 153 ms: 1.36x slower                                                     |
| pickle_pure_python         | 292 us                                                                 | 399 us: 1.37x slower                                                     |
| logging_simple             | 6.14 us                                                                | 8.40 us: 1.37x slower                                                    |
| logging_format             | 6.92 us                                                                | 9.47 us: 1.37x slower                                                    |
| chaos                      | 56.3 ms                                                                | 77.2 ms: 1.37x slower                                                    |
| genshi_xml                 | 49.1 ms                                                                | 67.4 ms: 1.37x slower                                                    |
| crypto_pyaes               | 68.2 ms                                                                | 94.0 ms: 1.38x slower                                                    |
| meteor_contest             | 101 ms                                                                 | 140 ms: 1.38x slower                                                     |
| hexiom                     | 5.95 ms                                                                | 8.25 ms: 1.39x slower                                                    |
| scimark_monte_carlo        | 65.8 ms                                                                | 91.3 ms: 1.39x slower                                                    |
| richards_super             | 50.4 ms                                                                | 70.1 ms: 1.39x slower                                                    |
| richards                   | 44.4 ms                                                                | 62.1 ms: 1.40x slower                                                    |
| raytrace                   | 250 ms                                                                 | 356 ms: 1.42x slower                                                     |
| python_startup             | 11.0 ms                                                                | 15.9 ms: 1.44x slower                                                    |
| fannkuch                   | 376 ms                                                                 | 542 ms: 1.44x slower                                                     |
| genshi_text                | 21.7 ms                                                                | 31.6 ms: 1.45x slower                                                    |
| mako                       | 11.2 ms                                                                | 16.6 ms: 1.48x slower                                                    |
| deltablue                  | 3.10 ms                                                                | 4.64 ms: 1.50x slower                                                    |
| python_startup_no_site     | 7.41 ms                                                                | 11.2 ms: 1.51x slower                                                    |
| nbody                      | 85.3 ms                                                                | 152 ms: 1.78x slower                                                     |
| bench_thread_pool          | 924 us                                                                 | 3.20 ms: 3.46x slower                                                    |
| bench_mp_pool              | 11.0 ms                                                                | 98.6 ms: 8.97x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.19x slower                                                             |

Benchmark hidden because not significant (2): asyncio_websockets, pylint
Ignored benchmarks (19) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250410-3.14.0a6+-57c2a44-NOGIL/bm-20250410-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-57c2a44.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.124x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.12x
- 95% likely to have a slowdown of 1.12x
- 99% likely to have a slowdown of 1.09x

# Memory
- memory change: 1.36x