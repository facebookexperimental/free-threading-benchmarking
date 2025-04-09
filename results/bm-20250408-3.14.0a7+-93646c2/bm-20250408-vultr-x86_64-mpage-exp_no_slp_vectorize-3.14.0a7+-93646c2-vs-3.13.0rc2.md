# Results vs. 3.13.0rc2

- fork: mpage
- ref: exp_no_slp_vectorize
- machine: linux-x86_64
- commit hash: 93646c2
- commit date: 2025-04-08
- overall geometric mean: 1.078x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a7+-93646c2 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 245 ms: 1.06x faster                                                  |
| docutils       | 2.63 sec                                                               | 2.52 sec: 1.04x faster                                                |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a7+-93646c2 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization     | 459 ms                                                                 | 309 ms: 1.49x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 608 ms: 1.48x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 613 ms: 1.44x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 494 ms: 1.35x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 271 ms: 1.30x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 315 ms: 1.30x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 256 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 491 ms: 1.29x faster                                                  |
| async_generators           | 375 ms                                                                 | 323 ms: 1.16x faster                                                  |
| Geometric mean             | (ref)                                                                  | 1.27x faster                                                          |

Benchmark hidden because not significant (2): coroutines, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a7+-93646c2 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 76.7 ms                                                                | 68.3 ms: 1.12x faster                                                 |
| pidigits       | 216 ms                                                                 | 199 ms: 1.09x faster                                                  |
| nbody          | 85.3 ms                                                                | 82.0 ms: 1.04x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.08x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a7+-93646c2 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.80 ms: 1.15x faster                                                 |
| regex_v8       | 23.2 ms                                                                | 21.4 ms: 1.08x faster                                                 |
| regex_dna      | 189 ms                                                                 | 174 ms: 1.08x faster                                                  |
| regex_compile  | 131 ms                                                                 | 123 ms: 1.07x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.09x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a7+-93646c2 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                               | 1.86 sec: 1.08x faster                                                |
| xml_etree_parse      | 136 ms                                                                 | 128 ms: 1.06x faster                                                  |
| xml_etree_iterparse  | 94.4 ms                                                                | 91.9 ms: 1.03x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                                | 83.3 ms: 1.03x faster                                                 |
| xml_etree_process    | 59.2 ms                                                                | 58.7 ms: 1.01x faster                                                 |
| unpickle_pure_python | 208 us                                                                 | 209 us: 1.00x slower                                                  |
| pickle_pure_python   | 292 us                                                                 | 301 us: 1.03x slower                                                  |
| json_loads           | 27.3 us                                                                | 28.4 us: 1.04x slower                                                 |
| json_dumps           | 10.6 ms                                                                | 11.2 ms: 1.05x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a7+-93646c2 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 8.62 ms: 1.16x slower                                                 |
| python_startup         | 11.0 ms                                                                | 15.0 ms: 1.36x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.26x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a7+-93646c2 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 21.7 ms                                                                | 20.6 ms: 1.06x faster                                                 |
| genshi_xml      | 49.1 ms                                                                | 47.7 ms: 1.03x faster                                                 |
| mako            | 11.2 ms                                                                | 11.8 ms: 1.05x slower                                                 |
| django_template | 34.2 ms                                                                | 35.9 ms: 1.05x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.00x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a7+-93646c2 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.34 sec                                                               | 1.13 sec: 2.07x faster                                                |
| async_tree_memoization     | 459 ms                                                                 | 309 ms: 1.49x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 608 ms: 1.48x faster                                                  |
| deepcopy                   | 357 us                                                                 | 248 us: 1.44x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 613 ms: 1.44x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 494 ms: 1.35x faster                                                  |
| go                         | 141 ms                                                                 | 105 ms: 1.33x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 29.0 us: 1.31x faster                                                 |
| async_tree_none            | 353 ms                                                                 | 271 ms: 1.30x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 315 ms: 1.30x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 256 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 491 ms: 1.29x faster                                                  |
| scimark_sor                | 134 ms                                                                 | 108 ms: 1.24x faster                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 2.60 us: 1.20x faster                                                 |
| spectral_norm              | 108 ms                                                                 | 91.9 ms: 1.17x faster                                                 |
| async_generators           | 375 ms                                                                 | 323 ms: 1.16x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.80 ms: 1.15x faster                                                 |
| pylint                     | 317 ms                                                                 | 278 ms: 1.14x faster                                                  |
| float                      | 76.7 ms                                                                | 68.3 ms: 1.12x faster                                                 |
| pyflate                    | 449 ms                                                                 | 400 ms: 1.12x faster                                                  |
| dulwich_log                | 74.5 ms                                                                | 66.8 ms: 1.11x faster                                                 |
| scimark_fft                | 348 ms                                                                 | 314 ms: 1.11x faster                                                  |
| richards                   | 44.4 ms                                                                | 40.3 ms: 1.10x faster                                                 |
| scimark_monte_carlo        | 65.8 ms                                                                | 59.9 ms: 1.10x faster                                                 |
| richards_super             | 50.4 ms                                                                | 46.2 ms: 1.09x faster                                                 |
| telco                      | 7.77 ms                                                                | 7.13 ms: 1.09x faster                                                 |
| pidigits                   | 216 ms                                                                 | 199 ms: 1.09x faster                                                  |
| regex_v8                   | 23.2 ms                                                                | 21.4 ms: 1.08x faster                                                 |
| regex_dna                  | 189 ms                                                                 | 174 ms: 1.08x faster                                                  |
| tomli_loads                | 2.01 sec                                                               | 1.86 sec: 1.08x faster                                                |
| chaos                      | 56.3 ms                                                                | 52.5 ms: 1.07x faster                                                 |
| regex_compile              | 131 ms                                                                 | 123 ms: 1.07x faster                                                  |
| hexiom                     | 5.95 ms                                                                | 5.60 ms: 1.06x faster                                                 |
| xml_etree_parse            | 136 ms                                                                 | 128 ms: 1.06x faster                                                  |
| 2to3                       | 259 ms                                                                 | 245 ms: 1.06x faster                                                  |
| bpe_tokeniser              | 4.46 sec                                                               | 4.21 sec: 1.06x faster                                                |
| logging_silent             | 98.2 ns                                                                | 92.8 ns: 1.06x faster                                                 |
| genshi_text                | 21.7 ms                                                                | 20.6 ms: 1.06x faster                                                 |
| logging_format             | 6.92 us                                                                | 6.54 us: 1.06x faster                                                 |
| generators                 | 28.5 ms                                                                | 27.1 ms: 1.05x faster                                                 |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.53 ms: 1.05x faster                                                 |
| logging_simple             | 6.14 us                                                                | 5.88 us: 1.05x faster                                                 |
| docutils                   | 2.63 sec                                                               | 2.52 sec: 1.04x faster                                                |
| sympy_integrate            | 19.7 ms                                                                | 18.9 ms: 1.04x faster                                                 |
| sqlite_synth               | 2.25 us                                                                | 2.16 us: 1.04x faster                                                 |
| nbody                      | 85.3 ms                                                                | 82.0 ms: 1.04x faster                                                 |
| meteor_contest             | 101 ms                                                                 | 98.3 ms: 1.03x faster                                                 |
| pycparser                  | 1.12 sec                                                               | 1.09 sec: 1.03x faster                                                |
| nqueens                    | 77.7 ms                                                                | 75.5 ms: 1.03x faster                                                 |
| genshi_xml                 | 49.1 ms                                                                | 47.7 ms: 1.03x faster                                                 |
| xml_etree_iterparse        | 94.4 ms                                                                | 91.9 ms: 1.03x faster                                                 |
| raytrace                   | 250 ms                                                                 | 243 ms: 1.03x faster                                                  |
| xml_etree_generate         | 85.4 ms                                                                | 83.3 ms: 1.03x faster                                                 |
| coverage                   | 82.5 ms                                                                | 80.6 ms: 1.02x faster                                                 |
| crypto_pyaes               | 68.2 ms                                                                | 66.7 ms: 1.02x faster                                                 |
| pprint_pformat             | 1.46 sec                                                               | 1.43 sec: 1.02x faster                                                |
| pprint_safe_repr           | 719 ms                                                                 | 705 ms: 1.02x faster                                                  |
| pathlib                    | 19.3 ms                                                                | 19.0 ms: 1.02x faster                                                 |
| comprehensions             | 16.6 us                                                                | 16.3 us: 1.01x faster                                                 |
| sympy_str                  | 274 ms                                                                 | 271 ms: 1.01x faster                                                  |
| typing_runtime_protocols   | 156 us                                                                 | 154 us: 1.01x faster                                                  |
| xml_etree_process          | 59.2 ms                                                                | 58.7 ms: 1.01x faster                                                 |
| fannkuch                   | 376 ms                                                                 | 373 ms: 1.01x faster                                                  |
| unpickle_pure_python       | 208 us                                                                 | 209 us: 1.00x slower                                                  |
| sympy_sum                  | 154 ms                                                                 | 155 ms: 1.00x slower                                                  |
| sympy_expand               | 454 ms                                                                 | 460 ms: 1.01x slower                                                  |
| deltablue                  | 3.10 ms                                                                | 3.16 ms: 1.02x slower                                                 |
| json                       | 4.98 ms                                                                | 5.10 ms: 1.02x slower                                                 |
| pickle_pure_python         | 292 us                                                                 | 301 us: 1.03x slower                                                  |
| json_loads                 | 27.3 us                                                                | 28.4 us: 1.04x slower                                                 |
| mako                       | 11.2 ms                                                                | 11.8 ms: 1.05x slower                                                 |
| django_template            | 34.2 ms                                                                | 35.9 ms: 1.05x slower                                                 |
| json_dumps                 | 10.6 ms                                                                | 11.2 ms: 1.05x slower                                                 |
| bench_thread_pool          | 924 us                                                                 | 1.05 ms: 1.13x slower                                                 |
| python_startup_no_site     | 7.41 ms                                                                | 8.62 ms: 1.16x slower                                                 |
| gc_traversal               | 3.32 ms                                                                | 4.24 ms: 1.28x slower                                                 |
| python_startup             | 11.0 ms                                                                | 15.0 ms: 1.36x slower                                                 |
| create_gc_cycles           | 1.33 ms                                                                | 1.86 ms: 1.40x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                                | 88.4 ms: 8.03x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.05x faster                                                          |

Benchmark hidden because not significant (3): coroutines, asyncio_websockets, scimark_lu
Ignored benchmarks (20) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250408-3.14.0a7+-93646c2/bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a7+-93646c2.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.078x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.13x