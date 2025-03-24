# Results vs. 3.13.0rc2

- fork: python
- ref: bc26f95e8ff60ccca981
- machine: linux-x86_64
- commit hash: bc26f95
- commit date: 2025-03-22
- overall geometric mean: 1.028x faster
- HPT reliability: 95.91%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 257 ms: 1.01x faster                                                   |
| docutils       | 2.63 sec                                                               | 2.60 sec: 1.01x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_memoization     | 459 ms                                                                 | 321 ms: 1.43x faster                                                   |
| async_tree_io_tg           | 901 ms                                                                 | 641 ms: 1.41x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 632 ms: 1.40x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 311 ms: 1.32x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 261 ms: 1.28x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 279 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 535 ms: 1.24x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 524 ms: 1.21x faster                                                   |
| async_generators           | 375 ms                                                                 | 337 ms: 1.11x faster                                                   |
| asyncio_tcp                | 502 ms                                                                 | 499 ms: 1.01x faster                                                   |
| coroutines                 | 23.3 ms                                                                | 23.6 ms: 1.01x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.19x faster                                                           |

Benchmark hidden because not significant (2): asyncio_tcp_ssl, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 76.7 ms                                                                | 72.2 ms: 1.06x faster                                                  |
| pidigits       | 216 ms                                                                 | 210 ms: 1.03x faster                                                   |
| nbody          | 85.3 ms                                                                | 98.6 ms: 1.16x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.82 ms: 1.14x faster                                                  |
| regex_dna      | 189 ms                                                                 | 181 ms: 1.04x faster                                                   |
| regex_v8       | 23.2 ms                                                                | 22.3 ms: 1.04x faster                                                  |
| regex_compile  | 131 ms                                                                 | 128 ms: 1.03x faster                                                   |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| unpickle             | 14.6 us                                                                | 13.3 us: 1.10x faster                                                  |
| pickle_dict          | 32.7 us                                                                | 30.3 us: 1.08x faster                                                  |
| xml_etree_parse      | 136 ms                                                                 | 131 ms: 1.04x faster                                                   |
| xml_etree_iterparse  | 94.4 ms                                                                | 92.9 ms: 1.02x faster                                                  |
| tomli_loads          | 2.01 sec                                                               | 1.98 sec: 1.02x faster                                                 |
| xml_etree_process    | 59.2 ms                                                                | 60.3 ms: 1.02x slower                                                  |
| json_loads           | 27.3 us                                                                | 27.9 us: 1.02x slower                                                  |
| pickle_list          | 4.81 us                                                                | 4.92 us: 1.02x slower                                                  |
| unpickle_list        | 4.60 us                                                                | 4.82 us: 1.05x slower                                                  |
| json_dumps           | 10.6 ms                                                                | 11.3 ms: 1.06x slower                                                  |
| unpickle_pure_python | 208 us                                                                 | 221 us: 1.06x slower                                                   |
| pickle               | 11.4 us                                                                | 12.3 us: 1.08x slower                                                  |
| pickle_pure_python   | 292 us                                                                 | 322 us: 1.11x slower                                                   |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                           |

Benchmark hidden because not significant (1): xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 8.61 ms: 1.16x slower                                                  |
| python_startup         | 11.0 ms                                                                | 14.9 ms: 1.36x slower                                                  |
| Geometric mean         | (ref)                                                                  | 1.25x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 21.7 ms                                                                | 21.9 ms: 1.01x slower                                                  |
| genshi_xml      | 49.1 ms                                                                | 50.5 ms: 1.03x slower                                                  |
| django_template | 34.2 ms                                                                | 36.1 ms: 1.05x slower                                                  |
| mako            | 11.2 ms                                                                | 12.1 ms: 1.08x slower                                                  |
| Geometric mean  | (ref)                                                                  | 1.04x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_memoization     | 459 ms                                                                 | 321 ms: 1.43x faster                                                   |
| async_tree_io_tg           | 901 ms                                                                 | 641 ms: 1.41x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 632 ms: 1.40x faster                                                   |
| deepcopy                   | 357 us                                                                 | 264 us: 1.35x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 311 ms: 1.32x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 261 ms: 1.28x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 279 ms: 1.27x faster                                                   |
| deepcopy_memo              | 38.1 us                                                                | 30.3 us: 1.25x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 535 ms: 1.24x faster                                                   |
| go                         | 141 ms                                                                 | 113 ms: 1.24x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 524 ms: 1.21x faster                                                   |
| spectral_norm              | 108 ms                                                                 | 92.8 ms: 1.16x faster                                                  |
| scimark_sor                | 134 ms                                                                 | 115 ms: 1.16x faster                                                   |
| deepcopy_reduce            | 3.12 us                                                                | 2.74 us: 1.14x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.82 ms: 1.14x faster                                                  |
| pylint                     | 317 ms                                                                 | 284 ms: 1.12x faster                                                   |
| async_generators           | 375 ms                                                                 | 337 ms: 1.11x faster                                                   |
| dulwich_log                | 74.5 ms                                                                | 66.9 ms: 1.11x faster                                                  |
| unpickle                   | 14.6 us                                                                | 13.3 us: 1.10x faster                                                  |
| pickle_dict                | 32.7 us                                                                | 30.3 us: 1.08x faster                                                  |
| pyflate                    | 449 ms                                                                 | 418 ms: 1.08x faster                                                   |
| float                      | 76.7 ms                                                                | 72.2 ms: 1.06x faster                                                  |
| scimark_fft                | 348 ms                                                                 | 332 ms: 1.05x faster                                                   |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.53 ms: 1.05x faster                                                  |
| regex_dna                  | 189 ms                                                                 | 181 ms: 1.04x faster                                                   |
| regex_v8                   | 23.2 ms                                                                | 22.3 ms: 1.04x faster                                                  |
| coverage                   | 82.5 ms                                                                | 79.5 ms: 1.04x faster                                                  |
| xml_etree_parse            | 136 ms                                                                 | 131 ms: 1.04x faster                                                   |
| telco                      | 7.77 ms                                                                | 7.50 ms: 1.04x faster                                                  |
| pidigits                   | 216 ms                                                                 | 210 ms: 1.03x faster                                                   |
| regex_compile              | 131 ms                                                                 | 128 ms: 1.03x faster                                                   |
| bpe_tokeniser              | 4.46 sec                                                               | 4.35 sec: 1.02x faster                                                 |
| sqlite_synth               | 2.25 us                                                                | 2.20 us: 1.02x faster                                                  |
| logging_format             | 6.92 us                                                                | 6.77 us: 1.02x faster                                                  |
| json                       | 4.98 ms                                                                | 4.88 ms: 1.02x faster                                                  |
| richards                   | 44.4 ms                                                                | 43.6 ms: 1.02x faster                                                  |
| xml_etree_iterparse        | 94.4 ms                                                                | 92.9 ms: 1.02x faster                                                  |
| tomli_loads                | 2.01 sec                                                               | 1.98 sec: 1.02x faster                                                 |
| docutils                   | 2.63 sec                                                               | 2.60 sec: 1.01x faster                                                 |
| 2to3                       | 259 ms                                                                 | 257 ms: 1.01x faster                                                   |
| richards_super             | 50.4 ms                                                                | 50.0 ms: 1.01x faster                                                  |
| asyncio_tcp                | 502 ms                                                                 | 499 ms: 1.01x faster                                                   |
| logging_silent             | 98.2 ns                                                                | 97.7 ns: 1.01x faster                                                  |
| mdp                        | 2.34 sec                                                               | 2.33 sec: 1.00x faster                                                 |
| genshi_text                | 21.7 ms                                                                | 21.9 ms: 1.01x slower                                                  |
| sympy_str                  | 274 ms                                                                 | 276 ms: 1.01x slower                                                   |
| scimark_monte_carlo        | 65.8 ms                                                                | 66.4 ms: 1.01x slower                                                  |
| pycparser                  | 1.12 sec                                                               | 1.13 sec: 1.01x slower                                                 |
| pathlib                    | 19.3 ms                                                                | 19.4 ms: 1.01x slower                                                  |
| coroutines                 | 23.3 ms                                                                | 23.6 ms: 1.01x slower                                                  |
| meteor_contest             | 101 ms                                                                 | 103 ms: 1.01x slower                                                   |
| scimark_lu                 | 112 ms                                                                 | 114 ms: 1.01x slower                                                   |
| comprehensions             | 16.6 us                                                                | 16.8 us: 1.02x slower                                                  |
| sympy_sum                  | 154 ms                                                                 | 157 ms: 1.02x slower                                                   |
| xml_etree_process          | 59.2 ms                                                                | 60.3 ms: 1.02x slower                                                  |
| deltablue                  | 3.10 ms                                                                | 3.15 ms: 1.02x slower                                                  |
| thrift                     | 772 us                                                                 | 786 us: 1.02x slower                                                   |
| json_loads                 | 27.3 us                                                                | 27.9 us: 1.02x slower                                                  |
| pprint_safe_repr           | 719 ms                                                                 | 733 ms: 1.02x slower                                                   |
| pickle_list                | 4.81 us                                                                | 4.92 us: 1.02x slower                                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.49 sec: 1.02x slower                                                 |
| hexiom                     | 5.95 ms                                                                | 6.09 ms: 1.02x slower                                                  |
| typing_runtime_protocols   | 156 us                                                                 | 159 us: 1.02x slower                                                   |
| sympy_expand               | 454 ms                                                                 | 466 ms: 1.03x slower                                                   |
| chaos                      | 56.3 ms                                                                | 57.8 ms: 1.03x slower                                                  |
| genshi_xml                 | 49.1 ms                                                                | 50.5 ms: 1.03x slower                                                  |
| crypto_pyaes               | 68.2 ms                                                                | 70.9 ms: 1.04x slower                                                  |
| generators                 | 28.5 ms                                                                | 29.7 ms: 1.04x slower                                                  |
| unpickle_list              | 4.60 us                                                                | 4.82 us: 1.05x slower                                                  |
| nqueens                    | 77.7 ms                                                                | 81.8 ms: 1.05x slower                                                  |
| django_template            | 34.2 ms                                                                | 36.1 ms: 1.05x slower                                                  |
| json_dumps                 | 10.6 ms                                                                | 11.3 ms: 1.06x slower                                                  |
| unpickle_pure_python       | 208 us                                                                 | 221 us: 1.06x slower                                                   |
| fannkuch                   | 376 ms                                                                 | 401 ms: 1.07x slower                                                   |
| raytrace                   | 250 ms                                                                 | 267 ms: 1.07x slower                                                   |
| mako                       | 11.2 ms                                                                | 12.1 ms: 1.08x slower                                                  |
| pickle                     | 11.4 us                                                                | 12.3 us: 1.08x slower                                                  |
| pickle_pure_python         | 292 us                                                                 | 322 us: 1.11x slower                                                   |
| bench_thread_pool          | 924 us                                                                 | 1.05 ms: 1.14x slower                                                  |
| nbody                      | 85.3 ms                                                                | 98.6 ms: 1.16x slower                                                  |
| python_startup_no_site     | 7.41 ms                                                                | 8.61 ms: 1.16x slower                                                  |
| gc_traversal               | 3.32 ms                                                                | 4.24 ms: 1.28x slower                                                  |
| unpack_sequence            | 39.3 ns                                                                | 52.7 ns: 1.34x slower                                                  |
| python_startup             | 11.0 ms                                                                | 14.9 ms: 1.36x slower                                                  |
| create_gc_cycles           | 1.33 ms                                                                | 1.87 ms: 1.40x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                                | 89.5 ms: 8.14x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                           |

Benchmark hidden because not significant (5): logging_simple, xml_etree_generate, asyncio_tcp_ssl, asyncio_websockets, sympy_integrate
Ignored benchmarks (11) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, html5lib, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250322-3.14.0a6+-bc26f95/bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.028x faster

# HPT report

- Reliability score: 95.91% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.12x