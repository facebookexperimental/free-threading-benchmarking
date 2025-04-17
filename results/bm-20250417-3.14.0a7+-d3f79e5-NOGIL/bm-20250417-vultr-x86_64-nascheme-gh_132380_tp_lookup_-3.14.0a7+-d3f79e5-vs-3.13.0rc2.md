# Results vs. 3.13.0rc2

- fork: nascheme
- ref: gh_132380_tp_lookup_
- machine: linux-x86_64
- commit hash: d3f79e5
- commit date: 2025-04-17
- overall geometric mean: 1.006x slower
- HPT reliability: 95.17%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250417-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.14.0a7+-d3f79e5 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 278 ms: 1.07x slower                                                     |
| docutils       | 2.63 sec                                                               | 2.68 sec: 1.02x slower                                                   |
| html5lib       | 68.6 ms                                                                | 66.4 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250417-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.14.0a7+-d3f79e5 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 518 ms: 1.74x faster                                                     |
| async_tree_io              | 881 ms                                                                 | 543 ms: 1.62x faster                                                     |
| async_tree_memoization     | 459 ms                                                                 | 309 ms: 1.49x faster                                                     |
| async_tree_none_tg         | 333 ms                                                                 | 224 ms: 1.49x faster                                                     |
| async_tree_memoization_tg  | 410 ms                                                                 | 282 ms: 1.45x faster                                                     |
| async_tree_none            | 353 ms                                                                 | 256 ms: 1.38x faster                                                     |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 478 ms: 1.33x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 505 ms: 1.32x faster                                                     |
| async_generators           | 375 ms                                                                 | 363 ms: 1.03x faster                                                     |
| coroutines                 | 23.3 ms                                                                | 22.9 ms: 1.02x faster                                                    |
| Geometric mean             | (ref)                                                                  | 1.33x faster                                                             |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250417-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.14.0a7+-d3f79e5 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 76.7 ms                                                                | 67.0 ms: 1.14x faster                                                    |
| pidigits       | 216 ms                                                                 | 193 ms: 1.12x faster                                                     |
| nbody          | 85.3 ms                                                                | 110 ms: 1.29x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250417-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.14.0a7+-d3f79e5 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.86 ms: 1.12x faster                                                    |
| regex_v8       | 23.2 ms                                                                | 21.7 ms: 1.07x faster                                                    |
| regex_dna      | 189 ms                                                                 | 187 ms: 1.01x faster                                                     |
| regex_compile  | 131 ms                                                                 | 142 ms: 1.08x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250417-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.14.0a7+-d3f79e5 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 86.8 ms: 1.09x faster                                                    |
| xml_etree_parse      | 136 ms                                                                 | 129 ms: 1.05x faster                                                     |
| tomli_loads          | 2.01 sec                                                               | 2.08 sec: 1.04x slower                                                   |
| unpickle_pure_python | 208 us                                                                 | 225 us: 1.08x slower                                                     |
| xml_etree_generate   | 85.4 ms                                                                | 93.0 ms: 1.09x slower                                                    |
| pickle_pure_python   | 292 us                                                                 | 325 us: 1.11x slower                                                     |
| json_loads           | 27.3 us                                                                | 30.5 us: 1.12x slower                                                    |
| xml_etree_process    | 59.2 ms                                                                | 66.4 ms: 1.12x slower                                                    |
| json_dumps           | 10.6 ms                                                                | 12.6 ms: 1.19x slower                                                    |
| Geometric mean       | (ref)                                                                  | 1.06x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250417-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.14.0a7+-d3f79e5 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 15.8 ms: 1.43x slower                                                    |
| python_startup_no_site | 7.41 ms                                                                | 11.1 ms: 1.50x slower                                                    |
| Geometric mean         | (ref)                                                                  | 1.46x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250417-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.14.0a7+-d3f79e5 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 55.0 ms: 1.12x slower                                                    |
| django_template | 34.2 ms                                                                | 39.7 ms: 1.16x slower                                                    |
| genshi_text     | 21.7 ms                                                                | 25.9 ms: 1.19x slower                                                    |
| mako            | 11.2 ms                                                                | 15.2 ms: 1.36x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.20x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250417-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.14.0a7+-d3f79e5 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.76 ms: 1.88x faster                                                    |
| mdp                        | 2.34 sec                                                               | 1.31 sec: 1.79x faster                                                   |
| async_tree_io_tg           | 901 ms                                                                 | 518 ms: 1.74x faster                                                     |
| async_tree_io              | 881 ms                                                                 | 543 ms: 1.62x faster                                                     |
| async_tree_memoization     | 459 ms                                                                 | 309 ms: 1.49x faster                                                     |
| async_tree_none_tg         | 333 ms                                                                 | 224 ms: 1.49x faster                                                     |
| async_tree_memoization_tg  | 410 ms                                                                 | 282 ms: 1.45x faster                                                     |
| async_tree_none            | 353 ms                                                                 | 256 ms: 1.38x faster                                                     |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 478 ms: 1.33x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 505 ms: 1.32x faster                                                     |
| deepcopy                   | 357 us                                                                 | 289 us: 1.24x faster                                                     |
| float                      | 76.7 ms                                                                | 67.0 ms: 1.14x faster                                                    |
| scimark_sor                | 134 ms                                                                 | 117 ms: 1.14x faster                                                     |
| go                         | 141 ms                                                                 | 124 ms: 1.13x faster                                                     |
| pidigits                   | 216 ms                                                                 | 193 ms: 1.12x faster                                                     |
| regex_effbot               | 3.21 ms                                                                | 2.86 ms: 1.12x faster                                                    |
| sqlite_synth               | 2.25 us                                                                | 2.02 us: 1.11x faster                                                    |
| deepcopy_memo              | 38.1 us                                                                | 34.6 us: 1.10x faster                                                    |
| xml_etree_iterparse        | 94.4 ms                                                                | 86.8 ms: 1.09x faster                                                    |
| regex_v8                   | 23.2 ms                                                                | 21.7 ms: 1.07x faster                                                    |
| dulwich_log                | 74.5 ms                                                                | 70.2 ms: 1.06x faster                                                    |
| deepcopy_reduce            | 3.12 us                                                                | 2.95 us: 1.06x faster                                                    |
| xml_etree_parse            | 136 ms                                                                 | 129 ms: 1.05x faster                                                     |
| html5lib                   | 68.6 ms                                                                | 66.4 ms: 1.03x faster                                                    |
| async_generators           | 375 ms                                                                 | 363 ms: 1.03x faster                                                     |
| spectral_norm              | 108 ms                                                                 | 104 ms: 1.03x faster                                                     |
| coroutines                 | 23.3 ms                                                                | 22.9 ms: 1.02x faster                                                    |
| regex_dna                  | 189 ms                                                                 | 187 ms: 1.01x faster                                                     |
| bpe_tokeniser              | 4.46 sec                                                               | 4.51 sec: 1.01x slower                                                   |
| pyflate                    | 449 ms                                                                 | 455 ms: 1.01x slower                                                     |
| scimark_fft                | 348 ms                                                                 | 353 ms: 1.01x slower                                                     |
| docutils                   | 2.63 sec                                                               | 2.68 sec: 1.02x slower                                                   |
| tomli_loads                | 2.01 sec                                                               | 2.08 sec: 1.04x slower                                                   |
| json                       | 4.98 ms                                                                | 5.16 ms: 1.04x slower                                                    |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.94 ms: 1.04x slower                                                    |
| logging_silent             | 98.2 ns                                                                | 102 ns: 1.04x slower                                                     |
| telco                      | 7.77 ms                                                                | 8.27 ms: 1.06x slower                                                    |
| generators                 | 28.5 ms                                                                | 30.6 ms: 1.07x slower                                                    |
| 2to3                       | 259 ms                                                                 | 278 ms: 1.07x slower                                                     |
| pprint_safe_repr           | 719 ms                                                                 | 773 ms: 1.08x slower                                                     |
| unpickle_pure_python       | 208 us                                                                 | 225 us: 1.08x slower                                                     |
| regex_compile              | 131 ms                                                                 | 142 ms: 1.08x slower                                                     |
| pprint_pformat             | 1.46 sec                                                               | 1.58 sec: 1.09x slower                                                   |
| xml_etree_generate         | 85.4 ms                                                                | 93.0 ms: 1.09x slower                                                    |
| chaos                      | 56.3 ms                                                                | 61.3 ms: 1.09x slower                                                    |
| hexiom                     | 5.95 ms                                                                | 6.63 ms: 1.11x slower                                                    |
| pickle_pure_python         | 292 us                                                                 | 325 us: 1.11x slower                                                     |
| nqueens                    | 77.7 ms                                                                | 86.7 ms: 1.11x slower                                                    |
| json_loads                 | 27.3 us                                                                | 30.5 us: 1.12x slower                                                    |
| sympy_integrate            | 19.7 ms                                                                | 22.0 ms: 1.12x slower                                                    |
| scimark_monte_carlo        | 65.8 ms                                                                | 73.7 ms: 1.12x slower                                                    |
| xml_etree_process          | 59.2 ms                                                                | 66.4 ms: 1.12x slower                                                    |
| genshi_xml                 | 49.1 ms                                                                | 55.0 ms: 1.12x slower                                                    |
| logging_format             | 6.92 us                                                                | 7.83 us: 1.13x slower                                                    |
| logging_simple             | 6.14 us                                                                | 6.97 us: 1.14x slower                                                    |
| richards                   | 44.4 ms                                                                | 50.8 ms: 1.14x slower                                                    |
| sympy_str                  | 274 ms                                                                 | 314 ms: 1.15x slower                                                     |
| comprehensions             | 16.6 us                                                                | 19.1 us: 1.15x slower                                                    |
| sympy_sum                  | 154 ms                                                                 | 178 ms: 1.15x slower                                                     |
| scimark_lu                 | 112 ms                                                                 | 130 ms: 1.15x slower                                                     |
| raytrace                   | 250 ms                                                                 | 289 ms: 1.16x slower                                                     |
| deltablue                  | 3.10 ms                                                                | 3.59 ms: 1.16x slower                                                    |
| django_template            | 34.2 ms                                                                | 39.7 ms: 1.16x slower                                                    |
| richards_super             | 50.4 ms                                                                | 58.5 ms: 1.16x slower                                                    |
| sympy_expand               | 454 ms                                                                 | 531 ms: 1.17x slower                                                     |
| json_dumps                 | 10.6 ms                                                                | 12.6 ms: 1.19x slower                                                    |
| genshi_text                | 21.7 ms                                                                | 25.9 ms: 1.19x slower                                                    |
| fannkuch                   | 376 ms                                                                 | 451 ms: 1.20x slower                                                     |
| crypto_pyaes               | 68.2 ms                                                                | 83.1 ms: 1.22x slower                                                    |
| typing_runtime_protocols   | 156 us                                                                 | 193 us: 1.24x slower                                                     |
| meteor_contest             | 101 ms                                                                 | 126 ms: 1.25x slower                                                     |
| nbody                      | 85.3 ms                                                                | 110 ms: 1.29x slower                                                     |
| coverage                   | 82.5 ms                                                                | 109 ms: 1.32x slower                                                     |
| mako                       | 11.2 ms                                                                | 15.2 ms: 1.36x slower                                                    |
| python_startup             | 11.0 ms                                                                | 15.8 ms: 1.43x slower                                                    |
| python_startup_no_site     | 7.41 ms                                                                | 11.1 ms: 1.50x slower                                                    |
| bench_thread_pool          | 924 us                                                                 | 3.14 ms: 3.39x slower                                                    |
| bench_mp_pool              | 11.0 ms                                                                | 94.9 ms: 8.63x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.05x slower                                                             |

Benchmark hidden because not significant (5): pylint, pathlib, asyncio_websockets, pycparser, create_gc_cycles
Ignored benchmarks (19) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250417-3.14.0a7+-d3f79e5-NOGIL/bm-20250417-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.14.0a7+-d3f79e5.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.006x slower

# HPT report

- Reliability score: 95.17% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.36x