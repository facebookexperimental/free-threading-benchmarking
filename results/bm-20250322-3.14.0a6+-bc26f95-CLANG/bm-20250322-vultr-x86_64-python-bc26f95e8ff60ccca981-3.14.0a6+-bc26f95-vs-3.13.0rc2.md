# Results vs. 3.13.0rc2

- fork: python
- ref: bc26f95e8ff60ccca981
- machine: linux-x86_64
- commit hash: bc26f95
- commit date: 2025-03-22
- overall geometric mean: 1.103x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 244 ms: 1.06x faster                                                   |
| docutils       | 2.63 sec                                                               | 2.51 sec: 1.05x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_memoization     | 459 ms                                                                 | 295 ms: 1.56x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 583 ms: 1.51x faster                                                   |
| async_tree_io_tg           | 901 ms                                                                 | 601 ms: 1.50x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 285 ms: 1.44x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 468 ms: 1.42x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 449 ms: 1.41x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 239 ms: 1.39x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 256 ms: 1.38x faster                                                   |
| async_generators           | 375 ms                                                                 | 315 ms: 1.19x faster                                                   |
| coroutines                 | 23.3 ms                                                                | 20.6 ms: 1.13x faster                                                  |
| asyncio_tcp                | 502 ms                                                                 | 492 ms: 1.02x faster                                                   |
| asyncio_tcp_ssl            | 1.51 sec                                                               | 1.50 sec: 1.01x faster                                                 |
| Geometric mean             | (ref)                                                                  | 1.29x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 191 ms: 1.13x faster                                                   |
| float          | 76.7 ms                                                                | 69.4 ms: 1.11x faster                                                  |
| nbody          | 85.3 ms                                                                | 79.6 ms: 1.07x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.10x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 131 ms                                                                 | 123 ms: 1.07x faster                                                   |
| regex_v8       | 23.2 ms                                                                | 22.0 ms: 1.05x faster                                                  |
| regex_effbot   | 3.21 ms                                                                | 3.10 ms: 1.04x faster                                                  |
| regex_dna      | 189 ms                                                                 | 185 ms: 1.02x faster                                                   |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                               | 1.80 sec: 1.12x faster                                                 |
| unpickle             | 14.6 us                                                                | 13.3 us: 1.10x faster                                                  |
| unpickle_list        | 4.60 us                                                                | 4.24 us: 1.09x faster                                                  |
| xml_etree_process    | 59.2 ms                                                                | 54.7 ms: 1.08x faster                                                  |
| xml_etree_generate   | 85.4 ms                                                                | 80.0 ms: 1.07x faster                                                  |
| json_loads           | 27.3 us                                                                | 26.1 us: 1.05x faster                                                  |
| pickle_dict          | 32.7 us                                                                | 31.5 us: 1.04x faster                                                  |
| unpickle_pure_python | 208 us                                                                 | 202 us: 1.03x faster                                                   |
| xml_etree_iterparse  | 94.4 ms                                                                | 93.9 ms: 1.00x faster                                                  |
| pickle_pure_python   | 292 us                                                                 | 294 us: 1.01x slower                                                   |
| pickle_list          | 4.81 us                                                                | 4.97 us: 1.03x slower                                                  |
| xml_etree_parse      | 136 ms                                                                 | 144 ms: 1.06x slower                                                   |
| pickle               | 11.4 us                                                                | 12.2 us: 1.07x slower                                                  |
| json_dumps           | 10.6 ms                                                                | 11.5 ms: 1.08x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.02x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 8.60 ms: 1.16x slower                                                  |
| python_startup         | 11.0 ms                                                                | 14.9 ms: 1.35x slower                                                  |
| Geometric mean         | (ref)                                                                  | 1.25x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 21.7 ms                                                                | 19.4 ms: 1.12x faster                                                  |
| genshi_xml      | 49.1 ms                                                                | 45.6 ms: 1.08x faster                                                  |
| django_template | 34.2 ms                                                                | 32.4 ms: 1.05x faster                                                  |
| mako            | 11.2 ms                                                                | 11.3 ms: 1.01x slower                                                  |
| Geometric mean  | (ref)                                                                  | 1.06x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| deepcopy                   | 357 us                                                                 | 229 us: 1.56x faster                                                   |
| async_tree_memoization     | 459 ms                                                                 | 295 ms: 1.56x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 583 ms: 1.51x faster                                                   |
| async_tree_io_tg           | 901 ms                                                                 | 601 ms: 1.50x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 285 ms: 1.44x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 468 ms: 1.42x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 449 ms: 1.41x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 239 ms: 1.39x faster                                                   |
| deepcopy_memo              | 38.1 us                                                                | 27.5 us: 1.38x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 256 ms: 1.38x faster                                                   |
| spectral_norm              | 108 ms                                                                 | 78.3 ms: 1.37x faster                                                  |
| go                         | 141 ms                                                                 | 104 ms: 1.35x faster                                                   |
| deepcopy_reduce            | 3.12 us                                                                | 2.34 us: 1.34x faster                                                  |
| scimark_sor                | 134 ms                                                                 | 100 ms: 1.33x faster                                                   |
| scimark_fft                | 348 ms                                                                 | 282 ms: 1.23x faster                                                   |
| async_generators           | 375 ms                                                                 | 315 ms: 1.19x faster                                                   |
| pylint                     | 317 ms                                                                 | 270 ms: 1.18x faster                                                   |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.04 ms: 1.18x faster                                                  |
| logging_silent             | 98.2 ns                                                                | 83.6 ns: 1.17x faster                                                  |
| pyflate                    | 449 ms                                                                 | 385 ms: 1.17x faster                                                   |
| scimark_monte_carlo        | 65.8 ms                                                                | 56.6 ms: 1.16x faster                                                  |
| richards                   | 44.4 ms                                                                | 38.6 ms: 1.15x faster                                                  |
| dulwich_log                | 74.5 ms                                                                | 65.6 ms: 1.14x faster                                                  |
| pidigits                   | 216 ms                                                                 | 191 ms: 1.13x faster                                                   |
| coroutines                 | 23.3 ms                                                                | 20.6 ms: 1.13x faster                                                  |
| telco                      | 7.77 ms                                                                | 6.89 ms: 1.13x faster                                                  |
| richards_super             | 50.4 ms                                                                | 44.8 ms: 1.13x faster                                                  |
| comprehensions             | 16.6 us                                                                | 14.7 us: 1.13x faster                                                  |
| genshi_text                | 21.7 ms                                                                | 19.4 ms: 1.12x faster                                                  |
| scimark_lu                 | 112 ms                                                                 | 100 ms: 1.12x faster                                                   |
| tomli_loads                | 2.01 sec                                                               | 1.80 sec: 1.12x faster                                                 |
| coverage                   | 82.5 ms                                                                | 73.9 ms: 1.12x faster                                                  |
| float                      | 76.7 ms                                                                | 69.4 ms: 1.11x faster                                                  |
| chaos                      | 56.3 ms                                                                | 50.9 ms: 1.10x faster                                                  |
| logging_simple             | 6.14 us                                                                | 5.58 us: 1.10x faster                                                  |
| unpickle                   | 14.6 us                                                                | 13.3 us: 1.10x faster                                                  |
| logging_format             | 6.92 us                                                                | 6.32 us: 1.09x faster                                                  |
| unpickle_list              | 4.60 us                                                                | 4.24 us: 1.09x faster                                                  |
| hexiom                     | 5.95 ms                                                                | 5.49 ms: 1.08x faster                                                  |
| xml_etree_process          | 59.2 ms                                                                | 54.7 ms: 1.08x faster                                                  |
| bpe_tokeniser              | 4.46 sec                                                               | 4.14 sec: 1.08x faster                                                 |
| nqueens                    | 77.7 ms                                                                | 72.2 ms: 1.08x faster                                                  |
| genshi_xml                 | 49.1 ms                                                                | 45.6 ms: 1.08x faster                                                  |
| deltablue                  | 3.10 ms                                                                | 2.88 ms: 1.08x faster                                                  |
| sympy_integrate            | 19.7 ms                                                                | 18.4 ms: 1.07x faster                                                  |
| nbody                      | 85.3 ms                                                                | 79.6 ms: 1.07x faster                                                  |
| typing_runtime_protocols   | 156 us                                                                 | 145 us: 1.07x faster                                                   |
| regex_compile              | 131 ms                                                                 | 123 ms: 1.07x faster                                                   |
| thrift                     | 772 us                                                                 | 722 us: 1.07x faster                                                   |
| xml_etree_generate         | 85.4 ms                                                                | 80.0 ms: 1.07x faster                                                  |
| generators                 | 28.5 ms                                                                | 26.7 ms: 1.07x faster                                                  |
| 2to3                       | 259 ms                                                                 | 244 ms: 1.06x faster                                                   |
| raytrace                   | 250 ms                                                                 | 237 ms: 1.06x faster                                                   |
| sympy_str                  | 274 ms                                                                 | 260 ms: 1.06x faster                                                   |
| regex_v8                   | 23.2 ms                                                                | 22.0 ms: 1.05x faster                                                  |
| django_template            | 34.2 ms                                                                | 32.4 ms: 1.05x faster                                                  |
| pathlib                    | 19.3 ms                                                                | 18.3 ms: 1.05x faster                                                  |
| sympy_sum                  | 154 ms                                                                 | 147 ms: 1.05x faster                                                   |
| docutils                   | 2.63 sec                                                               | 2.51 sec: 1.05x faster                                                 |
| json_loads                 | 27.3 us                                                                | 26.1 us: 1.05x faster                                                  |
| pycparser                  | 1.12 sec                                                               | 1.07 sec: 1.04x faster                                                 |
| sqlite_synth               | 2.25 us                                                                | 2.16 us: 1.04x faster                                                  |
| sympy_expand               | 454 ms                                                                 | 437 ms: 1.04x faster                                                   |
| json                       | 4.98 ms                                                                | 4.80 ms: 1.04x faster                                                  |
| pickle_dict                | 32.7 us                                                                | 31.5 us: 1.04x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 3.10 ms: 1.04x faster                                                  |
| unpickle_pure_python       | 208 us                                                                 | 202 us: 1.03x faster                                                   |
| pprint_safe_repr           | 719 ms                                                                 | 698 ms: 1.03x faster                                                   |
| pprint_pformat             | 1.46 sec                                                               | 1.42 sec: 1.02x faster                                                 |
| regex_dna                  | 189 ms                                                                 | 185 ms: 1.02x faster                                                   |
| asyncio_tcp                | 502 ms                                                                 | 492 ms: 1.02x faster                                                   |
| asyncio_tcp_ssl            | 1.51 sec                                                               | 1.50 sec: 1.01x faster                                                 |
| crypto_pyaes               | 68.2 ms                                                                | 67.8 ms: 1.01x faster                                                  |
| xml_etree_iterparse        | 94.4 ms                                                                | 93.9 ms: 1.00x faster                                                  |
| pickle_pure_python         | 292 us                                                                 | 294 us: 1.01x slower                                                   |
| mako                       | 11.2 ms                                                                | 11.3 ms: 1.01x slower                                                  |
| fannkuch                   | 376 ms                                                                 | 381 ms: 1.01x slower                                                   |
| meteor_contest             | 101 ms                                                                 | 103 ms: 1.02x slower                                                   |
| pickle_list                | 4.81 us                                                                | 4.97 us: 1.03x slower                                                  |
| xml_etree_parse            | 136 ms                                                                 | 144 ms: 1.06x slower                                                   |
| pickle                     | 11.4 us                                                                | 12.2 us: 1.07x slower                                                  |
| bench_thread_pool          | 924 us                                                                 | 998 us: 1.08x slower                                                   |
| json_dumps                 | 10.6 ms                                                                | 11.5 ms: 1.08x slower                                                  |
| mdp                        | 2.34 sec                                                               | 2.67 sec: 1.14x slower                                                 |
| python_startup_no_site     | 7.41 ms                                                                | 8.60 ms: 1.16x slower                                                  |
| gc_traversal               | 3.32 ms                                                                | 4.19 ms: 1.26x slower                                                  |
| unpack_sequence            | 39.3 ns                                                                | 50.7 ns: 1.29x slower                                                  |
| python_startup             | 11.0 ms                                                                | 14.9 ms: 1.35x slower                                                  |
| create_gc_cycles           | 1.33 ms                                                                | 1.94 ms: 1.45x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                                | 87.4 ms: 7.95x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.07x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (11) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, html5lib, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250322-3.14.0a6+-bc26f95-CLANG/bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.103x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.16x