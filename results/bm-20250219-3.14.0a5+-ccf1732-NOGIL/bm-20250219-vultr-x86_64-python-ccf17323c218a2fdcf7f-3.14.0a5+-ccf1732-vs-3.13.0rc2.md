# Results vs. 3.13.0rc2

- fork: python
- ref: ccf17323c218a2fdcf7f
- machine: linux-x86_64
- commit hash: ccf1732
- commit date: 2025-02-19
- overall geometric mean: 1.076x slower
- HPT reliability: 99.98%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-python-ccf17323c218a2fdcf7f-3.14.0a5+-ccf1732 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 303 ms: 1.17x slower                                                   |
| docutils       | 2.63 sec                                                               | 2.79 sec: 1.06x slower                                                 |
| html5lib       | 68.6 ms                                                                | 70.0 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.08x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-python-ccf17323c218a2fdcf7f-3.14.0a5+-ccf1732 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 555 ms: 1.62x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 587 ms: 1.50x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 240 ms: 1.39x faster                                                   |
| async_tree_memoization     | 459 ms                                                                 | 340 ms: 1.35x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 308 ms: 1.33x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 494 ms: 1.28x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 277 ms: 1.28x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 529 ms: 1.26x faster                                                   |
| async_generators           | 375 ms                                                                 | 372 ms: 1.01x faster                                                   |
| coroutines                 | 23.3 ms                                                                | 23.5 ms: 1.01x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.26x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-python-ccf17323c218a2fdcf7f-3.14.0a5+-ccf1732 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 191 ms: 1.13x faster                                                   |
| nbody          | 85.3 ms                                                                | 130 ms: 1.52x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.10x slower                                                           |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-python-ccf17323c218a2fdcf7f-3.14.0a5+-ccf1732 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.76 ms: 1.16x faster                                                  |
| regex_dna      | 189 ms                                                                 | 172 ms: 1.09x faster                                                   |
| regex_v8       | 23.2 ms                                                                | 23.1 ms: 1.01x faster                                                  |
| regex_compile  | 131 ms                                                                 | 155 ms: 1.18x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-python-ccf17323c218a2fdcf7f-3.14.0a5+-ccf1732 |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 87.9 ms: 1.07x faster                                                  |
| xml_etree_parse      | 136 ms                                                                 | 128 ms: 1.06x faster                                                   |
| xml_etree_generate   | 85.4 ms                                                                | 95.3 ms: 1.12x slower                                                  |
| json_loads           | 27.3 us                                                                | 31.6 us: 1.16x slower                                                  |
| tomli_loads          | 2.01 sec                                                               | 2.35 sec: 1.17x slower                                                 |
| xml_etree_process    | 59.2 ms                                                                | 69.8 ms: 1.18x slower                                                  |
| unpickle_pure_python | 208 us                                                                 | 250 us: 1.20x slower                                                   |
| json_dumps           | 10.6 ms                                                                | 12.8 ms: 1.21x slower                                                  |
| pickle_pure_python   | 292 us                                                                 | 363 us: 1.24x slower                                                   |
| Geometric mean       | (ref)                                                                  | 1.12x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-python-ccf17323c218a2fdcf7f-3.14.0a5+-ccf1732 |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.62 ms: 1.30x slower                                                  |
| python_startup         | 11.0 ms                                                                | 15.6 ms: 1.41x slower                                                  |
| Geometric mean         | (ref)                                                                  | 1.35x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-python-ccf17323c218a2fdcf7f-3.14.0a5+-ccf1732 |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 59.2 ms: 1.21x slower                                                  |
| django_template | 34.2 ms                                                                | 42.5 ms: 1.24x slower                                                  |
| genshi_text     | 21.7 ms                                                                | 27.8 ms: 1.28x slower                                                  |
| mako            | 11.2 ms                                                                | 15.7 ms: 1.40x slower                                                  |
| Geometric mean  | (ref)                                                                  | 1.28x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250219-vultr-x86_64-python-ccf17323c218a2fdcf7f-3.14.0a5+-ccf1732 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.73 ms: 1.92x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 555 ms: 1.62x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 587 ms: 1.50x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 240 ms: 1.39x faster                                                   |
| async_tree_memoization     | 459 ms                                                                 | 340 ms: 1.35x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 308 ms: 1.33x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 494 ms: 1.28x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 277 ms: 1.28x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 529 ms: 1.26x faster                                                   |
| regex_effbot               | 3.21 ms                                                                | 2.76 ms: 1.16x faster                                                  |
| deepcopy                   | 357 us                                                                 | 314 us: 1.14x faster                                                   |
| pidigits                   | 216 ms                                                                 | 191 ms: 1.13x faster                                                   |
| sqlite_synth               | 2.25 us                                                                | 2.03 us: 1.11x faster                                                  |
| regex_dna                  | 189 ms                                                                 | 172 ms: 1.09x faster                                                   |
| xml_etree_iterparse        | 94.4 ms                                                                | 87.9 ms: 1.07x faster                                                  |
| xml_etree_parse            | 136 ms                                                                 | 128 ms: 1.06x faster                                                   |
| scimark_sor                | 134 ms                                                                 | 132 ms: 1.01x faster                                                   |
| regex_v8                   | 23.2 ms                                                                | 23.1 ms: 1.01x faster                                                  |
| async_generators           | 375 ms                                                                 | 372 ms: 1.01x faster                                                   |
| go                         | 141 ms                                                                 | 140 ms: 1.01x faster                                                   |
| coroutines                 | 23.3 ms                                                                | 23.5 ms: 1.01x slower                                                  |
| deepcopy_memo              | 38.1 us                                                                | 38.5 us: 1.01x slower                                                  |
| html5lib                   | 68.6 ms                                                                | 70.0 ms: 1.02x slower                                                  |
| spectral_norm              | 108 ms                                                                 | 110 ms: 1.02x slower                                                   |
| create_gc_cycles           | 1.33 ms                                                                | 1.37 ms: 1.02x slower                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 3.24 us: 1.04x slower                                                  |
| pathlib                    | 19.3 ms                                                                | 20.0 ms: 1.04x slower                                                  |
| bpe_tokeniser              | 4.46 sec                                                               | 4.71 sec: 1.06x slower                                                 |
| docutils                   | 2.63 sec                                                               | 2.79 sec: 1.06x slower                                                 |
| pycparser                  | 1.12 sec                                                               | 1.19 sec: 1.06x slower                                                 |
| json                       | 4.98 ms                                                                | 5.35 ms: 1.07x slower                                                  |
| dulwich_log                | 74.5 ms                                                                | 82.5 ms: 1.11x slower                                                  |
| telco                      | 7.77 ms                                                                | 8.63 ms: 1.11x slower                                                  |
| pyflate                    | 449 ms                                                                 | 500 ms: 1.11x slower                                                   |
| xml_etree_generate         | 85.4 ms                                                                | 95.3 ms: 1.12x slower                                                  |
| generators                 | 28.5 ms                                                                | 31.9 ms: 1.12x slower                                                  |
| scimark_fft                | 348 ms                                                                 | 390 ms: 1.12x slower                                                   |
| sqlglot_normalize          | 106 ms                                                                 | 121 ms: 1.15x slower                                                   |
| json_loads                 | 27.3 us                                                                | 31.6 us: 1.16x slower                                                  |
| pprint_safe_repr           | 719 ms                                                                 | 833 ms: 1.16x slower                                                   |
| tomli_loads                | 2.01 sec                                                               | 2.35 sec: 1.17x slower                                                 |
| 2to3                       | 259 ms                                                                 | 303 ms: 1.17x slower                                                   |
| sqlglot_optimize           | 52.7 ms                                                                | 61.5 ms: 1.17x slower                                                  |
| logging_silent             | 98.2 ns                                                                | 115 ns: 1.17x slower                                                   |
| logging_simple             | 6.14 us                                                                | 7.22 us: 1.18x slower                                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.71 sec: 1.18x slower                                                 |
| xml_etree_process          | 59.2 ms                                                                | 69.8 ms: 1.18x slower                                                  |
| thrift                     | 772 us                                                                 | 910 us: 1.18x slower                                                   |
| regex_compile              | 131 ms                                                                 | 155 ms: 1.18x slower                                                   |
| coverage                   | 82.5 ms                                                                | 97.4 ms: 1.18x slower                                                  |
| mdp                        | 2.34 sec                                                               | 2.77 sec: 1.18x slower                                                 |
| comprehensions             | 16.6 us                                                                | 19.7 us: 1.19x slower                                                  |
| unpickle_pure_python       | 208 us                                                                 | 250 us: 1.20x slower                                                   |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.71 ms: 1.20x slower                                                  |
| json_dumps                 | 10.6 ms                                                                | 12.8 ms: 1.21x slower                                                  |
| genshi_xml                 | 49.1 ms                                                                | 59.2 ms: 1.21x slower                                                  |
| logging_format             | 6.92 us                                                                | 8.37 us: 1.21x slower                                                  |
| sympy_sum                  | 154 ms                                                                 | 187 ms: 1.21x slower                                                   |
| sympy_expand               | 454 ms                                                                 | 550 ms: 1.21x slower                                                   |
| sympy_integrate            | 19.7 ms                                                                | 24.0 ms: 1.22x slower                                                  |
| sympy_str                  | 274 ms                                                                 | 334 ms: 1.22x slower                                                   |
| scimark_lu                 | 112 ms                                                                 | 139 ms: 1.23x slower                                                   |
| hexiom                     | 5.95 ms                                                                | 7.35 ms: 1.23x slower                                                  |
| sqlglot_transpile          | 1.55 ms                                                                | 1.92 ms: 1.24x slower                                                  |
| django_template            | 34.2 ms                                                                | 42.5 ms: 1.24x slower                                                  |
| pickle_pure_python         | 292 us                                                                 | 363 us: 1.24x slower                                                   |
| richards                   | 44.4 ms                                                                | 55.4 ms: 1.25x slower                                                  |
| nqueens                    | 77.7 ms                                                                | 97.1 ms: 1.25x slower                                                  |
| deltablue                  | 3.10 ms                                                                | 3.87 ms: 1.25x slower                                                  |
| chaos                      | 56.3 ms                                                                | 70.5 ms: 1.25x slower                                                  |
| scimark_monte_carlo        | 65.8 ms                                                                | 83.1 ms: 1.26x slower                                                  |
| genshi_text                | 21.7 ms                                                                | 27.8 ms: 1.28x slower                                                  |
| crypto_pyaes               | 68.2 ms                                                                | 87.2 ms: 1.28x slower                                                  |
| sqlglot_parse              | 1.25 ms                                                                | 1.59 ms: 1.28x slower                                                  |
| typing_runtime_protocols   | 156 us                                                                 | 200 us: 1.28x slower                                                   |
| richards_super             | 50.4 ms                                                                | 64.8 ms: 1.28x slower                                                  |
| meteor_contest             | 101 ms                                                                 | 130 ms: 1.29x slower                                                   |
| python_startup_no_site     | 7.41 ms                                                                | 9.62 ms: 1.30x slower                                                  |
| raytrace                   | 250 ms                                                                 | 325 ms: 1.30x slower                                                   |
| fannkuch                   | 376 ms                                                                 | 491 ms: 1.30x slower                                                   |
| mako                       | 11.2 ms                                                                | 15.7 ms: 1.40x slower                                                  |
| python_startup             | 11.0 ms                                                                | 15.6 ms: 1.41x slower                                                  |
| nbody                      | 85.3 ms                                                                | 130 ms: 1.52x slower                                                   |
| bench_thread_pool          | 924 us                                                                 | 3.31 ms: 3.58x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                                | 94.8 ms: 8.61x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.12x slower                                                           |

Benchmark hidden because not significant (3): pylint, float, asyncio_websockets
Ignored benchmarks (14) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250219-3.14.0a5+-ccf1732-NOGIL/bm-20250219-vultr-x86_64-python-ccf17323c218a2fdcf7f-3.14.0a5+-ccf1732.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.076x slower

# HPT report

- Reliability score: 99.98% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.34x