# Results vs. 3.12.6

- fork: python
- ref: cdcacec79f7a216c3c98
- machine: linux-x86_64
- commit hash: cdcacec
- commit date: 2025-02-05
- overall geometric mean: 1.085x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 252 ms: 1.05x faster                                                   |
| docutils       | 2.64 sec                                               | 2.54 sec: 1.04x faster                                                 |
| Geometric mean | (ref)                                                  | 1.04x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 623 ms: 1.78x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 317 ms: 1.77x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 621 ms: 1.74x faster                                                   |
| async_tree_none            | 464 ms                                                 | 268 ms: 1.73x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 259 ms: 1.73x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 323 ms: 1.72x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 484 ms: 1.49x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 500 ms: 1.43x faster                                                   |
| async_generators           | 384 ms                                                 | 321 ms: 1.20x faster                                                   |
| coroutines                 | 23.9 ms                                                | 21.6 ms: 1.11x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.49x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 71.5 ms: 1.13x faster                                                  |
| pidigits       | 184 ms                                                 | 187 ms: 1.01x slower                                                   |
| nbody          | 89.3 ms                                                | 95.9 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.71 ms: 1.17x faster                                                  |
| regex_compile  | 142 ms                                                 | 126 ms: 1.13x faster                                                   |
| regex_dna      | 168 ms                                                 | 165 ms: 1.02x faster                                                   |
| regex_v8       | 20.6 ms                                                | 23.8 ms: 1.16x slower                                                  |
| Geometric mean | (ref)                                                  | 1.04x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.92 sec: 1.10x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                                   |
| xml_etree_iterparse  | 96.7 ms                                                | 91.1 ms: 1.06x faster                                                  |
| unpickle_pure_python | 221 us                                                 | 212 us: 1.04x faster                                                   |
| xml_etree_generate   | 85.2 ms                                                | 82.7 ms: 1.03x faster                                                  |
| xml_etree_process    | 59.0 ms                                                | 57.6 ms: 1.02x faster                                                  |
| pickle_pure_python   | 308 us                                                 | 309 us: 1.01x slower                                                   |
| json_loads           | 26.5 us                                                | 28.7 us: 1.08x slower                                                  |
| json_dumps           | 10.4 ms                                                | 11.2 ms: 1.09x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.47 ms: 1.04x slower                                                  |
| python_startup         | 9.93 ms                                                | 14.7 ms: 1.48x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.24x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 21.1 ms: 1.08x faster                                                  |
| genshi_xml      | 50.2 ms                                                | 48.0 ms: 1.05x faster                                                  |
| django_template | 34.7 ms                                                | 33.6 ms: 1.03x faster                                                  |
| mako            | 11.0 ms                                                | 11.8 ms: 1.07x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.02x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 623 ms: 1.78x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 317 ms: 1.77x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 621 ms: 1.74x faster                                                   |
| async_tree_none            | 464 ms                                                 | 268 ms: 1.73x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 259 ms: 1.73x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 323 ms: 1.72x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 484 ms: 1.49x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 500 ms: 1.43x faster                                                   |
| deepcopy                   | 352 us                                                 | 249 us: 1.41x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 30.2 us: 1.34x faster                                                  |
| go                         | 139 ms                                                 | 114 ms: 1.22x faster                                                   |
| spectral_norm              | 110 ms                                                 | 91.1 ms: 1.21x faster                                                  |
| comprehensions             | 19.8 us                                                | 16.5 us: 1.20x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.57 us: 1.20x faster                                                  |
| async_generators           | 384 ms                                                 | 321 ms: 1.20x faster                                                   |
| pathlib                    | 21.5 ms                                                | 18.1 ms: 1.19x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.71 ms: 1.17x faster                                                  |
| pylint                     | 319 ms                                                 | 276 ms: 1.16x faster                                                   |
| raytrace                   | 299 ms                                                 | 260 ms: 1.15x faster                                                   |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.0 ms: 1.15x faster                                                  |
| crypto_pyaes               | 76.6 ms                                                | 67.2 ms: 1.14x faster                                                  |
| scimark_sor                | 130 ms                                                 | 115 ms: 1.13x faster                                                   |
| regex_compile              | 142 ms                                                 | 126 ms: 1.13x faster                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 4.19 sec: 1.13x faster                                                 |
| float                      | 80.8 ms                                                | 71.5 ms: 1.13x faster                                                  |
| sqlalchemy_declarative     | 143 ms                                                 | 127 ms: 1.13x faster                                                   |
| logging_simple             | 6.63 us                                                | 5.90 us: 1.12x faster                                                  |
| generators                 | 32.2 ms                                                | 28.8 ms: 1.12x faster                                                  |
| coroutines                 | 23.9 ms                                                | 21.6 ms: 1.11x faster                                                  |
| chaos                      | 62.8 ms                                                | 56.6 ms: 1.11x faster                                                  |
| deltablue                  | 3.45 ms                                                | 3.12 ms: 1.10x faster                                                  |
| sqlglot_parse              | 1.36 ms                                                | 1.23 ms: 1.10x faster                                                  |
| tomli_loads                | 2.11 sec                                               | 1.92 sec: 1.10x faster                                                 |
| richards                   | 45.9 ms                                                | 41.9 ms: 1.10x faster                                                  |
| thrift                     | 791 us                                                 | 723 us: 1.09x faster                                                   |
| pyflate                    | 448 ms                                                 | 409 ms: 1.09x faster                                                   |
| sqlglot_transpile          | 1.67 ms                                                | 1.53 ms: 1.09x faster                                                  |
| sympy_sum                  | 166 ms                                                 | 152 ms: 1.09x faster                                                   |
| typing_runtime_protocols   | 163 us                                                 | 150 us: 1.09x faster                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 63.1 ms: 1.08x faster                                                  |
| pprint_safe_repr           | 743 ms                                                 | 686 ms: 1.08x faster                                                   |
| genshi_text                | 22.8 ms                                                | 21.1 ms: 1.08x faster                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.40 sec: 1.08x faster                                                 |
| richards_super             | 51.9 ms                                                | 48.0 ms: 1.08x faster                                                  |
| sympy_str                  | 292 ms                                                 | 270 ms: 1.08x faster                                                   |
| logging_format             | 7.35 us                                                | 6.80 us: 1.08x faster                                                  |
| scimark_fft                | 342 ms                                                 | 317 ms: 1.08x faster                                                   |
| logging_silent             | 109 ns                                                 | 102 ns: 1.07x faster                                                   |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 91.1 ms: 1.06x faster                                                  |
| meteor_contest             | 104 ms                                                 | 97.8 ms: 1.06x faster                                                  |
| hexiom                     | 6.17 ms                                                | 5.83 ms: 1.06x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 74.9 ms: 1.05x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.11 sec: 1.05x faster                                                 |
| sympy_integrate            | 20.5 ms                                                | 19.5 ms: 1.05x faster                                                  |
| genshi_xml                 | 50.2 ms                                                | 48.0 ms: 1.05x faster                                                  |
| 2to3                       | 264 ms                                                 | 252 ms: 1.05x faster                                                   |
| mdp                        | 2.42 sec                                               | 2.32 sec: 1.04x faster                                                 |
| sqlglot_optimize           | 53.3 ms                                                | 51.0 ms: 1.04x faster                                                  |
| docutils                   | 2.64 sec                                               | 2.54 sec: 1.04x faster                                                 |
| unpickle_pure_python       | 221 us                                                 | 212 us: 1.04x faster                                                   |
| django_template            | 34.7 ms                                                | 33.6 ms: 1.03x faster                                                  |
| sympy_expand               | 468 ms                                                 | 453 ms: 1.03x faster                                                   |
| xml_etree_generate         | 85.2 ms                                                | 82.7 ms: 1.03x faster                                                  |
| nqueens                    | 80.1 ms                                                | 78.2 ms: 1.02x faster                                                  |
| xml_etree_process          | 59.0 ms                                                | 57.6 ms: 1.02x faster                                                  |
| regex_dna                  | 168 ms                                                 | 165 ms: 1.02x faster                                                   |
| scimark_lu                 | 114 ms                                                 | 113 ms: 1.01x faster                                                   |
| fannkuch                   | 372 ms                                                 | 369 ms: 1.01x faster                                                   |
| pickle_pure_python         | 308 us                                                 | 309 us: 1.01x slower                                                   |
| pidigits                   | 184 ms                                                 | 187 ms: 1.01x slower                                                   |
| json                       | 5.02 ms                                                | 5.09 ms: 1.01x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.47 ms: 1.02x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 7.47 ms: 1.04x slower                                                  |
| mako                       | 11.0 ms                                                | 11.8 ms: 1.07x slower                                                  |
| nbody                      | 89.3 ms                                                | 95.9 ms: 1.07x slower                                                  |
| json_loads                 | 26.5 us                                                | 28.7 us: 1.08x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 11.2 ms: 1.09x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.03 ms: 1.09x slower                                                  |
| coverage                   | 71.4 ms                                                | 78.8 ms: 1.10x slower                                                  |
| telco                      | 6.53 ms                                                | 7.33 ms: 1.12x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 23.8 ms: 1.16x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 4.22 ms: 1.22x slower                                                  |
| python_startup             | 9.93 ms                                                | 14.7 ms: 1.48x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.86 ms: 1.71x slower                                                  |
| sqlglot_normalize          | 107 ms                                                 | 281 ms: 2.64x slower                                                   |
| bench_mp_pool              | 10.8 ms                                                | 88.0 ms: 8.15x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                           |

Benchmark hidden because not significant (2): sqlite_synth, asyncio_websockets
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250205-3.14.0a4+-cdcacec/bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.085x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.11x