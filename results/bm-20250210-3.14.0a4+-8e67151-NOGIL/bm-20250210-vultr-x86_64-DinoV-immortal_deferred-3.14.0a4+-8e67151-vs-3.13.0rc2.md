# Results vs. 3.13.0rc2

- fork: DinoV
- ref: immortal_deferred
- machine: linux-x86_64
- commit hash: 8e67151
- commit date: 2025-02-10
- overall geometric mean: 1.078x slower
- HPT reliability: 99.97%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250210-vultr-x86_64-DinoV-immortal_deferred-3.14.0a4+-8e67151 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 302 ms: 1.17x slower                                               |
| docutils       | 2.63 sec                                                               | 2.79 sec: 1.06x slower                                             |
| html5lib       | 68.6 ms                                                                | 69.9 ms: 1.02x slower                                              |
| Geometric mean | (ref)                                                                  | 1.08x slower                                                       |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250210-vultr-x86_64-DinoV-immortal_deferred-3.14.0a4+-8e67151 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 577 ms: 1.56x faster                                               |
| async_tree_io              | 881 ms                                                                 | 605 ms: 1.46x faster                                               |
| async_tree_none_tg         | 333 ms                                                                 | 252 ms: 1.32x faster                                               |
| async_tree_memoization     | 459 ms                                                                 | 351 ms: 1.31x faster                                               |
| async_tree_memoization_tg  | 410 ms                                                                 | 320 ms: 1.28x faster                                               |
| async_tree_none            | 353 ms                                                                 | 291 ms: 1.21x faster                                               |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 523 ms: 1.21x faster                                               |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 555 ms: 1.20x faster                                               |
| coroutines                 | 23.3 ms                                                                | 23.2 ms: 1.01x faster                                              |
| Geometric mean             | (ref)                                                                  | 1.22x faster                                                       |

Benchmark hidden because not significant (2): asyncio_websockets, async_generators

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250210-vultr-x86_64-DinoV-immortal_deferred-3.14.0a4+-8e67151 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 200 ms: 1.08x faster                                               |
| float          | 76.7 ms                                                                | 75.1 ms: 1.02x faster                                              |
| nbody          | 85.3 ms                                                                | 135 ms: 1.58x slower                                               |
| Geometric mean | (ref)                                                                  | 1.13x slower                                                       |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250210-vultr-x86_64-DinoV-immortal_deferred-3.14.0a4+-8e67151 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.92 ms: 1.10x faster                                              |
| regex_dna      | 189 ms                                                                 | 186 ms: 1.01x faster                                               |
| regex_v8       | 23.2 ms                                                                | 24.2 ms: 1.04x slower                                              |
| regex_compile  | 131 ms                                                                 | 148 ms: 1.13x slower                                               |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                       |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250210-vultr-x86_64-DinoV-immortal_deferred-3.14.0a4+-8e67151 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                                 | 127 ms: 1.07x faster                                               |
| xml_etree_iterparse  | 94.4 ms                                                                | 88.0 ms: 1.07x faster                                              |
| xml_etree_generate   | 85.4 ms                                                                | 95.8 ms: 1.12x slower                                              |
| json_loads           | 27.3 us                                                                | 31.1 us: 1.14x slower                                              |
| tomli_loads          | 2.01 sec                                                               | 2.30 sec: 1.14x slower                                             |
| xml_etree_process    | 59.2 ms                                                                | 68.8 ms: 1.16x slower                                              |
| json_dumps           | 10.6 ms                                                                | 12.7 ms: 1.19x slower                                              |
| unpickle_pure_python | 208 us                                                                 | 250 us: 1.20x slower                                               |
| pickle_pure_python   | 292 us                                                                 | 374 us: 1.28x slower                                               |
| Geometric mean       | (ref)                                                                  | 1.12x slower                                                       |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250210-vultr-x86_64-DinoV-immortal_deferred-3.14.0a4+-8e67151 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.61 ms: 1.30x slower                                              |
| python_startup         | 11.0 ms                                                                | 15.3 ms: 1.39x slower                                              |
| Geometric mean         | (ref)                                                                  | 1.34x slower                                                       |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250210-vultr-x86_64-DinoV-immortal_deferred-3.14.0a4+-8e67151 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 60.4 ms: 1.23x slower                                              |
| django_template | 34.2 ms                                                                | 42.6 ms: 1.25x slower                                              |
| genshi_text     | 21.7 ms                                                                | 28.1 ms: 1.29x slower                                              |
| mako            | 11.2 ms                                                                | 16.0 ms: 1.43x slower                                              |
| Geometric mean  | (ref)                                                                  | 1.30x slower                                                       |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250210-vultr-x86_64-DinoV-immortal_deferred-3.14.0a4+-8e67151 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.73 ms: 1.91x faster                                              |
| async_tree_io_tg           | 901 ms                                                                 | 577 ms: 1.56x faster                                               |
| async_tree_io              | 881 ms                                                                 | 605 ms: 1.46x faster                                               |
| async_tree_none_tg         | 333 ms                                                                 | 252 ms: 1.32x faster                                               |
| async_tree_memoization     | 459 ms                                                                 | 351 ms: 1.31x faster                                               |
| async_tree_memoization_tg  | 410 ms                                                                 | 320 ms: 1.28x faster                                               |
| async_tree_none            | 353 ms                                                                 | 291 ms: 1.21x faster                                               |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 523 ms: 1.21x faster                                               |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 555 ms: 1.20x faster                                               |
| deepcopy                   | 357 us                                                                 | 310 us: 1.15x faster                                               |
| sqlite_synth               | 2.25 us                                                                | 2.02 us: 1.11x faster                                              |
| regex_effbot               | 3.21 ms                                                                | 2.92 ms: 1.10x faster                                              |
| pidigits                   | 216 ms                                                                 | 200 ms: 1.08x faster                                               |
| xml_etree_parse            | 136 ms                                                                 | 127 ms: 1.07x faster                                               |
| xml_etree_iterparse        | 94.4 ms                                                                | 88.0 ms: 1.07x faster                                              |
| pathlib                    | 19.3 ms                                                                | 18.7 ms: 1.03x faster                                              |
| scimark_sor                | 134 ms                                                                 | 130 ms: 1.03x faster                                               |
| go                         | 141 ms                                                                 | 137 ms: 1.03x faster                                               |
| spectral_norm              | 108 ms                                                                 | 105 ms: 1.02x faster                                               |
| float                      | 76.7 ms                                                                | 75.1 ms: 1.02x faster                                              |
| regex_dna                  | 189 ms                                                                 | 186 ms: 1.01x faster                                               |
| coroutines                 | 23.3 ms                                                                | 23.2 ms: 1.01x faster                                              |
| deepcopy_memo              | 38.1 us                                                                | 38.4 us: 1.01x slower                                              |
| html5lib                   | 68.6 ms                                                                | 69.9 ms: 1.02x slower                                              |
| deepcopy_reduce            | 3.12 us                                                                | 3.20 us: 1.02x slower                                              |
| create_gc_cycles           | 1.33 ms                                                                | 1.37 ms: 1.03x slower                                              |
| bpe_tokeniser              | 4.46 sec                                                               | 4.62 sec: 1.04x slower                                             |
| regex_v8                   | 23.2 ms                                                                | 24.2 ms: 1.04x slower                                              |
| pycparser                  | 1.12 sec                                                               | 1.18 sec: 1.06x slower                                             |
| docutils                   | 2.63 sec                                                               | 2.79 sec: 1.06x slower                                             |
| json                       | 4.98 ms                                                                | 5.36 ms: 1.08x slower                                              |
| pyflate                    | 449 ms                                                                 | 487 ms: 1.08x slower                                               |
| dulwich_log                | 74.5 ms                                                                | 81.9 ms: 1.10x slower                                              |
| logging_silent             | 98.2 ns                                                                | 108 ns: 1.10x slower                                               |
| scimark_fft                | 348 ms                                                                 | 388 ms: 1.11x slower                                               |
| telco                      | 7.77 ms                                                                | 8.66 ms: 1.11x slower                                              |
| xml_etree_generate         | 85.4 ms                                                                | 95.8 ms: 1.12x slower                                              |
| pprint_safe_repr           | 719 ms                                                                 | 811 ms: 1.13x slower                                               |
| regex_compile              | 131 ms                                                                 | 148 ms: 1.13x slower                                               |
| sqlglot_normalize          | 106 ms                                                                 | 120 ms: 1.14x slower                                               |
| json_loads                 | 27.3 us                                                                | 31.1 us: 1.14x slower                                              |
| tomli_loads                | 2.01 sec                                                               | 2.30 sec: 1.14x slower                                             |
| pprint_pformat             | 1.46 sec                                                               | 1.67 sec: 1.15x slower                                             |
| sqlglot_optimize           | 52.7 ms                                                                | 61.0 ms: 1.16x slower                                              |
| thrift                     | 772 us                                                                 | 894 us: 1.16x slower                                               |
| mdp                        | 2.34 sec                                                               | 2.72 sec: 1.16x slower                                             |
| xml_etree_process          | 59.2 ms                                                                | 68.8 ms: 1.16x slower                                              |
| 2to3                       | 259 ms                                                                 | 302 ms: 1.17x slower                                               |
| logging_simple             | 6.14 us                                                                | 7.18 us: 1.17x slower                                              |
| coverage                   | 82.5 ms                                                                | 97.5 ms: 1.18x slower                                              |
| logging_format             | 6.92 us                                                                | 8.20 us: 1.19x slower                                              |
| json_dumps                 | 10.6 ms                                                                | 12.7 ms: 1.19x slower                                              |
| generators                 | 28.5 ms                                                                | 34.0 ms: 1.19x slower                                              |
| sympy_sum                  | 154 ms                                                                 | 184 ms: 1.19x slower                                               |
| unpickle_pure_python       | 208 us                                                                 | 250 us: 1.20x slower                                               |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.70 ms: 1.20x slower                                              |
| sympy_expand               | 454 ms                                                                 | 547 ms: 1.20x slower                                               |
| comprehensions             | 16.6 us                                                                | 20.1 us: 1.21x slower                                              |
| scimark_lu                 | 112 ms                                                                 | 136 ms: 1.21x slower                                               |
| sqlglot_transpile          | 1.55 ms                                                                | 1.89 ms: 1.21x slower                                              |
| sympy_integrate            | 19.7 ms                                                                | 24.0 ms: 1.22x slower                                              |
| sympy_str                  | 274 ms                                                                 | 334 ms: 1.22x slower                                               |
| chaos                      | 56.3 ms                                                                | 68.9 ms: 1.22x slower                                              |
| hexiom                     | 5.95 ms                                                                | 7.32 ms: 1.23x slower                                              |
| genshi_xml                 | 49.1 ms                                                                | 60.4 ms: 1.23x slower                                              |
| django_template            | 34.2 ms                                                                | 42.6 ms: 1.25x slower                                              |
| nqueens                    | 77.7 ms                                                                | 96.9 ms: 1.25x slower                                              |
| deltablue                  | 3.10 ms                                                                | 3.86 ms: 1.25x slower                                              |
| scimark_monte_carlo        | 65.8 ms                                                                | 82.6 ms: 1.25x slower                                              |
| sqlglot_parse              | 1.25 ms                                                                | 1.57 ms: 1.26x slower                                              |
| richards                   | 44.4 ms                                                                | 56.3 ms: 1.27x slower                                              |
| typing_runtime_protocols   | 156 us                                                                 | 198 us: 1.27x slower                                               |
| pickle_pure_python         | 292 us                                                                 | 374 us: 1.28x slower                                               |
| meteor_contest             | 101 ms                                                                 | 130 ms: 1.28x slower                                               |
| genshi_text                | 21.7 ms                                                                | 28.1 ms: 1.29x slower                                              |
| python_startup_no_site     | 7.41 ms                                                                | 9.61 ms: 1.30x slower                                              |
| fannkuch                   | 376 ms                                                                 | 488 ms: 1.30x slower                                               |
| crypto_pyaes               | 68.2 ms                                                                | 88.7 ms: 1.30x slower                                              |
| raytrace                   | 250 ms                                                                 | 328 ms: 1.31x slower                                               |
| richards_super             | 50.4 ms                                                                | 66.9 ms: 1.33x slower                                              |
| python_startup             | 11.0 ms                                                                | 15.3 ms: 1.39x slower                                              |
| mako                       | 11.2 ms                                                                | 16.0 ms: 1.43x slower                                              |
| nbody                      | 85.3 ms                                                                | 135 ms: 1.58x slower                                               |
| bench_thread_pool          | 924 us                                                                 | 3.30 ms: 3.57x slower                                              |
| bench_mp_pool              | 11.0 ms                                                                | 94.6 ms: 8.60x slower                                              |
| Geometric mean             | (ref)                                                                  | 1.12x slower                                                       |

Benchmark hidden because not significant (3): pylint, asyncio_websockets, async_generators
Ignored benchmarks (14) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250210-3.14.0a4+-8e67151-NOGIL/bm-20250210-vultr-x86_64-DinoV-immortal_deferred-3.14.0a4+-8e67151.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.078x slower

# HPT report

- Reliability score: 99.97% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.34x