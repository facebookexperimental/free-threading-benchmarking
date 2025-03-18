# Results vs. 3.13.0rc2

- fork: mpage
- ref: load_fast_borrow_abs
- machine: linux-x86_64
- commit hash: 6c2f07d
- commit date: 2025-03-17
- overall geometric mean: 1.056x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6+-6c2f07d |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 249 ms: 1.04x faster                                                  |
| docutils       | 2.63 sec                                                               | 2.58 sec: 1.02x faster                                                |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6+-6c2f07d |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 615 ms: 1.46x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 322 ms: 1.43x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 618 ms: 1.43x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 503 ms: 1.32x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 270 ms: 1.31x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 314 ms: 1.30x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 257 ms: 1.29x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 491 ms: 1.29x faster                                                  |
| async_generators           | 375 ms                                                                 | 331 ms: 1.13x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 22.8 ms: 1.02x faster                                                 |
| Geometric mean             | (ref)                                                                  | 1.26x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6+-6c2f07d |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 76.7 ms                                                                | 69.3 ms: 1.11x faster                                                 |
| nbody          | 85.3 ms                                                                | 84.2 ms: 1.01x faster                                                 |
| pidigits       | 216 ms                                                                 | 220 ms: 1.01x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6+-6c2f07d |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.68 ms: 1.20x faster                                                 |
| regex_dna      | 189 ms                                                                 | 167 ms: 1.13x faster                                                  |
| regex_compile  | 131 ms                                                                 | 124 ms: 1.06x faster                                                  |
| regex_v8       | 23.2 ms                                                                | 24.2 ms: 1.04x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.08x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6+-6c2f07d |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                               | 1.91 sec: 1.05x faster                                                |
| xml_etree_parse      | 136 ms                                                                 | 130 ms: 1.05x faster                                                  |
| xml_etree_iterparse  | 94.4 ms                                                                | 91.2 ms: 1.04x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                                | 83.7 ms: 1.02x faster                                                 |
| unpickle_pure_python | 208 us                                                                 | 215 us: 1.03x slower                                                  |
| json_dumps           | 10.6 ms                                                                | 11.0 ms: 1.04x slower                                                 |
| pickle_pure_python   | 292 us                                                                 | 305 us: 1.05x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (2): xml_etree_process, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6+-6c2f07d |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 8.63 ms: 1.16x slower                                                 |
| python_startup         | 11.0 ms                                                                | 15.0 ms: 1.36x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.26x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6+-6c2f07d |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 21.7 ms                                                                | 20.3 ms: 1.07x faster                                                 |
| genshi_xml      | 49.1 ms                                                                | 47.6 ms: 1.03x faster                                                 |
| django_template | 34.2 ms                                                                | 35.9 ms: 1.05x slower                                                 |
| mako            | 11.2 ms                                                                | 12.0 ms: 1.07x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.01x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6+-6c2f07d |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 615 ms: 1.46x faster                                                  |
| deepcopy                   | 357 us                                                                 | 247 us: 1.45x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 322 ms: 1.43x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 618 ms: 1.43x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 28.6 us: 1.33x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 503 ms: 1.32x faster                                                  |
| go                         | 141 ms                                                                 | 107 ms: 1.32x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 270 ms: 1.31x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 314 ms: 1.30x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 257 ms: 1.29x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 491 ms: 1.29x faster                                                  |
| scimark_sor                | 134 ms                                                                 | 106 ms: 1.26x faster                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 2.55 us: 1.22x faster                                                 |
| regex_effbot               | 3.21 ms                                                                | 2.68 ms: 1.20x faster                                                 |
| spectral_norm              | 108 ms                                                                 | 94.6 ms: 1.14x faster                                                 |
| pylint                     | 317 ms                                                                 | 280 ms: 1.13x faster                                                  |
| async_generators           | 375 ms                                                                 | 331 ms: 1.13x faster                                                  |
| regex_dna                  | 189 ms                                                                 | 167 ms: 1.13x faster                                                  |
| pyflate                    | 449 ms                                                                 | 404 ms: 1.11x faster                                                  |
| scimark_fft                | 348 ms                                                                 | 314 ms: 1.11x faster                                                  |
| float                      | 76.7 ms                                                                | 69.3 ms: 1.11x faster                                                 |
| dulwich_log                | 74.5 ms                                                                | 67.3 ms: 1.11x faster                                                 |
| richards                   | 44.4 ms                                                                | 40.4 ms: 1.10x faster                                                 |
| richards_super             | 50.4 ms                                                                | 46.4 ms: 1.09x faster                                                 |
| scimark_monte_carlo        | 65.8 ms                                                                | 60.6 ms: 1.09x faster                                                 |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.39 ms: 1.08x faster                                                 |
| genshi_text                | 21.7 ms                                                                | 20.3 ms: 1.07x faster                                                 |
| telco                      | 7.77 ms                                                                | 7.32 ms: 1.06x faster                                                 |
| thrift                     | 772 us                                                                 | 728 us: 1.06x faster                                                  |
| regex_compile              | 131 ms                                                                 | 124 ms: 1.06x faster                                                  |
| tomli_loads                | 2.01 sec                                                               | 1.91 sec: 1.05x faster                                                |
| xml_etree_parse            | 136 ms                                                                 | 130 ms: 1.05x faster                                                  |
| sqlglot_normalize          | 106 ms                                                                 | 101 ms: 1.04x faster                                                  |
| logging_format             | 6.92 us                                                                | 6.64 us: 1.04x faster                                                 |
| 2to3                       | 259 ms                                                                 | 249 ms: 1.04x faster                                                  |
| bpe_tokeniser              | 4.46 sec                                                               | 4.28 sec: 1.04x faster                                                |
| logging_silent             | 98.2 ns                                                                | 94.5 ns: 1.04x faster                                                 |
| sqlglot_optimize           | 52.7 ms                                                                | 50.8 ms: 1.04x faster                                                 |
| xml_etree_iterparse        | 94.4 ms                                                                | 91.2 ms: 1.04x faster                                                 |
| sqlite_synth               | 2.25 us                                                                | 2.18 us: 1.03x faster                                                 |
| generators                 | 28.5 ms                                                                | 27.7 ms: 1.03x faster                                                 |
| genshi_xml                 | 49.1 ms                                                                | 47.6 ms: 1.03x faster                                                 |
| pprint_safe_repr           | 719 ms                                                                 | 697 ms: 1.03x faster                                                  |
| logging_simple             | 6.14 us                                                                | 5.97 us: 1.03x faster                                                 |
| json                       | 4.98 ms                                                                | 4.84 ms: 1.03x faster                                                 |
| sqlglot_transpile          | 1.55 ms                                                                | 1.51 ms: 1.03x faster                                                 |
| sqlglot_parse              | 1.25 ms                                                                | 1.22 ms: 1.03x faster                                                 |
| pprint_pformat             | 1.46 sec                                                               | 1.42 sec: 1.02x faster                                                |
| chaos                      | 56.3 ms                                                                | 55.0 ms: 1.02x faster                                                 |
| hexiom                     | 5.95 ms                                                                | 5.82 ms: 1.02x faster                                                 |
| coroutines                 | 23.3 ms                                                                | 22.8 ms: 1.02x faster                                                 |
| xml_etree_generate         | 85.4 ms                                                                | 83.7 ms: 1.02x faster                                                 |
| docutils                   | 2.63 sec                                                               | 2.58 sec: 1.02x faster                                                |
| pycparser                  | 1.12 sec                                                               | 1.10 sec: 1.01x faster                                                |
| nbody                      | 85.3 ms                                                                | 84.2 ms: 1.01x faster                                                 |
| scimark_lu                 | 112 ms                                                                 | 111 ms: 1.01x faster                                                  |
| sympy_str                  | 274 ms                                                                 | 272 ms: 1.01x faster                                                  |
| fannkuch                   | 376 ms                                                                 | 380 ms: 1.01x slower                                                  |
| nqueens                    | 77.7 ms                                                                | 78.8 ms: 1.01x slower                                                 |
| pidigits                   | 216 ms                                                                 | 220 ms: 1.01x slower                                                  |
| sympy_expand               | 454 ms                                                                 | 462 ms: 1.02x slower                                                  |
| crypto_pyaes               | 68.2 ms                                                                | 69.8 ms: 1.02x slower                                                 |
| unpickle_pure_python       | 208 us                                                                 | 215 us: 1.03x slower                                                  |
| mdp                        | 2.34 sec                                                               | 2.42 sec: 1.03x slower                                                |
| json_dumps                 | 10.6 ms                                                                | 11.0 ms: 1.04x slower                                                 |
| deltablue                  | 3.10 ms                                                                | 3.21 ms: 1.04x slower                                                 |
| regex_v8                   | 23.2 ms                                                                | 24.2 ms: 1.04x slower                                                 |
| pickle_pure_python         | 292 us                                                                 | 305 us: 1.05x slower                                                  |
| django_template            | 34.2 ms                                                                | 35.9 ms: 1.05x slower                                                 |
| mako                       | 11.2 ms                                                                | 12.0 ms: 1.07x slower                                                 |
| bench_thread_pool          | 924 us                                                                 | 1.04 ms: 1.12x slower                                                 |
| python_startup_no_site     | 7.41 ms                                                                | 8.63 ms: 1.16x slower                                                 |
| gc_traversal               | 3.32 ms                                                                | 4.21 ms: 1.27x slower                                                 |
| python_startup             | 11.0 ms                                                                | 15.0 ms: 1.36x slower                                                 |
| create_gc_cycles           | 1.33 ms                                                                | 1.82 ms: 1.37x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                                | 87.9 ms: 7.99x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.03x faster                                                          |

Benchmark hidden because not significant (11): meteor_contest, coverage, sympy_sum, asyncio_websockets, comprehensions, raytrace, sympy_integrate, xml_etree_process, pathlib, json_loads, typing_runtime_protocols
Ignored benchmarks (15) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250317-3.14.0a6+-6c2f07d/bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6+-6c2f07d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.056x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.11x