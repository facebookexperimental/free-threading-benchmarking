# Results vs. 3.13.0rc2

- fork: python
- ref: a936af924efc6e2fb59e
- machine: linux-x86_64
- commit hash: a936af9
- commit date: 2025-03-17
- overall geometric mean: 1.092x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 301 ms: 1.16x slower                                                   |
| docutils       | 2.63 sec                                                               | 2.81 sec: 1.07x slower                                                 |
| html5lib       | 68.6 ms                                                                | 70.3 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.08x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 562 ms: 1.60x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 587 ms: 1.50x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 240 ms: 1.38x faster                                                   |
| async_tree_memoization     | 459 ms                                                                 | 343 ms: 1.34x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 309 ms: 1.33x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 280 ms: 1.26x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 576 ms: 1.10x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 610 ms: 1.09x faster                                                   |
| async_generators           | 375 ms                                                                 | 380 ms: 1.01x slower                                                   |
| coroutines                 | 23.3 ms                                                                | 23.9 ms: 1.02x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.22x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 221 ms: 1.02x slower                                                   |
| float          | 76.7 ms                                                                | 79.0 ms: 1.03x slower                                                  |
| nbody          | 85.3 ms                                                                | 134 ms: 1.57x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.18x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.67 ms: 1.20x faster                                                  |
| regex_dna      | 189 ms                                                                 | 176 ms: 1.07x faster                                                   |
| regex_v8       | 23.2 ms                                                                | 24.1 ms: 1.04x slower                                                  |
| regex_compile  | 131 ms                                                                 | 160 ms: 1.22x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 88.8 ms: 1.06x faster                                                  |
| xml_etree_parse      | 136 ms                                                                 | 130 ms: 1.05x faster                                                   |
| json_loads           | 27.3 us                                                                | 29.5 us: 1.08x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                                | 97.8 ms: 1.15x slower                                                  |
| tomli_loads          | 2.01 sec                                                               | 2.36 sec: 1.18x slower                                                 |
| xml_etree_process    | 59.2 ms                                                                | 70.9 ms: 1.20x slower                                                  |
| json_dumps           | 10.6 ms                                                                | 12.9 ms: 1.21x slower                                                  |
| unpickle_pure_python | 208 us                                                                 | 259 us: 1.25x slower                                                   |
| pickle_pure_python   | 292 us                                                                 | 364 us: 1.25x slower                                                   |
| Geometric mean       | (ref)                                                                  | 1.13x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 15.8 ms: 1.43x slower                                                  |
| python_startup_no_site | 7.41 ms                                                                | 11.1 ms: 1.50x slower                                                  |
| Geometric mean         | (ref)                                                                  | 1.47x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 61.5 ms: 1.25x slower                                                  |
| django_template | 34.2 ms                                                                | 44.1 ms: 1.29x slower                                                  |
| genshi_text     | 21.7 ms                                                                | 29.1 ms: 1.34x slower                                                  |
| mako            | 11.2 ms                                                                | 16.0 ms: 1.42x slower                                                  |
| Geometric mean  | (ref)                                                                  | 1.32x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.71 ms: 1.94x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 562 ms: 1.60x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 587 ms: 1.50x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 240 ms: 1.38x faster                                                   |
| async_tree_memoization     | 459 ms                                                                 | 343 ms: 1.34x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 309 ms: 1.33x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 280 ms: 1.26x faster                                                   |
| regex_effbot               | 3.21 ms                                                                | 2.67 ms: 1.20x faster                                                  |
| deepcopy                   | 357 us                                                                 | 313 us: 1.14x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 576 ms: 1.10x faster                                                   |
| sqlite_synth               | 2.25 us                                                                | 2.06 us: 1.09x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 610 ms: 1.09x faster                                                   |
| regex_dna                  | 189 ms                                                                 | 176 ms: 1.07x faster                                                   |
| xml_etree_iterparse        | 94.4 ms                                                                | 88.8 ms: 1.06x faster                                                  |
| xml_etree_parse            | 136 ms                                                                 | 130 ms: 1.05x faster                                                   |
| create_gc_cycles           | 1.33 ms                                                                | 1.29 ms: 1.03x faster                                                  |
| dulwich_log                | 74.5 ms                                                                | 74.8 ms: 1.00x slower                                                  |
| async_generators           | 375 ms                                                                 | 380 ms: 1.01x slower                                                   |
| pidigits                   | 216 ms                                                                 | 221 ms: 1.02x slower                                                   |
| deepcopy_reduce            | 3.12 us                                                                | 3.19 us: 1.02x slower                                                  |
| coroutines                 | 23.3 ms                                                                | 23.9 ms: 1.02x slower                                                  |
| html5lib                   | 68.6 ms                                                                | 70.3 ms: 1.02x slower                                                  |
| json                       | 4.98 ms                                                                | 5.12 ms: 1.03x slower                                                  |
| scimark_sor                | 134 ms                                                                 | 137 ms: 1.03x slower                                                   |
| float                      | 76.7 ms                                                                | 79.0 ms: 1.03x slower                                                  |
| go                         | 141 ms                                                                 | 145 ms: 1.03x slower                                                   |
| regex_v8                   | 23.2 ms                                                                | 24.1 ms: 1.04x slower                                                  |
| deepcopy_memo              | 38.1 us                                                                | 39.8 us: 1.05x slower                                                  |
| pathlib                    | 19.3 ms                                                                | 20.2 ms: 1.05x slower                                                  |
| spectral_norm              | 108 ms                                                                 | 114 ms: 1.06x slower                                                   |
| docutils                   | 2.63 sec                                                               | 2.81 sec: 1.07x slower                                                 |
| pycparser                  | 1.12 sec                                                               | 1.21 sec: 1.08x slower                                                 |
| json_loads                 | 27.3 us                                                                | 29.5 us: 1.08x slower                                                  |
| bpe_tokeniser              | 4.46 sec                                                               | 4.90 sec: 1.10x slower                                                 |
| generators                 | 28.5 ms                                                                | 31.6 ms: 1.11x slower                                                  |
| telco                      | 7.77 ms                                                                | 8.74 ms: 1.12x slower                                                  |
| pyflate                    | 449 ms                                                                 | 513 ms: 1.14x slower                                                   |
| xml_etree_generate         | 85.4 ms                                                                | 97.8 ms: 1.15x slower                                                  |
| scimark_fft                | 348 ms                                                                 | 400 ms: 1.15x slower                                                   |
| thrift                     | 772 us                                                                 | 896 us: 1.16x slower                                                   |
| 2to3                       | 259 ms                                                                 | 301 ms: 1.16x slower                                                   |
| mdp                        | 2.34 sec                                                               | 2.72 sec: 1.16x slower                                                 |
| sqlglot_normalize          | 106 ms                                                                 | 123 ms: 1.16x slower                                                   |
| sqlglot_optimize           | 52.7 ms                                                                | 61.9 ms: 1.18x slower                                                  |
| tomli_loads                | 2.01 sec                                                               | 2.36 sec: 1.18x slower                                                 |
| logging_silent             | 98.2 ns                                                                | 116 ns: 1.18x slower                                                   |
| coverage                   | 82.5 ms                                                                | 97.3 ms: 1.18x slower                                                  |
| logging_simple             | 6.14 us                                                                | 7.25 us: 1.18x slower                                                  |
| logging_format             | 6.92 us                                                                | 8.19 us: 1.18x slower                                                  |
| xml_etree_process          | 59.2 ms                                                                | 70.9 ms: 1.20x slower                                                  |
| json_dumps                 | 10.6 ms                                                                | 12.9 ms: 1.21x slower                                                  |
| sympy_sum                  | 154 ms                                                                 | 188 ms: 1.22x slower                                                   |
| pprint_safe_repr           | 719 ms                                                                 | 876 ms: 1.22x slower                                                   |
| regex_compile              | 131 ms                                                                 | 160 ms: 1.22x slower                                                   |
| sympy_expand               | 454 ms                                                                 | 556 ms: 1.23x slower                                                   |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.88 ms: 1.24x slower                                                  |
| sympy_integrate            | 19.7 ms                                                                | 24.5 ms: 1.24x slower                                                  |
| sympy_str                  | 274 ms                                                                 | 341 ms: 1.24x slower                                                   |
| unpickle_pure_python       | 208 us                                                                 | 259 us: 1.25x slower                                                   |
| chaos                      | 56.3 ms                                                                | 70.2 ms: 1.25x slower                                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.82 sec: 1.25x slower                                                 |
| pickle_pure_python         | 292 us                                                                 | 364 us: 1.25x slower                                                   |
| sqlglot_transpile          | 1.55 ms                                                                | 1.94 ms: 1.25x slower                                                  |
| genshi_xml                 | 49.1 ms                                                                | 61.5 ms: 1.25x slower                                                  |
| deltablue                  | 3.10 ms                                                                | 3.89 ms: 1.26x slower                                                  |
| nqueens                    | 77.7 ms                                                                | 98.1 ms: 1.26x slower                                                  |
| scimark_lu                 | 112 ms                                                                 | 142 ms: 1.26x slower                                                   |
| richards                   | 44.4 ms                                                                | 56.3 ms: 1.27x slower                                                  |
| comprehensions             | 16.6 us                                                                | 21.1 us: 1.27x slower                                                  |
| typing_runtime_protocols   | 156 us                                                                 | 198 us: 1.27x slower                                                   |
| richards_super             | 50.4 ms                                                                | 65.1 ms: 1.29x slower                                                  |
| django_template            | 34.2 ms                                                                | 44.1 ms: 1.29x slower                                                  |
| hexiom                     | 5.95 ms                                                                | 7.70 ms: 1.29x slower                                                  |
| sqlglot_parse              | 1.25 ms                                                                | 1.61 ms: 1.29x slower                                                  |
| scimark_monte_carlo        | 65.8 ms                                                                | 85.5 ms: 1.30x slower                                                  |
| crypto_pyaes               | 68.2 ms                                                                | 89.1 ms: 1.31x slower                                                  |
| raytrace                   | 250 ms                                                                 | 328 ms: 1.31x slower                                                   |
| meteor_contest             | 101 ms                                                                 | 134 ms: 1.32x slower                                                   |
| fannkuch                   | 376 ms                                                                 | 500 ms: 1.33x slower                                                   |
| genshi_text                | 21.7 ms                                                                | 29.1 ms: 1.34x slower                                                  |
| mako                       | 11.2 ms                                                                | 16.0 ms: 1.42x slower                                                  |
| python_startup             | 11.0 ms                                                                | 15.8 ms: 1.43x slower                                                  |
| python_startup_no_site     | 7.41 ms                                                                | 11.1 ms: 1.50x slower                                                  |
| nbody                      | 85.3 ms                                                                | 134 ms: 1.57x slower                                                   |
| bench_thread_pool          | 924 us                                                                 | 3.17 ms: 3.43x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                                | 95.8 ms: 8.71x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.14x slower                                                           |

Benchmark hidden because not significant (2): asyncio_websockets, pylint
Ignored benchmarks (14) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250317-3.14.0a6+-a936af9-NOGIL/bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.092x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 1.35x