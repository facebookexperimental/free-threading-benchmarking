# Results vs. 3.13.0rc2

- fork: python
- ref: cebae977a63f32c3c03d
- machine: linux-x86_64
- commit hash: cebae97
- commit date: 2025-06-01
- overall geometric mean: 1.537x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 255 ms: 1.02x faster                                                  |
| docutils       | 2.63 sec                                                               | 2.58 sec: 1.02x faster                                                |
| html5lib       | 68.6 ms                                                                | 62.2 ms: 1.10x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization     | 459 ms                                                                 | 309 ms: 1.49x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 625 ms: 1.44x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 613 ms: 1.44x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 311 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 508 ms: 1.31x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 271 ms: 1.30x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 256 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 501 ms: 1.26x faster                                                  |
| async_generators           | 375 ms                                                                 | 352 ms: 1.07x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 23.2 ms: 1.01x faster                                                 |
| asyncio_tcp_ssl            | 1.51 sec                                                               | 1.52 sec: 1.00x slower                                                |
| Geometric mean             | (ref)                                                                  | 1.21x faster                                                          |

Benchmark hidden because not significant (2): asyncio_tcp, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 76.7 ms                                                                | 65.0 ms: 1.18x faster                                                 |
| pidigits       | 216 ms                                                                 | 194 ms: 1.12x faster                                                  |
| nbody          | 85.3 ms                                                                | 82.6 ms: 1.03x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.11x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.52 ms: 1.27x faster                                                 |
| regex_dna      | 189 ms                                                                 | 168 ms: 1.12x faster                                                  |
| regex_v8       | 23.2 ms                                                                | 21.3 ms: 1.09x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.16x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                               | 1.78 sec: 1.13x faster                                                |
| xml_etree_process    | 59.2 ms                                                                | 53.4 ms: 1.11x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                                | 77.9 ms: 1.10x faster                                                 |
| unpickle_pure_python | 208 us                                                                 | 191 us: 1.09x faster                                                  |
| unpickle             | 14.6 us                                                                | 13.9 us: 1.05x faster                                                 |
| xml_etree_parse      | 136 ms                                                                 | 131 ms: 1.04x faster                                                  |
| xml_etree_iterparse  | 94.4 ms                                                                | 92.3 ms: 1.02x faster                                                 |
| json_loads           | 27.3 us                                                                | 28.0 us: 1.02x slower                                                 |
| json_dumps           | 10.6 ms                                                                | 10.9 ms: 1.03x slower                                                 |
| pickle_list          | 4.81 us                                                                | 5.09 us: 1.06x slower                                                 |
| unpickle_list        | 4.60 us                                                                | 4.87 us: 1.06x slower                                                 |
| pickle_pure_python   | 292 us                                                                 | 310 us: 1.06x slower                                                  |
| pickle               | 11.4 us                                                                | 12.5 us: 1.09x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 7.31 ms: 1.01x faster                                                 |
| python_startup         | 11.0 ms                                                                | 12.5 ms: 1.13x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.06x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 21.7 ms                                                                | 20.5 ms: 1.06x faster                                                 |
| mako            | 11.2 ms                                                                | 11.1 ms: 1.01x faster                                                 |
| genshi_xml      | 49.1 ms                                                                | 48.7 ms: 1.01x faster                                                 |
| django_template | 34.2 ms                                                                | 34.9 ms: 1.02x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pprint_pformat             | 1.46 sec                                                               | 1.38 us: 1057870.32x faster                                           |
| pprint_safe_repr           | 719 ms                                                                 | 797 ns: 902152.38x faster                                             |
| mdp                        | 2.34 sec                                                               | 1.17 sec: 2.00x faster                                                |
| async_tree_memoization     | 459 ms                                                                 | 309 ms: 1.49x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 625 ms: 1.44x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 613 ms: 1.44x faster                                                  |
| deepcopy                   | 357 us                                                                 | 249 us: 1.43x faster                                                  |
| richards                   | 44.4 ms                                                                | 32.2 ms: 1.38x faster                                                 |
| richards_super             | 50.4 ms                                                                | 36.7 ms: 1.37x faster                                                 |
| async_tree_memoization_tg  | 410 ms                                                                 | 311 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 508 ms: 1.31x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 29.1 us: 1.31x faster                                                 |
| async_tree_none            | 353 ms                                                                 | 271 ms: 1.30x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 256 ms: 1.30x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.52 ms: 1.27x faster                                                 |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 501 ms: 1.26x faster                                                  |
| scimark_fft                | 348 ms                                                                 | 289 ms: 1.20x faster                                                  |
| spectral_norm              | 108 ms                                                                 | 89.6 ms: 1.20x faster                                                 |
| scimark_sor                | 134 ms                                                                 | 112 ms: 1.19x faster                                                  |
| float                      | 76.7 ms                                                                | 65.0 ms: 1.18x faster                                                 |
| deepcopy_reduce            | 3.12 us                                                                | 2.66 us: 1.17x faster                                                 |
| go                         | 141 ms                                                                 | 120 ms: 1.17x faster                                                  |
| pyflate                    | 449 ms                                                                 | 393 ms: 1.14x faster                                                  |
| tomli_loads                | 2.01 sec                                                               | 1.78 sec: 1.13x faster                                                |
| pylint                     | 317 ms                                                                 | 282 ms: 1.13x faster                                                  |
| regex_dna                  | 189 ms                                                                 | 168 ms: 1.12x faster                                                  |
| pidigits                   | 216 ms                                                                 | 194 ms: 1.12x faster                                                  |
| bpe_tokeniser              | 4.46 sec                                                               | 4.00 sec: 1.11x faster                                                |
| xml_etree_process          | 59.2 ms                                                                | 53.4 ms: 1.11x faster                                                 |
| html5lib                   | 68.6 ms                                                                | 62.2 ms: 1.10x faster                                                 |
| dulwich_log                | 74.5 ms                                                                | 67.7 ms: 1.10x faster                                                 |
| xml_etree_generate         | 85.4 ms                                                                | 77.9 ms: 1.10x faster                                                 |
| regex_v8                   | 23.2 ms                                                                | 21.3 ms: 1.09x faster                                                 |
| unpickle_pure_python       | 208 us                                                                 | 191 us: 1.09x faster                                                  |
| telco                      | 7.77 ms                                                                | 7.13 ms: 1.09x faster                                                 |
| scimark_monte_carlo        | 65.8 ms                                                                | 60.5 ms: 1.09x faster                                                 |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.40 ms: 1.08x faster                                                 |
| async_generators           | 375 ms                                                                 | 352 ms: 1.07x faster                                                  |
| deltablue                  | 3.10 ms                                                                | 2.91 ms: 1.06x faster                                                 |
| genshi_text                | 21.7 ms                                                                | 20.5 ms: 1.06x faster                                                 |
| unpickle                   | 14.6 us                                                                | 13.9 us: 1.05x faster                                                 |
| generators                 | 28.5 ms                                                                | 27.4 ms: 1.04x faster                                                 |
| sqlite_synth               | 2.25 us                                                                | 2.17 us: 1.04x faster                                                 |
| xml_etree_parse            | 136 ms                                                                 | 131 ms: 1.04x faster                                                  |
| thrift                     | 772 us                                                                 | 746 us: 1.03x faster                                                  |
| nbody                      | 85.3 ms                                                                | 82.6 ms: 1.03x faster                                                 |
| sympy_integrate            | 19.7 ms                                                                | 19.1 ms: 1.03x faster                                                 |
| meteor_contest             | 101 ms                                                                 | 98.5 ms: 1.03x faster                                                 |
| scimark_lu                 | 112 ms                                                                 | 110 ms: 1.03x faster                                                  |
| xml_etree_iterparse        | 94.4 ms                                                                | 92.3 ms: 1.02x faster                                                 |
| docutils                   | 2.63 sec                                                               | 2.58 sec: 1.02x faster                                                |
| fannkuch                   | 376 ms                                                                 | 370 ms: 1.02x faster                                                  |
| 2to3                       | 259 ms                                                                 | 255 ms: 1.02x faster                                                  |
| python_startup_no_site     | 7.41 ms                                                                | 7.31 ms: 1.01x faster                                                 |
| sympy_str                  | 274 ms                                                                 | 271 ms: 1.01x faster                                                  |
| mako                       | 11.2 ms                                                                | 11.1 ms: 1.01x faster                                                 |
| typing_runtime_protocols   | 156 us                                                                 | 154 us: 1.01x faster                                                  |
| genshi_xml                 | 49.1 ms                                                                | 48.7 ms: 1.01x faster                                                 |
| coroutines                 | 23.3 ms                                                                | 23.2 ms: 1.01x faster                                                 |
| coverage                   | 82.5 ms                                                                | 81.9 ms: 1.01x faster                                                 |
| asyncio_tcp_ssl            | 1.51 sec                                                               | 1.52 sec: 1.00x slower                                                |
| chaos                      | 56.3 ms                                                                | 56.6 ms: 1.01x slower                                                 |
| nqueens                    | 77.7 ms                                                                | 78.3 ms: 1.01x slower                                                 |
| comprehensions             | 16.6 us                                                                | 16.7 us: 1.01x slower                                                 |
| json                       | 4.98 ms                                                                | 5.05 ms: 1.01x slower                                                 |
| raytrace                   | 250 ms                                                                 | 254 ms: 1.02x slower                                                  |
| pathlib                    | 19.3 ms                                                                | 19.6 ms: 1.02x slower                                                 |
| pycparser                  | 1.12 sec                                                               | 1.14 sec: 1.02x slower                                                |
| django_template            | 34.2 ms                                                                | 34.9 ms: 1.02x slower                                                 |
| json_loads                 | 27.3 us                                                                | 28.0 us: 1.02x slower                                                 |
| crypto_pyaes               | 68.2 ms                                                                | 69.8 ms: 1.02x slower                                                 |
| sympy_expand               | 454 ms                                                                 | 464 ms: 1.02x slower                                                  |
| json_dumps                 | 10.6 ms                                                                | 10.9 ms: 1.03x slower                                                 |
| hexiom                     | 5.95 ms                                                                | 6.26 ms: 1.05x slower                                                 |
| pickle_list                | 4.81 us                                                                | 5.09 us: 1.06x slower                                                 |
| unpickle_list              | 4.60 us                                                                | 4.87 us: 1.06x slower                                                 |
| pickle_pure_python         | 292 us                                                                 | 310 us: 1.06x slower                                                  |
| logging_format             | 6.92 us                                                                | 7.43 us: 1.07x slower                                                 |
| logging_simple             | 6.14 us                                                                | 6.69 us: 1.09x slower                                                 |
| pickle                     | 11.4 us                                                                | 12.5 us: 1.09x slower                                                 |
| python_startup             | 11.0 ms                                                                | 12.5 ms: 1.13x slower                                                 |
| bench_thread_pool          | 924 us                                                                 | 1.05 ms: 1.13x slower                                                 |
| gc_traversal               | 3.32 ms                                                                | 4.54 ms: 1.37x slower                                                 |
| create_gc_cycles           | 1.33 ms                                                                | 1.90 ms: 1.43x slower                                                 |
| unpack_sequence            | 39.3 ns                                                                | 61.7 ns: 1.57x slower                                                 |
| logging_silent             | 98.2 ns                                                                | 465 ns: 4.73x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                                | 98.3 ms: 8.93x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.38x faster                                                          |

Benchmark hidden because not significant (4): sympy_sum, asyncio_tcp, asyncio_websockets, pickle_dict
Ignored benchmarks (11) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, regex_compile, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20250601-3.15.0a0-cebae97-JIT/bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.537x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.15x