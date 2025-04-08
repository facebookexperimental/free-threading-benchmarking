# Results vs. 3.13.0rc2

- fork: mpage
- ref: exp_no_slp_vectorize
- machine: linux-x86_64
- commit hash: 09d4621
- commit date: 2025-04-08
- overall geometric mean: 1.085x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 246 ms: 1.06x faster                                                  |
| docutils       | 2.63 sec                                                               | 2.50 sec: 1.05x faster                                                |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization     | 459 ms                                                                 | 307 ms: 1.50x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 609 ms: 1.48x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 612 ms: 1.44x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 493 ms: 1.35x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 268 ms: 1.32x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 314 ms: 1.31x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 255 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 490 ms: 1.29x faster                                                  |
| async_generators           | 375 ms                                                                 | 320 ms: 1.17x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 22.7 ms: 1.03x faster                                                 |
| Geometric mean             | (ref)                                                                  | 1.28x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 76.7 ms                                                                | 68.2 ms: 1.13x faster                                                 |
| pidigits       | 216 ms                                                                 | 195 ms: 1.11x faster                                                  |
| nbody          | 85.3 ms                                                                | 82.7 ms: 1.03x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.09x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.77 ms: 1.16x faster                                                 |
| regex_compile  | 131 ms                                                                 | 122 ms: 1.08x faster                                                  |
| regex_dna      | 189 ms                                                                 | 175 ms: 1.08x faster                                                  |
| regex_v8       | 23.2 ms                                                                | 21.8 ms: 1.07x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.09x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                               | 1.85 sec: 1.09x faster                                                |
| xml_etree_parse      | 136 ms                                                                 | 128 ms: 1.06x faster                                                  |
| xml_etree_iterparse  | 94.4 ms                                                                | 90.8 ms: 1.04x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                                | 82.7 ms: 1.03x faster                                                 |
| xml_etree_process    | 59.2 ms                                                                | 58.0 ms: 1.02x faster                                                 |
| unpickle_pure_python | 208 us                                                                 | 207 us: 1.01x faster                                                  |
| json_loads           | 27.3 us                                                                | 28.0 us: 1.02x slower                                                 |
| pickle_pure_python   | 292 us                                                                 | 300 us: 1.03x slower                                                  |
| json_dumps           | 10.6 ms                                                                | 11.1 ms: 1.04x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.02x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 8.64 ms: 1.16x slower                                                 |
| python_startup         | 11.0 ms                                                                | 15.1 ms: 1.37x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.26x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text    | 21.7 ms                                                                | 20.1 ms: 1.08x faster                                                 |
| genshi_xml     | 49.1 ms                                                                | 48.0 ms: 1.02x faster                                                 |
| mako           | 11.2 ms                                                                | 11.6 ms: 1.04x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.34 sec                                                               | 1.12 sec: 2.08x faster                                                |
| async_tree_memoization     | 459 ms                                                                 | 307 ms: 1.50x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 609 ms: 1.48x faster                                                  |
| deepcopy                   | 357 us                                                                 | 246 us: 1.45x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 612 ms: 1.44x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 28.1 us: 1.35x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 493 ms: 1.35x faster                                                  |
| go                         | 141 ms                                                                 | 106 ms: 1.33x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 268 ms: 1.32x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 314 ms: 1.31x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 255 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 490 ms: 1.29x faster                                                  |
| scimark_sor                | 134 ms                                                                 | 106 ms: 1.26x faster                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 2.57 us: 1.21x faster                                                 |
| async_generators           | 375 ms                                                                 | 320 ms: 1.17x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.77 ms: 1.16x faster                                                 |
| spectral_norm              | 108 ms                                                                 | 93.4 ms: 1.15x faster                                                 |
| pylint                     | 317 ms                                                                 | 277 ms: 1.14x faster                                                  |
| float                      | 76.7 ms                                                                | 68.2 ms: 1.13x faster                                                 |
| scimark_fft                | 348 ms                                                                 | 310 ms: 1.12x faster                                                  |
| telco                      | 7.77 ms                                                                | 6.97 ms: 1.12x faster                                                 |
| pyflate                    | 449 ms                                                                 | 403 ms: 1.12x faster                                                  |
| dulwich_log                | 74.5 ms                                                                | 66.9 ms: 1.11x faster                                                 |
| pidigits                   | 216 ms                                                                 | 195 ms: 1.11x faster                                                  |
| richards                   | 44.4 ms                                                                | 40.3 ms: 1.10x faster                                                 |
| richards_super             | 50.4 ms                                                                | 46.1 ms: 1.09x faster                                                 |
| tomli_loads                | 2.01 sec                                                               | 1.85 sec: 1.09x faster                                                |
| scimark_monte_carlo        | 65.8 ms                                                                | 60.6 ms: 1.09x faster                                                 |
| genshi_text                | 21.7 ms                                                                | 20.1 ms: 1.08x faster                                                 |
| regex_compile              | 131 ms                                                                 | 122 ms: 1.08x faster                                                  |
| regex_dna                  | 189 ms                                                                 | 175 ms: 1.08x faster                                                  |
| logging_format             | 6.92 us                                                                | 6.44 us: 1.07x faster                                                 |
| chaos                      | 56.3 ms                                                                | 52.7 ms: 1.07x faster                                                 |
| generators                 | 28.5 ms                                                                | 26.7 ms: 1.07x faster                                                 |
| regex_v8                   | 23.2 ms                                                                | 21.8 ms: 1.07x faster                                                 |
| xml_etree_parse            | 136 ms                                                                 | 128 ms: 1.06x faster                                                  |
| bpe_tokeniser              | 4.46 sec                                                               | 4.20 sec: 1.06x faster                                                |
| 2to3                       | 259 ms                                                                 | 246 ms: 1.06x faster                                                  |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.51 ms: 1.05x faster                                                 |
| logging_simple             | 6.14 us                                                                | 5.84 us: 1.05x faster                                                 |
| hexiom                     | 5.95 ms                                                                | 5.66 ms: 1.05x faster                                                 |
| docutils                   | 2.63 sec                                                               | 2.50 sec: 1.05x faster                                                |
| sympy_integrate            | 19.7 ms                                                                | 18.8 ms: 1.05x faster                                                 |
| pprint_safe_repr           | 719 ms                                                                 | 688 ms: 1.04x faster                                                  |
| logging_silent             | 98.2 ns                                                                | 94.2 ns: 1.04x faster                                                 |
| coverage                   | 82.5 ms                                                                | 79.2 ms: 1.04x faster                                                 |
| xml_etree_iterparse        | 94.4 ms                                                                | 90.8 ms: 1.04x faster                                                 |
| meteor_contest             | 101 ms                                                                 | 97.6 ms: 1.04x faster                                                 |
| scimark_lu                 | 112 ms                                                                 | 108 ms: 1.04x faster                                                  |
| sqlite_synth               | 2.25 us                                                                | 2.17 us: 1.04x faster                                                 |
| xml_etree_generate         | 85.4 ms                                                                | 82.7 ms: 1.03x faster                                                 |
| nqueens                    | 77.7 ms                                                                | 75.3 ms: 1.03x faster                                                 |
| nbody                      | 85.3 ms                                                                | 82.7 ms: 1.03x faster                                                 |
| coroutines                 | 23.3 ms                                                                | 22.7 ms: 1.03x faster                                                 |
| raytrace                   | 250 ms                                                                 | 244 ms: 1.03x faster                                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.42 sec: 1.03x faster                                                |
| comprehensions             | 16.6 us                                                                | 16.2 us: 1.02x faster                                                 |
| pycparser                  | 1.12 sec                                                               | 1.10 sec: 1.02x faster                                                |
| xml_etree_process          | 59.2 ms                                                                | 58.0 ms: 1.02x faster                                                 |
| genshi_xml                 | 49.1 ms                                                                | 48.0 ms: 1.02x faster                                                 |
| crypto_pyaes               | 68.2 ms                                                                | 67.1 ms: 1.02x faster                                                 |
| sympy_str                  | 274 ms                                                                 | 270 ms: 1.02x faster                                                  |
| sympy_sum                  | 154 ms                                                                 | 152 ms: 1.01x faster                                                  |
| fannkuch                   | 376 ms                                                                 | 372 ms: 1.01x faster                                                  |
| unpickle_pure_python       | 208 us                                                                 | 207 us: 1.01x faster                                                  |
| pathlib                    | 19.3 ms                                                                | 19.5 ms: 1.01x slower                                                 |
| deltablue                  | 3.10 ms                                                                | 3.15 ms: 1.02x slower                                                 |
| json                       | 4.98 ms                                                                | 5.07 ms: 1.02x slower                                                 |
| json_loads                 | 27.3 us                                                                | 28.0 us: 1.02x slower                                                 |
| pickle_pure_python         | 292 us                                                                 | 300 us: 1.03x slower                                                  |
| mako                       | 11.2 ms                                                                | 11.6 ms: 1.04x slower                                                 |
| json_dumps                 | 10.6 ms                                                                | 11.1 ms: 1.04x slower                                                 |
| bench_thread_pool          | 924 us                                                                 | 1.04 ms: 1.13x slower                                                 |
| python_startup_no_site     | 7.41 ms                                                                | 8.64 ms: 1.16x slower                                                 |
| gc_traversal               | 3.32 ms                                                                | 4.04 ms: 1.22x slower                                                 |
| python_startup             | 11.0 ms                                                                | 15.1 ms: 1.37x slower                                                 |
| create_gc_cycles           | 1.33 ms                                                                | 1.85 ms: 1.39x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                                | 88.5 ms: 8.04x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.06x faster                                                          |

Benchmark hidden because not significant (4): django_template, asyncio_websockets, sympy_expand, typing_runtime_protocols
Ignored benchmarks (20) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250408-3.14.0a6+-09d4621/bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.085x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.12x