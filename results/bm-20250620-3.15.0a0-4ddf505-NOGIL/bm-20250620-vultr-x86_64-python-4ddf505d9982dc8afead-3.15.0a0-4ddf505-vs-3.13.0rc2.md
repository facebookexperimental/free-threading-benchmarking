# Results vs. 3.13.0rc2

- fork: python
- ref: 4ddf505d9982dc8afead
- machine: linux-x86_64
- commit hash: 4ddf505
- commit date: 2025-06-20
- overall geometric mean: 1.017x slower
- HPT reliability: 94.10%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.41x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 282 ms: 1.09x slower                                                  |
| docutils       | 2.63 sec                                                               | 2.67 sec: 1.02x slower                                                |
| html5lib       | 68.6 ms                                                                | 66.1 ms: 1.04x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 522 ms: 1.73x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 550 ms: 1.60x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 224 ms: 1.48x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 312 ms: 1.47x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 284 ms: 1.44x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 257 ms: 1.38x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 463 ms: 1.37x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 488 ms: 1.36x faster                                                  |
| async_generators           | 375 ms                                                                 | 364 ms: 1.03x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 23.1 ms: 1.01x faster                                                 |
| Geometric mean             | (ref)                                                                  | 1.33x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 182 ms: 1.19x faster                                                  |
| float          | 76.7 ms                                                                | 68.8 ms: 1.11x faster                                                 |
| nbody          | 85.3 ms                                                                | 121 ms: 1.42x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.66 ms: 1.21x faster                                                 |
| regex_dna      | 189 ms                                                                 | 168 ms: 1.12x faster                                                  |
| regex_v8       | 23.2 ms                                                                | 20.8 ms: 1.12x faster                                                 |
| regex_compile  | 131 ms                                                                 | 143 ms: 1.09x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.09x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 86.8 ms: 1.09x faster                                                 |
| xml_etree_parse      | 136 ms                                                                 | 129 ms: 1.05x faster                                                  |
| tomli_loads          | 2.01 sec                                                               | 2.15 sec: 1.07x slower                                                |
| unpickle_pure_python | 208 us                                                                 | 229 us: 1.10x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                                | 94.6 ms: 1.11x slower                                                 |
| json_dumps           | 10.6 ms                                                                | 11.8 ms: 1.11x slower                                                 |
| json_loads           | 27.3 us                                                                | 31.0 us: 1.13x slower                                                 |
| pickle_pure_python   | 292 us                                                                 | 337 us: 1.15x slower                                                  |
| xml_etree_process    | 59.2 ms                                                                | 68.6 ms: 1.16x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.07x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.61 ms: 1.30x slower                                                 |
| python_startup         | 11.0 ms                                                                | 16.1 ms: 1.46x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.37x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.2 ms                                                                | 39.4 ms: 1.15x slower                                                 |
| genshi_xml      | 49.1 ms                                                                | 58.2 ms: 1.19x slower                                                 |
| genshi_text     | 21.7 ms                                                                | 26.5 ms: 1.22x slower                                                 |
| mako            | 11.2 ms                                                                | 15.9 ms: 1.42x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.24x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.34 sec                                                               | 1.31 sec: 1.79x faster                                                |
| async_tree_io_tg           | 901 ms                                                                 | 522 ms: 1.73x faster                                                  |
| gc_traversal               | 3.32 ms                                                                | 1.93 ms: 1.72x faster                                                 |
| async_tree_io              | 881 ms                                                                 | 550 ms: 1.60x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 224 ms: 1.48x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 312 ms: 1.47x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 284 ms: 1.44x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 257 ms: 1.38x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 463 ms: 1.37x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 488 ms: 1.36x faster                                                  |
| deepcopy                   | 357 us                                                                 | 286 us: 1.25x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.66 ms: 1.21x faster                                                 |
| pidigits                   | 216 ms                                                                 | 182 ms: 1.19x faster                                                  |
| go                         | 141 ms                                                                 | 121 ms: 1.16x faster                                                  |
| regex_dna                  | 189 ms                                                                 | 168 ms: 1.12x faster                                                  |
| sqlite_synth               | 2.25 us                                                                | 2.02 us: 1.12x faster                                                 |
| regex_v8                   | 23.2 ms                                                                | 20.8 ms: 1.12x faster                                                 |
| float                      | 76.7 ms                                                                | 68.8 ms: 1.11x faster                                                 |
| deepcopy_memo              | 38.1 us                                                                | 34.4 us: 1.11x faster                                                 |
| scimark_sor                | 134 ms                                                                 | 122 ms: 1.09x faster                                                  |
| xml_etree_iterparse        | 94.4 ms                                                                | 86.8 ms: 1.09x faster                                                 |
| xml_etree_parse            | 136 ms                                                                 | 129 ms: 1.05x faster                                                  |
| dulwich_log                | 74.5 ms                                                                | 71.1 ms: 1.05x faster                                                 |
| deepcopy_reduce            | 3.12 us                                                                | 2.99 us: 1.04x faster                                                 |
| html5lib                   | 68.6 ms                                                                | 66.1 ms: 1.04x faster                                                 |
| async_generators           | 375 ms                                                                 | 364 ms: 1.03x faster                                                  |
| bpe_tokeniser              | 4.46 sec                                                               | 4.34 sec: 1.03x faster                                                |
| coroutines                 | 23.3 ms                                                                | 23.1 ms: 1.01x faster                                                 |
| spectral_norm              | 108 ms                                                                 | 108 ms: 1.01x slower                                                  |
| pycparser                  | 1.12 sec                                                               | 1.13 sec: 1.01x slower                                                |
| pathlib                    | 19.3 ms                                                                | 19.5 ms: 1.01x slower                                                 |
| docutils                   | 2.63 sec                                                               | 2.67 sec: 1.02x slower                                                |
| scimark_fft                | 348 ms                                                                 | 356 ms: 1.02x slower                                                  |
| json                       | 4.98 ms                                                                | 5.25 ms: 1.05x slower                                                 |
| pyflate                    | 449 ms                                                                 | 477 ms: 1.06x slower                                                  |
| hexiom                     | 5.95 ms                                                                | 6.33 ms: 1.06x slower                                                 |
| comprehensions             | 16.6 us                                                                | 17.6 us: 1.06x slower                                                 |
| tomli_loads                | 2.01 sec                                                               | 2.15 sec: 1.07x slower                                                |
| regex_compile              | 131 ms                                                                 | 143 ms: 1.09x slower                                                  |
| 2to3                       | 259 ms                                                                 | 282 ms: 1.09x slower                                                  |
| telco                      | 7.77 ms                                                                | 8.49 ms: 1.09x slower                                                 |
| chaos                      | 56.3 ms                                                                | 61.8 ms: 1.10x slower                                                 |
| unpickle_pure_python       | 208 us                                                                 | 229 us: 1.10x slower                                                  |
| nqueens                    | 77.7 ms                                                                | 85.8 ms: 1.10x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                                | 94.6 ms: 1.11x slower                                                 |
| generators                 | 28.5 ms                                                                | 31.7 ms: 1.11x slower                                                 |
| json_dumps                 | 10.6 ms                                                                | 11.8 ms: 1.11x slower                                                 |
| sympy_integrate            | 19.7 ms                                                                | 21.9 ms: 1.11x slower                                                 |
| create_gc_cycles           | 1.33 ms                                                                | 1.50 ms: 1.12x slower                                                 |
| scimark_lu                 | 112 ms                                                                 | 127 ms: 1.13x slower                                                  |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.36 ms: 1.13x slower                                                 |
| json_loads                 | 27.3 us                                                                | 31.0 us: 1.13x slower                                                 |
| thrift                     | 772 us                                                                 | 876 us: 1.13x slower                                                  |
| sympy_str                  | 274 ms                                                                 | 314 ms: 1.15x slower                                                  |
| sympy_expand               | 454 ms                                                                 | 522 ms: 1.15x slower                                                  |
| django_template            | 34.2 ms                                                                | 39.4 ms: 1.15x slower                                                 |
| scimark_monte_carlo        | 65.8 ms                                                                | 75.9 ms: 1.15x slower                                                 |
| pickle_pure_python         | 292 us                                                                 | 337 us: 1.15x slower                                                  |
| xml_etree_process          | 59.2 ms                                                                | 68.6 ms: 1.16x slower                                                 |
| deltablue                  | 3.10 ms                                                                | 3.60 ms: 1.16x slower                                                 |
| sympy_sum                  | 154 ms                                                                 | 179 ms: 1.16x slower                                                  |
| richards                   | 44.4 ms                                                                | 52.4 ms: 1.18x slower                                                 |
| genshi_xml                 | 49.1 ms                                                                | 58.2 ms: 1.19x slower                                                 |
| raytrace                   | 250 ms                                                                 | 297 ms: 1.19x slower                                                  |
| meteor_contest             | 101 ms                                                                 | 121 ms: 1.19x slower                                                  |
| richards_super             | 50.4 ms                                                                | 60.4 ms: 1.20x slower                                                 |
| typing_runtime_protocols   | 156 us                                                                 | 188 us: 1.21x slower                                                  |
| pprint_safe_repr           | 719 ms                                                                 | 868 ms: 1.21x slower                                                  |
| genshi_text                | 21.7 ms                                                                | 26.5 ms: 1.22x slower                                                 |
| pprint_pformat             | 1.46 sec                                                               | 1.79 sec: 1.23x slower                                                |
| fannkuch                   | 376 ms                                                                 | 463 ms: 1.23x slower                                                  |
| logging_simple             | 6.14 us                                                                | 7.60 us: 1.24x slower                                                 |
| logging_format             | 6.92 us                                                                | 8.62 us: 1.25x slower                                                 |
| crypto_pyaes               | 68.2 ms                                                                | 85.1 ms: 1.25x slower                                                 |
| python_startup_no_site     | 7.41 ms                                                                | 9.61 ms: 1.30x slower                                                 |
| coverage                   | 82.5 ms                                                                | 110 ms: 1.34x slower                                                  |
| nbody                      | 85.3 ms                                                                | 121 ms: 1.42x slower                                                  |
| mako                       | 11.2 ms                                                                | 15.9 ms: 1.42x slower                                                 |
| python_startup             | 11.0 ms                                                                | 16.1 ms: 1.46x slower                                                 |
| bench_thread_pool          | 924 us                                                                 | 3.11 ms: 3.36x slower                                                 |
| logging_silent             | 98.2 ns                                                                | 523 ns: 5.33x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                                | 103 ms: 9.39x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.08x slower                                                          |

Benchmark hidden because not significant (2): pylint, asyncio_websockets
Ignored benchmarks (18) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250620-3.15.0a0-4ddf505-NOGIL/bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.017x slower

# HPT report

- Reliability score: 94.10% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.41x