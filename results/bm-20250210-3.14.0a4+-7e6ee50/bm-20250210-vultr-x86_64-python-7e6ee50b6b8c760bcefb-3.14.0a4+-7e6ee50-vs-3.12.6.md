# Results vs. 3.12.6

- fork: python
- ref: 7e6ee50b6b8c760bcefb
- machine: linux-x86_64
- commit hash: 7e6ee50
- commit date: 2025-02-10
- overall geometric mean: 1.097x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 253 ms: 1.04x faster                                                   |
| docutils       | 2.64 sec                                               | 2.56 sec: 1.03x faster                                                 |
| Geometric mean | (ref)                                                  | 1.04x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 626 ms: 1.77x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 319 ms: 1.76x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 619 ms: 1.75x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 321 ms: 1.73x faster                                                   |
| async_tree_none            | 464 ms                                                 | 269 ms: 1.73x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 261 ms: 1.71x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 489 ms: 1.48x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 498 ms: 1.44x faster                                                   |
| async_generators           | 384 ms                                                 | 322 ms: 1.19x faster                                                   |
| coroutines                 | 23.9 ms                                                | 22.6 ms: 1.06x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.48x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 71.6 ms: 1.13x faster                                                  |
| pidigits       | 184 ms                                                 | 186 ms: 1.01x slower                                                   |
| nbody          | 89.3 ms                                                | 95.8 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.76 ms: 1.15x faster                                                  |
| regex_compile  | 142 ms                                                 | 127 ms: 1.12x faster                                                   |
| regex_dna      | 168 ms                                                 | 164 ms: 1.02x faster                                                   |
| regex_v8       | 20.6 ms                                                | 23.3 ms: 1.13x slower                                                  |
| Geometric mean | (ref)                                                  | 1.04x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.88 sec: 1.12x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.08x faster                                                   |
| xml_etree_iterparse  | 96.7 ms                                                | 90.8 ms: 1.06x faster                                                  |
| unpickle_pure_python | 221 us                                                 | 212 us: 1.04x faster                                                   |
| xml_etree_generate   | 85.2 ms                                                | 83.4 ms: 1.02x faster                                                  |
| xml_etree_process    | 59.0 ms                                                | 58.1 ms: 1.01x faster                                                  |
| json_loads           | 26.5 us                                                | 28.4 us: 1.07x slower                                                  |
| json_dumps           | 10.4 ms                                                | 11.4 ms: 1.10x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                           |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.51 ms: 1.05x slower                                                  |
| python_startup         | 9.93 ms                                                | 14.8 ms: 1.49x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.25x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.8 ms: 1.10x faster                                                  |
| genshi_xml      | 50.2 ms                                                | 48.6 ms: 1.03x faster                                                  |
| django_template | 34.7 ms                                                | 34.5 ms: 1.00x faster                                                  |
| mako            | 11.0 ms                                                | 11.7 ms: 1.06x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.02x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 626 ms: 1.77x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 319 ms: 1.76x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 619 ms: 1.75x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 321 ms: 1.73x faster                                                   |
| async_tree_none            | 464 ms                                                 | 269 ms: 1.73x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 261 ms: 1.71x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 489 ms: 1.48x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 498 ms: 1.44x faster                                                   |
| deepcopy                   | 352 us                                                 | 253 us: 1.39x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 30.0 us: 1.34x faster                                                  |
| go                         | 139 ms                                                 | 115 ms: 1.21x faster                                                   |
| comprehensions             | 19.8 us                                                | 16.4 us: 1.21x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.55 us: 1.21x faster                                                  |
| spectral_norm              | 110 ms                                                 | 91.4 ms: 1.20x faster                                                  |
| async_generators           | 384 ms                                                 | 322 ms: 1.19x faster                                                   |
| crypto_pyaes               | 76.6 ms                                                | 65.6 ms: 1.17x faster                                                  |
| scimark_sor                | 130 ms                                                 | 113 ms: 1.15x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.76 ms: 1.15x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.13 sec: 1.15x faster                                                 |
| pylint                     | 319 ms                                                 | 278 ms: 1.15x faster                                                   |
| pathlib                    | 21.5 ms                                                | 18.8 ms: 1.14x faster                                                  |
| raytrace                   | 299 ms                                                 | 262 ms: 1.14x faster                                                   |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.2 ms: 1.14x faster                                                  |
| float                      | 80.8 ms                                                | 71.6 ms: 1.13x faster                                                  |
| sqlalchemy_declarative     | 143 ms                                                 | 127 ms: 1.12x faster                                                   |
| regex_compile              | 142 ms                                                 | 127 ms: 1.12x faster                                                   |
| tomli_loads                | 2.11 sec                                               | 1.88 sec: 1.12x faster                                                 |
| logging_simple             | 6.63 us                                                | 5.96 us: 1.11x faster                                                  |
| generators                 | 32.2 ms                                                | 29.1 ms: 1.11x faster                                                  |
| logging_format             | 7.35 us                                                | 6.65 us: 1.11x faster                                                  |
| scimark_fft                | 342 ms                                                 | 310 ms: 1.10x faster                                                   |
| deltablue                  | 3.45 ms                                                | 3.13 ms: 1.10x faster                                                  |
| chaos                      | 62.8 ms                                                | 57.1 ms: 1.10x faster                                                  |
| sympy_sum                  | 166 ms                                                 | 151 ms: 1.10x faster                                                   |
| genshi_text                | 22.8 ms                                                | 20.8 ms: 1.10x faster                                                  |
| sqlglot_parse              | 1.36 ms                                                | 1.24 ms: 1.09x faster                                                  |
| sympy_str                  | 292 ms                                                 | 267 ms: 1.09x faster                                                   |
| richards                   | 45.9 ms                                                | 42.1 ms: 1.09x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                                   |
| sqlglot_transpile          | 1.67 ms                                                | 1.54 ms: 1.08x faster                                                  |
| pprint_safe_repr           | 743 ms                                                 | 687 ms: 1.08x faster                                                   |
| richards_super             | 51.9 ms                                                | 48.0 ms: 1.08x faster                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.41 sec: 1.08x faster                                                 |
| pyflate                    | 448 ms                                                 | 415 ms: 1.08x faster                                                   |
| thrift                     | 791 us                                                 | 735 us: 1.08x faster                                                   |
| typing_runtime_protocols   | 163 us                                                 | 152 us: 1.08x faster                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 63.9 ms: 1.07x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 90.8 ms: 1.06x faster                                                  |
| logging_silent             | 109 ns                                                 | 103 ns: 1.06x faster                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.14 ms: 1.06x faster                                                  |
| hexiom                     | 6.17 ms                                                | 5.83 ms: 1.06x faster                                                  |
| coroutines                 | 23.9 ms                                                | 22.6 ms: 1.06x faster                                                  |
| sympy_integrate            | 20.5 ms                                                | 19.5 ms: 1.05x faster                                                  |
| sqlglot_normalize          | 107 ms                                                 | 101 ms: 1.05x faster                                                   |
| mdp                        | 2.42 sec                                               | 2.30 sec: 1.05x faster                                                 |
| meteor_contest             | 104 ms                                                 | 99.1 ms: 1.04x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.12 sec: 1.04x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 75.6 ms: 1.04x faster                                                  |
| sqlglot_optimize           | 53.3 ms                                                | 51.1 ms: 1.04x faster                                                  |
| 2to3                       | 264 ms                                                 | 253 ms: 1.04x faster                                                   |
| sympy_expand               | 468 ms                                                 | 450 ms: 1.04x faster                                                   |
| unpickle_pure_python       | 221 us                                                 | 212 us: 1.04x faster                                                   |
| genshi_xml                 | 50.2 ms                                                | 48.6 ms: 1.03x faster                                                  |
| docutils                   | 2.64 sec                                               | 2.56 sec: 1.03x faster                                                 |
| regex_dna                  | 168 ms                                                 | 164 ms: 1.02x faster                                                   |
| xml_etree_generate         | 85.2 ms                                                | 83.4 ms: 1.02x faster                                                  |
| scimark_lu                 | 114 ms                                                 | 112 ms: 1.02x faster                                                   |
| xml_etree_process          | 59.0 ms                                                | 58.1 ms: 1.01x faster                                                  |
| fannkuch                   | 372 ms                                                 | 368 ms: 1.01x faster                                                   |
| sqlite_synth               | 2.20 us                                                | 2.19 us: 1.01x faster                                                  |
| nqueens                    | 80.1 ms                                                | 79.6 ms: 1.01x faster                                                  |
| django_template            | 34.7 ms                                                | 34.5 ms: 1.00x faster                                                  |
| pidigits                   | 184 ms                                                 | 186 ms: 1.01x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 7.51 ms: 1.05x slower                                                  |
| mako                       | 11.0 ms                                                | 11.7 ms: 1.06x slower                                                  |
| json_loads                 | 26.5 us                                                | 28.4 us: 1.07x slower                                                  |
| nbody                      | 89.3 ms                                                | 95.8 ms: 1.07x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.03 ms: 1.09x slower                                                  |
| telco                      | 6.53 ms                                                | 7.16 ms: 1.10x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 11.4 ms: 1.10x slower                                                  |
| coverage                   | 71.4 ms                                                | 79.0 ms: 1.11x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 23.3 ms: 1.13x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 4.24 ms: 1.23x slower                                                  |
| python_startup             | 9.93 ms                                                | 14.8 ms: 1.49x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.86 ms: 1.70x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 89.2 ms: 8.26x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                           |

Benchmark hidden because not significant (3): asyncio_websockets, pickle_pure_python, json
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250210-3.14.0a4+-7e6ee50/bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.097x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.12x