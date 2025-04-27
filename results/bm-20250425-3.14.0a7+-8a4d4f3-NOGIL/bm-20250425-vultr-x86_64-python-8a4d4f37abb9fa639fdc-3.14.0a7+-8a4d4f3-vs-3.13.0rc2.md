# Results vs. 3.13.0rc2

- fork: python
- ref: 8a4d4f37abb9fa639fdc
- machine: linux-x86_64
- commit hash: 8a4d4f3
- commit date: 2025-04-25
- overall geometric mean: 1.006x slower
- HPT reliability: 84.53%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250425-vultr-x86_64-python-8a4d4f37abb9fa639fdc-3.14.0a7+-8a4d4f3 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 280 ms: 1.08x slower                                                   |
| docutils       | 2.63 sec                                                               | 2.70 sec: 1.03x slower                                                 |
| html5lib       | 68.6 ms                                                                | 66.6 ms: 1.03x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250425-vultr-x86_64-python-8a4d4f37abb9fa639fdc-3.14.0a7+-8a4d4f3 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 522 ms: 1.73x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 549 ms: 1.61x faster                                                   |
| async_tree_memoization     | 459 ms                                                                 | 312 ms: 1.47x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 228 ms: 1.46x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 286 ms: 1.43x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 259 ms: 1.36x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 480 ms: 1.32x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 507 ms: 1.31x faster                                                   |
| async_generators           | 375 ms                                                                 | 367 ms: 1.02x faster                                                   |
| coroutines                 | 23.3 ms                                                                | 22.9 ms: 1.02x faster                                                  |
| asyncio_websockets         | 517 ms                                                                 | 515 ms: 1.00x faster                                                   |
| Geometric mean             | (ref)                                                                  | 1.32x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250425-vultr-x86_64-python-8a4d4f37abb9fa639fdc-3.14.0a7+-8a4d4f3 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 76.7 ms                                                                | 67.2 ms: 1.14x faster                                                  |
| pidigits       | 216 ms                                                                 | 198 ms: 1.10x faster                                                   |
| nbody          | 85.3 ms                                                                | 110 ms: 1.29x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250425-vultr-x86_64-python-8a4d4f37abb9fa639fdc-3.14.0a7+-8a4d4f3 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.85 ms: 1.13x faster                                                  |
| regex_v8       | 23.2 ms                                                                | 21.4 ms: 1.08x faster                                                  |
| regex_dna      | 189 ms                                                                 | 180 ms: 1.05x faster                                                   |
| regex_compile  | 131 ms                                                                 | 143 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250425-vultr-x86_64-python-8a4d4f37abb9fa639fdc-3.14.0a7+-8a4d4f3 |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 87.7 ms: 1.08x faster                                                  |
| xml_etree_parse      | 136 ms                                                                 | 129 ms: 1.05x faster                                                   |
| tomli_loads          | 2.01 sec                                                               | 2.06 sec: 1.02x slower                                                 |
| json_loads           | 27.3 us                                                                | 29.3 us: 1.07x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                                | 93.1 ms: 1.09x slower                                                  |
| unpickle_pure_python | 208 us                                                                 | 230 us: 1.10x slower                                                   |
| xml_etree_process    | 59.2 ms                                                                | 66.6 ms: 1.12x slower                                                  |
| pickle_pure_python   | 292 us                                                                 | 328 us: 1.13x slower                                                   |
| json_dumps           | 10.6 ms                                                                | 12.8 ms: 1.21x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.07x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250425-vultr-x86_64-python-8a4d4f37abb9fa639fdc-3.14.0a7+-8a4d4f3 |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 15.8 ms: 1.43x slower                                                  |
| python_startup_no_site | 7.41 ms                                                                | 11.1 ms: 1.50x slower                                                  |
| Geometric mean         | (ref)                                                                  | 1.47x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250425-vultr-x86_64-python-8a4d4f37abb9fa639fdc-3.14.0a7+-8a4d4f3 |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 55.5 ms: 1.13x slower                                                  |
| django_template | 34.2 ms                                                                | 40.2 ms: 1.18x slower                                                  |
| genshi_text     | 21.7 ms                                                                | 25.9 ms: 1.19x slower                                                  |
| mako            | 11.2 ms                                                                | 15.4 ms: 1.37x slower                                                  |
| Geometric mean  | (ref)                                                                  | 1.21x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250425-vultr-x86_64-python-8a4d4f37abb9fa639fdc-3.14.0a7+-8a4d4f3 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.80 ms: 1.84x faster                                                  |
| mdp                        | 2.34 sec                                                               | 1.32 sec: 1.78x faster                                                 |
| async_tree_io_tg           | 901 ms                                                                 | 522 ms: 1.73x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 549 ms: 1.61x faster                                                   |
| async_tree_memoization     | 459 ms                                                                 | 312 ms: 1.47x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 228 ms: 1.46x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 286 ms: 1.43x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 259 ms: 1.36x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 480 ms: 1.32x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 507 ms: 1.31x faster                                                   |
| deepcopy                   | 357 us                                                                 | 290 us: 1.23x faster                                                   |
| float                      | 76.7 ms                                                                | 67.2 ms: 1.14x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.85 ms: 1.13x faster                                                  |
| scimark_sor                | 134 ms                                                                 | 118 ms: 1.13x faster                                                   |
| go                         | 141 ms                                                                 | 125 ms: 1.13x faster                                                   |
| sqlite_synth               | 2.25 us                                                                | 2.01 us: 1.12x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 34.4 us: 1.11x faster                                                  |
| pidigits                   | 216 ms                                                                 | 198 ms: 1.10x faster                                                   |
| regex_v8                   | 23.2 ms                                                                | 21.4 ms: 1.08x faster                                                  |
| xml_etree_iterparse        | 94.4 ms                                                                | 87.7 ms: 1.08x faster                                                  |
| spectral_norm              | 108 ms                                                                 | 100 ms: 1.07x faster                                                   |
| dulwich_log                | 74.5 ms                                                                | 70.0 ms: 1.06x faster                                                  |
| xml_etree_parse            | 136 ms                                                                 | 129 ms: 1.05x faster                                                   |
| deepcopy_reduce            | 3.12 us                                                                | 2.97 us: 1.05x faster                                                  |
| regex_dna                  | 189 ms                                                                 | 180 ms: 1.05x faster                                                   |
| html5lib                   | 68.6 ms                                                                | 66.6 ms: 1.03x faster                                                  |
| scimark_fft                | 348 ms                                                                 | 339 ms: 1.03x faster                                                   |
| async_generators           | 375 ms                                                                 | 367 ms: 1.02x faster                                                   |
| bpe_tokeniser              | 4.46 sec                                                               | 4.37 sec: 1.02x faster                                                 |
| coroutines                 | 23.3 ms                                                                | 22.9 ms: 1.02x faster                                                  |
| asyncio_websockets         | 517 ms                                                                 | 515 ms: 1.00x faster                                                   |
| pathlib                    | 19.3 ms                                                                | 19.2 ms: 1.00x faster                                                  |
| pycparser                  | 1.12 sec                                                               | 1.13 sec: 1.01x slower                                                 |
| json                       | 4.98 ms                                                                | 5.03 ms: 1.01x slower                                                  |
| tomli_loads                | 2.01 sec                                                               | 2.06 sec: 1.02x slower                                                 |
| docutils                   | 2.63 sec                                                               | 2.70 sec: 1.03x slower                                                 |
| create_gc_cycles           | 1.33 ms                                                                | 1.37 ms: 1.03x slower                                                  |
| pyflate                    | 449 ms                                                                 | 463 ms: 1.03x slower                                                   |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.94 ms: 1.04x slower                                                  |
| logging_silent             | 98.2 ns                                                                | 104 ns: 1.06x slower                                                   |
| generators                 | 28.5 ms                                                                | 30.5 ms: 1.07x slower                                                  |
| json_loads                 | 27.3 us                                                                | 29.3 us: 1.07x slower                                                  |
| 2to3                       | 259 ms                                                                 | 280 ms: 1.08x slower                                                   |
| pprint_safe_repr           | 719 ms                                                                 | 776 ms: 1.08x slower                                                   |
| chaos                      | 56.3 ms                                                                | 60.9 ms: 1.08x slower                                                  |
| regex_compile              | 131 ms                                                                 | 143 ms: 1.09x slower                                                   |
| xml_etree_generate         | 85.4 ms                                                                | 93.1 ms: 1.09x slower                                                  |
| telco                      | 7.77 ms                                                                | 8.50 ms: 1.09x slower                                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.60 sec: 1.10x slower                                                 |
| unpickle_pure_python       | 208 us                                                                 | 230 us: 1.10x slower                                                   |
| sympy_integrate            | 19.7 ms                                                                | 21.8 ms: 1.11x slower                                                  |
| scimark_monte_carlo        | 65.8 ms                                                                | 73.4 ms: 1.12x slower                                                  |
| hexiom                     | 5.95 ms                                                                | 6.65 ms: 1.12x slower                                                  |
| nqueens                    | 77.7 ms                                                                | 87.0 ms: 1.12x slower                                                  |
| logging_simple             | 6.14 us                                                                | 6.88 us: 1.12x slower                                                  |
| xml_etree_process          | 59.2 ms                                                                | 66.6 ms: 1.12x slower                                                  |
| pickle_pure_python         | 292 us                                                                 | 328 us: 1.13x slower                                                   |
| genshi_xml                 | 49.1 ms                                                                | 55.5 ms: 1.13x slower                                                  |
| scimark_lu                 | 112 ms                                                                 | 127 ms: 1.13x slower                                                   |
| sympy_str                  | 274 ms                                                                 | 312 ms: 1.14x slower                                                   |
| richards                   | 44.4 ms                                                                | 50.6 ms: 1.14x slower                                                  |
| deltablue                  | 3.10 ms                                                                | 3.53 ms: 1.14x slower                                                  |
| logging_format             | 6.92 us                                                                | 7.91 us: 1.14x slower                                                  |
| sympy_sum                  | 154 ms                                                                 | 177 ms: 1.15x slower                                                   |
| sympy_expand               | 454 ms                                                                 | 523 ms: 1.15x slower                                                   |
| richards_super             | 50.4 ms                                                                | 58.3 ms: 1.16x slower                                                  |
| comprehensions             | 16.6 us                                                                | 19.2 us: 1.16x slower                                                  |
| raytrace                   | 250 ms                                                                 | 292 ms: 1.17x slower                                                   |
| django_template            | 34.2 ms                                                                | 40.2 ms: 1.18x slower                                                  |
| genshi_text                | 21.7 ms                                                                | 25.9 ms: 1.19x slower                                                  |
| json_dumps                 | 10.6 ms                                                                | 12.8 ms: 1.21x slower                                                  |
| fannkuch                   | 376 ms                                                                 | 454 ms: 1.21x slower                                                   |
| crypto_pyaes               | 68.2 ms                                                                | 82.7 ms: 1.21x slower                                                  |
| typing_runtime_protocols   | 156 us                                                                 | 189 us: 1.21x slower                                                   |
| meteor_contest             | 101 ms                                                                 | 126 ms: 1.24x slower                                                   |
| nbody                      | 85.3 ms                                                                | 110 ms: 1.29x slower                                                   |
| coverage                   | 82.5 ms                                                                | 108 ms: 1.32x slower                                                   |
| mako                       | 11.2 ms                                                                | 15.4 ms: 1.37x slower                                                  |
| python_startup             | 11.0 ms                                                                | 15.8 ms: 1.43x slower                                                  |
| python_startup_no_site     | 7.41 ms                                                                | 11.1 ms: 1.50x slower                                                  |
| bench_thread_pool          | 924 us                                                                 | 3.12 ms: 3.38x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                                | 95.7 ms: 8.70x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.05x slower                                                           |

Benchmark hidden because not significant (1): pylint
Ignored benchmarks (19) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250425-3.14.0a7+-8a4d4f3-NOGIL/bm-20250425-vultr-x86_64-python-8a4d4f37abb9fa639fdc-3.14.0a7+-8a4d4f3.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.006x slower

# HPT report

- Reliability score: 84.53% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.36x