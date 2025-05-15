# Results vs. 3.13.0rc2

- fork: python
- ref: e123a1d09bcb75aae0c5
- machine: linux-x86_64
- commit hash: e123a1d
- commit date: 2025-05-14
- overall geometric mean: 1.021x slower
- HPT reliability: 95.61%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.40x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 285 ms: 1.10x slower                                                  |
| docutils       | 2.63 sec                                                               | 2.70 sec: 1.03x slower                                                |
| html5lib       | 68.6 ms                                                                | 65.8 ms: 1.04x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 521 ms: 1.73x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 550 ms: 1.60x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 313 ms: 1.47x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 227 ms: 1.47x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 284 ms: 1.44x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 261 ms: 1.35x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 480 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 510 ms: 1.31x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 23.0 ms: 1.01x faster                                                 |
| async_generators           | 375 ms                                                                 | 371 ms: 1.01x faster                                                  |
| Geometric mean             | (ref)                                                                  | 1.32x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 76.7 ms                                                                | 70.0 ms: 1.10x faster                                                 |
| pidigits       | 216 ms                                                                 | 199 ms: 1.09x faster                                                  |
| nbody          | 85.3 ms                                                                | 120 ms: 1.41x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.06x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.77 ms: 1.16x faster                                                 |
| regex_v8       | 23.2 ms                                                                | 21.0 ms: 1.10x faster                                                 |
| regex_dna      | 189 ms                                                                 | 177 ms: 1.07x faster                                                  |
| regex_compile  | 131 ms                                                                 | 145 ms: 1.10x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 88.3 ms: 1.07x faster                                                 |
| xml_etree_parse      | 136 ms                                                                 | 131 ms: 1.03x faster                                                  |
| tomli_loads          | 2.01 sec                                                               | 2.15 sec: 1.07x slower                                                |
| json_dumps           | 10.6 ms                                                                | 11.6 ms: 1.09x slower                                                 |
| unpickle_pure_python | 208 us                                                                 | 229 us: 1.10x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                                | 95.4 ms: 1.12x slower                                                 |
| json_loads           | 27.3 us                                                                | 30.6 us: 1.12x slower                                                 |
| pickle_pure_python   | 292 us                                                                 | 334 us: 1.15x slower                                                  |
| xml_etree_process    | 59.2 ms                                                                | 68.6 ms: 1.16x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.08x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.57 ms: 1.29x slower                                                 |
| python_startup         | 11.0 ms                                                                | 16.0 ms: 1.45x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.37x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 55.8 ms: 1.14x slower                                                 |
| django_template | 34.2 ms                                                                | 40.5 ms: 1.18x slower                                                 |
| genshi_text     | 21.7 ms                                                                | 26.2 ms: 1.20x slower                                                 |
| mako            | 11.2 ms                                                                | 15.6 ms: 1.39x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.22x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.34 sec                                                               | 1.33 sec: 1.76x faster                                                |
| gc_traversal               | 3.32 ms                                                                | 1.89 ms: 1.75x faster                                                 |
| async_tree_io_tg           | 901 ms                                                                 | 521 ms: 1.73x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 550 ms: 1.60x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 313 ms: 1.47x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 227 ms: 1.47x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 284 ms: 1.44x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 261 ms: 1.35x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 480 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 510 ms: 1.31x faster                                                  |
| deepcopy                   | 357 us                                                                 | 292 us: 1.23x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.77 ms: 1.16x faster                                                 |
| go                         | 141 ms                                                                 | 123 ms: 1.14x faster                                                  |
| regex_v8                   | 23.2 ms                                                                | 21.0 ms: 1.10x faster                                                 |
| scimark_sor                | 134 ms                                                                 | 122 ms: 1.10x faster                                                  |
| float                      | 76.7 ms                                                                | 70.0 ms: 1.10x faster                                                 |
| pidigits                   | 216 ms                                                                 | 199 ms: 1.09x faster                                                  |
| sqlite_synth               | 2.25 us                                                                | 2.07 us: 1.09x faster                                                 |
| deepcopy_memo              | 38.1 us                                                                | 35.5 us: 1.07x faster                                                 |
| xml_etree_iterparse        | 94.4 ms                                                                | 88.3 ms: 1.07x faster                                                 |
| regex_dna                  | 189 ms                                                                 | 177 ms: 1.07x faster                                                  |
| dulwich_log                | 74.5 ms                                                                | 71.0 ms: 1.05x faster                                                 |
| deepcopy_reduce            | 3.12 us                                                                | 2.99 us: 1.04x faster                                                 |
| html5lib                   | 68.6 ms                                                                | 65.8 ms: 1.04x faster                                                 |
| xml_etree_parse            | 136 ms                                                                 | 131 ms: 1.03x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 23.0 ms: 1.01x faster                                                 |
| async_generators           | 375 ms                                                                 | 371 ms: 1.01x faster                                                  |
| bpe_tokeniser              | 4.46 sec                                                               | 4.43 sec: 1.01x faster                                                |
| generators                 | 28.5 ms                                                                | 28.9 ms: 1.01x slower                                                 |
| spectral_norm              | 108 ms                                                                 | 109 ms: 1.01x slower                                                  |
| pycparser                  | 1.12 sec                                                               | 1.13 sec: 1.01x slower                                                |
| pathlib                    | 19.3 ms                                                                | 19.6 ms: 1.02x slower                                                 |
| docutils                   | 2.63 sec                                                               | 2.70 sec: 1.03x slower                                                |
| json                       | 4.98 ms                                                                | 5.16 ms: 1.04x slower                                                 |
| scimark_fft                | 348 ms                                                                 | 365 ms: 1.05x slower                                                  |
| tomli_loads                | 2.01 sec                                                               | 2.15 sec: 1.07x slower                                                |
| pprint_safe_repr           | 719 ms                                                                 | 776 ms: 1.08x slower                                                  |
| pyflate                    | 449 ms                                                                 | 486 ms: 1.08x slower                                                  |
| json_dumps                 | 10.6 ms                                                                | 11.6 ms: 1.09x slower                                                 |
| create_gc_cycles           | 1.33 ms                                                                | 1.46 ms: 1.09x slower                                                 |
| unpickle_pure_python       | 208 us                                                                 | 229 us: 1.10x slower                                                  |
| 2to3                       | 259 ms                                                                 | 285 ms: 1.10x slower                                                  |
| regex_compile              | 131 ms                                                                 | 145 ms: 1.10x slower                                                  |
| chaos                      | 56.3 ms                                                                | 62.1 ms: 1.10x slower                                                 |
| hexiom                     | 5.95 ms                                                                | 6.58 ms: 1.11x slower                                                 |
| pprint_pformat             | 1.46 sec                                                               | 1.61 sec: 1.11x slower                                                |
| thrift                     | 772 us                                                                 | 858 us: 1.11x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                                | 95.4 ms: 1.12x slower                                                 |
| json_loads                 | 27.3 us                                                                | 30.6 us: 1.12x slower                                                 |
| sympy_integrate            | 19.7 ms                                                                | 22.2 ms: 1.12x slower                                                 |
| scimark_lu                 | 112 ms                                                                 | 126 ms: 1.12x slower                                                  |
| nqueens                    | 77.7 ms                                                                | 87.6 ms: 1.13x slower                                                 |
| telco                      | 7.77 ms                                                                | 8.80 ms: 1.13x slower                                                 |
| richards                   | 44.4 ms                                                                | 50.5 ms: 1.14x slower                                                 |
| genshi_xml                 | 49.1 ms                                                                | 55.8 ms: 1.14x slower                                                 |
| deltablue                  | 3.10 ms                                                                | 3.53 ms: 1.14x slower                                                 |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.42 ms: 1.14x slower                                                 |
| richards_super             | 50.4 ms                                                                | 57.7 ms: 1.15x slower                                                 |
| pickle_pure_python         | 292 us                                                                 | 334 us: 1.15x slower                                                  |
| sympy_sum                  | 154 ms                                                                 | 178 ms: 1.16x slower                                                  |
| sympy_str                  | 274 ms                                                                 | 317 ms: 1.16x slower                                                  |
| xml_etree_process          | 59.2 ms                                                                | 68.6 ms: 1.16x slower                                                 |
| comprehensions             | 16.6 us                                                                | 19.3 us: 1.16x slower                                                 |
| scimark_monte_carlo        | 65.8 ms                                                                | 76.7 ms: 1.17x slower                                                 |
| sympy_expand               | 454 ms                                                                 | 532 ms: 1.17x slower                                                  |
| raytrace                   | 250 ms                                                                 | 294 ms: 1.18x slower                                                  |
| django_template            | 34.2 ms                                                                | 40.5 ms: 1.18x slower                                                 |
| genshi_text                | 21.7 ms                                                                | 26.2 ms: 1.20x slower                                                 |
| meteor_contest             | 101 ms                                                                 | 127 ms: 1.25x slower                                                  |
| logging_simple             | 6.14 us                                                                | 7.69 us: 1.25x slower                                                 |
| crypto_pyaes               | 68.2 ms                                                                | 85.4 ms: 1.25x slower                                                 |
| fannkuch                   | 376 ms                                                                 | 475 ms: 1.26x slower                                                  |
| typing_runtime_protocols   | 156 us                                                                 | 197 us: 1.27x slower                                                  |
| logging_format             | 6.92 us                                                                | 8.77 us: 1.27x slower                                                 |
| python_startup_no_site     | 7.41 ms                                                                | 9.57 ms: 1.29x slower                                                 |
| coverage                   | 82.5 ms                                                                | 109 ms: 1.32x slower                                                  |
| mako                       | 11.2 ms                                                                | 15.6 ms: 1.39x slower                                                 |
| nbody                      | 85.3 ms                                                                | 120 ms: 1.41x slower                                                  |
| python_startup             | 11.0 ms                                                                | 16.0 ms: 1.45x slower                                                 |
| bench_thread_pool          | 924 us                                                                 | 3.13 ms: 3.39x slower                                                 |
| logging_silent             | 98.2 ns                                                                | 539 ns: 5.49x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                                | 103 ms: 9.41x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.08x slower                                                          |

Benchmark hidden because not significant (2): pylint, asyncio_websockets
Ignored benchmarks (18) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250514-3.15.0a0-e123a1d-NOGIL/bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.021x slower

# HPT report

- Reliability score: 95.61% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.40x