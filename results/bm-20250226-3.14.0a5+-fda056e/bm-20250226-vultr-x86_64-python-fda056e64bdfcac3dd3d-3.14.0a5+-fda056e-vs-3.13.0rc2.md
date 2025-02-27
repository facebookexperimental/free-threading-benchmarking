# Results vs. 3.13.0rc2

- fork: python
- ref: fda056e64bdfcac3dd3d
- machine: linux-x86_64
- commit hash: fda056e
- commit date: 2025-02-26
- overall geometric mean: 1.059x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 250 ms: 1.04x faster                                                   |
| docutils       | 2.63 sec                                                               | 2.53 sec: 1.04x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 600 ms: 1.50x faster                                                   |
| async_tree_memoization     | 459 ms                                                                 | 311 ms: 1.47x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 599 ms: 1.47x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 487 ms: 1.37x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 259 ms: 1.37x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 307 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 478 ms: 1.33x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 254 ms: 1.31x faster                                                   |
| async_generators           | 375 ms                                                                 | 316 ms: 1.18x faster                                                   |
| coroutines                 | 23.3 ms                                                                | 21.3 ms: 1.10x faster                                                  |
| asyncio_websockets         | 517 ms                                                                 | 516 ms: 1.00x faster                                                   |
| Geometric mean             | (ref)                                                                  | 1.30x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 76.7 ms                                                                | 70.4 ms: 1.09x faster                                                  |
| pidigits       | 216 ms                                                                 | 212 ms: 1.02x faster                                                   |
| nbody          | 85.3 ms                                                                | 84.1 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.73 ms: 1.18x faster                                                  |
| regex_dna      | 189 ms                                                                 | 173 ms: 1.09x faster                                                   |
| regex_compile  | 131 ms                                                                 | 124 ms: 1.06x faster                                                   |
| regex_v8       | 23.2 ms                                                                | 24.8 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|---------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads         | 2.01 sec                                                               | 1.85 sec: 1.09x faster                                                 |
| xml_etree_parse     | 136 ms                                                                 | 128 ms: 1.06x faster                                                   |
| xml_etree_iterparse | 94.4 ms                                                                | 89.7 ms: 1.05x faster                                                  |
| xml_etree_generate  | 85.4 ms                                                                | 81.5 ms: 1.05x faster                                                  |
| xml_etree_process   | 59.2 ms                                                                | 56.8 ms: 1.04x faster                                                  |
| pickle_pure_python  | 292 us                                                                 | 304 us: 1.04x slower                                                   |
| json_loads          | 27.3 us                                                                | 28.6 us: 1.05x slower                                                  |
| json_dumps          | 10.6 ms                                                                | 11.2 ms: 1.05x slower                                                  |
| Geometric mean      | (ref)                                                                  | 1.02x faster                                                           |

Benchmark hidden because not significant (1): unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 7.54 ms: 1.02x slower                                                  |
| python_startup         | 11.0 ms                                                                | 14.8 ms: 1.34x slower                                                  |
| Geometric mean         | (ref)                                                                  | 1.17x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 21.7 ms                                                                | 20.3 ms: 1.07x faster                                                  |
| django_template | 34.2 ms                                                                | 32.8 ms: 1.04x faster                                                  |
| genshi_xml      | 49.1 ms                                                                | 47.1 ms: 1.04x faster                                                  |
| mako            | 11.2 ms                                                                | 11.5 ms: 1.03x slower                                                  |
| Geometric mean  | (ref)                                                                  | 1.03x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 600 ms: 1.50x faster                                                   |
| async_tree_memoization     | 459 ms                                                                 | 311 ms: 1.47x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 599 ms: 1.47x faster                                                   |
| deepcopy                   | 357 us                                                                 | 244 us: 1.47x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 487 ms: 1.37x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 259 ms: 1.37x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 307 ms: 1.34x faster                                                   |
| deepcopy_memo              | 38.1 us                                                                | 28.7 us: 1.33x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 478 ms: 1.33x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 254 ms: 1.31x faster                                                   |
| go                         | 141 ms                                                                 | 111 ms: 1.27x faster                                                   |
| spectral_norm              | 108 ms                                                                 | 86.6 ms: 1.24x faster                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 2.52 us: 1.24x faster                                                  |
| scimark_sor                | 134 ms                                                                 | 110 ms: 1.21x faster                                                   |
| async_generators           | 375 ms                                                                 | 316 ms: 1.18x faster                                                   |
| regex_effbot               | 3.21 ms                                                                | 2.73 ms: 1.18x faster                                                  |
| pylint                     | 317 ms                                                                 | 274 ms: 1.16x faster                                                   |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.19 ms: 1.13x faster                                                  |
| pyflate                    | 449 ms                                                                 | 396 ms: 1.13x faster                                                   |
| scimark_fft                | 348 ms                                                                 | 311 ms: 1.12x faster                                                   |
| coroutines                 | 23.3 ms                                                                | 21.3 ms: 1.10x faster                                                  |
| float                      | 76.7 ms                                                                | 70.4 ms: 1.09x faster                                                  |
| tomli_loads                | 2.01 sec                                                               | 1.85 sec: 1.09x faster                                                 |
| regex_dna                  | 189 ms                                                                 | 173 ms: 1.09x faster                                                   |
| telco                      | 7.77 ms                                                                | 7.17 ms: 1.08x faster                                                  |
| bpe_tokeniser              | 4.46 sec                                                               | 4.12 sec: 1.08x faster                                                 |
| generators                 | 28.5 ms                                                                | 26.6 ms: 1.07x faster                                                  |
| richards                   | 44.4 ms                                                                | 41.4 ms: 1.07x faster                                                  |
| genshi_text                | 21.7 ms                                                                | 20.3 ms: 1.07x faster                                                  |
| richards_super             | 50.4 ms                                                                | 47.0 ms: 1.07x faster                                                  |
| scimark_monte_carlo        | 65.8 ms                                                                | 61.7 ms: 1.07x faster                                                  |
| hexiom                     | 5.95 ms                                                                | 5.59 ms: 1.06x faster                                                  |
| xml_etree_parse            | 136 ms                                                                 | 128 ms: 1.06x faster                                                   |
| regex_compile              | 131 ms                                                                 | 124 ms: 1.06x faster                                                   |
| meteor_contest             | 101 ms                                                                 | 95.8 ms: 1.06x faster                                                  |
| pprint_safe_repr           | 719 ms                                                                 | 681 ms: 1.06x faster                                                   |
| xml_etree_iterparse        | 94.4 ms                                                                | 89.7 ms: 1.05x faster                                                  |
| chaos                      | 56.3 ms                                                                | 53.7 ms: 1.05x faster                                                  |
| xml_etree_generate         | 85.4 ms                                                                | 81.5 ms: 1.05x faster                                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.39 sec: 1.05x faster                                                 |
| coverage                   | 82.5 ms                                                                | 78.9 ms: 1.05x faster                                                  |
| sqlglot_optimize           | 52.7 ms                                                                | 50.4 ms: 1.05x faster                                                  |
| xml_etree_process          | 59.2 ms                                                                | 56.8 ms: 1.04x faster                                                  |
| django_template            | 34.2 ms                                                                | 32.8 ms: 1.04x faster                                                  |
| nqueens                    | 77.7 ms                                                                | 74.6 ms: 1.04x faster                                                  |
| thrift                     | 772 us                                                                 | 741 us: 1.04x faster                                                   |
| genshi_xml                 | 49.1 ms                                                                | 47.1 ms: 1.04x faster                                                  |
| docutils                   | 2.63 sec                                                               | 2.53 sec: 1.04x faster                                                 |
| comprehensions             | 16.6 us                                                                | 16.0 us: 1.04x faster                                                  |
| logging_simple             | 6.14 us                                                                | 5.92 us: 1.04x faster                                                  |
| 2to3                       | 259 ms                                                                 | 250 ms: 1.04x faster                                                   |
| crypto_pyaes               | 68.2 ms                                                                | 65.9 ms: 1.03x faster                                                  |
| typing_runtime_protocols   | 156 us                                                                 | 151 us: 1.03x faster                                                   |
| logging_format             | 6.92 us                                                                | 6.71 us: 1.03x faster                                                  |
| sympy_str                  | 274 ms                                                                 | 266 ms: 1.03x faster                                                   |
| sympy_sum                  | 154 ms                                                                 | 150 ms: 1.03x faster                                                   |
| sympy_integrate            | 19.7 ms                                                                | 19.3 ms: 1.02x faster                                                  |
| fannkuch                   | 376 ms                                                                 | 367 ms: 1.02x faster                                                   |
| pidigits                   | 216 ms                                                                 | 212 ms: 1.02x faster                                                   |
| sqlglot_transpile          | 1.55 ms                                                                | 1.52 ms: 1.02x faster                                                  |
| sqlite_synth               | 2.25 us                                                                | 2.20 us: 1.02x faster                                                  |
| sympy_expand               | 454 ms                                                                 | 446 ms: 1.02x faster                                                   |
| sqlglot_parse              | 1.25 ms                                                                | 1.23 ms: 1.02x faster                                                  |
| nbody                      | 85.3 ms                                                                | 84.1 ms: 1.01x faster                                                  |
| pycparser                  | 1.12 sec                                                               | 1.10 sec: 1.01x faster                                                 |
| scimark_lu                 | 112 ms                                                                 | 111 ms: 1.01x faster                                                   |
| deltablue                  | 3.10 ms                                                                | 3.07 ms: 1.01x faster                                                  |
| pathlib                    | 19.3 ms                                                                | 19.1 ms: 1.01x faster                                                  |
| asyncio_websockets         | 517 ms                                                                 | 516 ms: 1.00x faster                                                   |
| json                       | 4.98 ms                                                                | 5.06 ms: 1.02x slower                                                  |
| python_startup_no_site     | 7.41 ms                                                                | 7.54 ms: 1.02x slower                                                  |
| dulwich_log                | 74.5 ms                                                                | 75.9 ms: 1.02x slower                                                  |
| raytrace                   | 250 ms                                                                 | 255 ms: 1.02x slower                                                   |
| mako                       | 11.2 ms                                                                | 11.5 ms: 1.03x slower                                                  |
| mdp                        | 2.34 sec                                                               | 2.42 sec: 1.03x slower                                                 |
| logging_silent             | 98.2 ns                                                                | 102 ns: 1.04x slower                                                   |
| pickle_pure_python         | 292 us                                                                 | 304 us: 1.04x slower                                                   |
| json_loads                 | 27.3 us                                                                | 28.6 us: 1.05x slower                                                  |
| json_dumps                 | 10.6 ms                                                                | 11.2 ms: 1.05x slower                                                  |
| regex_v8                   | 23.2 ms                                                                | 24.8 ms: 1.07x slower                                                  |
| bench_thread_pool          | 924 us                                                                 | 1.03 ms: 1.11x slower                                                  |
| gc_traversal               | 3.32 ms                                                                | 4.44 ms: 1.34x slower                                                  |
| python_startup             | 11.0 ms                                                                | 14.8 ms: 1.34x slower                                                  |
| create_gc_cycles           | 1.33 ms                                                                | 1.83 ms: 1.37x slower                                                  |
| sqlglot_normalize          | 106 ms                                                                 | 277 ms: 2.62x slower                                                   |
| bench_mp_pool              | 11.0 ms                                                                | 88.0 ms: 8.00x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (1): unpickle_pure_python
Ignored benchmarks (15) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250226-3.14.0a5+-fda056e/bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.059x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.10x