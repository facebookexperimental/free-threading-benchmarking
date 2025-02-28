# Results vs. 3.13.0rc2

- fork: nascheme
- ref: pgo_benchmark_task
- machine: linux-x86_64
- commit hash: aae2849
- commit date: 2025-02-27
- overall geometric mean: 1.099x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250227-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-aae2849 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 318 ms: 1.23x slower                                                   |
| docutils       | 2.63 sec                                                               | 2.88 sec: 1.10x slower                                                 |
| html5lib       | 68.6 ms                                                                | 71.8 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.12x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250227-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-aae2849 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 576 ms: 1.56x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 602 ms: 1.46x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 242 ms: 1.37x faster                                                   |
| async_tree_memoization     | 459 ms                                                                 | 346 ms: 1.33x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 313 ms: 1.31x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 280 ms: 1.26x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 566 ms: 1.12x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 600 ms: 1.11x faster                                                   |
| asyncio_websockets         | 517 ms                                                                 | 512 ms: 1.01x faster                                                   |
| async_generators           | 375 ms                                                                 | 377 ms: 1.01x slower                                                   |
| coroutines                 | 23.3 ms                                                                | 24.0 ms: 1.03x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.21x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250227-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-aae2849 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 201 ms: 1.08x faster                                                   |
| float          | 76.7 ms                                                                | 76.2 ms: 1.01x faster                                                  |
| nbody          | 85.3 ms                                                                | 135 ms: 1.58x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.13x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250227-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-aae2849 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.57 ms: 1.25x faster                                                  |
| regex_dna      | 189 ms                                                                 | 163 ms: 1.16x faster                                                   |
| regex_v8       | 23.2 ms                                                                | 25.6 ms: 1.10x slower                                                  |
| regex_compile  | 131 ms                                                                 | 161 ms: 1.23x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250227-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-aae2849 |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 95.8 ms: 1.01x slower                                                  |
| xml_etree_parse      | 136 ms                                                                 | 148 ms: 1.09x slower                                                   |
| json_loads           | 27.3 us                                                                | 30.5 us: 1.12x slower                                                  |
| json_dumps           | 10.6 ms                                                                | 12.0 ms: 1.13x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                                | 103 ms: 1.21x slower                                                   |
| tomli_loads          | 2.01 sec                                                               | 2.50 sec: 1.24x slower                                                 |
| xml_etree_process    | 59.2 ms                                                                | 75.1 ms: 1.27x slower                                                  |
| unpickle_pure_python | 208 us                                                                 | 278 us: 1.33x slower                                                   |
| pickle_pure_python   | 292 us                                                                 | 408 us: 1.40x slower                                                   |
| Geometric mean       | (ref)                                                                  | 1.20x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250227-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-aae2849 |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.79 ms: 1.32x slower                                                  |
| python_startup         | 11.0 ms                                                                | 15.9 ms: 1.44x slower                                                  |
| Geometric mean         | (ref)                                                                  | 1.38x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250227-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-aae2849 |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 62.5 ms: 1.27x slower                                                  |
| django_template | 34.2 ms                                                                | 44.0 ms: 1.29x slower                                                  |
| genshi_text     | 21.7 ms                                                                | 29.5 ms: 1.35x slower                                                  |
| mako            | 11.2 ms                                                                | 15.9 ms: 1.42x slower                                                  |
| Geometric mean  | (ref)                                                                  | 1.33x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250227-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-aae2849 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.69 ms: 1.97x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 576 ms: 1.56x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 602 ms: 1.46x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 242 ms: 1.37x faster                                                   |
| async_tree_memoization     | 459 ms                                                                 | 346 ms: 1.33x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 313 ms: 1.31x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 280 ms: 1.26x faster                                                   |
| regex_effbot               | 3.21 ms                                                                | 2.57 ms: 1.25x faster                                                  |
| regex_dna                  | 189 ms                                                                 | 163 ms: 1.16x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 566 ms: 1.12x faster                                                   |
| deepcopy                   | 357 us                                                                 | 321 us: 1.11x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 600 ms: 1.11x faster                                                   |
| pidigits                   | 216 ms                                                                 | 201 ms: 1.08x faster                                                   |
| sqlite_synth               | 2.25 us                                                                | 2.09 us: 1.08x faster                                                  |
| create_gc_cycles           | 1.33 ms                                                                | 1.27 ms: 1.05x faster                                                  |
| telco                      | 7.77 ms                                                                | 7.63 ms: 1.02x faster                                                  |
| asyncio_websockets         | 517 ms                                                                 | 512 ms: 1.01x faster                                                   |
| float                      | 76.7 ms                                                                | 76.2 ms: 1.01x faster                                                  |
| async_generators           | 375 ms                                                                 | 377 ms: 1.01x slower                                                   |
| deepcopy_memo              | 38.1 us                                                                | 38.6 us: 1.01x slower                                                  |
| xml_etree_iterparse        | 94.4 ms                                                                | 95.8 ms: 1.01x slower                                                  |
| spectral_norm              | 108 ms                                                                 | 110 ms: 1.02x slower                                                   |
| scimark_sor                | 134 ms                                                                 | 137 ms: 1.03x slower                                                   |
| coroutines                 | 23.3 ms                                                                | 24.0 ms: 1.03x slower                                                  |
| go                         | 141 ms                                                                 | 145 ms: 1.03x slower                                                   |
| mdp                        | 2.34 sec                                                               | 2.42 sec: 1.04x slower                                                 |
| html5lib                   | 68.6 ms                                                                | 71.8 ms: 1.05x slower                                                  |
| bpe_tokeniser              | 4.46 sec                                                               | 4.69 sec: 1.05x slower                                                 |
| pathlib                    | 19.3 ms                                                                | 20.3 ms: 1.05x slower                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 3.34 us: 1.07x slower                                                  |
| xml_etree_parse            | 136 ms                                                                 | 148 ms: 1.09x slower                                                   |
| docutils                   | 2.63 sec                                                               | 2.88 sec: 1.10x slower                                                 |
| json                       | 4.98 ms                                                                | 5.47 ms: 1.10x slower                                                  |
| regex_v8                   | 23.2 ms                                                                | 25.6 ms: 1.10x slower                                                  |
| json_loads                 | 27.3 us                                                                | 30.5 us: 1.12x slower                                                  |
| scimark_fft                | 348 ms                                                                 | 389 ms: 1.12x slower                                                   |
| pycparser                  | 1.12 sec                                                               | 1.26 sec: 1.12x slower                                                 |
| json_dumps                 | 10.6 ms                                                                | 12.0 ms: 1.13x slower                                                  |
| dulwich_log                | 74.5 ms                                                                | 85.7 ms: 1.15x slower                                                  |
| generators                 | 28.5 ms                                                                | 33.0 ms: 1.16x slower                                                  |
| pprint_safe_repr           | 719 ms                                                                 | 839 ms: 1.17x slower                                                   |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.55 ms: 1.17x slower                                                  |
| meteor_contest             | 101 ms                                                                 | 119 ms: 1.18x slower                                                   |
| sqlglot_normalize          | 106 ms                                                                 | 125 ms: 1.19x slower                                                   |
| pprint_pformat             | 1.46 sec                                                               | 1.73 sec: 1.19x slower                                                 |
| pyflate                    | 449 ms                                                                 | 535 ms: 1.19x slower                                                   |
| logging_silent             | 98.2 ns                                                                | 117 ns: 1.19x slower                                                   |
| sqlglot_optimize           | 52.7 ms                                                                | 63.7 ms: 1.21x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                                | 103 ms: 1.21x slower                                                   |
| comprehensions             | 16.6 us                                                                | 20.3 us: 1.22x slower                                                  |
| 2to3                       | 259 ms                                                                 | 318 ms: 1.23x slower                                                   |
| regex_compile              | 131 ms                                                                 | 161 ms: 1.23x slower                                                   |
| logging_simple             | 6.14 us                                                                | 7.60 us: 1.24x slower                                                  |
| fannkuch                   | 376 ms                                                                 | 466 ms: 1.24x slower                                                   |
| tomli_loads                | 2.01 sec                                                               | 2.50 sec: 1.24x slower                                                 |
| chaos                      | 56.3 ms                                                                | 70.1 ms: 1.25x slower                                                  |
| logging_format             | 6.92 us                                                                | 8.64 us: 1.25x slower                                                  |
| scimark_lu                 | 112 ms                                                                 | 141 ms: 1.25x slower                                                   |
| sympy_sum                  | 154 ms                                                                 | 194 ms: 1.26x slower                                                   |
| nqueens                    | 77.7 ms                                                                | 97.9 ms: 1.26x slower                                                  |
| coverage                   | 82.5 ms                                                                | 104 ms: 1.26x slower                                                   |
| xml_etree_process          | 59.2 ms                                                                | 75.1 ms: 1.27x slower                                                  |
| thrift                     | 772 us                                                                 | 980 us: 1.27x slower                                                   |
| genshi_xml                 | 49.1 ms                                                                | 62.5 ms: 1.27x slower                                                  |
| sympy_integrate            | 19.7 ms                                                                | 25.2 ms: 1.28x slower                                                  |
| scimark_monte_carlo        | 65.8 ms                                                                | 84.1 ms: 1.28x slower                                                  |
| sympy_expand               | 454 ms                                                                 | 580 ms: 1.28x slower                                                   |
| sympy_str                  | 274 ms                                                                 | 352 ms: 1.28x slower                                                   |
| sqlglot_transpile          | 1.55 ms                                                                | 2.00 ms: 1.28x slower                                                  |
| django_template            | 34.2 ms                                                                | 44.0 ms: 1.29x slower                                                  |
| hexiom                     | 5.95 ms                                                                | 7.68 ms: 1.29x slower                                                  |
| deltablue                  | 3.10 ms                                                                | 4.02 ms: 1.30x slower                                                  |
| raytrace                   | 250 ms                                                                 | 325 ms: 1.30x slower                                                   |
| python_startup_no_site     | 7.41 ms                                                                | 9.79 ms: 1.32x slower                                                  |
| typing_runtime_protocols   | 156 us                                                                 | 206 us: 1.32x slower                                                   |
| richards                   | 44.4 ms                                                                | 59.2 ms: 1.33x slower                                                  |
| unpickle_pure_python       | 208 us                                                                 | 278 us: 1.33x slower                                                   |
| crypto_pyaes               | 68.2 ms                                                                | 91.3 ms: 1.34x slower                                                  |
| sqlglot_parse              | 1.25 ms                                                                | 1.67 ms: 1.34x slower                                                  |
| richards_super             | 50.4 ms                                                                | 68.2 ms: 1.35x slower                                                  |
| genshi_text                | 21.7 ms                                                                | 29.5 ms: 1.35x slower                                                  |
| pickle_pure_python         | 292 us                                                                 | 408 us: 1.40x slower                                                   |
| mako                       | 11.2 ms                                                                | 15.9 ms: 1.42x slower                                                  |
| python_startup             | 11.0 ms                                                                | 15.9 ms: 1.44x slower                                                  |
| nbody                      | 85.3 ms                                                                | 135 ms: 1.58x slower                                                   |
| bench_thread_pool          | 924 us                                                                 | 3.63 ms: 3.92x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                                | 96.6 ms: 8.78x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.15x slower                                                           |

Benchmark hidden because not significant (1): pylint
Ignored benchmarks (14) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250227-3.14.0a5+-aae2849-NOGIL/bm-20250227-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-aae2849.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.099x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: 1.33x