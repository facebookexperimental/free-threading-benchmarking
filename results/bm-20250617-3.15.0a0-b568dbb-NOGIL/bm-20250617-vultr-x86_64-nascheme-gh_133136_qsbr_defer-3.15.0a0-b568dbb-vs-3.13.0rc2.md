# Results vs. 3.13.0rc2

- fork: nascheme
- ref: gh_133136_qsbr_defer
- machine: linux-x86_64
- commit hash: b568dbb
- commit date: 2025-06-17
- overall geometric mean: 1.018x slower
- HPT reliability: 94.65%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.37x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250617-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-b568dbb |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 282 ms: 1.09x slower                                                    |
| docutils       | 2.63 sec                                                               | 2.67 sec: 1.02x slower                                                  |
| html5lib       | 68.6 ms                                                                | 64.9 ms: 1.06x faster                                                   |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250617-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-b568dbb |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 526 ms: 1.71x faster                                                    |
| async_tree_io              | 881 ms                                                                 | 551 ms: 1.60x faster                                                    |
| async_tree_none_tg         | 333 ms                                                                 | 226 ms: 1.47x faster                                                    |
| async_tree_memoization     | 459 ms                                                                 | 312 ms: 1.47x faster                                                    |
| async_tree_memoization_tg  | 410 ms                                                                 | 285 ms: 1.44x faster                                                    |
| async_tree_none            | 353 ms                                                                 | 259 ms: 1.36x faster                                                    |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 475 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 504 ms: 1.32x faster                                                    |
| asyncio_websockets         | 517 ms                                                                 | 513 ms: 1.01x faster                                                    |
| coroutines                 | 23.3 ms                                                                | 23.2 ms: 1.01x faster                                                   |
| async_generators           | 375 ms                                                                 | 372 ms: 1.01x faster                                                    |
| Geometric mean             | (ref)                                                                  | 1.32x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250617-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-b568dbb |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 76.7 ms                                                                | 69.2 ms: 1.11x faster                                                   |
| pidigits       | 216 ms                                                                 | 211 ms: 1.03x faster                                                    |
| nbody          | 85.3 ms                                                                | 121 ms: 1.42x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.08x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250617-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-b568dbb |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.65 ms: 1.21x faster                                                   |
| regex_dna      | 189 ms                                                                 | 164 ms: 1.15x faster                                                    |
| regex_v8       | 23.2 ms                                                                | 20.4 ms: 1.14x faster                                                   |
| regex_compile  | 131 ms                                                                 | 142 ms: 1.08x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.10x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250617-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-b568dbb |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 87.3 ms: 1.08x faster                                                   |
| xml_etree_parse      | 136 ms                                                                 | 129 ms: 1.06x faster                                                    |
| tomli_loads          | 2.01 sec                                                               | 2.15 sec: 1.07x slower                                                  |
| unpickle_pure_python | 208 us                                                                 | 229 us: 1.10x slower                                                    |
| xml_etree_generate   | 85.4 ms                                                                | 95.1 ms: 1.11x slower                                                   |
| json_dumps           | 10.6 ms                                                                | 12.0 ms: 1.13x slower                                                   |
| json_loads           | 27.3 us                                                                | 30.8 us: 1.13x slower                                                   |
| pickle_pure_python   | 292 us                                                                 | 337 us: 1.16x slower                                                    |
| xml_etree_process    | 59.2 ms                                                                | 69.2 ms: 1.17x slower                                                   |
| Geometric mean       | (ref)                                                                  | 1.08x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250617-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-b568dbb |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.58 ms: 1.29x slower                                                   |
| python_startup         | 11.0 ms                                                                | 16.0 ms: 1.45x slower                                                   |
| Geometric mean         | (ref)                                                                  | 1.37x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250617-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-b568dbb |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| django_template | 34.2 ms                                                                | 38.9 ms: 1.14x slower                                                   |
| genshi_xml      | 49.1 ms                                                                | 58.1 ms: 1.18x slower                                                   |
| genshi_text     | 21.7 ms                                                                | 26.7 ms: 1.23x slower                                                   |
| mako            | 11.2 ms                                                                | 16.0 ms: 1.42x slower                                                   |
| Geometric mean  | (ref)                                                                  | 1.24x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250617-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-b568dbb |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                        | 2.34 sec                                                               | 1.30 sec: 1.79x faster                                                  |
| gc_traversal               | 3.32 ms                                                                | 1.92 ms: 1.73x faster                                                   |
| async_tree_io_tg           | 901 ms                                                                 | 526 ms: 1.71x faster                                                    |
| async_tree_io              | 881 ms                                                                 | 551 ms: 1.60x faster                                                    |
| async_tree_none_tg         | 333 ms                                                                 | 226 ms: 1.47x faster                                                    |
| async_tree_memoization     | 459 ms                                                                 | 312 ms: 1.47x faster                                                    |
| async_tree_memoization_tg  | 410 ms                                                                 | 285 ms: 1.44x faster                                                    |
| async_tree_none            | 353 ms                                                                 | 259 ms: 1.36x faster                                                    |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 475 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 504 ms: 1.32x faster                                                    |
| deepcopy                   | 357 us                                                                 | 288 us: 1.24x faster                                                    |
| regex_effbot               | 3.21 ms                                                                | 2.65 ms: 1.21x faster                                                   |
| go                         | 141 ms                                                                 | 120 ms: 1.17x faster                                                    |
| regex_dna                  | 189 ms                                                                 | 164 ms: 1.15x faster                                                    |
| regex_v8                   | 23.2 ms                                                                | 20.4 ms: 1.14x faster                                                   |
| float                      | 76.7 ms                                                                | 69.2 ms: 1.11x faster                                                   |
| sqlite_synth               | 2.25 us                                                                | 2.04 us: 1.10x faster                                                   |
| deepcopy_memo              | 38.1 us                                                                | 34.6 us: 1.10x faster                                                   |
| scimark_sor                | 134 ms                                                                 | 123 ms: 1.08x faster                                                    |
| xml_etree_iterparse        | 94.4 ms                                                                | 87.3 ms: 1.08x faster                                                   |
| html5lib                   | 68.6 ms                                                                | 64.9 ms: 1.06x faster                                                   |
| xml_etree_parse            | 136 ms                                                                 | 129 ms: 1.06x faster                                                    |
| dulwich_log                | 74.5 ms                                                                | 70.6 ms: 1.05x faster                                                   |
| deepcopy_reduce            | 3.12 us                                                                | 3.01 us: 1.04x faster                                                   |
| pidigits                   | 216 ms                                                                 | 211 ms: 1.03x faster                                                    |
| bpe_tokeniser              | 4.46 sec                                                               | 4.39 sec: 1.02x faster                                                  |
| asyncio_websockets         | 517 ms                                                                 | 513 ms: 1.01x faster                                                    |
| coroutines                 | 23.3 ms                                                                | 23.2 ms: 1.01x faster                                                   |
| async_generators           | 375 ms                                                                 | 372 ms: 1.01x faster                                                    |
| docutils                   | 2.63 sec                                                               | 2.67 sec: 1.02x slower                                                  |
| pyflate                    | 449 ms                                                                 | 459 ms: 1.02x slower                                                    |
| scimark_fft                | 348 ms                                                                 | 363 ms: 1.04x slower                                                    |
| comprehensions             | 16.6 us                                                                | 17.4 us: 1.05x slower                                                   |
| generators                 | 28.5 ms                                                                | 30.0 ms: 1.05x slower                                                   |
| spectral_norm              | 108 ms                                                                 | 114 ms: 1.06x slower                                                    |
| hexiom                     | 5.95 ms                                                                | 6.30 ms: 1.06x slower                                                   |
| json                       | 4.98 ms                                                                | 5.29 ms: 1.06x slower                                                   |
| tomli_loads                | 2.01 sec                                                               | 2.15 sec: 1.07x slower                                                  |
| regex_compile              | 131 ms                                                                 | 142 ms: 1.08x slower                                                    |
| 2to3                       | 259 ms                                                                 | 282 ms: 1.09x slower                                                    |
| telco                      | 7.77 ms                                                                | 8.51 ms: 1.09x slower                                                   |
| unpickle_pure_python       | 208 us                                                                 | 229 us: 1.10x slower                                                    |
| chaos                      | 56.3 ms                                                                | 62.0 ms: 1.10x slower                                                   |
| nqueens                    | 77.7 ms                                                                | 85.8 ms: 1.10x slower                                                   |
| sympy_integrate            | 19.7 ms                                                                | 21.9 ms: 1.11x slower                                                   |
| xml_etree_generate         | 85.4 ms                                                                | 95.1 ms: 1.11x slower                                                   |
| create_gc_cycles           | 1.33 ms                                                                | 1.50 ms: 1.12x slower                                                   |
| scimark_lu                 | 112 ms                                                                 | 127 ms: 1.13x slower                                                    |
| json_dumps                 | 10.6 ms                                                                | 12.0 ms: 1.13x slower                                                   |
| deltablue                  | 3.10 ms                                                                | 3.49 ms: 1.13x slower                                                   |
| json_loads                 | 27.3 us                                                                | 30.8 us: 1.13x slower                                                   |
| thrift                     | 772 us                                                                 | 874 us: 1.13x slower                                                    |
| sympy_str                  | 274 ms                                                                 | 311 ms: 1.14x slower                                                    |
| django_template            | 34.2 ms                                                                | 38.9 ms: 1.14x slower                                                   |
| sympy_expand               | 454 ms                                                                 | 517 ms: 1.14x slower                                                    |
| scimark_monte_carlo        | 65.8 ms                                                                | 75.4 ms: 1.15x slower                                                   |
| sympy_sum                  | 154 ms                                                                 | 178 ms: 1.15x slower                                                    |
| pickle_pure_python         | 292 us                                                                 | 337 us: 1.16x slower                                                    |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.51 ms: 1.16x slower                                                   |
| richards                   | 44.4 ms                                                                | 51.6 ms: 1.16x slower                                                   |
| xml_etree_process          | 59.2 ms                                                                | 69.2 ms: 1.17x slower                                                   |
| raytrace                   | 250 ms                                                                 | 292 ms: 1.17x slower                                                    |
| meteor_contest             | 101 ms                                                                 | 120 ms: 1.18x slower                                                    |
| genshi_xml                 | 49.1 ms                                                                | 58.1 ms: 1.18x slower                                                   |
| richards_super             | 50.4 ms                                                                | 59.7 ms: 1.18x slower                                                   |
| pprint_safe_repr           | 719 ms                                                                 | 871 ms: 1.21x slower                                                    |
| typing_runtime_protocols   | 156 us                                                                 | 190 us: 1.22x slower                                                    |
| fannkuch                   | 376 ms                                                                 | 461 ms: 1.23x slower                                                    |
| genshi_text                | 21.7 ms                                                                | 26.7 ms: 1.23x slower                                                   |
| pprint_pformat             | 1.46 sec                                                               | 1.80 sec: 1.24x slower                                                  |
| crypto_pyaes               | 68.2 ms                                                                | 85.4 ms: 1.25x slower                                                   |
| logging_simple             | 6.14 us                                                                | 7.69 us: 1.25x slower                                                   |
| logging_format             | 6.92 us                                                                | 8.70 us: 1.26x slower                                                   |
| python_startup_no_site     | 7.41 ms                                                                | 9.58 ms: 1.29x slower                                                   |
| coverage                   | 82.5 ms                                                                | 109 ms: 1.33x slower                                                    |
| nbody                      | 85.3 ms                                                                | 121 ms: 1.42x slower                                                    |
| mako                       | 11.2 ms                                                                | 16.0 ms: 1.42x slower                                                   |
| python_startup             | 11.0 ms                                                                | 16.0 ms: 1.45x slower                                                   |
| bench_thread_pool          | 924 us                                                                 | 3.15 ms: 3.41x slower                                                   |
| logging_silent             | 98.2 ns                                                                | 531 ns: 5.41x slower                                                    |
| bench_mp_pool              | 11.0 ms                                                                | 104 ms: 9.49x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.08x slower                                                            |

Benchmark hidden because not significant (3): pylint, pathlib, pycparser
Ignored benchmarks (18) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250617-3.15.0a0-b568dbb-NOGIL/bm-20250617-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-b568dbb.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.018x slower

# HPT report

- Reliability score: 94.65% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.37x