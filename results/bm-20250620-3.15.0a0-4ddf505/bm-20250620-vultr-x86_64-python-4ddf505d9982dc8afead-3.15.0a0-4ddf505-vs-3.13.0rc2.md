# Results vs. 3.13.0rc2

- fork: python
- ref: 4ddf505d9982dc8afead
- machine: linux-x86_64
- commit hash: 4ddf505
- commit date: 2025-06-20
- overall geometric mean: 1.070x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 249 ms: 1.04x faster                                                  |
| docutils       | 2.63 sec                                                               | 2.53 sec: 1.04x faster                                                |
| html5lib       | 68.6 ms                                                                | 60.8 ms: 1.13x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.07x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization     | 459 ms                                                                 | 308 ms: 1.49x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 622 ms: 1.45x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 609 ms: 1.45x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 307 ms: 1.33x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 250 ms: 1.33x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 268 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 511 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 509 ms: 1.24x faster                                                  |
| async_generators           | 375 ms                                                                 | 332 ms: 1.13x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 22.9 ms: 1.02x faster                                                 |
| Geometric mean             | (ref)                                                                  | 1.27x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 196 ms: 1.10x faster                                                  |
| float          | 76.7 ms                                                                | 71.6 ms: 1.07x faster                                                 |
| nbody          | 85.3 ms                                                                | 88.5 ms: 1.04x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.88 ms: 1.11x faster                                                 |
| regex_dna      | 189 ms                                                                 | 175 ms: 1.08x faster                                                  |
| regex_compile  | 131 ms                                                                 | 124 ms: 1.06x faster                                                  |
| regex_v8       | 23.2 ms                                                                | 22.7 ms: 1.02x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.07x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|---------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads         | 2.01 sec                                                               | 1.90 sec: 1.06x faster                                                |
| xml_etree_generate  | 85.4 ms                                                                | 83.0 ms: 1.03x faster                                                 |
| xml_etree_iterparse | 94.4 ms                                                                | 92.1 ms: 1.02x faster                                                 |
| xml_etree_parse     | 136 ms                                                                 | 133 ms: 1.02x faster                                                  |
| xml_etree_process   | 59.2 ms                                                                | 58.2 ms: 1.02x faster                                                 |
| json_dumps          | 10.6 ms                                                                | 10.7 ms: 1.01x slower                                                 |
| json_loads          | 27.3 us                                                                | 28.6 us: 1.05x slower                                                 |
| pickle_pure_python  | 292 us                                                                 | 309 us: 1.06x slower                                                  |
| Geometric mean      | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (1): unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 7.33 ms: 1.01x faster                                                 |
| python_startup         | 11.0 ms                                                                | 12.6 ms: 1.14x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.06x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 21.7 ms                                                                | 21.1 ms: 1.03x faster                                                 |
| genshi_xml      | 49.1 ms                                                                | 48.2 ms: 1.02x faster                                                 |
| django_template | 34.2 ms                                                                | 34.5 ms: 1.01x slower                                                 |
| mako            | 11.2 ms                                                                | 11.7 ms: 1.04x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.00x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.34 sec                                                               | 1.14 sec: 2.05x faster                                                |
| async_tree_memoization     | 459 ms                                                                 | 308 ms: 1.49x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 622 ms: 1.45x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 609 ms: 1.45x faster                                                  |
| deepcopy                   | 357 us                                                                 | 252 us: 1.42x faster                                                  |
| go                         | 141 ms                                                                 | 103 ms: 1.37x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 307 ms: 1.33x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 250 ms: 1.33x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 28.8 us: 1.32x faster                                                 |
| async_tree_none            | 353 ms                                                                 | 268 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 511 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 509 ms: 1.24x faster                                                  |
| scimark_sor                | 134 ms                                                                 | 107 ms: 1.24x faster                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 2.64 us: 1.18x faster                                                 |
| pyflate                    | 449 ms                                                                 | 391 ms: 1.15x faster                                                  |
| pylint                     | 317 ms                                                                 | 278 ms: 1.14x faster                                                  |
| async_generators           | 375 ms                                                                 | 332 ms: 1.13x faster                                                  |
| html5lib                   | 68.6 ms                                                                | 60.8 ms: 1.13x faster                                                 |
| spectral_norm              | 108 ms                                                                 | 96.4 ms: 1.12x faster                                                 |
| regex_effbot               | 3.21 ms                                                                | 2.88 ms: 1.11x faster                                                 |
| dulwich_log                | 74.5 ms                                                                | 66.9 ms: 1.11x faster                                                 |
| pidigits                   | 216 ms                                                                 | 196 ms: 1.10x faster                                                  |
| scimark_monte_carlo        | 65.8 ms                                                                | 60.2 ms: 1.09x faster                                                 |
| richards                   | 44.4 ms                                                                | 40.8 ms: 1.09x faster                                                 |
| richards_super             | 50.4 ms                                                                | 46.5 ms: 1.08x faster                                                 |
| telco                      | 7.77 ms                                                                | 7.19 ms: 1.08x faster                                                 |
| regex_dna                  | 189 ms                                                                 | 175 ms: 1.08x faster                                                  |
| bpe_tokeniser              | 4.46 sec                                                               | 4.15 sec: 1.07x faster                                                |
| float                      | 76.7 ms                                                                | 71.6 ms: 1.07x faster                                                 |
| comprehensions             | 16.6 us                                                                | 15.6 us: 1.06x faster                                                 |
| tomli_loads                | 2.01 sec                                                               | 1.90 sec: 1.06x faster                                                |
| regex_compile              | 131 ms                                                                 | 124 ms: 1.06x faster                                                  |
| sympy_integrate            | 19.7 ms                                                                | 18.6 ms: 1.06x faster                                                 |
| scimark_fft                | 348 ms                                                                 | 330 ms: 1.06x faster                                                  |
| hexiom                     | 5.95 ms                                                                | 5.65 ms: 1.05x faster                                                 |
| thrift                     | 772 us                                                                 | 736 us: 1.05x faster                                                  |
| 2to3                       | 259 ms                                                                 | 249 ms: 1.04x faster                                                  |
| docutils                   | 2.63 sec                                                               | 2.53 sec: 1.04x faster                                                |
| generators                 | 28.5 ms                                                                | 27.6 ms: 1.03x faster                                                 |
| genshi_text                | 21.7 ms                                                                | 21.1 ms: 1.03x faster                                                 |
| scimark_lu                 | 112 ms                                                                 | 109 ms: 1.03x faster                                                  |
| nqueens                    | 77.7 ms                                                                | 75.4 ms: 1.03x faster                                                 |
| xml_etree_generate         | 85.4 ms                                                                | 83.0 ms: 1.03x faster                                                 |
| sympy_str                  | 274 ms                                                                 | 267 ms: 1.03x faster                                                  |
| xml_etree_iterparse        | 94.4 ms                                                                | 92.1 ms: 1.02x faster                                                 |
| xml_etree_parse            | 136 ms                                                                 | 133 ms: 1.02x faster                                                  |
| regex_v8                   | 23.2 ms                                                                | 22.7 ms: 1.02x faster                                                 |
| sympy_expand               | 454 ms                                                                 | 445 ms: 1.02x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 22.9 ms: 1.02x faster                                                 |
| genshi_xml                 | 49.1 ms                                                                | 48.2 ms: 1.02x faster                                                 |
| xml_etree_process          | 59.2 ms                                                                | 58.2 ms: 1.02x faster                                                 |
| chaos                      | 56.3 ms                                                                | 55.4 ms: 1.02x faster                                                 |
| crypto_pyaes               | 68.2 ms                                                                | 67.2 ms: 1.02x faster                                                 |
| meteor_contest             | 101 ms                                                                 | 100 ms: 1.01x faster                                                  |
| python_startup_no_site     | 7.41 ms                                                                | 7.33 ms: 1.01x faster                                                 |
| typing_runtime_protocols   | 156 us                                                                 | 154 us: 1.01x faster                                                  |
| coverage                   | 82.5 ms                                                                | 81.6 ms: 1.01x faster                                                 |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.70 ms: 1.01x faster                                                 |
| sympy_sum                  | 154 ms                                                                 | 153 ms: 1.01x faster                                                  |
| fannkuch                   | 376 ms                                                                 | 374 ms: 1.01x faster                                                  |
| json_dumps                 | 10.6 ms                                                                | 10.7 ms: 1.01x slower                                                 |
| pycparser                  | 1.12 sec                                                               | 1.13 sec: 1.01x slower                                                |
| django_template            | 34.2 ms                                                                | 34.5 ms: 1.01x slower                                                 |
| json                       | 4.98 ms                                                                | 5.15 ms: 1.03x slower                                                 |
| deltablue                  | 3.10 ms                                                                | 3.20 ms: 1.03x slower                                                 |
| nbody                      | 85.3 ms                                                                | 88.5 ms: 1.04x slower                                                 |
| mako                       | 11.2 ms                                                                | 11.7 ms: 1.04x slower                                                 |
| json_loads                 | 27.3 us                                                                | 28.6 us: 1.05x slower                                                 |
| logging_format             | 6.92 us                                                                | 7.27 us: 1.05x slower                                                 |
| logging_simple             | 6.14 us                                                                | 6.48 us: 1.06x slower                                                 |
| pickle_pure_python         | 292 us                                                                 | 309 us: 1.06x slower                                                  |
| pprint_safe_repr           | 719 ms                                                                 | 764 ms: 1.06x slower                                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.56 sec: 1.07x slower                                                |
| bench_thread_pool          | 924 us                                                                 | 1.04 ms: 1.13x slower                                                 |
| python_startup             | 11.0 ms                                                                | 12.6 ms: 1.14x slower                                                 |
| gc_traversal               | 3.32 ms                                                                | 4.38 ms: 1.32x slower                                                 |
| create_gc_cycles           | 1.33 ms                                                                | 1.91 ms: 1.43x slower                                                 |
| logging_silent             | 98.2 ns                                                                | 464 ns: 4.73x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                                | 99.4 ms: 9.04x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (5): asyncio_websockets, pathlib, unpickle_pure_python, raytrace, sqlite_synth
Ignored benchmarks (18) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250620-3.15.0a0-4ddf505/bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.070x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.15x