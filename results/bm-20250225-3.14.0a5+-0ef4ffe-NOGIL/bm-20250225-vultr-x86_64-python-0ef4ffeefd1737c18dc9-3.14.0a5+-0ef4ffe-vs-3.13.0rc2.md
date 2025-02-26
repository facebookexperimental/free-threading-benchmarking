# Results vs. 3.13.0rc2

- fork: python
- ref: 0ef4ffeefd1737c18dc9
- machine: linux-x86_64
- commit hash: 0ef4ffe
- commit date: 2025-02-25
- overall geometric mean: 1.079x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 303 ms: 1.17x slower                                                   |
| docutils       | 2.63 sec                                                               | 2.79 sec: 1.06x slower                                                 |
| html5lib       | 68.6 ms                                                                | 73.0 ms: 1.06x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.10x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 551 ms: 1.64x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 583 ms: 1.51x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 236 ms: 1.41x faster                                                   |
| async_tree_memoization     | 459 ms                                                                 | 336 ms: 1.37x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 304 ms: 1.35x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 274 ms: 1.29x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 570 ms: 1.11x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 599 ms: 1.11x faster                                                   |
| async_generators           | 375 ms                                                                 | 367 ms: 1.02x faster                                                   |
| coroutines                 | 23.3 ms                                                                | 22.8 ms: 1.02x faster                                                  |
| asyncio_websockets         | 517 ms                                                                 | 511 ms: 1.01x faster                                                   |
| Geometric mean             | (ref)                                                                  | 1.24x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 76.7 ms                                                                | 76.4 ms: 1.00x faster                                                  |
| pidigits       | 216 ms                                                                 | 244 ms: 1.13x slower                                                   |
| nbody          | 85.3 ms                                                                | 132 ms: 1.55x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.20x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.78 ms: 1.15x faster                                                  |
| regex_dna      | 189 ms                                                                 | 184 ms: 1.02x faster                                                   |
| regex_v8       | 23.2 ms                                                                | 23.4 ms: 1.01x slower                                                  |
| regex_compile  | 131 ms                                                                 | 155 ms: 1.18x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 88.2 ms: 1.07x faster                                                  |
| xml_etree_parse      | 136 ms                                                                 | 128 ms: 1.06x faster                                                   |
| json_loads           | 27.3 us                                                                | 29.2 us: 1.07x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                                | 95.7 ms: 1.12x slower                                                  |
| xml_etree_process    | 59.2 ms                                                                | 69.5 ms: 1.17x slower                                                  |
| tomli_loads          | 2.01 sec                                                               | 2.36 sec: 1.18x slower                                                 |
| unpickle_pure_python | 208 us                                                                 | 247 us: 1.18x slower                                                   |
| json_dumps           | 10.6 ms                                                                | 13.0 ms: 1.22x slower                                                  |
| pickle_pure_python   | 292 us                                                                 | 360 us: 1.23x slower                                                   |
| Geometric mean       | (ref)                                                                  | 1.11x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.64 ms: 1.30x slower                                                  |
| python_startup         | 11.0 ms                                                                | 15.6 ms: 1.41x slower                                                  |
| Geometric mean         | (ref)                                                                  | 1.36x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 59.6 ms: 1.22x slower                                                  |
| django_template | 34.2 ms                                                                | 42.2 ms: 1.23x slower                                                  |
| genshi_text     | 21.7 ms                                                                | 28.0 ms: 1.29x slower                                                  |
| mako            | 11.2 ms                                                                | 15.7 ms: 1.40x slower                                                  |
| Geometric mean  | (ref)                                                                  | 1.28x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.72 ms: 1.93x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 551 ms: 1.64x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 583 ms: 1.51x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 236 ms: 1.41x faster                                                   |
| async_tree_memoization     | 459 ms                                                                 | 336 ms: 1.37x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 304 ms: 1.35x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 274 ms: 1.29x faster                                                   |
| deepcopy                   | 357 us                                                                 | 310 us: 1.15x faster                                                   |
| regex_effbot               | 3.21 ms                                                                | 2.78 ms: 1.15x faster                                                  |
| sqlite_synth               | 2.25 us                                                                | 2.00 us: 1.12x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 570 ms: 1.11x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 599 ms: 1.11x faster                                                   |
| xml_etree_iterparse        | 94.4 ms                                                                | 88.2 ms: 1.07x faster                                                  |
| xml_etree_parse            | 136 ms                                                                 | 128 ms: 1.06x faster                                                   |
| regex_dna                  | 189 ms                                                                 | 184 ms: 1.02x faster                                                   |
| go                         | 141 ms                                                                 | 138 ms: 1.02x faster                                                   |
| create_gc_cycles           | 1.33 ms                                                                | 1.31 ms: 1.02x faster                                                  |
| async_generators           | 375 ms                                                                 | 367 ms: 1.02x faster                                                   |
| coroutines                 | 23.3 ms                                                                | 22.8 ms: 1.02x faster                                                  |
| asyncio_websockets         | 517 ms                                                                 | 511 ms: 1.01x faster                                                   |
| float                      | 76.7 ms                                                                | 76.4 ms: 1.00x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 37.9 us: 1.00x faster                                                  |
| regex_v8                   | 23.2 ms                                                                | 23.4 ms: 1.01x slower                                                  |
| pathlib                    | 19.3 ms                                                                | 19.6 ms: 1.02x slower                                                  |
| scimark_sor                | 134 ms                                                                 | 136 ms: 1.02x slower                                                   |
| json                       | 4.98 ms                                                                | 5.09 ms: 1.02x slower                                                  |
| spectral_norm              | 108 ms                                                                 | 113 ms: 1.05x slower                                                   |
| pycparser                  | 1.12 sec                                                               | 1.19 sec: 1.06x slower                                                 |
| docutils                   | 2.63 sec                                                               | 2.79 sec: 1.06x slower                                                 |
| html5lib                   | 68.6 ms                                                                | 73.0 ms: 1.06x slower                                                  |
| bpe_tokeniser              | 4.46 sec                                                               | 4.75 sec: 1.07x slower                                                 |
| json_loads                 | 27.3 us                                                                | 29.2 us: 1.07x slower                                                  |
| pyflate                    | 449 ms                                                                 | 495 ms: 1.10x slower                                                   |
| logging_silent             | 98.2 ns                                                                | 109 ns: 1.11x slower                                                   |
| dulwich_log                | 74.5 ms                                                                | 82.7 ms: 1.11x slower                                                  |
| telco                      | 7.77 ms                                                                | 8.67 ms: 1.11x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                                | 95.7 ms: 1.12x slower                                                  |
| pidigits                   | 216 ms                                                                 | 244 ms: 1.13x slower                                                   |
| thrift                     | 772 us                                                                 | 873 us: 1.13x slower                                                   |
| generators                 | 28.5 ms                                                                | 32.5 ms: 1.14x slower                                                  |
| scimark_fft                | 348 ms                                                                 | 397 ms: 1.14x slower                                                   |
| sqlglot_normalize          | 106 ms                                                                 | 121 ms: 1.15x slower                                                   |
| pprint_safe_repr           | 719 ms                                                                 | 835 ms: 1.16x slower                                                   |
| sqlglot_optimize           | 52.7 ms                                                                | 61.3 ms: 1.16x slower                                                  |
| 2to3                       | 259 ms                                                                 | 303 ms: 1.17x slower                                                   |
| coverage                   | 82.5 ms                                                                | 96.5 ms: 1.17x slower                                                  |
| xml_etree_process          | 59.2 ms                                                                | 69.5 ms: 1.17x slower                                                  |
| tomli_loads                | 2.01 sec                                                               | 2.36 sec: 1.18x slower                                                 |
| regex_compile              | 131 ms                                                                 | 155 ms: 1.18x slower                                                   |
| logging_simple             | 6.14 us                                                                | 7.25 us: 1.18x slower                                                  |
| unpickle_pure_python       | 208 us                                                                 | 247 us: 1.18x slower                                                   |
| pprint_pformat             | 1.46 sec                                                               | 1.73 sec: 1.19x slower                                                 |
| mdp                        | 2.34 sec                                                               | 2.79 sec: 1.19x slower                                                 |
| comprehensions             | 16.6 us                                                                | 19.8 us: 1.20x slower                                                  |
| sympy_expand               | 454 ms                                                                 | 546 ms: 1.20x slower                                                   |
| logging_format             | 6.92 us                                                                | 8.33 us: 1.20x slower                                                  |
| sympy_sum                  | 154 ms                                                                 | 186 ms: 1.21x slower                                                   |
| genshi_xml                 | 49.1 ms                                                                | 59.6 ms: 1.22x slower                                                  |
| sympy_integrate            | 19.7 ms                                                                | 24.0 ms: 1.22x slower                                                  |
| deltablue                  | 3.10 ms                                                                | 3.77 ms: 1.22x slower                                                  |
| json_dumps                 | 10.6 ms                                                                | 13.0 ms: 1.22x slower                                                  |
| sympy_str                  | 274 ms                                                                 | 335 ms: 1.22x slower                                                   |
| chaos                      | 56.3 ms                                                                | 69.1 ms: 1.23x slower                                                  |
| richards                   | 44.4 ms                                                                | 54.7 ms: 1.23x slower                                                  |
| pickle_pure_python         | 292 us                                                                 | 360 us: 1.23x slower                                                   |
| django_template            | 34.2 ms                                                                | 42.2 ms: 1.23x slower                                                  |
| sqlglot_transpile          | 1.55 ms                                                                | 1.92 ms: 1.24x slower                                                  |
| hexiom                     | 5.95 ms                                                                | 7.38 ms: 1.24x slower                                                  |
| scimark_lu                 | 112 ms                                                                 | 140 ms: 1.24x slower                                                   |
| scimark_monte_carlo        | 65.8 ms                                                                | 82.4 ms: 1.25x slower                                                  |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.95 ms: 1.25x slower                                                  |
| nqueens                    | 77.7 ms                                                                | 97.4 ms: 1.25x slower                                                  |
| richards_super             | 50.4 ms                                                                | 63.4 ms: 1.26x slower                                                  |
| raytrace                   | 250 ms                                                                 | 315 ms: 1.26x slower                                                   |
| crypto_pyaes               | 68.2 ms                                                                | 86.6 ms: 1.27x slower                                                  |
| sqlglot_parse              | 1.25 ms                                                                | 1.60 ms: 1.28x slower                                                  |
| typing_runtime_protocols   | 156 us                                                                 | 200 us: 1.29x slower                                                   |
| genshi_text                | 21.7 ms                                                                | 28.0 ms: 1.29x slower                                                  |
| meteor_contest             | 101 ms                                                                 | 131 ms: 1.29x slower                                                   |
| python_startup_no_site     | 7.41 ms                                                                | 9.64 ms: 1.30x slower                                                  |
| fannkuch                   | 376 ms                                                                 | 497 ms: 1.32x slower                                                   |
| mako                       | 11.2 ms                                                                | 15.7 ms: 1.40x slower                                                  |
| python_startup             | 11.0 ms                                                                | 15.6 ms: 1.41x slower                                                  |
| nbody                      | 85.3 ms                                                                | 132 ms: 1.55x slower                                                   |
| bench_thread_pool          | 924 us                                                                 | 3.31 ms: 3.58x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                                | 95.0 ms: 8.64x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.13x slower                                                           |

Benchmark hidden because not significant (2): pylint, deepcopy_reduce
Ignored benchmarks (14) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250225-3.14.0a5+-0ef4ffe-NOGIL/bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.079x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 1.34x