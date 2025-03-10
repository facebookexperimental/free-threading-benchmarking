# Results vs. 3.13.0rc2

- fork: python
- ref: 98fa4a49fecbac3c990a
- machine: linux-x86_64
- commit hash: 98fa4a4
- commit date: 2025-03-09
- overall geometric mean: 1.074x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250309-vultr-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 245 ms: 1.06x faster                                                   |
| docutils       | 2.63 sec                                                               | 2.53 sec: 1.04x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250309-vultr-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 605 ms: 1.49x faster                                                   |
| async_tree_memoization     | 459 ms                                                                 | 312 ms: 1.47x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 604 ms: 1.46x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 259 ms: 1.36x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 490 ms: 1.36x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 308 ms: 1.33x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 252 ms: 1.32x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 479 ms: 1.32x faster                                                   |
| async_generators           | 375 ms                                                                 | 318 ms: 1.18x faster                                                   |
| coroutines                 | 23.3 ms                                                                | 22.0 ms: 1.06x faster                                                  |
| Geometric mean             | (ref)                                                                  | 1.30x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250309-vultr-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 191 ms: 1.14x faster                                                   |
| float          | 76.7 ms                                                                | 70.7 ms: 1.09x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.07x faster                                                           |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250309-vultr-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.78 ms: 1.15x faster                                                  |
| regex_dna      | 189 ms                                                                 | 175 ms: 1.07x faster                                                   |
| regex_compile  | 131 ms                                                                 | 123 ms: 1.07x faster                                                   |
| regex_v8       | 23.2 ms                                                                | 24.2 ms: 1.04x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250309-vultr-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                               | 1.88 sec: 1.07x faster                                                 |
| xml_etree_parse      | 136 ms                                                                 | 128 ms: 1.06x faster                                                   |
| xml_etree_iterparse  | 94.4 ms                                                                | 90.0 ms: 1.05x faster                                                  |
| xml_etree_generate   | 85.4 ms                                                                | 82.1 ms: 1.04x faster                                                  |
| xml_etree_process    | 59.2 ms                                                                | 57.2 ms: 1.04x faster                                                  |
| unpickle_pure_python | 208 us                                                                 | 206 us: 1.01x faster                                                   |
| pickle_pure_python   | 292 us                                                                 | 299 us: 1.03x slower                                                   |
| json_dumps           | 10.6 ms                                                                | 11.0 ms: 1.03x slower                                                  |
| json_loads           | 27.3 us                                                                | 28.3 us: 1.03x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.02x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250309-vultr-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 8.53 ms: 1.15x slower                                                  |
| python_startup         | 11.0 ms                                                                | 14.8 ms: 1.34x slower                                                  |
| Geometric mean         | (ref)                                                                  | 1.24x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250309-vultr-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 21.7 ms                                                                | 20.6 ms: 1.06x faster                                                  |
| django_template | 34.2 ms                                                                | 32.7 ms: 1.04x faster                                                  |
| genshi_xml      | 49.1 ms                                                                | 47.0 ms: 1.04x faster                                                  |
| mako            | 11.2 ms                                                                | 11.6 ms: 1.03x slower                                                  |
| Geometric mean  | (ref)                                                                  | 1.03x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250309-vultr-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 605 ms: 1.49x faster                                                   |
| async_tree_memoization     | 459 ms                                                                 | 312 ms: 1.47x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 604 ms: 1.46x faster                                                   |
| deepcopy                   | 357 us                                                                 | 246 us: 1.45x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 259 ms: 1.36x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 490 ms: 1.36x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 308 ms: 1.33x faster                                                   |
| deepcopy_memo              | 38.1 us                                                                | 28.6 us: 1.33x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 252 ms: 1.32x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 479 ms: 1.32x faster                                                   |
| go                         | 141 ms                                                                 | 110 ms: 1.28x faster                                                   |
| deepcopy_reduce            | 3.12 us                                                                | 2.50 us: 1.25x faster                                                  |
| scimark_sor                | 134 ms                                                                 | 111 ms: 1.20x faster                                                   |
| spectral_norm              | 108 ms                                                                 | 91.0 ms: 1.18x faster                                                  |
| async_generators           | 375 ms                                                                 | 318 ms: 1.18x faster                                                   |
| pylint                     | 317 ms                                                                 | 273 ms: 1.16x faster                                                   |
| regex_effbot               | 3.21 ms                                                                | 2.78 ms: 1.15x faster                                                  |
| dulwich_log                | 74.5 ms                                                                | 65.6 ms: 1.14x faster                                                  |
| pidigits                   | 216 ms                                                                 | 191 ms: 1.14x faster                                                   |
| pyflate                    | 449 ms                                                                 | 399 ms: 1.13x faster                                                   |
| scimark_fft                | 348 ms                                                                 | 317 ms: 1.10x faster                                                   |
| float                      | 76.7 ms                                                                | 70.7 ms: 1.09x faster                                                  |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.38 ms: 1.09x faster                                                  |
| thrift                     | 772 us                                                                 | 716 us: 1.08x faster                                                   |
| richards                   | 44.4 ms                                                                | 41.2 ms: 1.08x faster                                                  |
| bpe_tokeniser              | 4.46 sec                                                               | 4.14 sec: 1.08x faster                                                 |
| regex_dna                  | 189 ms                                                                 | 175 ms: 1.07x faster                                                   |
| richards_super             | 50.4 ms                                                                | 47.1 ms: 1.07x faster                                                  |
| regex_compile              | 131 ms                                                                 | 123 ms: 1.07x faster                                                   |
| logging_simple             | 6.14 us                                                                | 5.75 us: 1.07x faster                                                  |
| logging_format             | 6.92 us                                                                | 6.47 us: 1.07x faster                                                  |
| tomli_loads                | 2.01 sec                                                               | 1.88 sec: 1.07x faster                                                 |
| generators                 | 28.5 ms                                                                | 26.7 ms: 1.07x faster                                                  |
| pprint_safe_repr           | 719 ms                                                                 | 675 ms: 1.06x faster                                                   |
| xml_etree_parse            | 136 ms                                                                 | 128 ms: 1.06x faster                                                   |
| 2to3                       | 259 ms                                                                 | 245 ms: 1.06x faster                                                   |
| coroutines                 | 23.3 ms                                                                | 22.0 ms: 1.06x faster                                                  |
| telco                      | 7.77 ms                                                                | 7.34 ms: 1.06x faster                                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.38 sec: 1.06x faster                                                 |
| nqueens                    | 77.7 ms                                                                | 73.5 ms: 1.06x faster                                                  |
| genshi_text                | 21.7 ms                                                                | 20.6 ms: 1.06x faster                                                  |
| scimark_monte_carlo        | 65.8 ms                                                                | 62.3 ms: 1.06x faster                                                  |
| sqlglot_normalize          | 106 ms                                                                 | 100 ms: 1.05x faster                                                   |
| comprehensions             | 16.6 us                                                                | 15.8 us: 1.05x faster                                                  |
| hexiom                     | 5.95 ms                                                                | 5.66 ms: 1.05x faster                                                  |
| xml_etree_iterparse        | 94.4 ms                                                                | 90.0 ms: 1.05x faster                                                  |
| sqlglot_optimize           | 52.7 ms                                                                | 50.3 ms: 1.05x faster                                                  |
| django_template            | 34.2 ms                                                                | 32.7 ms: 1.04x faster                                                  |
| genshi_xml                 | 49.1 ms                                                                | 47.0 ms: 1.04x faster                                                  |
| chaos                      | 56.3 ms                                                                | 54.0 ms: 1.04x faster                                                  |
| typing_runtime_protocols   | 156 us                                                                 | 149 us: 1.04x faster                                                   |
| coverage                   | 82.5 ms                                                                | 79.2 ms: 1.04x faster                                                  |
| docutils                   | 2.63 sec                                                               | 2.53 sec: 1.04x faster                                                 |
| xml_etree_generate         | 85.4 ms                                                                | 82.1 ms: 1.04x faster                                                  |
| sqlite_synth               | 2.25 us                                                                | 2.17 us: 1.04x faster                                                  |
| xml_etree_process          | 59.2 ms                                                                | 57.2 ms: 1.04x faster                                                  |
| mdp                        | 2.34 sec                                                               | 2.27 sec: 1.03x faster                                                 |
| deltablue                  | 3.10 ms                                                                | 3.00 ms: 1.03x faster                                                  |
| meteor_contest             | 101 ms                                                                 | 98.3 ms: 1.03x faster                                                  |
| sympy_sum                  | 154 ms                                                                 | 150 ms: 1.03x faster                                                   |
| sympy_str                  | 274 ms                                                                 | 266 ms: 1.03x faster                                                   |
| sympy_integrate            | 19.7 ms                                                                | 19.2 ms: 1.03x faster                                                  |
| scimark_lu                 | 112 ms                                                                 | 110 ms: 1.02x faster                                                   |
| pycparser                  | 1.12 sec                                                               | 1.10 sec: 1.02x faster                                                 |
| fannkuch                   | 376 ms                                                                 | 368 ms: 1.02x faster                                                   |
| sqlglot_transpile          | 1.55 ms                                                                | 1.53 ms: 1.02x faster                                                  |
| crypto_pyaes               | 68.2 ms                                                                | 67.3 ms: 1.01x faster                                                  |
| unpickle_pure_python       | 208 us                                                                 | 206 us: 1.01x faster                                                   |
| sqlglot_parse              | 1.25 ms                                                                | 1.24 ms: 1.01x faster                                                  |
| sympy_expand               | 454 ms                                                                 | 450 ms: 1.01x faster                                                   |
| pathlib                    | 19.3 ms                                                                | 19.1 ms: 1.01x faster                                                  |
| raytrace                   | 250 ms                                                                 | 251 ms: 1.01x slower                                                   |
| pickle_pure_python         | 292 us                                                                 | 299 us: 1.03x slower                                                   |
| mako                       | 11.2 ms                                                                | 11.6 ms: 1.03x slower                                                  |
| json_dumps                 | 10.6 ms                                                                | 11.0 ms: 1.03x slower                                                  |
| json_loads                 | 27.3 us                                                                | 28.3 us: 1.03x slower                                                  |
| regex_v8                   | 23.2 ms                                                                | 24.2 ms: 1.04x slower                                                  |
| bench_thread_pool          | 924 us                                                                 | 1.03 ms: 1.11x slower                                                  |
| python_startup_no_site     | 7.41 ms                                                                | 8.53 ms: 1.15x slower                                                  |
| gc_traversal               | 3.32 ms                                                                | 4.21 ms: 1.27x slower                                                  |
| python_startup             | 11.0 ms                                                                | 14.8 ms: 1.34x slower                                                  |
| create_gc_cycles           | 1.33 ms                                                                | 1.84 ms: 1.38x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                                | 86.7 ms: 7.89x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.05x faster                                                           |

Benchmark hidden because not significant (4): json, logging_silent, asyncio_websockets, nbody
Ignored benchmarks (15) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250309-3.14.0a5+-98fa4a4/bm-20250309-vultr-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.074x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.10x