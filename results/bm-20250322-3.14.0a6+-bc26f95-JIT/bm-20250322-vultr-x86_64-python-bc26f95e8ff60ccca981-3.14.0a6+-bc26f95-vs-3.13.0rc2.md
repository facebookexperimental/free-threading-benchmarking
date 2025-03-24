# Results vs. 3.13.0rc2

- fork: python
- ref: bc26f95e8ff60ccca981
- machine: linux-x86_64
- commit hash: bc26f95
- commit date: 2025-03-22
- overall geometric mean: 1.055x faster
- HPT reliability: 99.78%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 260 ms: 1.00x slower                                                   |
| docutils       | 2.63 sec                                                               | 2.64 sec: 1.01x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_memoization     | 459 ms                                                                 | 312 ms: 1.47x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 616 ms: 1.43x faster                                                   |
| async_tree_io_tg           | 901 ms                                                                 | 630 ms: 1.43x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 303 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 500 ms: 1.33x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 253 ms: 1.31x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 485 ms: 1.31x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 272 ms: 1.30x faster                                                   |
| async_generators           | 375 ms                                                                 | 354 ms: 1.06x faster                                                   |
| coroutines                 | 23.3 ms                                                                | 22.7 ms: 1.03x faster                                                  |
| Geometric mean             | (ref)                                                                  | 1.22x faster                                                           |

Benchmark hidden because not significant (3): asyncio_tcp, asyncio_websockets, asyncio_tcp_ssl

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 76.7 ms                                                                | 66.3 ms: 1.16x faster                                                  |
| pidigits       | 216 ms                                                                 | 192 ms: 1.13x faster                                                   |
| nbody          | 85.3 ms                                                                | 82.7 ms: 1.03x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.11x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.72 ms: 1.18x faster                                                  |
| regex_dna      | 189 ms                                                                 | 175 ms: 1.08x faster                                                   |
| regex_v8       | 23.2 ms                                                                | 21.7 ms: 1.07x faster                                                  |
| regex_compile  | 131 ms                                                                 | 127 ms: 1.03x faster                                                   |
| Geometric mean | (ref)                                                                  | 1.09x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| unpickle             | 14.6 us                                                                | 13.3 us: 1.10x faster                                                  |
| tomli_loads          | 2.01 sec                                                               | 1.84 sec: 1.09x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                                | 79.8 ms: 1.07x faster                                                  |
| pickle_dict          | 32.7 us                                                                | 30.8 us: 1.06x faster                                                  |
| xml_etree_process    | 59.2 ms                                                                | 55.8 ms: 1.06x faster                                                  |
| xml_etree_parse      | 136 ms                                                                 | 130 ms: 1.05x faster                                                   |
| xml_etree_iterparse  | 94.4 ms                                                                | 91.1 ms: 1.04x faster                                                  |
| unpickle_pure_python | 208 us                                                                 | 205 us: 1.02x faster                                                   |
| json_loads           | 27.3 us                                                                | 28.0 us: 1.02x slower                                                  |
| pickle_list          | 4.81 us                                                                | 5.00 us: 1.04x slower                                                  |
| unpickle_list        | 4.60 us                                                                | 4.79 us: 1.04x slower                                                  |
| pickle               | 11.4 us                                                                | 12.1 us: 1.06x slower                                                  |
| pickle_pure_python   | 292 us                                                                 | 312 us: 1.07x slower                                                   |
| json_dumps           | 10.6 ms                                                                | 11.4 ms: 1.07x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 8.65 ms: 1.17x slower                                                  |
| python_startup         | 11.0 ms                                                                | 15.0 ms: 1.36x slower                                                  |
| Geometric mean         | (ref)                                                                  | 1.26x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 21.7 ms                                                                | 20.7 ms: 1.05x faster                                                  |
| genshi_xml      | 49.1 ms                                                                | 49.3 ms: 1.00x slower                                                  |
| mako            | 11.2 ms                                                                | 11.5 ms: 1.02x slower                                                  |
| django_template | 34.2 ms                                                                | 35.0 ms: 1.02x slower                                                  |
| Geometric mean  | (ref)                                                                  | 1.00x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_memoization     | 459 ms                                                                 | 312 ms: 1.47x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 616 ms: 1.43x faster                                                   |
| async_tree_io_tg           | 901 ms                                                                 | 630 ms: 1.43x faster                                                   |
| deepcopy                   | 357 us                                                                 | 252 us: 1.42x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 303 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 500 ms: 1.33x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 253 ms: 1.31x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 485 ms: 1.31x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 272 ms: 1.30x faster                                                   |
| richards                   | 44.4 ms                                                                | 34.9 ms: 1.27x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 30.0 us: 1.27x faster                                                  |
| richards_super             | 50.4 ms                                                                | 40.7 ms: 1.24x faster                                                  |
| scimark_fft                | 348 ms                                                                 | 285 ms: 1.22x faster                                                   |
| spectral_norm              | 108 ms                                                                 | 88.0 ms: 1.22x faster                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 2.59 us: 1.21x faster                                                  |
| scimark_sor                | 134 ms                                                                 | 112 ms: 1.19x faster                                                   |
| regex_effbot               | 3.21 ms                                                                | 2.72 ms: 1.18x faster                                                  |
| float                      | 76.7 ms                                                                | 66.3 ms: 1.16x faster                                                  |
| pidigits                   | 216 ms                                                                 | 192 ms: 1.13x faster                                                   |
| pylint                     | 317 ms                                                                 | 282 ms: 1.12x faster                                                   |
| dulwich_log                | 74.5 ms                                                                | 67.2 ms: 1.11x faster                                                  |
| pyflate                    | 449 ms                                                                 | 408 ms: 1.10x faster                                                   |
| go                         | 141 ms                                                                 | 128 ms: 1.10x faster                                                   |
| unpickle                   | 14.6 us                                                                | 13.3 us: 1.10x faster                                                  |
| telco                      | 7.77 ms                                                                | 7.12 ms: 1.09x faster                                                  |
| tomli_loads                | 2.01 sec                                                               | 1.84 sec: 1.09x faster                                                 |
| regex_dna                  | 189 ms                                                                 | 175 ms: 1.08x faster                                                   |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.42 ms: 1.08x faster                                                  |
| xml_etree_generate         | 85.4 ms                                                                | 79.8 ms: 1.07x faster                                                  |
| regex_v8                   | 23.2 ms                                                                | 21.7 ms: 1.07x faster                                                  |
| pickle_dict                | 32.7 us                                                                | 30.8 us: 1.06x faster                                                  |
| xml_etree_process          | 59.2 ms                                                                | 55.8 ms: 1.06x faster                                                  |
| deltablue                  | 3.10 ms                                                                | 2.92 ms: 1.06x faster                                                  |
| async_generators           | 375 ms                                                                 | 354 ms: 1.06x faster                                                   |
| sqlite_synth               | 2.25 us                                                                | 2.13 us: 1.06x faster                                                  |
| bpe_tokeniser              | 4.46 sec                                                               | 4.23 sec: 1.05x faster                                                 |
| logging_format             | 6.92 us                                                                | 6.57 us: 1.05x faster                                                  |
| genshi_text                | 21.7 ms                                                                | 20.7 ms: 1.05x faster                                                  |
| xml_etree_parse            | 136 ms                                                                 | 130 ms: 1.05x faster                                                   |
| generators                 | 28.5 ms                                                                | 27.3 ms: 1.05x faster                                                  |
| logging_simple             | 6.14 us                                                                | 5.88 us: 1.04x faster                                                  |
| coverage                   | 82.5 ms                                                                | 79.1 ms: 1.04x faster                                                  |
| xml_etree_iterparse        | 94.4 ms                                                                | 91.1 ms: 1.04x faster                                                  |
| regex_compile              | 131 ms                                                                 | 127 ms: 1.03x faster                                                   |
| nbody                      | 85.3 ms                                                                | 82.7 ms: 1.03x faster                                                  |
| scimark_monte_carlo        | 65.8 ms                                                                | 64.0 ms: 1.03x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 22.7 ms: 1.03x faster                                                  |
| json                       | 4.98 ms                                                                | 4.90 ms: 1.02x faster                                                  |
| unpickle_pure_python       | 208 us                                                                 | 205 us: 1.02x faster                                                   |
| logging_silent             | 98.2 ns                                                                | 97.9 ns: 1.00x faster                                                  |
| mdp                        | 2.34 sec                                                               | 2.33 sec: 1.00x faster                                                 |
| 2to3                       | 259 ms                                                                 | 260 ms: 1.00x slower                                                   |
| genshi_xml                 | 49.1 ms                                                                | 49.3 ms: 1.00x slower                                                  |
| docutils                   | 2.63 sec                                                               | 2.64 sec: 1.01x slower                                                 |
| pathlib                    | 19.3 ms                                                                | 19.4 ms: 1.01x slower                                                  |
| meteor_contest             | 101 ms                                                                 | 102 ms: 1.01x slower                                                   |
| fannkuch                   | 376 ms                                                                 | 380 ms: 1.01x slower                                                   |
| sympy_sum                  | 154 ms                                                                 | 157 ms: 1.01x slower                                                   |
| chaos                      | 56.3 ms                                                                | 57.1 ms: 1.01x slower                                                  |
| scimark_lu                 | 112 ms                                                                 | 114 ms: 1.02x slower                                                   |
| sympy_str                  | 274 ms                                                                 | 278 ms: 1.02x slower                                                   |
| mako                       | 11.2 ms                                                                | 11.5 ms: 1.02x slower                                                  |
| json_loads                 | 27.3 us                                                                | 28.0 us: 1.02x slower                                                  |
| django_template            | 34.2 ms                                                                | 35.0 ms: 1.02x slower                                                  |
| pycparser                  | 1.12 sec                                                               | 1.15 sec: 1.03x slower                                                 |
| nqueens                    | 77.7 ms                                                                | 80.4 ms: 1.03x slower                                                  |
| pickle_list                | 4.81 us                                                                | 5.00 us: 1.04x slower                                                  |
| unpickle_list              | 4.60 us                                                                | 4.79 us: 1.04x slower                                                  |
| crypto_pyaes               | 68.2 ms                                                                | 71.4 ms: 1.05x slower                                                  |
| raytrace                   | 250 ms                                                                 | 263 ms: 1.05x slower                                                   |
| sympy_expand               | 454 ms                                                                 | 478 ms: 1.05x slower                                                   |
| pickle                     | 11.4 us                                                                | 12.1 us: 1.06x slower                                                  |
| pickle_pure_python         | 292 us                                                                 | 312 us: 1.07x slower                                                   |
| json_dumps                 | 10.6 ms                                                                | 11.4 ms: 1.07x slower                                                  |
| pprint_safe_repr           | 719 ms                                                                 | 795 ms: 1.11x slower                                                   |
| comprehensions             | 16.6 us                                                                | 18.4 us: 1.11x slower                                                  |
| hexiom                     | 5.95 ms                                                                | 6.61 ms: 1.11x slower                                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.62 sec: 1.12x slower                                                 |
| bench_thread_pool          | 924 us                                                                 | 1.06 ms: 1.14x slower                                                  |
| python_startup_no_site     | 7.41 ms                                                                | 8.65 ms: 1.17x slower                                                  |
| gc_traversal               | 3.32 ms                                                                | 4.24 ms: 1.28x slower                                                  |
| python_startup             | 11.0 ms                                                                | 15.0 ms: 1.36x slower                                                  |
| create_gc_cycles           | 1.33 ms                                                                | 1.84 ms: 1.38x slower                                                  |
| unpack_sequence            | 39.3 ns                                                                | 66.0 ns: 1.68x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                                | 89.9 ms: 8.17x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.02x faster                                                           |

Benchmark hidden because not significant (6): asyncio_tcp, asyncio_websockets, thrift, asyncio_tcp_ssl, sympy_integrate, typing_runtime_protocols
Ignored benchmarks (11) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, html5lib, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250322-3.14.0a6+-bc26f95-JIT/bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.055x faster

# HPT report

- Reliability score: 99.78% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.13x