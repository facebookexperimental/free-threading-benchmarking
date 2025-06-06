# Results vs. 3.13.0rc2

- fork: mpage
- ref: exp_no_slp_vectorize
- machine: linux-x86_64
- commit hash: 93646c2
- commit date: 2025-04-08
- overall geometric mean: 1.003x slower
- HPT reliability: 92.87%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a7+-93646c2 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 280 ms: 1.08x slower                                                  |
| docutils       | 2.63 sec                                                               | 2.71 sec: 1.03x slower                                                |
| html5lib       | 68.6 ms                                                                | 64.8 ms: 1.06x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a7+-93646c2 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 512 ms: 1.76x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 541 ms: 1.63x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 222 ms: 1.50x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 309 ms: 1.49x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 280 ms: 1.46x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 252 ms: 1.40x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 521 ms: 1.22x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 549 ms: 1.21x faster                                                  |
| async_generators           | 375 ms                                                                 | 354 ms: 1.06x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 22.3 ms: 1.05x faster                                                 |
| Geometric mean             | (ref)                                                                  | 1.32x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a7+-93646c2 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 76.7 ms                                                                | 67.2 ms: 1.14x faster                                                 |
| pidigits       | 216 ms                                                                 | 223 ms: 1.03x slower                                                  |
| nbody          | 85.3 ms                                                                | 107 ms: 1.26x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a7+-93646c2 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.86 ms: 1.12x faster                                                 |
| regex_v8       | 23.2 ms                                                                | 21.5 ms: 1.08x faster                                                 |
| regex_dna      | 189 ms                                                                 | 176 ms: 1.07x faster                                                  |
| regex_compile  | 131 ms                                                                 | 142 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a7+-93646c2 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 84.1 ms: 1.12x faster                                                 |
| xml_etree_parse      | 136 ms                                                                 | 126 ms: 1.07x faster                                                  |
| tomli_loads          | 2.01 sec                                                               | 2.08 sec: 1.03x slower                                                |
| xml_etree_generate   | 85.4 ms                                                                | 92.1 ms: 1.08x slower                                                 |
| unpickle_pure_python | 208 us                                                                 | 226 us: 1.08x slower                                                  |
| json_loads           | 27.3 us                                                                | 30.2 us: 1.11x slower                                                 |
| xml_etree_process    | 59.2 ms                                                                | 65.6 ms: 1.11x slower                                                 |
| pickle_pure_python   | 292 us                                                                 | 328 us: 1.13x slower                                                  |
| json_dumps           | 10.6 ms                                                                | 12.5 ms: 1.18x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.06x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a7+-93646c2 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 15.8 ms: 1.43x slower                                                 |
| python_startup_no_site | 7.41 ms                                                                | 11.1 ms: 1.50x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.47x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a7+-93646c2 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 54.3 ms: 1.11x slower                                                 |
| django_template | 34.2 ms                                                                | 39.8 ms: 1.16x slower                                                 |
| genshi_text     | 21.7 ms                                                                | 25.5 ms: 1.17x slower                                                 |
| mako            | 11.2 ms                                                                | 15.3 ms: 1.37x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.20x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a7+-93646c2 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.78 ms: 1.87x faster                                                 |
| mdp                        | 2.34 sec                                                               | 1.30 sec: 1.80x faster                                                |
| async_tree_io_tg           | 901 ms                                                                 | 512 ms: 1.76x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 541 ms: 1.63x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 222 ms: 1.50x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 309 ms: 1.49x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 280 ms: 1.46x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 252 ms: 1.40x faster                                                  |
| deepcopy                   | 357 us                                                                 | 289 us: 1.24x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 521 ms: 1.22x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 549 ms: 1.21x faster                                                  |
| float                      | 76.7 ms                                                                | 67.2 ms: 1.14x faster                                                 |
| go                         | 141 ms                                                                 | 124 ms: 1.14x faster                                                  |
| xml_etree_iterparse        | 94.4 ms                                                                | 84.1 ms: 1.12x faster                                                 |
| regex_effbot               | 3.21 ms                                                                | 2.86 ms: 1.12x faster                                                 |
| sqlite_synth               | 2.25 us                                                                | 2.01 us: 1.12x faster                                                 |
| scimark_sor                | 134 ms                                                                 | 119 ms: 1.12x faster                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 2.88 us: 1.08x faster                                                 |
| regex_v8                   | 23.2 ms                                                                | 21.5 ms: 1.08x faster                                                 |
| deepcopy_memo              | 38.1 us                                                                | 35.4 us: 1.08x faster                                                 |
| xml_etree_parse            | 136 ms                                                                 | 126 ms: 1.07x faster                                                  |
| regex_dna                  | 189 ms                                                                 | 176 ms: 1.07x faster                                                  |
| async_generators           | 375 ms                                                                 | 354 ms: 1.06x faster                                                  |
| html5lib                   | 68.6 ms                                                                | 64.8 ms: 1.06x faster                                                 |
| spectral_norm              | 108 ms                                                                 | 102 ms: 1.06x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 22.3 ms: 1.05x faster                                                 |
| dulwich_log                | 74.5 ms                                                                | 71.5 ms: 1.04x faster                                                 |
| scimark_fft                | 348 ms                                                                 | 343 ms: 1.02x faster                                                  |
| pathlib                    | 19.3 ms                                                                | 19.0 ms: 1.01x faster                                                 |
| bpe_tokeniser              | 4.46 sec                                                               | 4.47 sec: 1.00x slower                                                |
| pycparser                  | 1.12 sec                                                               | 1.13 sec: 1.01x slower                                                |
| pyflate                    | 449 ms                                                                 | 458 ms: 1.02x slower                                                  |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.85 ms: 1.02x slower                                                 |
| pidigits                   | 216 ms                                                                 | 223 ms: 1.03x slower                                                  |
| docutils                   | 2.63 sec                                                               | 2.71 sec: 1.03x slower                                                |
| generators                 | 28.5 ms                                                                | 29.5 ms: 1.03x slower                                                 |
| tomli_loads                | 2.01 sec                                                               | 2.08 sec: 1.03x slower                                                |
| logging_silent             | 98.2 ns                                                                | 102 ns: 1.04x slower                                                  |
| json                       | 4.98 ms                                                                | 5.23 ms: 1.05x slower                                                 |
| pprint_safe_repr           | 719 ms                                                                 | 762 ms: 1.06x slower                                                  |
| telco                      | 7.77 ms                                                                | 8.25 ms: 1.06x slower                                                 |
| chaos                      | 56.3 ms                                                                | 60.1 ms: 1.07x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                                | 92.1 ms: 1.08x slower                                                 |
| 2to3                       | 259 ms                                                                 | 280 ms: 1.08x slower                                                  |
| regex_compile              | 131 ms                                                                 | 142 ms: 1.08x slower                                                  |
| nqueens                    | 77.7 ms                                                                | 84.2 ms: 1.08x slower                                                 |
| unpickle_pure_python       | 208 us                                                                 | 226 us: 1.08x slower                                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.58 sec: 1.09x slower                                                |
| json_loads                 | 27.3 us                                                                | 30.2 us: 1.11x slower                                                 |
| genshi_xml                 | 49.1 ms                                                                | 54.3 ms: 1.11x slower                                                 |
| xml_etree_process          | 59.2 ms                                                                | 65.6 ms: 1.11x slower                                                 |
| hexiom                     | 5.95 ms                                                                | 6.62 ms: 1.11x slower                                                 |
| scimark_monte_carlo        | 65.8 ms                                                                | 73.2 ms: 1.11x slower                                                 |
| scimark_lu                 | 112 ms                                                                 | 126 ms: 1.12x slower                                                  |
| pickle_pure_python         | 292 us                                                                 | 328 us: 1.13x slower                                                  |
| deltablue                  | 3.10 ms                                                                | 3.50 ms: 1.13x slower                                                 |
| sympy_integrate            | 19.7 ms                                                                | 22.3 ms: 1.13x slower                                                 |
| richards                   | 44.4 ms                                                                | 50.4 ms: 1.14x slower                                                 |
| raytrace                   | 250 ms                                                                 | 284 ms: 1.14x slower                                                  |
| richards_super             | 50.4 ms                                                                | 57.7 ms: 1.14x slower                                                 |
| logging_simple             | 6.14 us                                                                | 7.04 us: 1.15x slower                                                 |
| comprehensions             | 16.6 us                                                                | 19.0 us: 1.15x slower                                                 |
| sympy_expand               | 454 ms                                                                 | 522 ms: 1.15x slower                                                  |
| logging_format             | 6.92 us                                                                | 7.96 us: 1.15x slower                                                 |
| sympy_str                  | 274 ms                                                                 | 318 ms: 1.16x slower                                                  |
| django_template            | 34.2 ms                                                                | 39.8 ms: 1.16x slower                                                 |
| sympy_sum                  | 154 ms                                                                 | 180 ms: 1.17x slower                                                  |
| genshi_text                | 21.7 ms                                                                | 25.5 ms: 1.17x slower                                                 |
| json_dumps                 | 10.6 ms                                                                | 12.5 ms: 1.18x slower                                                 |
| fannkuch                   | 376 ms                                                                 | 444 ms: 1.18x slower                                                  |
| meteor_contest             | 101 ms                                                                 | 123 ms: 1.21x slower                                                  |
| typing_runtime_protocols   | 156 us                                                                 | 190 us: 1.22x slower                                                  |
| crypto_pyaes               | 68.2 ms                                                                | 83.5 ms: 1.22x slower                                                 |
| nbody                      | 85.3 ms                                                                | 107 ms: 1.26x slower                                                  |
| coverage                   | 82.5 ms                                                                | 109 ms: 1.32x slower                                                  |
| mako                       | 11.2 ms                                                                | 15.3 ms: 1.37x slower                                                 |
| python_startup             | 11.0 ms                                                                | 15.8 ms: 1.43x slower                                                 |
| python_startup_no_site     | 7.41 ms                                                                | 11.1 ms: 1.50x slower                                                 |
| bench_thread_pool          | 924 us                                                                 | 3.14 ms: 3.39x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                                | 95.0 ms: 8.64x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.04x slower                                                          |

Benchmark hidden because not significant (3): pylint, asyncio_websockets, create_gc_cycles
Ignored benchmarks (19) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250408-3.14.0a7+-93646c2-NOGIL/bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a7+-93646c2.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.003x slower

# HPT report

- Reliability score: 92.87% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.35x