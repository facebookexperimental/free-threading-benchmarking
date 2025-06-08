# Results vs. 3.13.0rc2

- fork: python
- ref: 8fdbbf8b18f1405abe67
- machine: linux-x86_64
- commit hash: 8fdbbf8
- commit date: 2025-06-07
- overall geometric mean: 1.119x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 242 ms: 1.07x faster                                                  |
| docutils       | 2.63 sec                                                               | 2.50 sec: 1.05x faster                                                |
| html5lib       | 68.6 ms                                                                | 59.9 ms: 1.15x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.09x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization     | 459 ms                                                                 | 300 ms: 1.53x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 577 ms: 1.53x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 598 ms: 1.51x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 484 ms: 1.38x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 244 ms: 1.36x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 260 ms: 1.36x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 302 ms: 1.36x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 479 ms: 1.32x faster                                                  |
| async_generators           | 375 ms                                                                 | 315 ms: 1.19x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 21.6 ms: 1.08x faster                                                 |
| asyncio_tcp                | 502 ms                                                                 | 496 ms: 1.01x faster                                                  |
| asyncio_tcp_ssl            | 1.51 sec                                                               | 1.51 sec: 1.01x faster                                                |
| Geometric mean             | (ref)                                                                  | 1.26x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 76.7 ms                                                                | 66.1 ms: 1.16x faster                                                 |
| pidigits       | 216 ms                                                                 | 192 ms: 1.13x faster                                                  |
| nbody          | 85.3 ms                                                                | 80.7 ms: 1.06x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.11x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 131 ms                                                                 | 117 ms: 1.12x faster                                                  |
| regex_effbot   | 3.21 ms                                                                | 3.12 ms: 1.03x faster                                                 |
| regex_v8       | 23.2 ms                                                                | 22.6 ms: 1.03x faster                                                 |
| regex_dna      | 189 ms                                                                 | 195 ms: 1.03x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                               | 1.79 sec: 1.13x faster                                                |
| unpickle             | 14.6 us                                                                | 13.3 us: 1.09x faster                                                 |
| json_loads           | 27.3 us                                                                | 25.1 us: 1.09x faster                                                 |
| unpickle_pure_python | 208 us                                                                 | 195 us: 1.07x faster                                                  |
| xml_etree_generate   | 85.4 ms                                                                | 80.8 ms: 1.06x faster                                                 |
| unpickle_list        | 4.60 us                                                                | 4.39 us: 1.05x faster                                                 |
| xml_etree_process    | 59.2 ms                                                                | 56.6 ms: 1.05x faster                                                 |
| pickle_dict          | 32.7 us                                                                | 31.6 us: 1.03x faster                                                 |
| xml_etree_iterparse  | 94.4 ms                                                                | 94.8 ms: 1.00x slower                                                 |
| json_dumps           | 10.6 ms                                                                | 10.8 ms: 1.01x slower                                                 |
| pickle_pure_python   | 292 us                                                                 | 296 us: 1.02x slower                                                  |
| pickle_list          | 4.81 us                                                                | 4.96 us: 1.03x slower                                                 |
| xml_etree_parse      | 136 ms                                                                 | 146 ms: 1.07x slower                                                  |
| pickle               | 11.4 us                                                                | 12.6 us: 1.10x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.02x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 7.39 ms: 1.00x faster                                                 |
| python_startup         | 11.0 ms                                                                | 12.6 ms: 1.14x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.07x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 21.7 ms                                                                | 19.8 ms: 1.10x faster                                                 |
| genshi_xml      | 49.1 ms                                                                | 46.1 ms: 1.06x faster                                                 |
| django_template | 34.2 ms                                                                | 32.7 ms: 1.05x faster                                                 |
| mako            | 11.2 ms                                                                | 11.5 ms: 1.02x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.05x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.34 sec                                                               | 1.08 sec: 2.17x faster                                                |
| deepcopy                   | 357 us                                                                 | 228 us: 1.57x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 300 ms: 1.53x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 577 ms: 1.53x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 598 ms: 1.51x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 25.9 us: 1.47x faster                                                 |
| go                         | 141 ms                                                                 | 95.9 ms: 1.47x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 484 ms: 1.38x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 244 ms: 1.36x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 260 ms: 1.36x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 302 ms: 1.36x faster                                                  |
| scimark_sor                | 134 ms                                                                 | 99.9 ms: 1.34x faster                                                 |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 479 ms: 1.32x faster                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 2.39 us: 1.31x faster                                                 |
| scimark_fft                | 348 ms                                                                 | 268 ms: 1.30x faster                                                  |
| spectral_norm              | 108 ms                                                                 | 83.1 ms: 1.30x faster                                                 |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 3.89 ms: 1.22x faster                                                 |
| richards                   | 44.4 ms                                                                | 36.5 ms: 1.21x faster                                                 |
| scimark_monte_carlo        | 65.8 ms                                                                | 54.4 ms: 1.21x faster                                                 |
| richards_super             | 50.4 ms                                                                | 42.0 ms: 1.20x faster                                                 |
| async_generators           | 375 ms                                                                 | 315 ms: 1.19x faster                                                  |
| comprehensions             | 16.6 us                                                                | 14.0 us: 1.18x faster                                                 |
| pylint                     | 317 ms                                                                 | 273 ms: 1.16x faster                                                  |
| float                      | 76.7 ms                                                                | 66.1 ms: 1.16x faster                                                 |
| pyflate                    | 449 ms                                                                 | 388 ms: 1.16x faster                                                  |
| hexiom                     | 5.95 ms                                                                | 5.15 ms: 1.16x faster                                                 |
| scimark_lu                 | 112 ms                                                                 | 97.8 ms: 1.15x faster                                                 |
| chaos                      | 56.3 ms                                                                | 49.0 ms: 1.15x faster                                                 |
| html5lib                   | 68.6 ms                                                                | 59.9 ms: 1.15x faster                                                 |
| dulwich_log                | 74.5 ms                                                                | 65.5 ms: 1.14x faster                                                 |
| pidigits                   | 216 ms                                                                 | 192 ms: 1.13x faster                                                  |
| tomli_loads                | 2.01 sec                                                               | 1.79 sec: 1.13x faster                                                |
| telco                      | 7.77 ms                                                                | 6.92 ms: 1.12x faster                                                 |
| bpe_tokeniser              | 4.46 sec                                                               | 3.97 sec: 1.12x faster                                                |
| regex_compile              | 131 ms                                                                 | 117 ms: 1.12x faster                                                  |
| typing_runtime_protocols   | 156 us                                                                 | 140 us: 1.11x faster                                                  |
| genshi_text                | 21.7 ms                                                                | 19.8 ms: 1.10x faster                                                 |
| sympy_integrate            | 19.7 ms                                                                | 18.0 ms: 1.10x faster                                                 |
| unpickle                   | 14.6 us                                                                | 13.3 us: 1.09x faster                                                 |
| json_loads                 | 27.3 us                                                                | 25.1 us: 1.09x faster                                                 |
| deltablue                  | 3.10 ms                                                                | 2.85 ms: 1.09x faster                                                 |
| coverage                   | 82.5 ms                                                                | 76.0 ms: 1.09x faster                                                 |
| raytrace                   | 250 ms                                                                 | 231 ms: 1.08x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 21.6 ms: 1.08x faster                                                 |
| thrift                     | 772 us                                                                 | 716 us: 1.08x faster                                                  |
| 2to3                       | 259 ms                                                                 | 242 ms: 1.07x faster                                                  |
| sympy_str                  | 274 ms                                                                 | 257 ms: 1.07x faster                                                  |
| unpickle_pure_python       | 208 us                                                                 | 195 us: 1.07x faster                                                  |
| genshi_xml                 | 49.1 ms                                                                | 46.1 ms: 1.06x faster                                                 |
| generators                 | 28.5 ms                                                                | 26.9 ms: 1.06x faster                                                 |
| sympy_expand               | 454 ms                                                                 | 428 ms: 1.06x faster                                                  |
| nbody                      | 85.3 ms                                                                | 80.7 ms: 1.06x faster                                                 |
| xml_etree_generate         | 85.4 ms                                                                | 80.8 ms: 1.06x faster                                                 |
| docutils                   | 2.63 sec                                                               | 2.50 sec: 1.05x faster                                                |
| unpickle_list              | 4.60 us                                                                | 4.39 us: 1.05x faster                                                 |
| xml_etree_process          | 59.2 ms                                                                | 56.6 ms: 1.05x faster                                                 |
| nqueens                    | 77.7 ms                                                                | 74.3 ms: 1.05x faster                                                 |
| django_template            | 34.2 ms                                                                | 32.7 ms: 1.05x faster                                                 |
| pycparser                  | 1.12 sec                                                               | 1.07 sec: 1.04x faster                                                |
| sympy_sum                  | 154 ms                                                                 | 148 ms: 1.04x faster                                                  |
| pickle_dict                | 32.7 us                                                                | 31.6 us: 1.03x faster                                                 |
| regex_effbot               | 3.21 ms                                                                | 3.12 ms: 1.03x faster                                                 |
| crypto_pyaes               | 68.2 ms                                                                | 66.3 ms: 1.03x faster                                                 |
| pathlib                    | 19.3 ms                                                                | 18.7 ms: 1.03x faster                                                 |
| regex_v8                   | 23.2 ms                                                                | 22.6 ms: 1.03x faster                                                 |
| fannkuch                   | 376 ms                                                                 | 366 ms: 1.03x faster                                                  |
| sqlite_synth               | 2.25 us                                                                | 2.21 us: 1.02x faster                                                 |
| json                       | 4.98 ms                                                                | 4.91 ms: 1.01x faster                                                 |
| asyncio_tcp                | 502 ms                                                                 | 496 ms: 1.01x faster                                                  |
| asyncio_tcp_ssl            | 1.51 sec                                                               | 1.51 sec: 1.01x faster                                                |
| python_startup_no_site     | 7.41 ms                                                                | 7.39 ms: 1.00x faster                                                 |
| xml_etree_iterparse        | 94.4 ms                                                                | 94.8 ms: 1.00x slower                                                 |
| meteor_contest             | 101 ms                                                                 | 102 ms: 1.01x slower                                                  |
| json_dumps                 | 10.6 ms                                                                | 10.8 ms: 1.01x slower                                                 |
| pickle_pure_python         | 292 us                                                                 | 296 us: 1.02x slower                                                  |
| mako                       | 11.2 ms                                                                | 11.5 ms: 1.02x slower                                                 |
| logging_format             | 6.92 us                                                                | 7.12 us: 1.03x slower                                                 |
| pickle_list                | 4.81 us                                                                | 4.96 us: 1.03x slower                                                 |
| regex_dna                  | 189 ms                                                                 | 195 ms: 1.03x slower                                                  |
| pprint_safe_repr           | 719 ms                                                                 | 749 ms: 1.04x slower                                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.53 sec: 1.05x slower                                                |
| xml_etree_parse            | 136 ms                                                                 | 146 ms: 1.07x slower                                                  |
| bench_thread_pool          | 924 us                                                                 | 1.01 ms: 1.09x slower                                                 |
| pickle                     | 11.4 us                                                                | 12.6 us: 1.10x slower                                                 |
| python_startup             | 11.0 ms                                                                | 12.6 ms: 1.14x slower                                                 |
| unpack_sequence            | 39.3 ns                                                                | 47.3 ns: 1.20x slower                                                 |
| gc_traversal               | 3.32 ms                                                                | 4.26 ms: 1.28x slower                                                 |
| create_gc_cycles           | 1.33 ms                                                                | 2.00 ms: 1.50x slower                                                 |
| logging_silent             | 98.2 ns                                                                | 458 ns: 4.67x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                                | 97.3 ms: 8.85x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.06x faster                                                          |

Benchmark hidden because not significant (2): asyncio_websockets, logging_simple
Ignored benchmarks (10) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20250607-3.15.0a0-8fdbbf8-CLANG/bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.119x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.18x