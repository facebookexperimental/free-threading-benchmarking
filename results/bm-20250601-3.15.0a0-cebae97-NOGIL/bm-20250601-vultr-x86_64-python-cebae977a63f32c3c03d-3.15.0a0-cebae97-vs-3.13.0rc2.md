# Results vs. 3.13.0rc2

- fork: python
- ref: cebae977a63f32c3c03d
- machine: linux-x86_64
- commit hash: cebae97
- commit date: 2025-06-01
- overall geometric mean: 1.022x slower
- HPT reliability: 94.75%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.40x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 284 ms: 1.09x slower                                                  |
| docutils       | 2.63 sec                                                               | 2.70 sec: 1.03x slower                                                |
| html5lib       | 68.6 ms                                                                | 67.0 ms: 1.02x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 528 ms: 1.71x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 559 ms: 1.58x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 229 ms: 1.45x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 316 ms: 1.45x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 287 ms: 1.43x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 261 ms: 1.35x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 475 ms: 1.33x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 503 ms: 1.32x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 22.8 ms: 1.02x faster                                                 |
| async_generators           | 375 ms                                                                 | 370 ms: 1.01x faster                                                  |
| asyncio_websockets         | 517 ms                                                                 | 516 ms: 1.00x faster                                                  |
| asyncio_tcp                | 502 ms                                                                 | 535 ms: 1.07x slower                                                  |
| asyncio_tcp_ssl            | 1.51 sec                                                               | 1.79 sec: 1.18x slower                                                |
| Geometric mean             | (ref)                                                                  | 1.24x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 195 ms: 1.11x faster                                                  |
| float          | 76.7 ms                                                                | 69.4 ms: 1.11x faster                                                 |
| nbody          | 85.3 ms                                                                | 118 ms: 1.39x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.68 ms: 1.20x faster                                                 |
| regex_v8       | 23.2 ms                                                                | 20.2 ms: 1.15x faster                                                 |
| regex_dna      | 189 ms                                                                 | 175 ms: 1.08x faster                                                  |
| regex_compile  | 131 ms                                                                 | 144 ms: 1.09x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.08x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 87.2 ms: 1.08x faster                                                 |
| xml_etree_parse      | 136 ms                                                                 | 130 ms: 1.05x faster                                                  |
| pickle_dict          | 32.7 us                                                                | 31.8 us: 1.03x faster                                                 |
| pickle_list          | 4.81 us                                                                | 4.95 us: 1.03x slower                                                 |
| unpickle             | 14.6 us                                                                | 15.3 us: 1.05x slower                                                 |
| tomli_loads          | 2.01 sec                                                               | 2.13 sec: 1.06x slower                                                |
| pickle               | 11.4 us                                                                | 12.3 us: 1.08x slower                                                 |
| unpickle_pure_python | 208 us                                                                 | 230 us: 1.11x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                                | 94.9 ms: 1.11x slower                                                 |
| json_dumps           | 10.6 ms                                                                | 12.0 ms: 1.13x slower                                                 |
| pickle_pure_python   | 292 us                                                                 | 335 us: 1.15x slower                                                  |
| json_loads           | 27.3 us                                                                | 31.5 us: 1.15x slower                                                 |
| xml_etree_process    | 59.2 ms                                                                | 68.7 ms: 1.16x slower                                                 |
| unpickle_list        | 4.60 us                                                                | 5.38 us: 1.17x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.07x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.62 ms: 1.30x slower                                                 |
| python_startup         | 11.0 ms                                                                | 16.0 ms: 1.45x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.37x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.2 ms                                                                | 39.8 ms: 1.16x slower                                                 |
| genshi_xml      | 49.1 ms                                                                | 57.8 ms: 1.18x slower                                                 |
| genshi_text     | 21.7 ms                                                                | 26.6 ms: 1.22x slower                                                 |
| mako            | 11.2 ms                                                                | 15.7 ms: 1.40x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.24x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.34 sec                                                               | 1.32 sec: 1.77x faster                                                |
| gc_traversal               | 3.32 ms                                                                | 1.93 ms: 1.72x faster                                                 |
| async_tree_io_tg           | 901 ms                                                                 | 528 ms: 1.71x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 559 ms: 1.58x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 229 ms: 1.45x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 316 ms: 1.45x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 287 ms: 1.43x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 261 ms: 1.35x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 475 ms: 1.33x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 503 ms: 1.32x faster                                                  |
| deepcopy                   | 357 us                                                                 | 291 us: 1.23x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.68 ms: 1.20x faster                                                 |
| go                         | 141 ms                                                                 | 121 ms: 1.16x faster                                                  |
| regex_v8                   | 23.2 ms                                                                | 20.2 ms: 1.15x faster                                                 |
| pidigits                   | 216 ms                                                                 | 195 ms: 1.11x faster                                                  |
| float                      | 76.7 ms                                                                | 69.4 ms: 1.11x faster                                                 |
| deepcopy_memo              | 38.1 us                                                                | 34.5 us: 1.10x faster                                                 |
| sqlite_synth               | 2.25 us                                                                | 2.04 us: 1.10x faster                                                 |
| scimark_sor                | 134 ms                                                                 | 122 ms: 1.09x faster                                                  |
| xml_etree_iterparse        | 94.4 ms                                                                | 87.2 ms: 1.08x faster                                                 |
| regex_dna                  | 189 ms                                                                 | 175 ms: 1.08x faster                                                  |
| xml_etree_parse            | 136 ms                                                                 | 130 ms: 1.05x faster                                                  |
| dulwich_log                | 74.5 ms                                                                | 71.4 ms: 1.04x faster                                                 |
| pickle_dict                | 32.7 us                                                                | 31.8 us: 1.03x faster                                                 |
| bpe_tokeniser              | 4.46 sec                                                               | 4.33 sec: 1.03x faster                                                |
| html5lib                   | 68.6 ms                                                                | 67.0 ms: 1.02x faster                                                 |
| coroutines                 | 23.3 ms                                                                | 22.8 ms: 1.02x faster                                                 |
| deepcopy_reduce            | 3.12 us                                                                | 3.06 us: 1.02x faster                                                 |
| async_generators           | 375 ms                                                                 | 370 ms: 1.01x faster                                                  |
| asyncio_websockets         | 517 ms                                                                 | 516 ms: 1.00x faster                                                  |
| pathlib                    | 19.3 ms                                                                | 19.5 ms: 1.01x slower                                                 |
| spectral_norm              | 108 ms                                                                 | 109 ms: 1.02x slower                                                  |
| docutils                   | 2.63 sec                                                               | 2.70 sec: 1.03x slower                                                |
| pickle_list                | 4.81 us                                                                | 4.95 us: 1.03x slower                                                 |
| pyflate                    | 449 ms                                                                 | 465 ms: 1.03x slower                                                  |
| generators                 | 28.5 ms                                                                | 29.7 ms: 1.04x slower                                                 |
| scimark_fft                | 348 ms                                                                 | 365 ms: 1.05x slower                                                  |
| unpickle                   | 14.6 us                                                                | 15.3 us: 1.05x slower                                                 |
| tomli_loads                | 2.01 sec                                                               | 2.13 sec: 1.06x slower                                                |
| comprehensions             | 16.6 us                                                                | 17.6 us: 1.06x slower                                                 |
| hexiom                     | 5.95 ms                                                                | 6.33 ms: 1.06x slower                                                 |
| asyncio_tcp                | 502 ms                                                                 | 535 ms: 1.07x slower                                                  |
| json                       | 4.98 ms                                                                | 5.37 ms: 1.08x slower                                                 |
| pickle                     | 11.4 us                                                                | 12.3 us: 1.08x slower                                                 |
| 2to3                       | 259 ms                                                                 | 284 ms: 1.09x slower                                                  |
| regex_compile              | 131 ms                                                                 | 144 ms: 1.09x slower                                                  |
| nqueens                    | 77.7 ms                                                                | 85.4 ms: 1.10x slower                                                 |
| chaos                      | 56.3 ms                                                                | 61.9 ms: 1.10x slower                                                 |
| unpickle_pure_python       | 208 us                                                                 | 230 us: 1.11x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                                | 94.9 ms: 1.11x slower                                                 |
| sympy_integrate            | 19.7 ms                                                                | 22.0 ms: 1.12x slower                                                 |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.33 ms: 1.12x slower                                                 |
| telco                      | 7.77 ms                                                                | 8.73 ms: 1.12x slower                                                 |
| create_gc_cycles           | 1.33 ms                                                                | 1.50 ms: 1.13x slower                                                 |
| json_dumps                 | 10.6 ms                                                                | 12.0 ms: 1.13x slower                                                 |
| scimark_lu                 | 112 ms                                                                 | 128 ms: 1.14x slower                                                  |
| sympy_str                  | 274 ms                                                                 | 315 ms: 1.15x slower                                                  |
| pickle_pure_python         | 292 us                                                                 | 335 us: 1.15x slower                                                  |
| json_loads                 | 27.3 us                                                                | 31.5 us: 1.15x slower                                                 |
| thrift                     | 772 us                                                                 | 893 us: 1.16x slower                                                  |
| richards                   | 44.4 ms                                                                | 51.5 ms: 1.16x slower                                                 |
| xml_etree_process          | 59.2 ms                                                                | 68.7 ms: 1.16x slower                                                 |
| django_template            | 34.2 ms                                                                | 39.8 ms: 1.16x slower                                                 |
| sympy_expand               | 454 ms                                                                 | 528 ms: 1.16x slower                                                  |
| richards_super             | 50.4 ms                                                                | 58.7 ms: 1.17x slower                                                 |
| unpickle_list              | 4.60 us                                                                | 5.38 us: 1.17x slower                                                 |
| scimark_monte_carlo        | 65.8 ms                                                                | 77.1 ms: 1.17x slower                                                 |
| sympy_sum                  | 154 ms                                                                 | 181 ms: 1.17x slower                                                  |
| deltablue                  | 3.10 ms                                                                | 3.63 ms: 1.17x slower                                                 |
| genshi_xml                 | 49.1 ms                                                                | 57.8 ms: 1.18x slower                                                 |
| asyncio_tcp_ssl            | 1.51 sec                                                               | 1.79 sec: 1.18x slower                                                |
| raytrace                   | 250 ms                                                                 | 296 ms: 1.19x slower                                                  |
| meteor_contest             | 101 ms                                                                 | 120 ms: 1.19x slower                                                  |
| fannkuch                   | 376 ms                                                                 | 459 ms: 1.22x slower                                                  |
| genshi_text                | 21.7 ms                                                                | 26.6 ms: 1.22x slower                                                 |
| typing_runtime_protocols   | 156 us                                                                 | 191 us: 1.22x slower                                                  |
| pprint_safe_repr           | 719 ms                                                                 | 883 ms: 1.23x slower                                                  |
| crypto_pyaes               | 68.2 ms                                                                | 85.1 ms: 1.25x slower                                                 |
| pprint_pformat             | 1.46 sec                                                               | 1.83 sec: 1.26x slower                                                |
| logging_simple             | 6.14 us                                                                | 7.79 us: 1.27x slower                                                 |
| python_startup_no_site     | 7.41 ms                                                                | 9.62 ms: 1.30x slower                                                 |
| logging_format             | 6.92 us                                                                | 9.01 us: 1.30x slower                                                 |
| unpack_sequence            | 39.3 ns                                                                | 52.9 ns: 1.34x slower                                                 |
| coverage                   | 82.5 ms                                                                | 111 ms: 1.35x slower                                                  |
| nbody                      | 85.3 ms                                                                | 118 ms: 1.39x slower                                                  |
| mako                       | 11.2 ms                                                                | 15.7 ms: 1.40x slower                                                 |
| python_startup             | 11.0 ms                                                                | 16.0 ms: 1.45x slower                                                 |
| bench_thread_pool          | 924 us                                                                 | 3.12 ms: 3.37x slower                                                 |
| logging_silent             | 98.2 ns                                                                | 533 ns: 5.42x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                                | 103 ms: 9.32x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.09x slower                                                          |

Benchmark hidden because not significant (2): pylint, pycparser
Ignored benchmarks (10) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20250601-3.15.0a0-cebae97-NOGIL/bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.022x slower

# HPT report

- Reliability score: 94.75% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.40x