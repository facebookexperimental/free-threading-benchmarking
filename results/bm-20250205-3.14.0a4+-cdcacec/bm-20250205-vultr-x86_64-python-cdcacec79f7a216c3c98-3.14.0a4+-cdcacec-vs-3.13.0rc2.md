# Results vs. 3.13.0rc2

- fork: python
- ref: cdcacec79f7a216c3c98
- machine: linux-x86_64
- commit hash: cdcacec
- commit date: 2025-02-05
- overall geometric mean: 1.046x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 252 ms: 1.03x faster                                                   |
| docutils       | 2.62 sec                                                     | 2.54 sec: 1.03x faster                                                 |
| Geometric mean | (ref)                                                        | 1.03x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 623 ms: 1.47x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 323 ms: 1.43x faster                                                   |
| async_tree_io              | 876 ms                                                       | 621 ms: 1.41x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 500 ms: 1.33x faster                                                   |
| async_tree_none            | 354 ms                                                       | 268 ms: 1.32x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 484 ms: 1.32x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 317 ms: 1.31x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 259 ms: 1.30x faster                                                   |
| async_generators           | 377 ms                                                       | 321 ms: 1.18x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 21.6 ms: 1.09x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 516 ms: 1.01x faster                                                   |
| Geometric mean             | (ref)                                                        | 1.28x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 187 ms: 1.16x faster                                                   |
| float          | 77.5 ms                                                      | 71.5 ms: 1.08x faster                                                  |
| nbody          | 85.1 ms                                                      | 95.9 ms: 1.13x slower                                                  |
| Geometric mean | (ref)                                                        | 1.04x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.71 ms: 1.14x faster                                                  |
| regex_dna      | 180 ms                                                       | 165 ms: 1.09x faster                                                   |
| regex_compile  | 132 ms                                                       | 126 ms: 1.05x faster                                                   |
| regex_v8       | 22.7 ms                                                      | 23.8 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                        | 1.06x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 130 ms: 1.05x faster                                                   |
| tomli_loads          | 2.01 sec                                                     | 1.92 sec: 1.05x faster                                                 |
| xml_etree_iterparse  | 94.9 ms                                                      | 91.1 ms: 1.04x faster                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 82.7 ms: 1.03x faster                                                  |
| xml_etree_process    | 59.3 ms                                                      | 57.6 ms: 1.03x faster                                                  |
| unpickle_pure_python | 210 us                                                       | 212 us: 1.01x slower                                                   |
| pickle_pure_python   | 294 us                                                       | 309 us: 1.05x slower                                                   |
| json_loads           | 27.0 us                                                      | 28.7 us: 1.06x slower                                                  |
| json_dumps           | 10.5 ms                                                      | 11.2 ms: 1.07x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.00x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.47 ms: 1.01x slower                                                  |
| python_startup         | 11.0 ms                                                      | 14.7 ms: 1.34x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.16x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 21.1 ms: 1.02x faster                                                  |
| genshi_xml      | 48.8 ms                                                      | 48.0 ms: 1.02x faster                                                  |
| django_template | 34.1 ms                                                      | 33.6 ms: 1.02x faster                                                  |
| mako            | 11.3 ms                                                      | 11.8 ms: 1.04x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.00x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 623 ms: 1.47x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 323 ms: 1.43x faster                                                   |
| deepcopy                   | 355 us                                                       | 249 us: 1.43x faster                                                   |
| async_tree_io              | 876 ms                                                       | 621 ms: 1.41x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 500 ms: 1.33x faster                                                   |
| async_tree_none            | 354 ms                                                       | 268 ms: 1.32x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 484 ms: 1.32x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 317 ms: 1.31x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 259 ms: 1.30x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 30.2 us: 1.29x faster                                                  |
| go                         | 141 ms                                                       | 114 ms: 1.23x faster                                                   |
| spectral_norm              | 111 ms                                                       | 91.1 ms: 1.22x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.57 us: 1.21x faster                                                  |
| async_generators           | 377 ms                                                       | 321 ms: 1.18x faster                                                   |
| scimark_sor                | 134 ms                                                       | 115 ms: 1.17x faster                                                   |
| pidigits                   | 217 ms                                                       | 187 ms: 1.16x faster                                                   |
| pylint                     | 317 ms                                                       | 276 ms: 1.15x faster                                                   |
| regex_effbot               | 3.08 ms                                                      | 2.71 ms: 1.14x faster                                                  |
| scimark_fft                | 349 ms                                                       | 317 ms: 1.10x faster                                                   |
| pyflate                    | 449 ms                                                       | 409 ms: 1.10x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 21.6 ms: 1.09x faster                                                  |
| regex_dna                  | 180 ms                                                       | 165 ms: 1.09x faster                                                   |
| float                      | 77.5 ms                                                      | 71.5 ms: 1.08x faster                                                  |
| richards                   | 45.2 ms                                                      | 41.9 ms: 1.08x faster                                                  |
| richards_super             | 51.6 ms                                                      | 48.0 ms: 1.08x faster                                                  |
| thrift                     | 778 us                                                       | 723 us: 1.08x faster                                                   |
| pprint_safe_repr           | 738 ms                                                       | 686 ms: 1.07x faster                                                   |
| telco                      | 7.82 ms                                                      | 7.33 ms: 1.07x faster                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.40 sec: 1.07x faster                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.19 sec: 1.06x faster                                                 |
| pathlib                    | 19.2 ms                                                      | 18.1 ms: 1.06x faster                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.47 ms: 1.05x faster                                                  |
| coverage                   | 83.0 ms                                                      | 78.8 ms: 1.05x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 130 ms: 1.05x faster                                                   |
| regex_compile              | 132 ms                                                       | 126 ms: 1.05x faster                                                   |
| tomli_loads                | 2.01 sec                                                     | 1.92 sec: 1.05x faster                                                 |
| logging_simple             | 6.16 us                                                      | 5.90 us: 1.04x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 91.1 ms: 1.04x faster                                                  |
| meteor_contest             | 102 ms                                                       | 97.8 ms: 1.04x faster                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 63.1 ms: 1.04x faster                                                  |
| sqlglot_optimize           | 52.7 ms                                                      | 51.0 ms: 1.03x faster                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 82.7 ms: 1.03x faster                                                  |
| xml_etree_process          | 59.3 ms                                                      | 57.6 ms: 1.03x faster                                                  |
| 2to3                       | 260 ms                                                       | 252 ms: 1.03x faster                                                   |
| docutils                   | 2.62 sec                                                     | 2.54 sec: 1.03x faster                                                 |
| typing_runtime_protocols   | 155 us                                                       | 150 us: 1.03x faster                                                   |
| hexiom                     | 5.99 ms                                                      | 5.83 ms: 1.03x faster                                                  |
| sympy_sum                  | 156 ms                                                       | 152 ms: 1.02x faster                                                   |
| genshi_text                | 21.5 ms                                                      | 21.1 ms: 1.02x faster                                                  |
| sqlglot_transpile          | 1.56 ms                                                      | 1.53 ms: 1.02x faster                                                  |
| sympy_str                  | 275 ms                                                       | 270 ms: 1.02x faster                                                   |
| genshi_xml                 | 48.8 ms                                                      | 48.0 ms: 1.02x faster                                                  |
| mdp                        | 2.36 sec                                                     | 2.32 sec: 1.02x faster                                                 |
| django_template            | 34.1 ms                                                      | 33.6 ms: 1.02x faster                                                  |
| sympy_integrate            | 19.8 ms                                                      | 19.5 ms: 1.01x faster                                                  |
| sqlglot_parse              | 1.25 ms                                                      | 1.23 ms: 1.01x faster                                                  |
| chaos                      | 57.3 ms                                                      | 56.6 ms: 1.01x faster                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 67.2 ms: 1.01x faster                                                  |
| sympy_expand               | 457 ms                                                       | 453 ms: 1.01x faster                                                   |
| sqlite_synth               | 2.21 us                                                      | 2.19 us: 1.01x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 516 ms: 1.01x faster                                                   |
| logging_silent             | 103 ns                                                       | 102 ns: 1.01x faster                                                   |
| pycparser                  | 1.12 sec                                                     | 1.11 sec: 1.01x faster                                                 |
| nqueens                    | 78.6 ms                                                      | 78.2 ms: 1.01x faster                                                  |
| comprehensions             | 16.5 us                                                      | 16.5 us: 1.00x slower                                                  |
| scimark_lu                 | 113 ms                                                       | 113 ms: 1.00x slower                                                   |
| python_startup_no_site     | 7.39 ms                                                      | 7.47 ms: 1.01x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 212 us: 1.01x slower                                                   |
| raytrace                   | 253 ms                                                       | 260 ms: 1.03x slower                                                   |
| json                       | 4.93 ms                                                      | 5.09 ms: 1.03x slower                                                  |
| mako                       | 11.3 ms                                                      | 11.8 ms: 1.04x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 309 us: 1.05x slower                                                   |
| regex_v8                   | 22.7 ms                                                      | 23.8 ms: 1.05x slower                                                  |
| json_loads                 | 27.0 us                                                      | 28.7 us: 1.06x slower                                                  |
| json_dumps                 | 10.5 ms                                                      | 11.2 ms: 1.07x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.03 ms: 1.12x slower                                                  |
| nbody                      | 85.1 ms                                                      | 95.9 ms: 1.13x slower                                                  |
| python_startup             | 11.0 ms                                                      | 14.7 ms: 1.34x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 4.22 ms: 1.34x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.86 ms: 1.39x slower                                                  |
| sqlglot_normalize          | 106 ms                                                       | 281 ms: 2.66x slower                                                   |
| bench_mp_pool              | 11.0 ms                                                      | 88.0 ms: 8.00x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.02x faster                                                           |

Benchmark hidden because not significant (5): logging_format, fannkuch, generators, deltablue, dulwich_log
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250205-3.14.0a4+-cdcacec/bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.046x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.10x