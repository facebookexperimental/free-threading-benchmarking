# Results vs. 3.12.6

- fork: python
- ref: 1feaecc2bc42cb96f2d7
- machine: linux-x86_64
- commit hash: 1feaecc
- commit date: 2025-02-10
- overall geometric mean: 1.099x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 252 ms: 1.05x faster                                                   |
| docutils       | 2.64 sec                                               | 2.55 sec: 1.03x faster                                                 |
| Geometric mean | (ref)                                                  | 1.04x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 630 ms: 1.76x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 318 ms: 1.76x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 623 ms: 1.74x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 321 ms: 1.73x faster                                                   |
| async_tree_none            | 464 ms                                                 | 269 ms: 1.73x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 260 ms: 1.72x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 489 ms: 1.48x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 500 ms: 1.43x faster                                                   |
| async_generators           | 384 ms                                                 | 325 ms: 1.18x faster                                                   |
| coroutines                 | 23.9 ms                                                | 21.4 ms: 1.12x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.48x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 70.0 ms: 1.15x faster                                                  |
| pidigits       | 184 ms                                                 | 187 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                  | 1.04x faster                                                           |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.73 ms: 1.16x faster                                                  |
| regex_compile  | 142 ms                                                 | 126 ms: 1.13x faster                                                   |
| regex_dna      | 168 ms                                                 | 164 ms: 1.02x faster                                                   |
| regex_v8       | 20.6 ms                                                | 23.3 ms: 1.13x slower                                                  |
| Geometric mean | (ref)                                                  | 1.04x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.90 sec: 1.11x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.08x faster                                                   |
| xml_etree_iterparse  | 96.7 ms                                                | 91.1 ms: 1.06x faster                                                  |
| unpickle_pure_python | 221 us                                                 | 212 us: 1.04x faster                                                   |
| xml_etree_generate   | 85.2 ms                                                | 82.6 ms: 1.03x faster                                                  |
| xml_etree_process    | 59.0 ms                                                | 57.6 ms: 1.02x faster                                                  |
| pickle_pure_python   | 308 us                                                 | 311 us: 1.01x slower                                                   |
| json_loads           | 26.5 us                                                | 28.6 us: 1.08x slower                                                  |
| json_dumps           | 10.4 ms                                                | 11.5 ms: 1.11x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.47 ms: 1.04x slower                                                  |
| python_startup         | 9.93 ms                                                | 14.7 ms: 1.48x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.24x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.9 ms: 1.09x faster                                                  |
| genshi_xml      | 50.2 ms                                                | 47.0 ms: 1.07x faster                                                  |
| django_template | 34.7 ms                                                | 34.2 ms: 1.01x faster                                                  |
| mako            | 11.0 ms                                                | 11.8 ms: 1.07x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.02x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 630 ms: 1.76x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 318 ms: 1.76x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 623 ms: 1.74x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 321 ms: 1.73x faster                                                   |
| async_tree_none            | 464 ms                                                 | 269 ms: 1.73x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 260 ms: 1.72x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 489 ms: 1.48x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 500 ms: 1.43x faster                                                   |
| deepcopy                   | 352 us                                                 | 252 us: 1.40x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 29.8 us: 1.35x faster                                                  |
| go                         | 139 ms                                                 | 114 ms: 1.22x faster                                                   |
| comprehensions             | 19.8 us                                                | 16.3 us: 1.22x faster                                                  |
| spectral_norm              | 110 ms                                                 | 91.1 ms: 1.21x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.60 us: 1.19x faster                                                  |
| async_generators           | 384 ms                                                 | 325 ms: 1.18x faster                                                   |
| crypto_pyaes               | 76.6 ms                                                | 65.6 ms: 1.17x faster                                                  |
| raytrace                   | 299 ms                                                 | 256 ms: 1.17x faster                                                   |
| scimark_sor                | 130 ms                                                 | 112 ms: 1.16x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.73 ms: 1.16x faster                                                  |
| float                      | 80.8 ms                                                | 70.0 ms: 1.15x faster                                                  |
| pathlib                    | 21.5 ms                                                | 18.7 ms: 1.15x faster                                                  |
| pylint                     | 319 ms                                                 | 277 ms: 1.15x faster                                                   |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.0 ms: 1.15x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.14 sec: 1.14x faster                                                 |
| regex_compile              | 142 ms                                                 | 126 ms: 1.13x faster                                                   |
| chaos                      | 62.8 ms                                                | 55.6 ms: 1.13x faster                                                  |
| sqlalchemy_declarative     | 143 ms                                                 | 127 ms: 1.12x faster                                                   |
| logging_simple             | 6.63 us                                                | 5.92 us: 1.12x faster                                                  |
| coroutines                 | 23.9 ms                                                | 21.4 ms: 1.12x faster                                                  |
| generators                 | 32.2 ms                                                | 28.9 ms: 1.12x faster                                                  |
| deltablue                  | 3.45 ms                                                | 3.10 ms: 1.11x faster                                                  |
| logging_format             | 7.35 us                                                | 6.63 us: 1.11x faster                                                  |
| tomli_loads                | 2.11 sec                                               | 1.90 sec: 1.11x faster                                                 |
| richards                   | 45.9 ms                                                | 41.5 ms: 1.11x faster                                                  |
| sympy_sum                  | 166 ms                                                 | 151 ms: 1.10x faster                                                   |
| sqlglot_parse              | 1.36 ms                                                | 1.23 ms: 1.10x faster                                                  |
| sympy_str                  | 292 ms                                                 | 267 ms: 1.09x faster                                                   |
| richards_super             | 51.9 ms                                                | 47.5 ms: 1.09x faster                                                  |
| pyflate                    | 448 ms                                                 | 410 ms: 1.09x faster                                                   |
| sqlglot_transpile          | 1.67 ms                                                | 1.53 ms: 1.09x faster                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 62.8 ms: 1.09x faster                                                  |
| genshi_text                | 22.8 ms                                                | 20.9 ms: 1.09x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.08x faster                                                   |
| typing_runtime_protocols   | 163 us                                                 | 152 us: 1.08x faster                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.41 sec: 1.07x faster                                                 |
| scimark_fft                | 342 ms                                                 | 319 ms: 1.07x faster                                                   |
| pprint_safe_repr           | 743 ms                                                 | 693 ms: 1.07x faster                                                   |
| meteor_contest             | 104 ms                                                 | 96.7 ms: 1.07x faster                                                  |
| genshi_xml                 | 50.2 ms                                                | 47.0 ms: 1.07x faster                                                  |
| thrift                     | 791 us                                                 | 741 us: 1.07x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 91.1 ms: 1.06x faster                                                  |
| hexiom                     | 6.17 ms                                                | 5.87 ms: 1.05x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.11 sec: 1.05x faster                                                 |
| sqlglot_normalize          | 107 ms                                                 | 101 ms: 1.05x faster                                                   |
| sympy_integrate            | 20.5 ms                                                | 19.6 ms: 1.05x faster                                                  |
| 2to3                       | 264 ms                                                 | 252 ms: 1.05x faster                                                   |
| dulwich_log                | 78.9 ms                                                | 75.4 ms: 1.05x faster                                                  |
| logging_silent             | 109 ns                                                 | 104 ns: 1.05x faster                                                   |
| sqlglot_optimize           | 53.3 ms                                                | 51.0 ms: 1.04x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 212 us: 1.04x faster                                                   |
| sympy_expand               | 468 ms                                                 | 450 ms: 1.04x faster                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.24 ms: 1.04x faster                                                  |
| docutils                   | 2.64 sec                                               | 2.55 sec: 1.03x faster                                                 |
| xml_etree_generate         | 85.2 ms                                                | 82.6 ms: 1.03x faster                                                  |
| xml_etree_process          | 59.0 ms                                                | 57.6 ms: 1.02x faster                                                  |
| regex_dna                  | 168 ms                                                 | 164 ms: 1.02x faster                                                   |
| nqueens                    | 80.1 ms                                                | 78.2 ms: 1.02x faster                                                  |
| django_template            | 34.7 ms                                                | 34.2 ms: 1.01x faster                                                  |
| fannkuch                   | 372 ms                                                 | 368 ms: 1.01x faster                                                   |
| scimark_lu                 | 114 ms                                                 | 113 ms: 1.01x faster                                                   |
| pickle_pure_python         | 308 us                                                 | 311 us: 1.01x slower                                                   |
| mdp                        | 2.42 sec                                               | 2.45 sec: 1.01x slower                                                 |
| pidigits                   | 184 ms                                                 | 187 ms: 1.01x slower                                                   |
| json                       | 5.02 ms                                                | 5.13 ms: 1.02x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 7.47 ms: 1.04x slower                                                  |
| mako                       | 11.0 ms                                                | 11.8 ms: 1.07x slower                                                  |
| json_loads                 | 26.5 us                                                | 28.6 us: 1.08x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.03 ms: 1.09x slower                                                  |
| coverage                   | 71.4 ms                                                | 78.8 ms: 1.10x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 11.5 ms: 1.11x slower                                                  |
| telco                      | 6.53 ms                                                | 7.36 ms: 1.13x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 23.3 ms: 1.13x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 4.25 ms: 1.23x slower                                                  |
| python_startup             | 9.93 ms                                                | 14.7 ms: 1.48x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.86 ms: 1.70x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 88.5 ms: 8.20x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                           |

Benchmark hidden because not significant (3): sqlite_synth, asyncio_websockets, nbody
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250210-3.14.0a4+-1feaecc/bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.099x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.12x