# Results vs. 3.13.0rc2

- fork: python
- ref: 0eeaa0ef8bf60fd3b144
- machine: linux-x86_64
- commit hash: 0eeaa0e
- commit date: 2025-05-05
- overall geometric mean: 1.020x faster
- HPT reliability: 80.24%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.45x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250505-vultr-x86_64-python-0eeaa0ef8bf60fd3b144-3.14.0a7+-0eeaa0e |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 268 ms: 1.03x slower                                                   |
| docutils       | 2.63 sec                                                               | 2.67 sec: 1.02x slower                                                 |
| html5lib       | 68.6 ms                                                                | 63.2 ms: 1.09x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250505-vultr-x86_64-python-0eeaa0ef8bf60fd3b144-3.14.0a7+-0eeaa0e |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 488 ms: 1.85x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 517 ms: 1.70x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 212 ms: 1.57x faster                                                   |
| async_tree_memoization     | 459 ms                                                                 | 301 ms: 1.53x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 269 ms: 1.52x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 247 ms: 1.43x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 444 ms: 1.43x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 470 ms: 1.42x faster                                                   |
| coroutines                 | 23.3 ms                                                                | 20.8 ms: 1.12x faster                                                  |
| async_generators           | 375 ms                                                                 | 334 ms: 1.12x faster                                                   |
| Geometric mean             | (ref)                                                                  | 1.40x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250505-vultr-x86_64-python-0eeaa0ef8bf60fd3b144-3.14.0a7+-0eeaa0e |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 76.7 ms                                                                | 66.3 ms: 1.16x faster                                                  |
| pidigits       | 216 ms                                                                 | 187 ms: 1.16x faster                                                   |
| nbody          | 85.3 ms                                                                | 113 ms: 1.33x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250505-vultr-x86_64-python-0eeaa0ef8bf60fd3b144-3.14.0a7+-0eeaa0e |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 131 ms                                                                 | 138 ms: 1.05x slower                                                   |
| regex_v8       | 23.2 ms                                                                | 24.6 ms: 1.06x slower                                                  |
| regex_effbot   | 3.21 ms                                                                | 3.47 ms: 1.08x slower                                                  |
| regex_dna      | 189 ms                                                                 | 209 ms: 1.11x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.07x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250505-vultr-x86_64-python-0eeaa0ef8bf60fd3b144-3.14.0a7+-0eeaa0e |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 85.4 ms: 1.11x faster                                                  |
| tomli_loads          | 2.01 sec                                                               | 1.97 sec: 1.02x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                                | 86.9 ms: 1.02x slower                                                  |
| xml_etree_process    | 59.2 ms                                                                | 61.5 ms: 1.04x slower                                                  |
| xml_etree_parse      | 136 ms                                                                 | 142 ms: 1.04x slower                                                   |
| json_loads           | 27.3 us                                                                | 29.7 us: 1.09x slower                                                  |
| unpickle_pure_python | 208 us                                                                 | 227 us: 1.09x slower                                                   |
| pickle_pure_python   | 292 us                                                                 | 326 us: 1.12x slower                                                   |
| json_dumps           | 10.6 ms                                                                | 12.9 ms: 1.21x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.05x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250505-vultr-x86_64-python-0eeaa0ef8bf60fd3b144-3.14.0a7+-0eeaa0e |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.42 ms: 1.27x slower                                                  |
| python_startup         | 11.0 ms                                                                | 15.6 ms: 1.42x slower                                                  |
| Geometric mean         | (ref)                                                                  | 1.34x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250505-vultr-x86_64-python-0eeaa0ef8bf60fd3b144-3.14.0a7+-0eeaa0e |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 51.4 ms: 1.05x slower                                                  |
| django_template | 34.2 ms                                                                | 37.0 ms: 1.08x slower                                                  |
| genshi_text     | 21.7 ms                                                                | 24.1 ms: 1.11x slower                                                  |
| mako            | 11.2 ms                                                                | 14.7 ms: 1.31x slower                                                  |
| Geometric mean  | (ref)                                                                  | 1.13x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250505-vultr-x86_64-python-0eeaa0ef8bf60fd3b144-3.14.0a7+-0eeaa0e |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 488 ms: 1.85x faster                                                   |
| mdp                        | 2.34 sec                                                               | 1.28 sec: 1.82x faster                                                 |
| async_tree_io              | 881 ms                                                                 | 517 ms: 1.70x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 212 ms: 1.57x faster                                                   |
| gc_traversal               | 3.32 ms                                                                | 2.13 ms: 1.56x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 301 ms: 1.53x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 269 ms: 1.52x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 247 ms: 1.43x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 444 ms: 1.43x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 470 ms: 1.42x faster                                                   |
| deepcopy                   | 357 us                                                                 | 260 us: 1.38x faster                                                   |
| go                         | 141 ms                                                                 | 119 ms: 1.19x faster                                                   |
| deepcopy_reduce            | 3.12 us                                                                | 2.68 us: 1.16x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 32.9 us: 1.16x faster                                                  |
| float                      | 76.7 ms                                                                | 66.3 ms: 1.16x faster                                                  |
| pidigits                   | 216 ms                                                                 | 187 ms: 1.16x faster                                                   |
| scimark_sor                | 134 ms                                                                 | 116 ms: 1.16x faster                                                   |
| logging_silent             | 98.2 ns                                                                | 85.5 ns: 1.15x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 20.8 ms: 1.12x faster                                                  |
| async_generators           | 375 ms                                                                 | 334 ms: 1.12x faster                                                   |
| sqlite_synth               | 2.25 us                                                                | 2.03 us: 1.11x faster                                                  |
| xml_etree_iterparse        | 94.4 ms                                                                | 85.4 ms: 1.11x faster                                                  |
| html5lib                   | 68.6 ms                                                                | 63.2 ms: 1.09x faster                                                  |
| spectral_norm              | 108 ms                                                                 | 99.1 ms: 1.09x faster                                                  |
| pylint                     | 317 ms                                                                 | 294 ms: 1.08x faster                                                   |
| bpe_tokeniser              | 4.46 sec                                                               | 4.20 sec: 1.06x faster                                                 |
| dulwich_log                | 74.5 ms                                                                | 71.8 ms: 1.04x faster                                                  |
| pathlib                    | 19.3 ms                                                                | 18.8 ms: 1.03x faster                                                  |
| tomli_loads                | 2.01 sec                                                               | 1.97 sec: 1.02x faster                                                 |
| pyflate                    | 449 ms                                                                 | 444 ms: 1.01x faster                                                   |
| pycparser                  | 1.12 sec                                                               | 1.13 sec: 1.01x slower                                                 |
| docutils                   | 2.63 sec                                                               | 2.67 sec: 1.02x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                                | 86.9 ms: 1.02x slower                                                  |
| 2to3                       | 259 ms                                                                 | 268 ms: 1.03x slower                                                   |
| chaos                      | 56.3 ms                                                                | 58.3 ms: 1.04x slower                                                  |
| xml_etree_process          | 59.2 ms                                                                | 61.5 ms: 1.04x slower                                                  |
| telco                      | 7.77 ms                                                                | 8.10 ms: 1.04x slower                                                  |
| xml_etree_parse            | 136 ms                                                                 | 142 ms: 1.04x slower                                                   |
| create_gc_cycles           | 1.33 ms                                                                | 1.39 ms: 1.04x slower                                                  |
| hexiom                     | 5.95 ms                                                                | 6.23 ms: 1.05x slower                                                  |
| regex_compile              | 131 ms                                                                 | 138 ms: 1.05x slower                                                   |
| genshi_xml                 | 49.1 ms                                                                | 51.4 ms: 1.05x slower                                                  |
| pprint_safe_repr           | 719 ms                                                                 | 754 ms: 1.05x slower                                                   |
| json                       | 4.98 ms                                                                | 5.25 ms: 1.05x slower                                                  |
| scimark_fft                | 348 ms                                                                 | 367 ms: 1.05x slower                                                   |
| nqueens                    | 77.7 ms                                                                | 82.0 ms: 1.05x slower                                                  |
| comprehensions             | 16.6 us                                                                | 17.5 us: 1.06x slower                                                  |
| sympy_integrate            | 19.7 ms                                                                | 20.9 ms: 1.06x slower                                                  |
| regex_v8                   | 23.2 ms                                                                | 24.6 ms: 1.06x slower                                                  |
| logging_format             | 6.92 us                                                                | 7.38 us: 1.07x slower                                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.56 sec: 1.07x slower                                                 |
| logging_simple             | 6.14 us                                                                | 6.63 us: 1.08x slower                                                  |
| regex_effbot               | 3.21 ms                                                                | 3.47 ms: 1.08x slower                                                  |
| django_template            | 34.2 ms                                                                | 37.0 ms: 1.08x slower                                                  |
| sympy_str                  | 274 ms                                                                 | 298 ms: 1.09x slower                                                   |
| json_loads                 | 27.3 us                                                                | 29.7 us: 1.09x slower                                                  |
| unpickle_pure_python       | 208 us                                                                 | 227 us: 1.09x slower                                                   |
| scimark_lu                 | 112 ms                                                                 | 122 ms: 1.09x slower                                                   |
| richards                   | 44.4 ms                                                                | 48.5 ms: 1.09x slower                                                  |
| fannkuch                   | 376 ms                                                                 | 412 ms: 1.10x slower                                                   |
| deltablue                  | 3.10 ms                                                                | 3.40 ms: 1.10x slower                                                  |
| sympy_sum                  | 154 ms                                                                 | 170 ms: 1.10x slower                                                   |
| regex_dna                  | 189 ms                                                                 | 209 ms: 1.11x slower                                                   |
| genshi_text                | 21.7 ms                                                                | 24.1 ms: 1.11x slower                                                  |
| raytrace                   | 250 ms                                                                 | 278 ms: 1.11x slower                                                   |
| scimark_monte_carlo        | 65.8 ms                                                                | 73.5 ms: 1.12x slower                                                  |
| pickle_pure_python         | 292 us                                                                 | 326 us: 1.12x slower                                                   |
| sympy_expand               | 454 ms                                                                 | 507 ms: 1.12x slower                                                   |
| typing_runtime_protocols   | 156 us                                                                 | 174 us: 1.12x slower                                                   |
| richards_super             | 50.4 ms                                                                | 57.2 ms: 1.13x slower                                                  |
| coverage                   | 82.5 ms                                                                | 96.5 ms: 1.17x slower                                                  |
| crypto_pyaes               | 68.2 ms                                                                | 80.7 ms: 1.18x slower                                                  |
| meteor_contest             | 101 ms                                                                 | 120 ms: 1.18x slower                                                   |
| json_dumps                 | 10.6 ms                                                                | 12.9 ms: 1.21x slower                                                  |
| python_startup_no_site     | 7.41 ms                                                                | 9.42 ms: 1.27x slower                                                  |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 6.16 ms: 1.30x slower                                                  |
| mako                       | 11.2 ms                                                                | 14.7 ms: 1.31x slower                                                  |
| nbody                      | 85.3 ms                                                                | 113 ms: 1.33x slower                                                   |
| python_startup             | 11.0 ms                                                                | 15.6 ms: 1.42x slower                                                  |
| bench_thread_pool          | 924 us                                                                 | 3.11 ms: 3.37x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                                | 84.6 ms: 7.69x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.02x slower                                                           |

Benchmark hidden because not significant (2): asyncio_websockets, generators
Ignored benchmarks (19) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250505-3.14.0a7+-0eeaa0e-CLANG,NOGIL/bm-20250505-vultr-x86_64-python-0eeaa0ef8bf60fd3b144-3.14.0a7+-0eeaa0e.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.020x faster

# HPT report

- Reliability score: 80.24% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.45x