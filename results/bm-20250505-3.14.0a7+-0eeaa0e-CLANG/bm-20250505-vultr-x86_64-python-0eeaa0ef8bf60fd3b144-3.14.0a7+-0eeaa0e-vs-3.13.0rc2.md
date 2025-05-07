# Results vs. 3.13.0rc2

- fork: python
- ref: 0eeaa0ef8bf60fd3b144
- machine: linux-x86_64
- commit hash: 0eeaa0e
- commit date: 2025-05-05
- overall geometric mean: 1.098x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250505-vultr-x86_64-python-0eeaa0ef8bf60fd3b144-3.14.0a7+-0eeaa0e |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 243 ms: 1.07x faster                                                   |
| docutils       | 2.63 sec                                                               | 2.52 sec: 1.04x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250505-vultr-x86_64-python-0eeaa0ef8bf60fd3b144-3.14.0a7+-0eeaa0e |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 591 ms: 1.52x faster                                                   |
| async_tree_memoization     | 459 ms                                                                 | 302 ms: 1.52x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 594 ms: 1.48x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 482 ms: 1.38x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 245 ms: 1.36x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 260 ms: 1.36x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 303 ms: 1.36x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 474 ms: 1.34x faster                                                   |
| async_generators           | 375 ms                                                                 | 320 ms: 1.17x faster                                                   |
| coroutines                 | 23.3 ms                                                                | 21.1 ms: 1.11x faster                                                  |
| Geometric mean             | (ref)                                                                  | 1.32x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250505-vultr-x86_64-python-0eeaa0ef8bf60fd3b144-3.14.0a7+-0eeaa0e |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 76.7 ms                                                                | 67.1 ms: 1.14x faster                                                  |
| pidigits       | 216 ms                                                                 | 194 ms: 1.12x faster                                                   |
| nbody          | 85.3 ms                                                                | 82.3 ms: 1.04x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.10x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250505-vultr-x86_64-python-0eeaa0ef8bf60fd3b144-3.14.0a7+-0eeaa0e |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 131 ms                                                                 | 121 ms: 1.08x faster                                                   |
| regex_effbot   | 3.21 ms                                                                | 2.99 ms: 1.08x faster                                                  |
| regex_dna      | 189 ms                                                                 | 181 ms: 1.04x faster                                                   |
| regex_v8       | 23.2 ms                                                                | 23.3 ms: 1.00x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250505-vultr-x86_64-python-0eeaa0ef8bf60fd3b144-3.14.0a7+-0eeaa0e |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                               | 1.84 sec: 1.10x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                                | 81.1 ms: 1.05x faster                                                  |
| xml_etree_process    | 59.2 ms                                                                | 56.3 ms: 1.05x faster                                                  |
| unpickle_pure_python | 208 us                                                                 | 201 us: 1.04x faster                                                   |
| pickle_pure_python   | 292 us                                                                 | 293 us: 1.00x slower                                                   |
| xml_etree_iterparse  | 94.4 ms                                                                | 95.1 ms: 1.01x slower                                                  |
| xml_etree_parse      | 136 ms                                                                 | 144 ms: 1.06x slower                                                   |
| json_dumps           | 10.6 ms                                                                | 12.0 ms: 1.13x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                           |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250505-vultr-x86_64-python-0eeaa0ef8bf60fd3b144-3.14.0a7+-0eeaa0e |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 7.36 ms: 1.01x faster                                                  |
| python_startup         | 11.0 ms                                                                | 15.0 ms: 1.36x slower                                                  |
| Geometric mean         | (ref)                                                                  | 1.16x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250505-vultr-x86_64-python-0eeaa0ef8bf60fd3b144-3.14.0a7+-0eeaa0e |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 21.7 ms                                                                | 19.3 ms: 1.13x faster                                                  |
| genshi_xml      | 49.1 ms                                                                | 45.4 ms: 1.08x faster                                                  |
| django_template | 34.2 ms                                                                | 32.7 ms: 1.04x faster                                                  |
| mako            | 11.2 ms                                                                | 11.6 ms: 1.03x slower                                                  |
| Geometric mean  | (ref)                                                                  | 1.05x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250505-vultr-x86_64-python-0eeaa0ef8bf60fd3b144-3.14.0a7+-0eeaa0e |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.34 sec                                                               | 1.11 sec: 2.11x faster                                                 |
| deepcopy                   | 357 us                                                                 | 231 us: 1.55x faster                                                   |
| async_tree_io_tg           | 901 ms                                                                 | 591 ms: 1.52x faster                                                   |
| async_tree_memoization     | 459 ms                                                                 | 302 ms: 1.52x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 594 ms: 1.48x faster                                                   |
| deepcopy_memo              | 38.1 us                                                                | 27.5 us: 1.38x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 482 ms: 1.38x faster                                                   |
| go                         | 141 ms                                                                 | 102 ms: 1.38x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 245 ms: 1.36x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 260 ms: 1.36x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 303 ms: 1.36x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 474 ms: 1.34x faster                                                   |
| deepcopy_reduce            | 3.12 us                                                                | 2.39 us: 1.30x faster                                                  |
| scimark_sor                | 134 ms                                                                 | 106 ms: 1.25x faster                                                   |
| spectral_norm              | 108 ms                                                                 | 89.1 ms: 1.21x faster                                                  |
| async_generators           | 375 ms                                                                 | 320 ms: 1.17x faster                                                   |
| logging_silent             | 98.2 ns                                                                | 84.1 ns: 1.17x faster                                                  |
| richards                   | 44.4 ms                                                                | 38.1 ms: 1.17x faster                                                  |
| pylint                     | 317 ms                                                                 | 274 ms: 1.16x faster                                                   |
| richards_super             | 50.4 ms                                                                | 43.6 ms: 1.16x faster                                                  |
| telco                      | 7.77 ms                                                                | 6.74 ms: 1.15x faster                                                  |
| float                      | 76.7 ms                                                                | 67.1 ms: 1.14x faster                                                  |
| pyflate                    | 449 ms                                                                 | 399 ms: 1.13x faster                                                   |
| genshi_text                | 21.7 ms                                                                | 19.3 ms: 1.13x faster                                                  |
| dulwich_log                | 74.5 ms                                                                | 66.5 ms: 1.12x faster                                                  |
| pidigits                   | 216 ms                                                                 | 194 ms: 1.12x faster                                                   |
| chaos                      | 56.3 ms                                                                | 50.5 ms: 1.11x faster                                                  |
| bpe_tokeniser              | 4.46 sec                                                               | 4.03 sec: 1.11x faster                                                 |
| coroutines                 | 23.3 ms                                                                | 21.1 ms: 1.11x faster                                                  |
| comprehensions             | 16.6 us                                                                | 15.0 us: 1.10x faster                                                  |
| hexiom                     | 5.95 ms                                                                | 5.43 ms: 1.10x faster                                                  |
| sympy_integrate            | 19.7 ms                                                                | 18.0 ms: 1.10x faster                                                  |
| tomli_loads                | 2.01 sec                                                               | 1.84 sec: 1.10x faster                                                 |
| logging_format             | 6.92 us                                                                | 6.35 us: 1.09x faster                                                  |
| regex_compile              | 131 ms                                                                 | 121 ms: 1.08x faster                                                   |
| genshi_xml                 | 49.1 ms                                                                | 45.4 ms: 1.08x faster                                                  |
| nqueens                    | 77.7 ms                                                                | 72.0 ms: 1.08x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.99 ms: 1.08x faster                                                  |
| 2to3                       | 259 ms                                                                 | 243 ms: 1.07x faster                                                   |
| logging_simple             | 6.14 us                                                                | 5.77 us: 1.07x faster                                                  |
| typing_runtime_protocols   | 156 us                                                                 | 146 us: 1.06x faster                                                   |
| scimark_monte_carlo        | 65.8 ms                                                                | 62.0 ms: 1.06x faster                                                  |
| raytrace                   | 250 ms                                                                 | 236 ms: 1.06x faster                                                   |
| generators                 | 28.5 ms                                                                | 27.0 ms: 1.06x faster                                                  |
| sympy_str                  | 274 ms                                                                 | 259 ms: 1.06x faster                                                   |
| xml_etree_generate         | 85.4 ms                                                                | 81.1 ms: 1.05x faster                                                  |
| xml_etree_process          | 59.2 ms                                                                | 56.3 ms: 1.05x faster                                                  |
| django_template            | 34.2 ms                                                                | 32.7 ms: 1.04x faster                                                  |
| sympy_sum                  | 154 ms                                                                 | 148 ms: 1.04x faster                                                   |
| regex_dna                  | 189 ms                                                                 | 181 ms: 1.04x faster                                                   |
| docutils                   | 2.63 sec                                                               | 2.52 sec: 1.04x faster                                                 |
| sympy_expand               | 454 ms                                                                 | 437 ms: 1.04x faster                                                   |
| nbody                      | 85.3 ms                                                                | 82.3 ms: 1.04x faster                                                  |
| scimark_fft                | 348 ms                                                                 | 336 ms: 1.04x faster                                                   |
| unpickle_pure_python       | 208 us                                                                 | 201 us: 1.04x faster                                                   |
| pathlib                    | 19.3 ms                                                                | 18.7 ms: 1.03x faster                                                  |
| sqlite_synth               | 2.25 us                                                                | 2.19 us: 1.03x faster                                                  |
| pycparser                  | 1.12 sec                                                               | 1.09 sec: 1.03x faster                                                 |
| crypto_pyaes               | 68.2 ms                                                                | 66.9 ms: 1.02x faster                                                  |
| pprint_safe_repr           | 719 ms                                                                 | 707 ms: 1.02x faster                                                   |
| pprint_pformat             | 1.46 sec                                                               | 1.43 sec: 1.02x faster                                                 |
| deltablue                  | 3.10 ms                                                                | 3.07 ms: 1.01x faster                                                  |
| scimark_lu                 | 112 ms                                                                 | 112 ms: 1.01x faster                                                   |
| python_startup_no_site     | 7.41 ms                                                                | 7.36 ms: 1.01x faster                                                  |
| regex_v8                   | 23.2 ms                                                                | 23.3 ms: 1.00x slower                                                  |
| pickle_pure_python         | 292 us                                                                 | 293 us: 1.00x slower                                                   |
| xml_etree_iterparse        | 94.4 ms                                                                | 95.1 ms: 1.01x slower                                                  |
| fannkuch                   | 376 ms                                                                 | 379 ms: 1.01x slower                                                   |
| mako                       | 11.2 ms                                                                | 11.6 ms: 1.03x slower                                                  |
| meteor_contest             | 101 ms                                                                 | 105 ms: 1.04x slower                                                   |
| xml_etree_parse            | 136 ms                                                                 | 144 ms: 1.06x slower                                                   |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.11 ms: 1.07x slower                                                  |
| bench_thread_pool          | 924 us                                                                 | 1.02 ms: 1.11x slower                                                  |
| json_dumps                 | 10.6 ms                                                                | 12.0 ms: 1.13x slower                                                  |
| gc_traversal               | 3.32 ms                                                                | 4.21 ms: 1.27x slower                                                  |
| python_startup             | 11.0 ms                                                                | 15.0 ms: 1.36x slower                                                  |
| create_gc_cycles           | 1.33 ms                                                                | 1.94 ms: 1.45x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                                | 87.2 ms: 7.93x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.07x faster                                                           |

Benchmark hidden because not significant (3): asyncio_websockets, json_loads, json
Ignored benchmarks (21) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, coverage, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250505-3.14.0a7+-0eeaa0e-CLANG/bm-20250505-vultr-x86_64-python-0eeaa0ef8bf60fd3b144-3.14.0a7+-0eeaa0e.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.098x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.16x