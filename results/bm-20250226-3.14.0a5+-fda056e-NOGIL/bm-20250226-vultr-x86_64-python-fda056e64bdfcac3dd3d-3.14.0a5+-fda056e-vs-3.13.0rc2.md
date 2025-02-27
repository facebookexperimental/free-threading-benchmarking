# Results vs. 3.13.0rc2

- fork: python
- ref: fda056e64bdfcac3dd3d
- machine: linux-x86_64
- commit hash: fda056e
- commit date: 2025-02-26
- overall geometric mean: 1.074x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 305 ms: 1.18x slower                                                   |
| docutils       | 2.63 sec                                                               | 2.80 sec: 1.06x slower                                                 |
| html5lib       | 68.6 ms                                                                | 70.8 ms: 1.03x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.09x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 552 ms: 1.63x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 579 ms: 1.52x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 238 ms: 1.40x faster                                                   |
| async_tree_memoization     | 459 ms                                                                 | 340 ms: 1.35x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 307 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 492 ms: 1.29x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 276 ms: 1.28x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 524 ms: 1.27x faster                                                   |
| async_generators           | 375 ms                                                                 | 373 ms: 1.01x faster                                                   |
| coroutines                 | 23.3 ms                                                                | 23.4 ms: 1.00x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.26x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 191 ms: 1.13x faster                                                   |
| float          | 76.7 ms                                                                | 76.1 ms: 1.01x faster                                                  |
| nbody          | 85.3 ms                                                                | 136 ms: 1.59x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.12x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.67 ms: 1.20x faster                                                  |
| regex_dna      | 189 ms                                                                 | 178 ms: 1.06x faster                                                   |
| regex_v8       | 23.2 ms                                                                | 23.9 ms: 1.03x slower                                                  |
| regex_compile  | 131 ms                                                                 | 155 ms: 1.18x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 87.6 ms: 1.08x faster                                                  |
| xml_etree_parse      | 136 ms                                                                 | 128 ms: 1.06x faster                                                   |
| json_loads           | 27.3 us                                                                | 29.4 us: 1.08x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                                | 95.7 ms: 1.12x slower                                                  |
| xml_etree_process    | 59.2 ms                                                                | 69.8 ms: 1.18x slower                                                  |
| tomli_loads          | 2.01 sec                                                               | 2.38 sec: 1.19x slower                                                 |
| unpickle_pure_python | 208 us                                                                 | 250 us: 1.20x slower                                                   |
| json_dumps           | 10.6 ms                                                                | 12.9 ms: 1.21x slower                                                  |
| pickle_pure_python   | 292 us                                                                 | 362 us: 1.24x slower                                                   |
| Geometric mean       | (ref)                                                                  | 1.11x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.68 ms: 1.31x slower                                                  |
| python_startup         | 11.0 ms                                                                | 15.7 ms: 1.42x slower                                                  |
| Geometric mean         | (ref)                                                                  | 1.36x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 60.3 ms: 1.23x slower                                                  |
| django_template | 34.2 ms                                                                | 42.6 ms: 1.25x slower                                                  |
| genshi_text     | 21.7 ms                                                                | 28.3 ms: 1.30x slower                                                  |
| mako            | 11.2 ms                                                                | 15.8 ms: 1.41x slower                                                  |
| Geometric mean  | (ref)                                                                  | 1.29x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.74 ms: 1.91x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 552 ms: 1.63x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 579 ms: 1.52x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 238 ms: 1.40x faster                                                   |
| async_tree_memoization     | 459 ms                                                                 | 340 ms: 1.35x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 307 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 492 ms: 1.29x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 276 ms: 1.28x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 524 ms: 1.27x faster                                                   |
| regex_effbot               | 3.21 ms                                                                | 2.67 ms: 1.20x faster                                                  |
| deepcopy                   | 357 us                                                                 | 313 us: 1.14x faster                                                   |
| pidigits                   | 216 ms                                                                 | 191 ms: 1.13x faster                                                   |
| sqlite_synth               | 2.25 us                                                                | 2.03 us: 1.11x faster                                                  |
| xml_etree_iterparse        | 94.4 ms                                                                | 87.6 ms: 1.08x faster                                                  |
| xml_etree_parse            | 136 ms                                                                 | 128 ms: 1.06x faster                                                   |
| regex_dna                  | 189 ms                                                                 | 178 ms: 1.06x faster                                                   |
| float                      | 76.7 ms                                                                | 76.1 ms: 1.01x faster                                                  |
| create_gc_cycles           | 1.33 ms                                                                | 1.32 ms: 1.01x faster                                                  |
| async_generators           | 375 ms                                                                 | 373 ms: 1.01x faster                                                   |
| coroutines                 | 23.3 ms                                                                | 23.4 ms: 1.00x slower                                                  |
| scimark_sor                | 134 ms                                                                 | 135 ms: 1.01x slower                                                   |
| json                       | 4.98 ms                                                                | 5.06 ms: 1.02x slower                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 3.18 us: 1.02x slower                                                  |
| pathlib                    | 19.3 ms                                                                | 19.6 ms: 1.02x slower                                                  |
| spectral_norm              | 108 ms                                                                 | 110 ms: 1.02x slower                                                   |
| regex_v8                   | 23.2 ms                                                                | 23.9 ms: 1.03x slower                                                  |
| html5lib                   | 68.6 ms                                                                | 70.8 ms: 1.03x slower                                                  |
| pycparser                  | 1.12 sec                                                               | 1.19 sec: 1.06x slower                                                 |
| docutils                   | 2.63 sec                                                               | 2.80 sec: 1.06x slower                                                 |
| bpe_tokeniser              | 4.46 sec                                                               | 4.78 sec: 1.07x slower                                                 |
| json_loads                 | 27.3 us                                                                | 29.4 us: 1.08x slower                                                  |
| generators                 | 28.5 ms                                                                | 31.6 ms: 1.11x slower                                                  |
| mdp                        | 2.34 sec                                                               | 2.60 sec: 1.11x slower                                                 |
| dulwich_log                | 74.5 ms                                                                | 83.0 ms: 1.11x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                                | 95.7 ms: 1.12x slower                                                  |
| pyflate                    | 449 ms                                                                 | 509 ms: 1.13x slower                                                   |
| logging_silent             | 98.2 ns                                                                | 112 ns: 1.14x slower                                                   |
| scimark_fft                | 348 ms                                                                 | 397 ms: 1.14x slower                                                   |
| thrift                     | 772 us                                                                 | 883 us: 1.14x slower                                                   |
| telco                      | 7.77 ms                                                                | 8.90 ms: 1.14x slower                                                  |
| sqlglot_normalize          | 106 ms                                                                 | 121 ms: 1.15x slower                                                   |
| pprint_safe_repr           | 719 ms                                                                 | 832 ms: 1.16x slower                                                   |
| sqlglot_optimize           | 52.7 ms                                                                | 61.5 ms: 1.17x slower                                                  |
| logging_simple             | 6.14 us                                                                | 7.17 us: 1.17x slower                                                  |
| 2to3                       | 259 ms                                                                 | 305 ms: 1.18x slower                                                   |
| xml_etree_process          | 59.2 ms                                                                | 69.8 ms: 1.18x slower                                                  |
| coverage                   | 82.5 ms                                                                | 97.2 ms: 1.18x slower                                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.72 sec: 1.18x slower                                                 |
| logging_format             | 6.92 us                                                                | 8.17 us: 1.18x slower                                                  |
| regex_compile              | 131 ms                                                                 | 155 ms: 1.18x slower                                                   |
| tomli_loads                | 2.01 sec                                                               | 2.38 sec: 1.19x slower                                                 |
| comprehensions             | 16.6 us                                                                | 19.8 us: 1.20x slower                                                  |
| unpickle_pure_python       | 208 us                                                                 | 250 us: 1.20x slower                                                   |
| sympy_sum                  | 154 ms                                                                 | 186 ms: 1.21x slower                                                   |
| json_dumps                 | 10.6 ms                                                                | 12.9 ms: 1.21x slower                                                  |
| sympy_expand               | 454 ms                                                                 | 551 ms: 1.21x slower                                                   |
| sympy_integrate            | 19.7 ms                                                                | 24.0 ms: 1.22x slower                                                  |
| deltablue                  | 3.10 ms                                                                | 3.77 ms: 1.22x slower                                                  |
| sympy_str                  | 274 ms                                                                 | 336 ms: 1.22x slower                                                   |
| sqlglot_transpile          | 1.55 ms                                                                | 1.91 ms: 1.23x slower                                                  |
| hexiom                     | 5.95 ms                                                                | 7.32 ms: 1.23x slower                                                  |
| genshi_xml                 | 49.1 ms                                                                | 60.3 ms: 1.23x slower                                                  |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.84 ms: 1.23x slower                                                  |
| chaos                      | 56.3 ms                                                                | 69.6 ms: 1.24x slower                                                  |
| richards                   | 44.4 ms                                                                | 54.9 ms: 1.24x slower                                                  |
| pickle_pure_python         | 292 us                                                                 | 362 us: 1.24x slower                                                   |
| django_template            | 34.2 ms                                                                | 42.6 ms: 1.25x slower                                                  |
| scimark_lu                 | 112 ms                                                                 | 140 ms: 1.25x slower                                                   |
| nqueens                    | 77.7 ms                                                                | 97.5 ms: 1.25x slower                                                  |
| sqlglot_parse              | 1.25 ms                                                                | 1.58 ms: 1.27x slower                                                  |
| scimark_monte_carlo        | 65.8 ms                                                                | 83.6 ms: 1.27x slower                                                  |
| richards_super             | 50.4 ms                                                                | 64.0 ms: 1.27x slower                                                  |
| raytrace                   | 250 ms                                                                 | 318 ms: 1.27x slower                                                   |
| typing_runtime_protocols   | 156 us                                                                 | 199 us: 1.28x slower                                                   |
| meteor_contest             | 101 ms                                                                 | 130 ms: 1.28x slower                                                   |
| crypto_pyaes               | 68.2 ms                                                                | 88.1 ms: 1.29x slower                                                  |
| genshi_text                | 21.7 ms                                                                | 28.3 ms: 1.30x slower                                                  |
| python_startup_no_site     | 7.41 ms                                                                | 9.68 ms: 1.31x slower                                                  |
| fannkuch                   | 376 ms                                                                 | 494 ms: 1.31x slower                                                   |
| mako                       | 11.2 ms                                                                | 15.8 ms: 1.41x slower                                                  |
| python_startup             | 11.0 ms                                                                | 15.7 ms: 1.42x slower                                                  |
| nbody                      | 85.3 ms                                                                | 136 ms: 1.59x slower                                                   |
| bench_thread_pool          | 924 us                                                                 | 3.31 ms: 3.58x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                                | 95.7 ms: 8.70x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.12x slower                                                           |

Benchmark hidden because not significant (4): pylint, go, asyncio_websockets, deepcopy_memo
Ignored benchmarks (14) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250226-3.14.0a5+-fda056e-NOGIL/bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.074x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.34x