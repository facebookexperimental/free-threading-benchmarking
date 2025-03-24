# Results vs. 3.13.0rc2

- fork: python
- ref: bc26f95e8ff60ccca981
- machine: linux-x86_64
- commit hash: bc26f95
- commit date: 2025-03-22
- overall geometric mean: 1.079x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.37x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 300 ms: 1.16x slower                                                   |
| docutils       | 2.63 sec                                                               | 2.79 sec: 1.06x slower                                                 |
| html5lib       | 68.6 ms                                                                | 69.9 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.08x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 547 ms: 1.65x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 586 ms: 1.50x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 237 ms: 1.40x faster                                                   |
| async_tree_memoization     | 459 ms                                                                 | 330 ms: 1.39x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 298 ms: 1.37x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 276 ms: 1.28x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 505 ms: 1.26x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 540 ms: 1.23x faster                                                   |
| asyncio_websockets         | 517 ms                                                                 | 516 ms: 1.00x faster                                                   |
| coroutines                 | 23.3 ms                                                                | 23.7 ms: 1.02x slower                                                  |
| async_generators           | 375 ms                                                                 | 385 ms: 1.03x slower                                                   |
| asyncio_tcp                | 502 ms                                                                 | 538 ms: 1.07x slower                                                   |
| asyncio_tcp_ssl            | 1.51 sec                                                               | 1.79 sec: 1.18x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.19x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 200 ms: 1.08x faster                                                   |
| float          | 76.7 ms                                                                | 77.3 ms: 1.01x slower                                                  |
| nbody          | 85.3 ms                                                                | 138 ms: 1.62x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.15x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.64 ms: 1.22x faster                                                  |
| regex_v8       | 23.2 ms                                                                | 21.6 ms: 1.08x faster                                                  |
| regex_dna      | 189 ms                                                                 | 176 ms: 1.07x faster                                                   |
| regex_compile  | 131 ms                                                                 | 157 ms: 1.20x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 88.6 ms: 1.07x faster                                                  |
| xml_etree_parse      | 136 ms                                                                 | 129 ms: 1.06x faster                                                   |
| unpickle             | 14.6 us                                                                | 14.3 us: 1.02x faster                                                  |
| pickle               | 11.4 us                                                                | 12.1 us: 1.07x slower                                                  |
| pickle_list          | 4.81 us                                                                | 5.14 us: 1.07x slower                                                  |
| json_loads           | 27.3 us                                                                | 29.5 us: 1.08x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                                | 96.9 ms: 1.13x slower                                                  |
| unpickle_list        | 4.60 us                                                                | 5.36 us: 1.17x slower                                                  |
| tomli_loads          | 2.01 sec                                                               | 2.39 sec: 1.19x slower                                                 |
| xml_etree_process    | 59.2 ms                                                                | 70.6 ms: 1.19x slower                                                  |
| json_dumps           | 10.6 ms                                                                | 12.9 ms: 1.22x slower                                                  |
| pickle_pure_python   | 292 us                                                                 | 359 us: 1.23x slower                                                   |
| unpickle_pure_python | 208 us                                                                 | 257 us: 1.24x slower                                                   |
| Geometric mean       | (ref)                                                                  | 1.10x slower                                                           |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 15.8 ms: 1.44x slower                                                  |
| python_startup_no_site | 7.41 ms                                                                | 11.2 ms: 1.51x slower                                                  |
| Geometric mean         | (ref)                                                                  | 1.47x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 60.8 ms: 1.24x slower                                                  |
| django_template | 34.2 ms                                                                | 43.4 ms: 1.27x slower                                                  |
| genshi_text     | 21.7 ms                                                                | 28.6 ms: 1.32x slower                                                  |
| mako            | 11.2 ms                                                                | 16.1 ms: 1.43x slower                                                  |
| Geometric mean  | (ref)                                                                  | 1.31x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.81 ms: 1.84x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 547 ms: 1.65x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 586 ms: 1.50x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 237 ms: 1.40x faster                                                   |
| async_tree_memoization     | 459 ms                                                                 | 330 ms: 1.39x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 298 ms: 1.37x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 276 ms: 1.28x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 505 ms: 1.26x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 540 ms: 1.23x faster                                                   |
| regex_effbot               | 3.21 ms                                                                | 2.64 ms: 1.22x faster                                                  |
| deepcopy                   | 357 us                                                                 | 314 us: 1.14x faster                                                   |
| sqlite_synth               | 2.25 us                                                                | 2.02 us: 1.11x faster                                                  |
| pidigits                   | 216 ms                                                                 | 200 ms: 1.08x faster                                                   |
| regex_v8                   | 23.2 ms                                                                | 21.6 ms: 1.08x faster                                                  |
| regex_dna                  | 189 ms                                                                 | 176 ms: 1.07x faster                                                   |
| xml_etree_iterparse        | 94.4 ms                                                                | 88.6 ms: 1.07x faster                                                  |
| xml_etree_parse            | 136 ms                                                                 | 129 ms: 1.06x faster                                                   |
| unpickle                   | 14.6 us                                                                | 14.3 us: 1.02x faster                                                  |
| dulwich_log                | 74.5 ms                                                                | 73.9 ms: 1.01x faster                                                  |
| asyncio_websockets         | 517 ms                                                                 | 516 ms: 1.00x faster                                                   |
| float                      | 76.7 ms                                                                | 77.3 ms: 1.01x slower                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 3.15 us: 1.01x slower                                                  |
| coroutines                 | 23.3 ms                                                                | 23.7 ms: 1.02x slower                                                  |
| html5lib                   | 68.6 ms                                                                | 69.9 ms: 1.02x slower                                                  |
| async_generators           | 375 ms                                                                 | 385 ms: 1.03x slower                                                   |
| deepcopy_memo              | 38.1 us                                                                | 39.2 us: 1.03x slower                                                  |
| go                         | 141 ms                                                                 | 145 ms: 1.03x slower                                                   |
| json                       | 4.98 ms                                                                | 5.13 ms: 1.03x slower                                                  |
| create_gc_cycles           | 1.33 ms                                                                | 1.38 ms: 1.03x slower                                                  |
| scimark_sor                | 134 ms                                                                 | 138 ms: 1.03x slower                                                   |
| pathlib                    | 19.3 ms                                                                | 20.2 ms: 1.05x slower                                                  |
| docutils                   | 2.63 sec                                                               | 2.79 sec: 1.06x slower                                                 |
| pickle                     | 11.4 us                                                                | 12.1 us: 1.07x slower                                                  |
| pickle_list                | 4.81 us                                                                | 5.14 us: 1.07x slower                                                  |
| pycparser                  | 1.12 sec                                                               | 1.20 sec: 1.07x slower                                                 |
| asyncio_tcp                | 502 ms                                                                 | 538 ms: 1.07x slower                                                   |
| json_loads                 | 27.3 us                                                                | 29.5 us: 1.08x slower                                                  |
| spectral_norm              | 108 ms                                                                 | 117 ms: 1.08x slower                                                   |
| bpe_tokeniser              | 4.46 sec                                                               | 4.89 sec: 1.10x slower                                                 |
| pyflate                    | 449 ms                                                                 | 499 ms: 1.11x slower                                                   |
| mdp                        | 2.34 sec                                                               | 2.62 sec: 1.12x slower                                                 |
| generators                 | 28.5 ms                                                                | 32.0 ms: 1.12x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                                | 96.9 ms: 1.13x slower                                                  |
| thrift                     | 772 us                                                                 | 875 us: 1.13x slower                                                   |
| logging_silent             | 98.2 ns                                                                | 112 ns: 1.14x slower                                                   |
| telco                      | 7.77 ms                                                                | 8.93 ms: 1.15x slower                                                  |
| 2to3                       | 259 ms                                                                 | 300 ms: 1.16x slower                                                   |
| unpickle_list              | 4.60 us                                                                | 5.36 us: 1.17x slower                                                  |
| pprint_safe_repr           | 719 ms                                                                 | 839 ms: 1.17x slower                                                   |
| scimark_fft                | 348 ms                                                                 | 407 ms: 1.17x slower                                                   |
| asyncio_tcp_ssl            | 1.51 sec                                                               | 1.79 sec: 1.18x slower                                                 |
| tomli_loads                | 2.01 sec                                                               | 2.39 sec: 1.19x slower                                                 |
| pprint_pformat             | 1.46 sec                                                               | 1.73 sec: 1.19x slower                                                 |
| xml_etree_process          | 59.2 ms                                                                | 70.6 ms: 1.19x slower                                                  |
| regex_compile              | 131 ms                                                                 | 157 ms: 1.20x slower                                                   |
| logging_simple             | 6.14 us                                                                | 7.38 us: 1.20x slower                                                  |
| sympy_integrate            | 19.7 ms                                                                | 23.7 ms: 1.20x slower                                                  |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.75 ms: 1.21x slower                                                  |
| sympy_sum                  | 154 ms                                                                 | 187 ms: 1.21x slower                                                   |
| json_dumps                 | 10.6 ms                                                                | 12.9 ms: 1.22x slower                                                  |
| logging_format             | 6.92 us                                                                | 8.41 us: 1.22x slower                                                  |
| sympy_expand               | 454 ms                                                                 | 554 ms: 1.22x slower                                                   |
| sympy_str                  | 274 ms                                                                 | 336 ms: 1.23x slower                                                   |
| chaos                      | 56.3 ms                                                                | 69.2 ms: 1.23x slower                                                  |
| pickle_pure_python         | 292 us                                                                 | 359 us: 1.23x slower                                                   |
| unpickle_pure_python       | 208 us                                                                 | 257 us: 1.24x slower                                                   |
| genshi_xml                 | 49.1 ms                                                                | 60.8 ms: 1.24x slower                                                  |
| deltablue                  | 3.10 ms                                                                | 3.88 ms: 1.25x slower                                                  |
| richards                   | 44.4 ms                                                                | 55.7 ms: 1.25x slower                                                  |
| comprehensions             | 16.6 us                                                                | 20.8 us: 1.26x slower                                                  |
| django_template            | 34.2 ms                                                                | 43.4 ms: 1.27x slower                                                  |
| meteor_contest             | 101 ms                                                                 | 129 ms: 1.27x slower                                                   |
| scimark_lu                 | 112 ms                                                                 | 143 ms: 1.27x slower                                                   |
| nqueens                    | 77.7 ms                                                                | 99.5 ms: 1.28x slower                                                  |
| scimark_monte_carlo        | 65.8 ms                                                                | 84.3 ms: 1.28x slower                                                  |
| hexiom                     | 5.95 ms                                                                | 7.65 ms: 1.29x slower                                                  |
| typing_runtime_protocols   | 156 us                                                                 | 201 us: 1.29x slower                                                   |
| richards_super             | 50.4 ms                                                                | 65.2 ms: 1.29x slower                                                  |
| raytrace                   | 250 ms                                                                 | 325 ms: 1.30x slower                                                   |
| crypto_pyaes               | 68.2 ms                                                                | 88.8 ms: 1.30x slower                                                  |
| genshi_text                | 21.7 ms                                                                | 28.6 ms: 1.32x slower                                                  |
| coverage                   | 82.5 ms                                                                | 109 ms: 1.32x slower                                                   |
| fannkuch                   | 376 ms                                                                 | 501 ms: 1.33x slower                                                   |
| unpack_sequence            | 39.3 ns                                                                | 55.2 ns: 1.40x slower                                                  |
| mako                       | 11.2 ms                                                                | 16.1 ms: 1.43x slower                                                  |
| python_startup             | 11.0 ms                                                                | 15.8 ms: 1.44x slower                                                  |
| python_startup_no_site     | 7.41 ms                                                                | 11.2 ms: 1.51x slower                                                  |
| nbody                      | 85.3 ms                                                                | 138 ms: 1.62x slower                                                   |
| bench_thread_pool          | 924 us                                                                 | 3.17 ms: 3.43x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                                | 97.9 ms: 8.90x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.13x slower                                                           |

Benchmark hidden because not significant (2): pylint, pickle_dict
Ignored benchmarks (10) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250322-3.14.0a6+-bc26f95-NOGIL/bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.079x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.37x