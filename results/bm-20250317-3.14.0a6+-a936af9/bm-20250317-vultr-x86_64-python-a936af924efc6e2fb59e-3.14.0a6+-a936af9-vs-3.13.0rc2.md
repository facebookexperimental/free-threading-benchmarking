# Results vs. 3.13.0rc2

- fork: python
- ref: a936af924efc6e2fb59e
- machine: linux-x86_64
- commit hash: a936af9
- commit date: 2025-03-17
- overall geometric mean: 1.020x faster
- HPT reliability: 74.34%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 258 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                           |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 636 ms: 1.42x faster                                                   |
| async_tree_memoization     | 459 ms                                                                 | 332 ms: 1.39x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 636 ms: 1.39x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 314 ms: 1.30x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 512 ms: 1.30x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 276 ms: 1.28x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 499 ms: 1.27x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 265 ms: 1.26x faster                                                   |
| async_generators           | 375 ms                                                                 | 339 ms: 1.11x faster                                                   |
| coroutines                 | 23.3 ms                                                                | 23.2 ms: 1.01x faster                                                  |
| Geometric mean             | (ref)                                                                  | 1.24x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 195 ms: 1.11x faster                                                   |
| float          | 76.7 ms                                                                | 75.8 ms: 1.01x faster                                                  |
| nbody          | 85.3 ms                                                                | 104 ms: 1.21x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.76 ms: 1.17x faster                                                  |
| regex_dna      | 189 ms                                                                 | 171 ms: 1.10x faster                                                   |
| regex_compile  | 131 ms                                                                 | 130 ms: 1.01x faster                                                   |
| regex_v8       | 23.2 ms                                                                | 24.6 ms: 1.06x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                                 | 129 ms: 1.05x faster                                                   |
| xml_etree_iterparse  | 94.4 ms                                                                | 93.0 ms: 1.01x faster                                                  |
| json_loads           | 27.3 us                                                                | 27.5 us: 1.01x slower                                                  |
| xml_etree_process    | 59.2 ms                                                                | 59.8 ms: 1.01x slower                                                  |
| json_dumps           | 10.6 ms                                                                | 11.3 ms: 1.06x slower                                                  |
| unpickle_pure_python | 208 us                                                                 | 225 us: 1.08x slower                                                   |
| pickle_pure_python   | 292 us                                                                 | 326 us: 1.12x slower                                                   |
| Geometric mean       | (ref)                                                                  | 1.02x slower                                                           |

Benchmark hidden because not significant (2): xml_etree_generate, tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 8.61 ms: 1.16x slower                                                  |
| python_startup         | 11.0 ms                                                                | 14.9 ms: 1.36x slower                                                  |
| Geometric mean         | (ref)                                                                  | 1.25x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 21.7 ms                                                                | 22.2 ms: 1.02x slower                                                  |
| genshi_xml      | 49.1 ms                                                                | 51.8 ms: 1.06x slower                                                  |
| django_template | 34.2 ms                                                                | 36.5 ms: 1.07x slower                                                  |
| mako            | 11.2 ms                                                                | 12.1 ms: 1.08x slower                                                  |
| Geometric mean  | (ref)                                                                  | 1.06x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 636 ms: 1.42x faster                                                   |
| async_tree_memoization     | 459 ms                                                                 | 332 ms: 1.39x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 636 ms: 1.39x faster                                                   |
| deepcopy                   | 357 us                                                                 | 265 us: 1.35x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 314 ms: 1.30x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 512 ms: 1.30x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 276 ms: 1.28x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 499 ms: 1.27x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 265 ms: 1.26x faster                                                   |
| deepcopy_memo              | 38.1 us                                                                | 30.7 us: 1.24x faster                                                  |
| go                         | 141 ms                                                                 | 117 ms: 1.20x faster                                                   |
| regex_effbot               | 3.21 ms                                                                | 2.76 ms: 1.17x faster                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 2.71 us: 1.15x faster                                                  |
| scimark_sor                | 134 ms                                                                 | 117 ms: 1.14x faster                                                   |
| pylint                     | 317 ms                                                                 | 285 ms: 1.11x faster                                                   |
| pidigits                   | 216 ms                                                                 | 195 ms: 1.11x faster                                                   |
| spectral_norm              | 108 ms                                                                 | 97.1 ms: 1.11x faster                                                  |
| async_generators           | 375 ms                                                                 | 339 ms: 1.11x faster                                                   |
| regex_dna                  | 189 ms                                                                 | 171 ms: 1.10x faster                                                   |
| dulwich_log                | 74.5 ms                                                                | 67.8 ms: 1.10x faster                                                  |
| xml_etree_parse            | 136 ms                                                                 | 129 ms: 1.05x faster                                                   |
| pyflate                    | 449 ms                                                                 | 428 ms: 1.05x faster                                                   |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.55 ms: 1.04x faster                                                  |
| scimark_fft                | 348 ms                                                                 | 336 ms: 1.04x faster                                                   |
| coverage                   | 82.5 ms                                                                | 80.4 ms: 1.03x faster                                                  |
| thrift                     | 772 us                                                                 | 755 us: 1.02x faster                                                   |
| logging_format             | 6.92 us                                                                | 6.77 us: 1.02x faster                                                  |
| sqlite_synth               | 2.25 us                                                                | 2.21 us: 1.02x faster                                                  |
| json                       | 4.98 ms                                                                | 4.89 ms: 1.02x faster                                                  |
| xml_etree_iterparse        | 94.4 ms                                                                | 93.0 ms: 1.01x faster                                                  |
| regex_compile              | 131 ms                                                                 | 130 ms: 1.01x faster                                                   |
| bpe_tokeniser              | 4.46 sec                                                               | 4.40 sec: 1.01x faster                                                 |
| float                      | 76.7 ms                                                                | 75.8 ms: 1.01x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 23.2 ms: 1.01x faster                                                  |
| 2to3                       | 259 ms                                                                 | 258 ms: 1.01x faster                                                   |
| sqlglot_normalize          | 106 ms                                                                 | 105 ms: 1.00x faster                                                   |
| json_loads                 | 27.3 us                                                                | 27.5 us: 1.01x slower                                                  |
| mdp                        | 2.34 sec                                                               | 2.36 sec: 1.01x slower                                                 |
| xml_etree_process          | 59.2 ms                                                                | 59.8 ms: 1.01x slower                                                  |
| meteor_contest             | 101 ms                                                                 | 102 ms: 1.01x slower                                                   |
| sqlglot_optimize           | 52.7 ms                                                                | 53.2 ms: 1.01x slower                                                  |
| richards_super             | 50.4 ms                                                                | 51.0 ms: 1.01x slower                                                  |
| sympy_integrate            | 19.7 ms                                                                | 20.0 ms: 1.02x slower                                                  |
| typing_runtime_protocols   | 156 us                                                                 | 158 us: 1.02x slower                                                   |
| sympy_sum                  | 154 ms                                                                 | 157 ms: 1.02x slower                                                   |
| deltablue                  | 3.10 ms                                                                | 3.16 ms: 1.02x slower                                                  |
| sympy_str                  | 274 ms                                                                 | 280 ms: 1.02x slower                                                   |
| scimark_monte_carlo        | 65.8 ms                                                                | 67.3 ms: 1.02x slower                                                  |
| genshi_text                | 21.7 ms                                                                | 22.2 ms: 1.02x slower                                                  |
| pprint_safe_repr           | 719 ms                                                                 | 737 ms: 1.03x slower                                                   |
| logging_silent             | 98.2 ns                                                                | 101 ns: 1.03x slower                                                   |
| pycparser                  | 1.12 sec                                                               | 1.15 sec: 1.03x slower                                                 |
| hexiom                     | 5.95 ms                                                                | 6.14 ms: 1.03x slower                                                  |
| generators                 | 28.5 ms                                                                | 29.5 ms: 1.03x slower                                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.51 sec: 1.04x slower                                                 |
| scimark_lu                 | 112 ms                                                                 | 117 ms: 1.04x slower                                                   |
| sympy_expand               | 454 ms                                                                 | 472 ms: 1.04x slower                                                   |
| sqlglot_transpile          | 1.55 ms                                                                | 1.62 ms: 1.04x slower                                                  |
| comprehensions             | 16.6 us                                                                | 17.3 us: 1.05x slower                                                  |
| chaos                      | 56.3 ms                                                                | 58.9 ms: 1.05x slower                                                  |
| sqlglot_parse              | 1.25 ms                                                                | 1.31 ms: 1.05x slower                                                  |
| genshi_xml                 | 49.1 ms                                                                | 51.8 ms: 1.06x slower                                                  |
| json_dumps                 | 10.6 ms                                                                | 11.3 ms: 1.06x slower                                                  |
| regex_v8                   | 23.2 ms                                                                | 24.6 ms: 1.06x slower                                                  |
| nqueens                    | 77.7 ms                                                                | 82.6 ms: 1.06x slower                                                  |
| crypto_pyaes               | 68.2 ms                                                                | 72.7 ms: 1.07x slower                                                  |
| django_template            | 34.2 ms                                                                | 36.5 ms: 1.07x slower                                                  |
| unpickle_pure_python       | 208 us                                                                 | 225 us: 1.08x slower                                                   |
| mako                       | 11.2 ms                                                                | 12.1 ms: 1.08x slower                                                  |
| fannkuch                   | 376 ms                                                                 | 408 ms: 1.09x slower                                                   |
| raytrace                   | 250 ms                                                                 | 273 ms: 1.09x slower                                                   |
| pickle_pure_python         | 292 us                                                                 | 326 us: 1.12x slower                                                   |
| bench_thread_pool          | 924 us                                                                 | 1.05 ms: 1.14x slower                                                  |
| python_startup_no_site     | 7.41 ms                                                                | 8.61 ms: 1.16x slower                                                  |
| nbody                      | 85.3 ms                                                                | 104 ms: 1.21x slower                                                   |
| gc_traversal               | 3.32 ms                                                                | 4.16 ms: 1.25x slower                                                  |
| python_startup             | 11.0 ms                                                                | 14.9 ms: 1.36x slower                                                  |
| create_gc_cycles           | 1.33 ms                                                                | 1.82 ms: 1.36x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                                | 88.3 ms: 8.02x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                           |

Benchmark hidden because not significant (8): richards, docutils, xml_etree_generate, logging_simple, tomli_loads, asyncio_websockets, pathlib, telco
Ignored benchmarks (15) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250317-3.14.0a6+-a936af9/bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.020x faster

# HPT report

- Reliability score: 74.34% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x