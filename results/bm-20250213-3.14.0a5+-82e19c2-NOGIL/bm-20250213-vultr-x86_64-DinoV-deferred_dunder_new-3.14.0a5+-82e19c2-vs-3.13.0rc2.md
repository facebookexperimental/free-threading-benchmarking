# Results vs. 3.13.0rc2

- fork: DinoV
- ref: deferred_dunder_new
- machine: linux-x86_64
- commit hash: 82e19c2
- commit date: 2025-02-13
- overall geometric mean: 1.079x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250213-vultr-x86_64-DinoV-deferred_dunder_new-3.14.0a5+-82e19c2 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 302 ms: 1.16x slower                                                 |
| docutils       | 2.63 sec                                                               | 2.77 sec: 1.06x slower                                               |
| html5lib       | 68.6 ms                                                                | 69.5 ms: 1.01x slower                                                |
| Geometric mean | (ref)                                                                  | 1.08x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250213-vultr-x86_64-DinoV-deferred_dunder_new-3.14.0a5+-82e19c2 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 578 ms: 1.56x faster                                                 |
| async_tree_io              | 881 ms                                                                 | 608 ms: 1.45x faster                                                 |
| async_tree_memoization     | 459 ms                                                                 | 354 ms: 1.30x faster                                                 |
| async_tree_none_tg         | 333 ms                                                                 | 259 ms: 1.28x faster                                                 |
| async_tree_memoization_tg  | 410 ms                                                                 | 319 ms: 1.28x faster                                                 |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 502 ms: 1.26x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 537 ms: 1.24x faster                                                 |
| async_tree_none            | 353 ms                                                                 | 288 ms: 1.23x faster                                                 |
| asyncio_websockets         | 517 ms                                                                 | 514 ms: 1.01x faster                                                 |
| async_generators           | 375 ms                                                                 | 373 ms: 1.00x faster                                                 |
| coroutines                 | 23.3 ms                                                                | 23.6 ms: 1.01x slower                                                |
| Geometric mean             | (ref)                                                                  | 1.22x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250213-vultr-x86_64-DinoV-deferred_dunder_new-3.14.0a5+-82e19c2 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 192 ms: 1.13x faster                                                 |
| float          | 76.7 ms                                                                | 76.4 ms: 1.00x faster                                                |
| nbody          | 85.3 ms                                                                | 133 ms: 1.56x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.11x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250213-vultr-x86_64-DinoV-deferred_dunder_new-3.14.0a5+-82e19c2 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.79 ms: 1.15x faster                                                |
| regex_dna      | 189 ms                                                                 | 181 ms: 1.04x faster                                                 |
| regex_v8       | 23.2 ms                                                                | 23.7 ms: 1.02x slower                                                |
| regex_compile  | 131 ms                                                                 | 152 ms: 1.15x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250213-vultr-x86_64-DinoV-deferred_dunder_new-3.14.0a5+-82e19c2 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 88.1 ms: 1.07x faster                                                |
| xml_etree_parse      | 136 ms                                                                 | 129 ms: 1.05x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                                | 96.2 ms: 1.13x slower                                                |
| json_loads           | 27.3 us                                                                | 31.3 us: 1.15x slower                                                |
| tomli_loads          | 2.01 sec                                                               | 2.35 sec: 1.17x slower                                               |
| xml_etree_process    | 59.2 ms                                                                | 70.1 ms: 1.18x slower                                                |
| json_dumps           | 10.6 ms                                                                | 12.7 ms: 1.19x slower                                                |
| unpickle_pure_python | 208 us                                                                 | 252 us: 1.21x slower                                                 |
| pickle_pure_python   | 292 us                                                                 | 362 us: 1.24x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.12x slower                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250213-vultr-x86_64-DinoV-deferred_dunder_new-3.14.0a5+-82e19c2 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.59 ms: 1.29x slower                                                |
| python_startup         | 11.0 ms                                                                | 15.3 ms: 1.38x slower                                                |
| Geometric mean         | (ref)                                                                  | 1.34x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250213-vultr-x86_64-DinoV-deferred_dunder_new-3.14.0a5+-82e19c2 |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 59.6 ms: 1.22x slower                                                |
| django_template | 34.2 ms                                                                | 42.0 ms: 1.23x slower                                                |
| genshi_text     | 21.7 ms                                                                | 27.9 ms: 1.28x slower                                                |
| mako            | 11.2 ms                                                                | 15.9 ms: 1.41x slower                                                |
| Geometric mean  | (ref)                                                                  | 1.28x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250213-vultr-x86_64-DinoV-deferred_dunder_new-3.14.0a5+-82e19c2 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.75 ms: 1.90x faster                                                |
| async_tree_io_tg           | 901 ms                                                                 | 578 ms: 1.56x faster                                                 |
| async_tree_io              | 881 ms                                                                 | 608 ms: 1.45x faster                                                 |
| async_tree_memoization     | 459 ms                                                                 | 354 ms: 1.30x faster                                                 |
| async_tree_none_tg         | 333 ms                                                                 | 259 ms: 1.28x faster                                                 |
| async_tree_memoization_tg  | 410 ms                                                                 | 319 ms: 1.28x faster                                                 |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 502 ms: 1.26x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 537 ms: 1.24x faster                                                 |
| async_tree_none            | 353 ms                                                                 | 288 ms: 1.23x faster                                                 |
| deepcopy                   | 357 us                                                                 | 307 us: 1.16x faster                                                 |
| regex_effbot               | 3.21 ms                                                                | 2.79 ms: 1.15x faster                                                |
| pidigits                   | 216 ms                                                                 | 192 ms: 1.13x faster                                                 |
| sqlite_synth               | 2.25 us                                                                | 2.03 us: 1.11x faster                                                |
| xml_etree_iterparse        | 94.4 ms                                                                | 88.1 ms: 1.07x faster                                                |
| xml_etree_parse            | 136 ms                                                                 | 129 ms: 1.05x faster                                                 |
| regex_dna                  | 189 ms                                                                 | 181 ms: 1.04x faster                                                 |
| asyncio_websockets         | 517 ms                                                                 | 514 ms: 1.01x faster                                                 |
| pathlib                    | 19.3 ms                                                                | 19.1 ms: 1.01x faster                                                |
| float                      | 76.7 ms                                                                | 76.4 ms: 1.00x faster                                                |
| async_generators           | 375 ms                                                                 | 373 ms: 1.00x faster                                                 |
| go                         | 141 ms                                                                 | 142 ms: 1.01x slower                                                 |
| coroutines                 | 23.3 ms                                                                | 23.6 ms: 1.01x slower                                                |
| html5lib                   | 68.6 ms                                                                | 69.5 ms: 1.01x slower                                                |
| deepcopy_reduce            | 3.12 us                                                                | 3.19 us: 1.02x slower                                                |
| regex_v8                   | 23.2 ms                                                                | 23.7 ms: 1.02x slower                                                |
| deepcopy_memo              | 38.1 us                                                                | 39.2 us: 1.03x slower                                                |
| spectral_norm              | 108 ms                                                                 | 111 ms: 1.03x slower                                                 |
| create_gc_cycles           | 1.33 ms                                                                | 1.39 ms: 1.04x slower                                                |
| bpe_tokeniser              | 4.46 sec                                                               | 4.66 sec: 1.05x slower                                               |
| pycparser                  | 1.12 sec                                                               | 1.18 sec: 1.05x slower                                               |
| docutils                   | 2.63 sec                                                               | 2.77 sec: 1.06x slower                                               |
| json                       | 4.98 ms                                                                | 5.38 ms: 1.08x slower                                                |
| telco                      | 7.77 ms                                                                | 8.56 ms: 1.10x slower                                                |
| dulwich_log                | 74.5 ms                                                                | 82.4 ms: 1.11x slower                                                |
| mdp                        | 2.34 sec                                                               | 2.60 sec: 1.11x slower                                               |
| xml_etree_generate         | 85.4 ms                                                                | 96.2 ms: 1.13x slower                                                |
| scimark_fft                | 348 ms                                                                 | 394 ms: 1.13x slower                                                 |
| sqlglot_normalize          | 106 ms                                                                 | 120 ms: 1.14x slower                                                 |
| generators                 | 28.5 ms                                                                | 32.5 ms: 1.14x slower                                                |
| pyflate                    | 449 ms                                                                 | 512 ms: 1.14x slower                                                 |
| json_loads                 | 27.3 us                                                                | 31.3 us: 1.15x slower                                                |
| regex_compile              | 131 ms                                                                 | 152 ms: 1.15x slower                                                 |
| pprint_safe_repr           | 719 ms                                                                 | 830 ms: 1.15x slower                                                 |
| thrift                     | 772 us                                                                 | 892 us: 1.16x slower                                                 |
| logging_simple             | 6.14 us                                                                | 7.12 us: 1.16x slower                                                |
| sqlglot_optimize           | 52.7 ms                                                                | 61.3 ms: 1.16x slower                                                |
| 2to3                       | 259 ms                                                                 | 302 ms: 1.16x slower                                                 |
| tomli_loads                | 2.01 sec                                                               | 2.35 sec: 1.17x slower                                               |
| pprint_pformat             | 1.46 sec                                                               | 1.70 sec: 1.17x slower                                               |
| logging_format             | 6.92 us                                                                | 8.10 us: 1.17x slower                                                |
| logging_silent             | 98.2 ns                                                                | 115 ns: 1.17x slower                                                 |
| coverage                   | 82.5 ms                                                                | 96.8 ms: 1.17x slower                                                |
| xml_etree_process          | 59.2 ms                                                                | 70.1 ms: 1.18x slower                                                |
| sympy_sum                  | 154 ms                                                                 | 184 ms: 1.19x slower                                                 |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.67 ms: 1.19x slower                                                |
| json_dumps                 | 10.6 ms                                                                | 12.7 ms: 1.19x slower                                                |
| comprehensions             | 16.6 us                                                                | 19.9 us: 1.20x slower                                                |
| sympy_expand               | 454 ms                                                                 | 545 ms: 1.20x slower                                                 |
| sympy_integrate            | 19.7 ms                                                                | 23.9 ms: 1.21x slower                                                |
| unpickle_pure_python       | 208 us                                                                 | 252 us: 1.21x slower                                                 |
| genshi_xml                 | 49.1 ms                                                                | 59.6 ms: 1.22x slower                                                |
| sympy_str                  | 274 ms                                                                 | 334 ms: 1.22x slower                                                 |
| django_template            | 34.2 ms                                                                | 42.0 ms: 1.23x slower                                                |
| sqlglot_transpile          | 1.55 ms                                                                | 1.93 ms: 1.24x slower                                                |
| pickle_pure_python         | 292 us                                                                 | 362 us: 1.24x slower                                                 |
| hexiom                     | 5.95 ms                                                                | 7.42 ms: 1.25x slower                                                |
| chaos                      | 56.3 ms                                                                | 70.3 ms: 1.25x slower                                                |
| richards                   | 44.4 ms                                                                | 55.5 ms: 1.25x slower                                                |
| scimark_lu                 | 112 ms                                                                 | 141 ms: 1.25x slower                                                 |
| nqueens                    | 77.7 ms                                                                | 98.3 ms: 1.26x slower                                                |
| scimark_monte_carlo        | 65.8 ms                                                                | 83.4 ms: 1.27x slower                                                |
| deltablue                  | 3.10 ms                                                                | 3.94 ms: 1.27x slower                                                |
| meteor_contest             | 101 ms                                                                 | 130 ms: 1.28x slower                                                 |
| richards_super             | 50.4 ms                                                                | 64.6 ms: 1.28x slower                                                |
| genshi_text                | 21.7 ms                                                                | 27.9 ms: 1.28x slower                                                |
| sqlglot_parse              | 1.25 ms                                                                | 1.60 ms: 1.28x slower                                                |
| typing_runtime_protocols   | 156 us                                                                 | 200 us: 1.29x slower                                                 |
| python_startup_no_site     | 7.41 ms                                                                | 9.59 ms: 1.29x slower                                                |
| crypto_pyaes               | 68.2 ms                                                                | 88.5 ms: 1.30x slower                                                |
| raytrace                   | 250 ms                                                                 | 332 ms: 1.33x slower                                                 |
| fannkuch                   | 376 ms                                                                 | 501 ms: 1.33x slower                                                 |
| python_startup             | 11.0 ms                                                                | 15.3 ms: 1.38x slower                                                |
| mako                       | 11.2 ms                                                                | 15.9 ms: 1.41x slower                                                |
| nbody                      | 85.3 ms                                                                | 133 ms: 1.56x slower                                                 |
| bench_thread_pool          | 924 us                                                                 | 3.32 ms: 3.59x slower                                                |
| bench_mp_pool              | 11.0 ms                                                                | 94.6 ms: 8.60x slower                                                |
| Geometric mean             | (ref)                                                                  | 1.13x slower                                                         |

Benchmark hidden because not significant (2): pylint, scimark_sor
Ignored benchmarks (14) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250213-3.14.0a5+-82e19c2-NOGIL/bm-20250213-vultr-x86_64-DinoV-deferred_dunder_new-3.14.0a5+-82e19c2.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.079x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.34x