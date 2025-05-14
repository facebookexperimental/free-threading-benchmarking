# Results vs. 3.13.0rc2

- fork: python
- ref: 9ad0c7b0f14c5fcda6bf
- machine: linux-x86_64
- commit hash: 9ad0c7b
- commit date: 2025-05-13
- overall geometric mean: 1.020x slower
- HPT reliability: 95.70%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.40x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 285 ms: 1.10x slower                                                  |
| docutils       | 2.63 sec                                                               | 2.70 sec: 1.03x slower                                                |
| html5lib       | 68.6 ms                                                                | 65.4 ms: 1.05x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 517 ms: 1.74x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 545 ms: 1.62x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 308 ms: 1.49x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 225 ms: 1.48x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 282 ms: 1.46x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 257 ms: 1.37x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 481 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 508 ms: 1.31x faster                                                  |
| async_generators           | 375 ms                                                                 | 367 ms: 1.02x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 23.0 ms: 1.01x faster                                                 |
| Geometric mean             | (ref)                                                                  | 1.33x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 190 ms: 1.14x faster                                                  |
| float          | 76.7 ms                                                                | 69.4 ms: 1.11x faster                                                 |
| nbody          | 85.3 ms                                                                | 117 ms: 1.37x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.82 ms: 1.14x faster                                                 |
| regex_v8       | 23.2 ms                                                                | 20.8 ms: 1.11x faster                                                 |
| regex_dna      | 189 ms                                                                 | 181 ms: 1.04x faster                                                  |
| regex_compile  | 131 ms                                                                 | 145 ms: 1.10x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 86.7 ms: 1.09x faster                                                 |
| xml_etree_parse      | 136 ms                                                                 | 130 ms: 1.04x faster                                                  |
| tomli_loads          | 2.01 sec                                                               | 2.15 sec: 1.07x slower                                                |
| json_dumps           | 10.6 ms                                                                | 11.5 ms: 1.09x slower                                                 |
| unpickle_pure_python | 208 us                                                                 | 229 us: 1.10x slower                                                  |
| json_loads           | 27.3 us                                                                | 30.1 us: 1.10x slower                                                 |
| xml_etree_generate   | 85.4 ms                                                                | 97.0 ms: 1.14x slower                                                 |
| pickle_pure_python   | 292 us                                                                 | 334 us: 1.15x slower                                                  |
| xml_etree_process    | 59.2 ms                                                                | 69.6 ms: 1.18x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.07x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.60 ms: 1.30x slower                                                 |
| python_startup         | 11.0 ms                                                                | 16.0 ms: 1.45x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.37x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 54.9 ms: 1.12x slower                                                 |
| django_template | 34.2 ms                                                                | 39.6 ms: 1.16x slower                                                 |
| genshi_text     | 21.7 ms                                                                | 26.0 ms: 1.20x slower                                                 |
| mako            | 11.2 ms                                                                | 15.8 ms: 1.40x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.21x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.34 sec                                                               | 1.33 sec: 1.76x faster                                                |
| async_tree_io_tg           | 901 ms                                                                 | 517 ms: 1.74x faster                                                  |
| gc_traversal               | 3.32 ms                                                                | 1.91 ms: 1.74x faster                                                 |
| async_tree_io              | 881 ms                                                                 | 545 ms: 1.62x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 308 ms: 1.49x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 225 ms: 1.48x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 282 ms: 1.46x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 257 ms: 1.37x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 481 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 508 ms: 1.31x faster                                                  |
| deepcopy                   | 357 us                                                                 | 288 us: 1.24x faster                                                  |
| go                         | 141 ms                                                                 | 123 ms: 1.14x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.82 ms: 1.14x faster                                                 |
| pidigits                   | 216 ms                                                                 | 190 ms: 1.14x faster                                                  |
| regex_v8                   | 23.2 ms                                                                | 20.8 ms: 1.11x faster                                                 |
| float                      | 76.7 ms                                                                | 69.4 ms: 1.11x faster                                                 |
| xml_etree_iterparse        | 94.4 ms                                                                | 86.7 ms: 1.09x faster                                                 |
| sqlite_synth               | 2.25 us                                                                | 2.07 us: 1.09x faster                                                 |
| scimark_sor                | 134 ms                                                                 | 123 ms: 1.08x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 35.4 us: 1.08x faster                                                 |
| deepcopy_reduce            | 3.12 us                                                                | 2.92 us: 1.07x faster                                                 |
| html5lib                   | 68.6 ms                                                                | 65.4 ms: 1.05x faster                                                 |
| xml_etree_parse            | 136 ms                                                                 | 130 ms: 1.04x faster                                                  |
| regex_dna                  | 189 ms                                                                 | 181 ms: 1.04x faster                                                  |
| dulwich_log                | 74.5 ms                                                                | 72.0 ms: 1.03x faster                                                 |
| async_generators           | 375 ms                                                                 | 367 ms: 1.02x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 23.0 ms: 1.01x faster                                                 |
| bpe_tokeniser              | 4.46 sec                                                               | 4.44 sec: 1.01x faster                                                |
| pycparser                  | 1.12 sec                                                               | 1.14 sec: 1.01x slower                                                |
| pathlib                    | 19.3 ms                                                                | 19.7 ms: 1.02x slower                                                 |
| docutils                   | 2.63 sec                                                               | 2.70 sec: 1.03x slower                                                |
| scimark_fft                | 348 ms                                                                 | 362 ms: 1.04x slower                                                  |
| json                       | 4.98 ms                                                                | 5.20 ms: 1.04x slower                                                 |
| spectral_norm              | 108 ms                                                                 | 114 ms: 1.06x slower                                                  |
| pyflate                    | 449 ms                                                                 | 479 ms: 1.07x slower                                                  |
| tomli_loads                | 2.01 sec                                                               | 2.15 sec: 1.07x slower                                                |
| pprint_safe_repr           | 719 ms                                                                 | 774 ms: 1.08x slower                                                  |
| generators                 | 28.5 ms                                                                | 30.9 ms: 1.08x slower                                                 |
| json_dumps                 | 10.6 ms                                                                | 11.5 ms: 1.09x slower                                                 |
| 2to3                       | 259 ms                                                                 | 285 ms: 1.10x slower                                                  |
| unpickle_pure_python       | 208 us                                                                 | 229 us: 1.10x slower                                                  |
| json_loads                 | 27.3 us                                                                | 30.1 us: 1.10x slower                                                 |
| regex_compile              | 131 ms                                                                 | 145 ms: 1.10x slower                                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.60 sec: 1.10x slower                                                |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.26 ms: 1.11x slower                                                 |
| create_gc_cycles           | 1.33 ms                                                                | 1.49 ms: 1.11x slower                                                 |
| chaos                      | 56.3 ms                                                                | 62.8 ms: 1.11x slower                                                 |
| genshi_xml                 | 49.1 ms                                                                | 54.9 ms: 1.12x slower                                                 |
| scimark_lu                 | 112 ms                                                                 | 126 ms: 1.12x slower                                                  |
| sympy_integrate            | 19.7 ms                                                                | 22.1 ms: 1.12x slower                                                 |
| richards                   | 44.4 ms                                                                | 49.9 ms: 1.12x slower                                                 |
| hexiom                     | 5.95 ms                                                                | 6.69 ms: 1.12x slower                                                 |
| nqueens                    | 77.7 ms                                                                | 87.6 ms: 1.13x slower                                                 |
| telco                      | 7.77 ms                                                                | 8.77 ms: 1.13x slower                                                 |
| thrift                     | 772 us                                                                 | 873 us: 1.13x slower                                                  |
| richards_super             | 50.4 ms                                                                | 57.1 ms: 1.13x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                                | 97.0 ms: 1.14x slower                                                 |
| deltablue                  | 3.10 ms                                                                | 3.54 ms: 1.14x slower                                                 |
| pickle_pure_python         | 292 us                                                                 | 334 us: 1.15x slower                                                  |
| sympy_str                  | 274 ms                                                                 | 315 ms: 1.15x slower                                                  |
| sympy_sum                  | 154 ms                                                                 | 178 ms: 1.15x slower                                                  |
| scimark_monte_carlo        | 65.8 ms                                                                | 76.1 ms: 1.16x slower                                                 |
| django_template            | 34.2 ms                                                                | 39.6 ms: 1.16x slower                                                 |
| sympy_expand               | 454 ms                                                                 | 530 ms: 1.17x slower                                                  |
| xml_etree_process          | 59.2 ms                                                                | 69.6 ms: 1.18x slower                                                 |
| raytrace                   | 250 ms                                                                 | 295 ms: 1.18x slower                                                  |
| comprehensions             | 16.6 us                                                                | 19.6 us: 1.18x slower                                                 |
| genshi_text                | 21.7 ms                                                                | 26.0 ms: 1.20x slower                                                 |
| typing_runtime_protocols   | 156 us                                                                 | 192 us: 1.24x slower                                                  |
| crypto_pyaes               | 68.2 ms                                                                | 84.7 ms: 1.24x slower                                                 |
| fannkuch                   | 376 ms                                                                 | 468 ms: 1.25x slower                                                  |
| logging_format             | 6.92 us                                                                | 8.81 us: 1.27x slower                                                 |
| meteor_contest             | 101 ms                                                                 | 129 ms: 1.27x slower                                                  |
| logging_simple             | 6.14 us                                                                | 7.88 us: 1.28x slower                                                 |
| python_startup_no_site     | 7.41 ms                                                                | 9.60 ms: 1.30x slower                                                 |
| coverage                   | 82.5 ms                                                                | 109 ms: 1.32x slower                                                  |
| nbody                      | 85.3 ms                                                                | 117 ms: 1.37x slower                                                  |
| mako                       | 11.2 ms                                                                | 15.8 ms: 1.40x slower                                                 |
| python_startup             | 11.0 ms                                                                | 16.0 ms: 1.45x slower                                                 |
| bench_thread_pool          | 924 us                                                                 | 3.13 ms: 3.39x slower                                                 |
| logging_silent             | 98.2 ns                                                                | 538 ns: 5.47x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                                | 104 ms: 9.45x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.08x slower                                                          |

Benchmark hidden because not significant (2): pylint, asyncio_websockets
Ignored benchmarks (18) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250513-3.15.0a0-9ad0c7b-NOGIL/bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.020x slower

# HPT report

- Reliability score: 95.70% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.40x