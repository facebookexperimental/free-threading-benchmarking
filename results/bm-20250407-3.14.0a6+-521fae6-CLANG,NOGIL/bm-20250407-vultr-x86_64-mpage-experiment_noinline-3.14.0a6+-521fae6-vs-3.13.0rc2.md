# Results vs. 3.13.0rc2

- fork: mpage
- ref: experiment_noinline
- machine: linux-x86_64
- commit hash: 521fae6
- commit date: 2025-04-07
- overall geometric mean: 1.052x faster
- HPT reliability: 90.65%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.39x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 271 ms: 1.05x slower                                                 |
| html5lib       | 68.6 ms                                                                | 60.8 ms: 1.13x faster                                                |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                         |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 481 ms: 1.87x faster                                                 |
| async_tree_io              | 881 ms                                                                 | 509 ms: 1.73x faster                                                 |
| async_tree_none_tg         | 333 ms                                                                 | 209 ms: 1.59x faster                                                 |
| async_tree_memoization     | 459 ms                                                                 | 291 ms: 1.58x faster                                                 |
| async_tree_memoization_tg  | 410 ms                                                                 | 262 ms: 1.56x faster                                                 |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 426 ms: 1.49x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 454 ms: 1.47x faster                                                 |
| async_tree_none            | 353 ms                                                                 | 243 ms: 1.46x faster                                                 |
| coroutines                 | 23.3 ms                                                                | 19.7 ms: 1.19x faster                                                |
| async_generators           | 375 ms                                                                 | 321 ms: 1.17x faster                                                 |
| asyncio_websockets         | 517 ms                                                                 | 516 ms: 1.00x faster                                                 |
| Geometric mean             | (ref)                                                                  | 1.44x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 76.7 ms                                                                | 63.8 ms: 1.20x faster                                                |
| pidigits       | 216 ms                                                                 | 186 ms: 1.16x faster                                                 |
| nbody          | 85.3 ms                                                                | 108 ms: 1.27x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.96 ms: 1.08x faster                                                |
| regex_v8       | 23.2 ms                                                                | 21.6 ms: 1.08x faster                                                |
| regex_dna      | 189 ms                                                                 | 179 ms: 1.05x faster                                                 |
| regex_compile  | 131 ms                                                                 | 133 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 84.3 ms: 1.12x faster                                                |
| xml_etree_generate   | 85.4 ms                                                                | 83.5 ms: 1.02x faster                                                |
| tomli_loads          | 2.01 sec                                                               | 1.97 sec: 1.02x faster                                               |
| xml_etree_process    | 59.2 ms                                                                | 59.6 ms: 1.01x slower                                                |
| xml_etree_parse      | 136 ms                                                                 | 141 ms: 1.04x slower                                                 |
| unpickle_pure_python | 208 us                                                                 | 222 us: 1.07x slower                                                 |
| json_loads           | 27.3 us                                                                | 29.5 us: 1.08x slower                                                |
| pickle_pure_python   | 292 us                                                                 | 317 us: 1.09x slower                                                 |
| json_dumps           | 10.6 ms                                                                | 12.7 ms: 1.19x slower                                                |
| Geometric mean       | (ref)                                                                  | 1.03x slower                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 15.5 ms: 1.41x slower                                                |
| python_startup_no_site | 7.41 ms                                                                | 11.0 ms: 1.48x slower                                                |
| Geometric mean         | (ref)                                                                  | 1.45x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 51.2 ms: 1.04x slower                                                |
| genshi_text     | 21.7 ms                                                                | 23.6 ms: 1.08x slower                                                |
| django_template | 34.2 ms                                                                | 37.4 ms: 1.09x slower                                                |
| mako            | 11.2 ms                                                                | 14.4 ms: 1.28x slower                                                |
| Geometric mean  | (ref)                                                                  | 1.12x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| mdp                        | 2.34 sec                                                               | 1.25 sec: 1.88x faster                                               |
| async_tree_io_tg           | 901 ms                                                                 | 481 ms: 1.87x faster                                                 |
| async_tree_io              | 881 ms                                                                 | 509 ms: 1.73x faster                                                 |
| async_tree_none_tg         | 333 ms                                                                 | 209 ms: 1.59x faster                                                 |
| gc_traversal               | 3.32 ms                                                                | 2.09 ms: 1.59x faster                                                |
| async_tree_memoization     | 459 ms                                                                 | 291 ms: 1.58x faster                                                 |
| async_tree_memoization_tg  | 410 ms                                                                 | 262 ms: 1.56x faster                                                 |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 426 ms: 1.49x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 454 ms: 1.47x faster                                                 |
| async_tree_none            | 353 ms                                                                 | 243 ms: 1.46x faster                                                 |
| deepcopy                   | 357 us                                                                 | 255 us: 1.40x faster                                                 |
| scimark_sor                | 134 ms                                                                 | 108 ms: 1.23x faster                                                 |
| deepcopy_reduce            | 3.12 us                                                                | 2.59 us: 1.21x faster                                                |
| float                      | 76.7 ms                                                                | 63.8 ms: 1.20x faster                                                |
| go                         | 141 ms                                                                 | 117 ms: 1.20x faster                                                 |
| coroutines                 | 23.3 ms                                                                | 19.7 ms: 1.19x faster                                                |
| deepcopy_memo              | 38.1 us                                                                | 32.2 us: 1.18x faster                                                |
| logging_silent             | 98.2 ns                                                                | 83.9 ns: 1.17x faster                                                |
| async_generators           | 375 ms                                                                 | 321 ms: 1.17x faster                                                 |
| pidigits                   | 216 ms                                                                 | 186 ms: 1.16x faster                                                 |
| sqlite_synth               | 2.25 us                                                                | 1.97 us: 1.14x faster                                                |
| spectral_norm              | 108 ms                                                                 | 95.1 ms: 1.13x faster                                                |
| html5lib                   | 68.6 ms                                                                | 60.8 ms: 1.13x faster                                                |
| xml_etree_iterparse        | 94.4 ms                                                                | 84.3 ms: 1.12x faster                                                |
| scimark_fft                | 348 ms                                                                 | 313 ms: 1.11x faster                                                 |
| pylint                     | 317 ms                                                                 | 291 ms: 1.09x faster                                                 |
| regex_effbot               | 3.21 ms                                                                | 2.96 ms: 1.08x faster                                                |
| regex_v8                   | 23.2 ms                                                                | 21.6 ms: 1.08x faster                                                |
| dulwich_log                | 74.5 ms                                                                | 70.6 ms: 1.05x faster                                                |
| regex_dna                  | 189 ms                                                                 | 179 ms: 1.05x faster                                                 |
| bpe_tokeniser              | 4.46 sec                                                               | 4.27 sec: 1.04x faster                                               |
| pathlib                    | 19.3 ms                                                                | 18.5 ms: 1.04x faster                                                |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.58 ms: 1.04x faster                                                |
| telco                      | 7.77 ms                                                                | 7.60 ms: 1.02x faster                                                |
| xml_etree_generate         | 85.4 ms                                                                | 83.5 ms: 1.02x faster                                                |
| tomli_loads                | 2.01 sec                                                               | 1.97 sec: 1.02x faster                                               |
| pyflate                    | 449 ms                                                                 | 442 ms: 1.02x faster                                                 |
| generators                 | 28.5 ms                                                                | 28.1 ms: 1.01x faster                                                |
| scimark_lu                 | 112 ms                                                                 | 111 ms: 1.01x faster                                                 |
| chaos                      | 56.3 ms                                                                | 55.7 ms: 1.01x faster                                                |
| pycparser                  | 1.12 sec                                                               | 1.11 sec: 1.01x faster                                               |
| asyncio_websockets         | 517 ms                                                                 | 516 ms: 1.00x faster                                                 |
| xml_etree_process          | 59.2 ms                                                                | 59.6 ms: 1.01x slower                                                |
| scimark_monte_carlo        | 65.8 ms                                                                | 66.4 ms: 1.01x slower                                                |
| nqueens                    | 77.7 ms                                                                | 78.6 ms: 1.01x slower                                                |
| regex_compile              | 131 ms                                                                 | 133 ms: 1.02x slower                                                 |
| richards                   | 44.4 ms                                                                | 45.3 ms: 1.02x slower                                                |
| comprehensions             | 16.6 us                                                                | 17.0 us: 1.03x slower                                                |
| xml_etree_parse            | 136 ms                                                                 | 141 ms: 1.04x slower                                                 |
| json                       | 4.98 ms                                                                | 5.16 ms: 1.04x slower                                                |
| pprint_safe_repr           | 719 ms                                                                 | 750 ms: 1.04x slower                                                 |
| genshi_xml                 | 49.1 ms                                                                | 51.2 ms: 1.04x slower                                                |
| 2to3                       | 259 ms                                                                 | 271 ms: 1.05x slower                                                 |
| logging_simple             | 6.14 us                                                                | 6.44 us: 1.05x slower                                                |
| hexiom                     | 5.95 ms                                                                | 6.25 ms: 1.05x slower                                                |
| sympy_integrate            | 19.7 ms                                                                | 20.7 ms: 1.05x slower                                                |
| pprint_pformat             | 1.46 sec                                                               | 1.54 sec: 1.06x slower                                               |
| richards_super             | 50.4 ms                                                                | 53.3 ms: 1.06x slower                                                |
| unpickle_pure_python       | 208 us                                                                 | 222 us: 1.07x slower                                                 |
| logging_format             | 6.92 us                                                                | 7.38 us: 1.07x slower                                                |
| json_loads                 | 27.3 us                                                                | 29.5 us: 1.08x slower                                                |
| raytrace                   | 250 ms                                                                 | 270 ms: 1.08x slower                                                 |
| genshi_text                | 21.7 ms                                                                | 23.6 ms: 1.08x slower                                                |
| pickle_pure_python         | 292 us                                                                 | 317 us: 1.09x slower                                                 |
| fannkuch                   | 376 ms                                                                 | 409 ms: 1.09x slower                                                 |
| sympy_sum                  | 154 ms                                                                 | 168 ms: 1.09x slower                                                 |
| sympy_str                  | 274 ms                                                                 | 300 ms: 1.09x slower                                                 |
| django_template            | 34.2 ms                                                                | 37.4 ms: 1.09x slower                                                |
| sympy_expand               | 454 ms                                                                 | 497 ms: 1.10x slower                                                 |
| typing_runtime_protocols   | 156 us                                                                 | 174 us: 1.12x slower                                                 |
| deltablue                  | 3.10 ms                                                                | 3.47 ms: 1.12x slower                                                |
| crypto_pyaes               | 68.2 ms                                                                | 78.3 ms: 1.15x slower                                                |
| coverage                   | 82.5 ms                                                                | 94.9 ms: 1.15x slower                                                |
| json_dumps                 | 10.6 ms                                                                | 12.7 ms: 1.19x slower                                                |
| meteor_contest             | 101 ms                                                                 | 122 ms: 1.20x slower                                                 |
| nbody                      | 85.3 ms                                                                | 108 ms: 1.27x slower                                                 |
| mako                       | 11.2 ms                                                                | 14.4 ms: 1.28x slower                                                |
| python_startup             | 11.0 ms                                                                | 15.5 ms: 1.41x slower                                                |
| python_startup_no_site     | 7.41 ms                                                                | 11.0 ms: 1.48x slower                                                |
| bench_thread_pool          | 924 us                                                                 | 3.07 ms: 3.33x slower                                                |
| bench_mp_pool              | 11.0 ms                                                                | 93.7 ms: 8.52x slower                                                |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                         |

Benchmark hidden because not significant (2): docutils, create_gc_cycles
Ignored benchmarks (19) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250407-3.14.0a6+-521fae6-CLANG,NOGIL/bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.052x faster

# HPT report

- Reliability score: 90.65% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.39x