# Results vs. 3.13.0rc2

- fork: python
- ref: cebae977a63f32c3c03d
- machine: linux-x86_64
- commit hash: cebae97
- commit date: 2025-06-01
- overall geometric mean: 1.114x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 244 ms: 1.06x faster                                                  |
| docutils       | 2.63 sec                                                               | 2.51 sec: 1.05x faster                                                |
| html5lib       | 68.6 ms                                                                | 57.7 ms: 1.19x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.10x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io              | 881 ms                                                                 | 576 ms: 1.53x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 301 ms: 1.52x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 600 ms: 1.50x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 479 ms: 1.39x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 244 ms: 1.37x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 300 ms: 1.37x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 260 ms: 1.36x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 472 ms: 1.34x faster                                                  |
| async_generators           | 375 ms                                                                 | 315 ms: 1.19x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 22.2 ms: 1.05x faster                                                 |
| asyncio_tcp                | 502 ms                                                                 | 494 ms: 1.02x faster                                                  |
| asyncio_tcp_ssl            | 1.51 sec                                                               | 1.51 sec: 1.00x faster                                                |
| Geometric mean             | (ref)                                                                  | 1.26x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 76.7 ms                                                                | 67.6 ms: 1.14x faster                                                 |
| pidigits       | 216 ms                                                                 | 192 ms: 1.13x faster                                                  |
| nbody          | 85.3 ms                                                                | 79.6 ms: 1.07x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.11x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 131 ms                                                                 | 120 ms: 1.10x faster                                                  |
| regex_effbot   | 3.21 ms                                                                | 3.14 ms: 1.02x faster                                                 |
| regex_dna      | 189 ms                                                                 | 189 ms: 1.00x slower                                                  |
| regex_v8       | 23.2 ms                                                                | 23.4 ms: 1.01x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                               | 1.82 sec: 1.11x faster                                                |
| unpickle             | 14.6 us                                                                | 13.2 us: 1.11x faster                                                 |
| json_loads           | 27.3 us                                                                | 25.0 us: 1.09x faster                                                 |
| unpickle_list        | 4.60 us                                                                | 4.25 us: 1.08x faster                                                 |
| pickle_dict          | 32.7 us                                                                | 30.5 us: 1.07x faster                                                 |
| unpickle_pure_python | 208 us                                                                 | 199 us: 1.05x faster                                                  |
| xml_etree_generate   | 85.4 ms                                                                | 81.4 ms: 1.05x faster                                                 |
| xml_etree_process    | 59.2 ms                                                                | 56.5 ms: 1.05x faster                                                 |
| pickle_list          | 4.81 us                                                                | 4.70 us: 1.02x faster                                                 |
| xml_etree_iterparse  | 94.4 ms                                                                | 94.9 ms: 1.01x slower                                                 |
| pickle_pure_python   | 292 us                                                                 | 294 us: 1.01x slower                                                  |
| json_dumps           | 10.6 ms                                                                | 10.8 ms: 1.02x slower                                                 |
| xml_etree_parse      | 136 ms                                                                 | 146 ms: 1.07x slower                                                  |
| pickle               | 11.4 us                                                                | 12.7 us: 1.11x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.03x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 7.39 ms: 1.00x faster                                                 |
| python_startup         | 11.0 ms                                                                | 12.5 ms: 1.13x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.06x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 21.7 ms                                                                | 19.3 ms: 1.13x faster                                                 |
| genshi_xml      | 49.1 ms                                                                | 45.7 ms: 1.07x faster                                                 |
| django_template | 34.2 ms                                                                | 32.8 ms: 1.04x faster                                                 |
| Geometric mean  | (ref)                                                                  | 1.06x faster                                                          |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.34 sec                                                               | 1.08 sec: 2.16x faster                                                |
| deepcopy                   | 357 us                                                                 | 231 us: 1.55x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 576 ms: 1.53x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 301 ms: 1.52x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 600 ms: 1.50x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 26.1 us: 1.46x faster                                                 |
| go                         | 141 ms                                                                 | 96.7 ms: 1.45x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 479 ms: 1.39x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 244 ms: 1.37x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 300 ms: 1.37x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 260 ms: 1.36x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 472 ms: 1.34x faster                                                  |
| scimark_sor                | 134 ms                                                                 | 100 ms: 1.33x faster                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 2.41 us: 1.30x faster                                                 |
| scimark_fft                | 348 ms                                                                 | 275 ms: 1.27x faster                                                  |
| spectral_norm              | 108 ms                                                                 | 86.1 ms: 1.25x faster                                                 |
| richards                   | 44.4 ms                                                                | 36.8 ms: 1.21x faster                                                 |
| comprehensions             | 16.6 us                                                                | 13.9 us: 1.20x faster                                                 |
| scimark_monte_carlo        | 65.8 ms                                                                | 55.1 ms: 1.19x faster                                                 |
| async_generators           | 375 ms                                                                 | 315 ms: 1.19x faster                                                  |
| html5lib                   | 68.6 ms                                                                | 57.7 ms: 1.19x faster                                                 |
| richards_super             | 50.4 ms                                                                | 42.8 ms: 1.18x faster                                                 |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.05 ms: 1.17x faster                                                 |
| pylint                     | 317 ms                                                                 | 273 ms: 1.16x faster                                                  |
| telco                      | 7.77 ms                                                                | 6.75 ms: 1.15x faster                                                 |
| pyflate                    | 449 ms                                                                 | 391 ms: 1.15x faster                                                  |
| hexiom                     | 5.95 ms                                                                | 5.21 ms: 1.14x faster                                                 |
| chaos                      | 56.3 ms                                                                | 49.5 ms: 1.14x faster                                                 |
| float                      | 76.7 ms                                                                | 67.6 ms: 1.14x faster                                                 |
| dulwich_log                | 74.5 ms                                                                | 65.7 ms: 1.13x faster                                                 |
| genshi_text                | 21.7 ms                                                                | 19.3 ms: 1.13x faster                                                 |
| pidigits                   | 216 ms                                                                 | 192 ms: 1.13x faster                                                  |
| scimark_lu                 | 112 ms                                                                 | 100 ms: 1.12x faster                                                  |
| bpe_tokeniser              | 4.46 sec                                                               | 3.98 sec: 1.12x faster                                                |
| tomli_loads                | 2.01 sec                                                               | 1.82 sec: 1.11x faster                                                |
| unpickle                   | 14.6 us                                                                | 13.2 us: 1.11x faster                                                 |
| regex_compile              | 131 ms                                                                 | 120 ms: 1.10x faster                                                  |
| json_loads                 | 27.3 us                                                                | 25.0 us: 1.09x faster                                                 |
| sympy_integrate            | 19.7 ms                                                                | 18.1 ms: 1.09x faster                                                 |
| unpickle_list              | 4.60 us                                                                | 4.25 us: 1.08x faster                                                 |
| coverage                   | 82.5 ms                                                                | 76.2 ms: 1.08x faster                                                 |
| typing_runtime_protocols   | 156 us                                                                 | 144 us: 1.08x faster                                                  |
| raytrace                   | 250 ms                                                                 | 231 ms: 1.08x faster                                                  |
| genshi_xml                 | 49.1 ms                                                                | 45.7 ms: 1.07x faster                                                 |
| pickle_dict                | 32.7 us                                                                | 30.5 us: 1.07x faster                                                 |
| deltablue                  | 3.10 ms                                                                | 2.89 ms: 1.07x faster                                                 |
| nbody                      | 85.3 ms                                                                | 79.6 ms: 1.07x faster                                                 |
| 2to3                       | 259 ms                                                                 | 244 ms: 1.06x faster                                                  |
| sympy_str                  | 274 ms                                                                 | 258 ms: 1.06x faster                                                  |
| thrift                     | 772 us                                                                 | 728 us: 1.06x faster                                                  |
| unpickle_pure_python       | 208 us                                                                 | 199 us: 1.05x faster                                                  |
| xml_etree_generate         | 85.4 ms                                                                | 81.4 ms: 1.05x faster                                                 |
| coroutines                 | 23.3 ms                                                                | 22.2 ms: 1.05x faster                                                 |
| xml_etree_process          | 59.2 ms                                                                | 56.5 ms: 1.05x faster                                                 |
| nqueens                    | 77.7 ms                                                                | 74.2 ms: 1.05x faster                                                 |
| docutils                   | 2.63 sec                                                               | 2.51 sec: 1.05x faster                                                |
| sympy_expand               | 454 ms                                                                 | 434 ms: 1.05x faster                                                  |
| sympy_sum                  | 154 ms                                                                 | 148 ms: 1.04x faster                                                  |
| django_template            | 34.2 ms                                                                | 32.8 ms: 1.04x faster                                                 |
| pathlib                    | 19.3 ms                                                                | 18.5 ms: 1.04x faster                                                 |
| generators                 | 28.5 ms                                                                | 27.8 ms: 1.03x faster                                                 |
| fannkuch                   | 376 ms                                                                 | 367 ms: 1.02x faster                                                  |
| pickle_list                | 4.81 us                                                                | 4.70 us: 1.02x faster                                                 |
| regex_effbot               | 3.21 ms                                                                | 3.14 ms: 1.02x faster                                                 |
| crypto_pyaes               | 68.2 ms                                                                | 66.9 ms: 1.02x faster                                                 |
| sqlite_synth               | 2.25 us                                                                | 2.21 us: 1.02x faster                                                 |
| asyncio_tcp                | 502 ms                                                                 | 494 ms: 1.02x faster                                                  |
| json                       | 4.98 ms                                                                | 4.92 ms: 1.01x faster                                                 |
| asyncio_tcp_ssl            | 1.51 sec                                                               | 1.51 sec: 1.00x faster                                                |
| python_startup_no_site     | 7.41 ms                                                                | 7.39 ms: 1.00x faster                                                 |
| regex_dna                  | 189 ms                                                                 | 189 ms: 1.00x slower                                                  |
| xml_etree_iterparse        | 94.4 ms                                                                | 94.9 ms: 1.01x slower                                                 |
| meteor_contest             | 101 ms                                                                 | 102 ms: 1.01x slower                                                  |
| pickle_pure_python         | 292 us                                                                 | 294 us: 1.01x slower                                                  |
| regex_v8                   | 23.2 ms                                                                | 23.4 ms: 1.01x slower                                                 |
| logging_simple             | 6.14 us                                                                | 6.24 us: 1.02x slower                                                 |
| json_dumps                 | 10.6 ms                                                                | 10.8 ms: 1.02x slower                                                 |
| logging_format             | 6.92 us                                                                | 7.12 us: 1.03x slower                                                 |
| pprint_safe_repr           | 719 ms                                                                 | 760 ms: 1.06x slower                                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.55 sec: 1.07x slower                                                |
| xml_etree_parse            | 136 ms                                                                 | 146 ms: 1.07x slower                                                  |
| bench_thread_pool          | 924 us                                                                 | 1.01 ms: 1.09x slower                                                 |
| pickle                     | 11.4 us                                                                | 12.7 us: 1.11x slower                                                 |
| python_startup             | 11.0 ms                                                                | 12.5 ms: 1.13x slower                                                 |
| unpack_sequence            | 39.3 ns                                                                | 47.9 ns: 1.22x slower                                                 |
| gc_traversal               | 3.32 ms                                                                | 4.38 ms: 1.32x slower                                                 |
| create_gc_cycles           | 1.33 ms                                                                | 1.99 ms: 1.49x slower                                                 |
| logging_silent             | 98.2 ns                                                                | 476 ns: 4.85x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                                | 97.3 ms: 8.85x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.06x faster                                                          |

Benchmark hidden because not significant (3): pycparser, asyncio_websockets, mako
Ignored benchmarks (10) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20250601-3.15.0a0-cebae97-CLANG/bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.114x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.18x