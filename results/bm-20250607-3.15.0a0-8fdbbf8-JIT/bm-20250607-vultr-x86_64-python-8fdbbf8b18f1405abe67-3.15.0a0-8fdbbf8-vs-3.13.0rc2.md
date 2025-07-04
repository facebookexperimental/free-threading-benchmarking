# Results vs. 3.13.0rc2

- fork: python
- ref: 8fdbbf8b18f1405abe67
- machine: linux-x86_64
- commit hash: 8fdbbf8
- commit date: 2025-06-07
- overall geometric mean: 1.079x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 255 ms: 1.02x faster                                                  |
| docutils       | 2.63 sec                                                               | 2.58 sec: 1.02x faster                                                |
| html5lib       | 68.6 ms                                                                | 61.3 ms: 1.12x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization     | 459 ms                                                                 | 311 ms: 1.48x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 614 ms: 1.44x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 629 ms: 1.43x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 502 ms: 1.33x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 312 ms: 1.31x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 254 ms: 1.31x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 269 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 506 ms: 1.25x faster                                                  |
| async_generators           | 375 ms                                                                 | 349 ms: 1.07x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 23.0 ms: 1.01x faster                                                 |
| Geometric mean             | (ref)                                                                  | 1.21x faster                                                          |

Benchmark hidden because not significant (3): asyncio_tcp, asyncio_tcp_ssl, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 76.7 ms                                                                | 64.2 ms: 1.19x faster                                                 |
| pidigits       | 216 ms                                                                 | 208 ms: 1.04x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.08x faster                                                          |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.60 ms: 1.23x faster                                                 |
| regex_dna      | 189 ms                                                                 | 168 ms: 1.12x faster                                                  |
| regex_v8       | 23.2 ms                                                                | 21.5 ms: 1.08x faster                                                 |
| regex_compile  | 131 ms                                                                 | 123 ms: 1.07x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.12x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                               | 1.81 sec: 1.11x faster                                                |
| pickle_dict          | 32.7 us                                                                | 29.9 us: 1.09x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                                | 78.4 ms: 1.09x faster                                                 |
| unpickle_pure_python | 208 us                                                                 | 191 us: 1.09x faster                                                  |
| xml_etree_process    | 59.2 ms                                                                | 54.5 ms: 1.09x faster                                                 |
| unpickle             | 14.6 us                                                                | 14.0 us: 1.04x faster                                                 |
| xml_etree_parse      | 136 ms                                                                 | 132 ms: 1.03x faster                                                  |
| xml_etree_iterparse  | 94.4 ms                                                                | 92.6 ms: 1.02x faster                                                 |
| json_dumps           | 10.6 ms                                                                | 10.8 ms: 1.02x slower                                                 |
| pickle_list          | 4.81 us                                                                | 4.91 us: 1.02x slower                                                 |
| json_loads           | 27.3 us                                                                | 28.1 us: 1.03x slower                                                 |
| unpickle_list        | 4.60 us                                                                | 4.76 us: 1.03x slower                                                 |
| pickle               | 11.4 us                                                                | 12.0 us: 1.06x slower                                                 |
| pickle_pure_python   | 292 us                                                                 | 308 us: 1.06x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.02x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 7.34 ms: 1.01x faster                                                 |
| python_startup         | 11.0 ms                                                                | 12.6 ms: 1.14x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.06x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 21.7 ms                                                                | 20.4 ms: 1.07x faster                                                 |
| genshi_xml      | 49.1 ms                                                                | 48.2 ms: 1.02x faster                                                 |
| mako            | 11.2 ms                                                                | 11.1 ms: 1.01x faster                                                 |
| django_template | 34.2 ms                                                                | 34.5 ms: 1.01x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.02x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.34 sec                                                               | 1.16 sec: 2.02x faster                                                |
| async_tree_memoization     | 459 ms                                                                 | 311 ms: 1.48x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 614 ms: 1.44x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 629 ms: 1.43x faster                                                  |
| deepcopy                   | 357 us                                                                 | 253 us: 1.41x faster                                                  |
| richards                   | 44.4 ms                                                                | 31.8 ms: 1.40x faster                                                 |
| richards_super             | 50.4 ms                                                                | 36.4 ms: 1.39x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 502 ms: 1.33x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 28.9 us: 1.32x faster                                                 |
| async_tree_memoization_tg  | 410 ms                                                                 | 312 ms: 1.31x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 254 ms: 1.31x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 269 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 506 ms: 1.25x faster                                                  |
| scimark_sor                | 134 ms                                                                 | 108 ms: 1.24x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.60 ms: 1.23x faster                                                 |
| go                         | 141 ms                                                                 | 118 ms: 1.19x faster                                                  |
| float                      | 76.7 ms                                                                | 64.2 ms: 1.19x faster                                                 |
| scimark_fft                | 348 ms                                                                 | 292 ms: 1.19x faster                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 2.64 us: 1.18x faster                                                 |
| spectral_norm              | 108 ms                                                                 | 92.1 ms: 1.17x faster                                                 |
| pyflate                    | 449 ms                                                                 | 395 ms: 1.14x faster                                                  |
| pylint                     | 317 ms                                                                 | 282 ms: 1.12x faster                                                  |
| regex_dna                  | 189 ms                                                                 | 168 ms: 1.12x faster                                                  |
| html5lib                   | 68.6 ms                                                                | 61.3 ms: 1.12x faster                                                 |
| tomli_loads                | 2.01 sec                                                               | 1.81 sec: 1.11x faster                                                |
| telco                      | 7.77 ms                                                                | 6.98 ms: 1.11x faster                                                 |
| bpe_tokeniser              | 4.46 sec                                                               | 4.03 sec: 1.11x faster                                                |
| dulwich_log                | 74.5 ms                                                                | 67.7 ms: 1.10x faster                                                 |
| scimark_monte_carlo        | 65.8 ms                                                                | 60.1 ms: 1.09x faster                                                 |
| pickle_dict                | 32.7 us                                                                | 29.9 us: 1.09x faster                                                 |
| xml_etree_generate         | 85.4 ms                                                                | 78.4 ms: 1.09x faster                                                 |
| unpickle_pure_python       | 208 us                                                                 | 191 us: 1.09x faster                                                  |
| xml_etree_process          | 59.2 ms                                                                | 54.5 ms: 1.09x faster                                                 |
| regex_v8                   | 23.2 ms                                                                | 21.5 ms: 1.08x faster                                                 |
| deltablue                  | 3.10 ms                                                                | 2.87 ms: 1.08x faster                                                 |
| async_generators           | 375 ms                                                                 | 349 ms: 1.07x faster                                                  |
| genshi_text                | 21.7 ms                                                                | 20.4 ms: 1.07x faster                                                 |
| regex_compile              | 131 ms                                                                 | 123 ms: 1.07x faster                                                  |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.48 ms: 1.06x faster                                                 |
| thrift                     | 772 us                                                                 | 738 us: 1.05x faster                                                  |
| pidigits                   | 216 ms                                                                 | 208 ms: 1.04x faster                                                  |
| unpickle                   | 14.6 us                                                                | 14.0 us: 1.04x faster                                                 |
| scimark_lu                 | 112 ms                                                                 | 109 ms: 1.03x faster                                                  |
| sympy_integrate            | 19.7 ms                                                                | 19.1 ms: 1.03x faster                                                 |
| xml_etree_parse            | 136 ms                                                                 | 132 ms: 1.03x faster                                                  |
| fannkuch                   | 376 ms                                                                 | 367 ms: 1.02x faster                                                  |
| docutils                   | 2.63 sec                                                               | 2.58 sec: 1.02x faster                                                |
| xml_etree_iterparse        | 94.4 ms                                                                | 92.6 ms: 1.02x faster                                                 |
| 2to3                       | 259 ms                                                                 | 255 ms: 1.02x faster                                                  |
| genshi_xml                 | 49.1 ms                                                                | 48.2 ms: 1.02x faster                                                 |
| sqlite_synth               | 2.25 us                                                                | 2.21 us: 1.02x faster                                                 |
| mako                       | 11.2 ms                                                                | 11.1 ms: 1.01x faster                                                 |
| coroutines                 | 23.3 ms                                                                | 23.0 ms: 1.01x faster                                                 |
| coverage                   | 82.5 ms                                                                | 81.6 ms: 1.01x faster                                                 |
| python_startup_no_site     | 7.41 ms                                                                | 7.34 ms: 1.01x faster                                                 |
| generators                 | 28.5 ms                                                                | 28.3 ms: 1.01x faster                                                 |
| meteor_contest             | 101 ms                                                                 | 101 ms: 1.01x faster                                                  |
| sympy_sum                  | 154 ms                                                                 | 154 ms: 1.00x faster                                                  |
| comprehensions             | 16.6 us                                                                | 16.7 us: 1.01x slower                                                 |
| crypto_pyaes               | 68.2 ms                                                                | 68.6 ms: 1.01x slower                                                 |
| raytrace                   | 250 ms                                                                 | 251 ms: 1.01x slower                                                  |
| django_template            | 34.2 ms                                                                | 34.5 ms: 1.01x slower                                                 |
| pathlib                    | 19.3 ms                                                                | 19.5 ms: 1.01x slower                                                 |
| typing_runtime_protocols   | 156 us                                                                 | 158 us: 1.01x slower                                                  |
| pycparser                  | 1.12 sec                                                               | 1.14 sec: 1.01x slower                                                |
| json_dumps                 | 10.6 ms                                                                | 10.8 ms: 1.02x slower                                                 |
| hexiom                     | 5.95 ms                                                                | 6.07 ms: 1.02x slower                                                 |
| pickle_list                | 4.81 us                                                                | 4.91 us: 1.02x slower                                                 |
| json                       | 4.98 ms                                                                | 5.11 ms: 1.03x slower                                                 |
| json_loads                 | 27.3 us                                                                | 28.1 us: 1.03x slower                                                 |
| sympy_expand               | 454 ms                                                                 | 469 ms: 1.03x slower                                                  |
| unpickle_list              | 4.60 us                                                                | 4.76 us: 1.03x slower                                                 |
| logging_simple             | 6.14 us                                                                | 6.42 us: 1.04x slower                                                 |
| logging_format             | 6.92 us                                                                | 7.23 us: 1.05x slower                                                 |
| pickle                     | 11.4 us                                                                | 12.0 us: 1.06x slower                                                 |
| pickle_pure_python         | 292 us                                                                 | 308 us: 1.06x slower                                                  |
| bench_thread_pool          | 924 us                                                                 | 1.04 ms: 1.13x slower                                                 |
| python_startup             | 11.0 ms                                                                | 12.6 ms: 1.14x slower                                                 |
| pprint_safe_repr           | 719 ms                                                                 | 853 ms: 1.19x slower                                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.76 sec: 1.21x slower                                                |
| gc_traversal               | 3.32 ms                                                                | 4.50 ms: 1.36x slower                                                 |
| create_gc_cycles           | 1.33 ms                                                                | 1.92 ms: 1.44x slower                                                 |
| unpack_sequence            | 39.3 ns                                                                | 60.6 ns: 1.54x slower                                                 |
| logging_silent             | 98.2 ns                                                                | 468 ns: 4.76x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                                | 98.4 ms: 8.95x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (7): asyncio_tcp, nbody, sympy_str, nqueens, asyncio_tcp_ssl, asyncio_websockets, chaos
Ignored benchmarks (10) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20250607-3.15.0a0-8fdbbf8-JIT/bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.079x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.16x