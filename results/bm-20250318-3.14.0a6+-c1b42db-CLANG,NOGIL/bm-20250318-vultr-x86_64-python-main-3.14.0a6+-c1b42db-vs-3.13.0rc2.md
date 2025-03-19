# Results vs. 3.13.0rc2

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: c1b42db
- commit date: 2025-03-18
- overall geometric mean: 1.015x faster
- HPT reliability: 79.80%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.39x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250318-vultr-x86_64-python-main-3.14.0a6+-c1b42db |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 275 ms: 1.06x slower                                   |
| html5lib       | 68.6 ms                                                                | 65.3 ms: 1.05x faster                                  |
| Geometric mean | (ref)                                                                  | 1.00x slower                                           |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250318-vultr-x86_64-python-main-3.14.0a6+-c1b42db |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 492 ms: 1.83x faster                                   |
| async_tree_io              | 881 ms                                                                 | 529 ms: 1.67x faster                                   |
| async_tree_none_tg         | 333 ms                                                                 | 215 ms: 1.55x faster                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 275 ms: 1.49x faster                                   |
| async_tree_memoization     | 459 ms                                                                 | 310 ms: 1.48x faster                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 431 ms: 1.47x faster                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 466 ms: 1.43x faster                                   |
| async_tree_none            | 353 ms                                                                 | 252 ms: 1.40x faster                                   |
| async_generators           | 375 ms                                                                 | 324 ms: 1.16x faster                                   |
| coroutines                 | 23.3 ms                                                                | 20.2 ms: 1.15x faster                                  |
| Geometric mean             | (ref)                                                                  | 1.40x faster                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250318-vultr-x86_64-python-main-3.14.0a6+-c1b42db |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 186 ms: 1.16x faster                                   |
| float          | 76.7 ms                                                                | 68.0 ms: 1.13x faster                                  |
| nbody          | 85.3 ms                                                                | 119 ms: 1.40x slower                                   |
| Geometric mean | (ref)                                                                  | 1.02x slower                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250318-vultr-x86_64-python-main-3.14.0a6+-c1b42db |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------:|
| regex_v8       | 23.2 ms                                                                | 21.3 ms: 1.09x faster                                  |
| regex_effbot   | 3.21 ms                                                                | 3.26 ms: 1.02x slower                                  |
| regex_compile  | 131 ms                                                                 | 138 ms: 1.05x slower                                   |
| regex_dna      | 189 ms                                                                 | 202 ms: 1.07x slower                                   |
| Geometric mean | (ref)                                                                  | 1.01x slower                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250318-vultr-x86_64-python-main-3.14.0a6+-c1b42db |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 84.3 ms: 1.12x faster                                  |
| xml_etree_generate   | 85.4 ms                                                                | 85.1 ms: 1.00x faster                                  |
| xml_etree_process    | 59.2 ms                                                                | 60.0 ms: 1.01x slower                                  |
| xml_etree_parse      | 136 ms                                                                 | 139 ms: 1.03x slower                                   |
| tomli_loads          | 2.01 sec                                                               | 2.13 sec: 1.06x slower                                 |
| unpickle_pure_python | 208 us                                                                 | 224 us: 1.08x slower                                   |
| json_loads           | 27.3 us                                                                | 29.7 us: 1.09x slower                                  |
| pickle_pure_python   | 292 us                                                                 | 325 us: 1.11x slower                                   |
| json_dumps           | 10.6 ms                                                                | 12.5 ms: 1.18x slower                                  |
| Geometric mean       | (ref)                                                                  | 1.05x slower                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250318-vultr-x86_64-python-main-3.14.0a6+-c1b42db |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 15.5 ms: 1.40x slower                                  |
| python_startup_no_site | 7.41 ms                                                                | 11.0 ms: 1.48x slower                                  |
| Geometric mean         | (ref)                                                                  | 1.44x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250318-vultr-x86_64-python-main-3.14.0a6+-c1b42db |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 52.0 ms: 1.06x slower                                  |
| django_template | 34.2 ms                                                                | 37.0 ms: 1.08x slower                                  |
| genshi_text     | 21.7 ms                                                                | 24.2 ms: 1.12x slower                                  |
| mako            | 11.2 ms                                                                | 14.8 ms: 1.32x slower                                  |
| Geometric mean  | (ref)                                                                  | 1.14x slower                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250318-vultr-x86_64-python-main-3.14.0a6+-c1b42db |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 492 ms: 1.83x faster                                   |
| gc_traversal               | 3.32 ms                                                                | 1.94 ms: 1.71x faster                                  |
| async_tree_io              | 881 ms                                                                 | 529 ms: 1.67x faster                                   |
| async_tree_none_tg         | 333 ms                                                                 | 215 ms: 1.55x faster                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 275 ms: 1.49x faster                                   |
| async_tree_memoization     | 459 ms                                                                 | 310 ms: 1.48x faster                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 431 ms: 1.47x faster                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 466 ms: 1.43x faster                                   |
| async_tree_none            | 353 ms                                                                 | 252 ms: 1.40x faster                                   |
| deepcopy                   | 357 us                                                                 | 268 us: 1.33x faster                                   |
| scimark_sor                | 134 ms                                                                 | 112 ms: 1.20x faster                                   |
| pidigits                   | 216 ms                                                                 | 186 ms: 1.16x faster                                   |
| async_generators           | 375 ms                                                                 | 324 ms: 1.16x faster                                   |
| coroutines                 | 23.3 ms                                                                | 20.2 ms: 1.15x faster                                  |
| go                         | 141 ms                                                                 | 122 ms: 1.15x faster                                   |
| deepcopy_reduce            | 3.12 us                                                                | 2.77 us: 1.13x faster                                  |
| deepcopy_memo              | 38.1 us                                                                | 33.7 us: 1.13x faster                                  |
| float                      | 76.7 ms                                                                | 68.0 ms: 1.13x faster                                  |
| logging_silent             | 98.2 ns                                                                | 87.0 ns: 1.13x faster                                  |
| spectral_norm              | 108 ms                                                                 | 96.1 ms: 1.12x faster                                  |
| xml_etree_iterparse        | 94.4 ms                                                                | 84.3 ms: 1.12x faster                                  |
| sqlite_synth               | 2.25 us                                                                | 2.02 us: 1.11x faster                                  |
| pylint                     | 317 ms                                                                 | 291 ms: 1.09x faster                                   |
| regex_v8                   | 23.2 ms                                                                | 21.3 ms: 1.09x faster                                  |
| dulwich_log                | 74.5 ms                                                                | 70.4 ms: 1.06x faster                                  |
| generators                 | 28.5 ms                                                                | 27.1 ms: 1.05x faster                                  |
| html5lib                   | 68.6 ms                                                                | 65.3 ms: 1.05x faster                                  |
| scimark_fft                | 348 ms                                                                 | 341 ms: 1.02x faster                                   |
| bpe_tokeniser              | 4.46 sec                                                               | 4.39 sec: 1.02x faster                                 |
| pyflate                    | 449 ms                                                                 | 443 ms: 1.01x faster                                   |
| pathlib                    | 19.3 ms                                                                | 19.0 ms: 1.01x faster                                  |
| xml_etree_generate         | 85.4 ms                                                                | 85.1 ms: 1.00x faster                                  |
| xml_etree_process          | 59.2 ms                                                                | 60.0 ms: 1.01x slower                                  |
| regex_effbot               | 3.21 ms                                                                | 3.26 ms: 1.02x slower                                  |
| xml_etree_parse            | 136 ms                                                                 | 139 ms: 1.03x slower                                   |
| scimark_lu                 | 112 ms                                                                 | 115 ms: 1.03x slower                                   |
| telco                      | 7.77 ms                                                                | 8.02 ms: 1.03x slower                                  |
| coverage                   | 82.5 ms                                                                | 85.3 ms: 1.03x slower                                  |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.92 ms: 1.04x slower                                  |
| json                       | 4.98 ms                                                                | 5.18 ms: 1.04x slower                                  |
| richards                   | 44.4 ms                                                                | 46.6 ms: 1.05x slower                                  |
| regex_compile              | 131 ms                                                                 | 138 ms: 1.05x slower                                   |
| scimark_monte_carlo        | 65.8 ms                                                                | 69.3 ms: 1.05x slower                                  |
| logging_simple             | 6.14 us                                                                | 6.48 us: 1.05x slower                                  |
| tomli_loads                | 2.01 sec                                                               | 2.13 sec: 1.06x slower                                 |
| 2to3                       | 259 ms                                                                 | 275 ms: 1.06x slower                                   |
| genshi_xml                 | 49.1 ms                                                                | 52.0 ms: 1.06x slower                                  |
| comprehensions             | 16.6 us                                                                | 17.6 us: 1.06x slower                                  |
| regex_dna                  | 189 ms                                                                 | 202 ms: 1.07x slower                                   |
| pprint_safe_repr           | 719 ms                                                                 | 769 ms: 1.07x slower                                   |
| logging_format             | 6.92 us                                                                | 7.41 us: 1.07x slower                                  |
| unpickle_pure_python       | 208 us                                                                 | 224 us: 1.08x slower                                   |
| chaos                      | 56.3 ms                                                                | 60.7 ms: 1.08x slower                                  |
| thrift                     | 772 us                                                                 | 832 us: 1.08x slower                                   |
| django_template            | 34.2 ms                                                                | 37.0 ms: 1.08x slower                                  |
| json_loads                 | 27.3 us                                                                | 29.7 us: 1.09x slower                                  |
| nqueens                    | 77.7 ms                                                                | 84.7 ms: 1.09x slower                                  |
| richards_super             | 50.4 ms                                                                | 55.0 ms: 1.09x slower                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.59 sec: 1.09x slower                                 |
| sympy_expand               | 454 ms                                                                 | 500 ms: 1.10x slower                                   |
| hexiom                     | 5.95 ms                                                                | 6.57 ms: 1.10x slower                                  |
| typing_runtime_protocols   | 156 us                                                                 | 172 us: 1.11x slower                                   |
| sympy_str                  | 274 ms                                                                 | 304 ms: 1.11x slower                                   |
| sympy_sum                  | 154 ms                                                                 | 171 ms: 1.11x slower                                   |
| sympy_integrate            | 19.7 ms                                                                | 22.0 ms: 1.11x slower                                  |
| pickle_pure_python         | 292 us                                                                 | 325 us: 1.11x slower                                   |
| genshi_text                | 21.7 ms                                                                | 24.2 ms: 1.12x slower                                  |
| raytrace                   | 250 ms                                                                 | 283 ms: 1.13x slower                                   |
| deltablue                  | 3.10 ms                                                                | 3.52 ms: 1.14x slower                                  |
| fannkuch                   | 376 ms                                                                 | 435 ms: 1.16x slower                                   |
| crypto_pyaes               | 68.2 ms                                                                | 79.5 ms: 1.17x slower                                  |
| mdp                        | 2.34 sec                                                               | 2.74 sec: 1.17x slower                                 |
| json_dumps                 | 10.6 ms                                                                | 12.5 ms: 1.18x slower                                  |
| meteor_contest             | 101 ms                                                                 | 122 ms: 1.21x slower                                   |
| mako                       | 11.2 ms                                                                | 14.8 ms: 1.32x slower                                  |
| nbody                      | 85.3 ms                                                                | 119 ms: 1.40x slower                                   |
| python_startup             | 11.0 ms                                                                | 15.5 ms: 1.40x slower                                  |
| python_startup_no_site     | 7.41 ms                                                                | 11.0 ms: 1.48x slower                                  |
| bench_thread_pool          | 924 us                                                                 | 3.11 ms: 3.36x slower                                  |
| bench_mp_pool              | 11.0 ms                                                                | 95.1 ms: 8.65x slower                                  |
| Geometric mean             | (ref)                                                                  | 1.02x slower                                           |

Benchmark hidden because not significant (4): asyncio_websockets, docutils, pycparser, create_gc_cycles
Ignored benchmarks (18) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250318-3.14.0a6+-c1b42db-CLANG,NOGIL/bm-20250318-vultr-x86_64-python-main-3.14.0a6+-c1b42db.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.015x faster

# HPT report

- Reliability score: 79.80% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.39x