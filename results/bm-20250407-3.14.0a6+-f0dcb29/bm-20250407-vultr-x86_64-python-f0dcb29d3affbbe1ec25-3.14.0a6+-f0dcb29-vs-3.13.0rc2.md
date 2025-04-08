# Results vs. 3.13.0rc2

- fork: python
- ref: f0dcb29d3affbbe1ec25
- machine: linux-x86_64
- commit hash: f0dcb29
- commit date: 2025-04-07
- overall geometric mean: 1.039x faster
- HPT reliability: 96.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 255 ms: 1.02x faster                                                   |
| docutils       | 2.63 sec                                                               | 2.58 sec: 1.02x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_memoization     | 459 ms                                                                 | 321 ms: 1.43x faster                                                   |
| async_tree_io_tg           | 901 ms                                                                 | 631 ms: 1.43x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 632 ms: 1.39x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 503 ms: 1.33x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 499 ms: 1.27x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 324 ms: 1.26x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 265 ms: 1.26x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 282 ms: 1.25x faster                                                   |
| async_generators           | 375 ms                                                                 | 337 ms: 1.11x faster                                                   |
| coroutines                 | 23.3 ms                                                                | 24.5 ms: 1.05x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.23x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 190 ms: 1.14x faster                                                   |
| float          | 76.7 ms                                                                | 71.4 ms: 1.08x faster                                                  |
| nbody          | 85.3 ms                                                                | 92.6 ms: 1.09x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.84 ms: 1.13x faster                                                  |
| regex_v8       | 23.2 ms                                                                | 22.1 ms: 1.05x faster                                                  |
| regex_dna      | 189 ms                                                                 | 181 ms: 1.04x faster                                                   |
| regex_compile  | 131 ms                                                                 | 130 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                                 | 130 ms: 1.05x faster                                                   |
| tomli_loads          | 2.01 sec                                                               | 1.99 sec: 1.01x faster                                                 |
| xml_etree_iterparse  | 94.4 ms                                                                | 93.7 ms: 1.01x faster                                                  |
| json_loads           | 27.3 us                                                                | 27.7 us: 1.01x slower                                                  |
| xml_etree_process    | 59.2 ms                                                                | 60.6 ms: 1.02x slower                                                  |
| json_dumps           | 10.6 ms                                                                | 11.2 ms: 1.06x slower                                                  |
| unpickle_pure_python | 208 us                                                                 | 222 us: 1.07x slower                                                   |
| pickle_pure_python   | 292 us                                                                 | 322 us: 1.10x slower                                                   |
| Geometric mean       | (ref)                                                                  | 1.02x slower                                                           |

Benchmark hidden because not significant (1): xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 8.64 ms: 1.17x slower                                                  |
| python_startup         | 11.0 ms                                                                | 15.1 ms: 1.37x slower                                                  |
| Geometric mean         | (ref)                                                                  | 1.26x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 21.7 ms                                                                | 22.0 ms: 1.01x slower                                                  |
| genshi_xml      | 49.1 ms                                                                | 50.5 ms: 1.03x slower                                                  |
| django_template | 34.2 ms                                                                | 36.6 ms: 1.07x slower                                                  |
| mako            | 11.2 ms                                                                | 12.2 ms: 1.09x slower                                                  |
| Geometric mean  | (ref)                                                                  | 1.05x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.34 sec                                                               | 1.18 sec: 1.98x faster                                                 |
| async_tree_memoization     | 459 ms                                                                 | 321 ms: 1.43x faster                                                   |
| async_tree_io_tg           | 901 ms                                                                 | 631 ms: 1.43x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 632 ms: 1.39x faster                                                   |
| deepcopy                   | 357 us                                                                 | 262 us: 1.36x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 503 ms: 1.33x faster                                                   |
| deepcopy_memo              | 38.1 us                                                                | 29.7 us: 1.28x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 499 ms: 1.27x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 324 ms: 1.26x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 265 ms: 1.26x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 282 ms: 1.25x faster                                                   |
| go                         | 141 ms                                                                 | 114 ms: 1.23x faster                                                   |
| deepcopy_reduce            | 3.12 us                                                                | 2.69 us: 1.16x faster                                                  |
| scimark_sor                | 134 ms                                                                 | 115 ms: 1.16x faster                                                   |
| pidigits                   | 216 ms                                                                 | 190 ms: 1.14x faster                                                   |
| regex_effbot               | 3.21 ms                                                                | 2.84 ms: 1.13x faster                                                  |
| async_generators           | 375 ms                                                                 | 337 ms: 1.11x faster                                                   |
| pylint                     | 317 ms                                                                 | 287 ms: 1.10x faster                                                   |
| spectral_norm              | 108 ms                                                                 | 98.0 ms: 1.10x faster                                                  |
| scimark_fft                | 348 ms                                                                 | 321 ms: 1.09x faster                                                   |
| dulwich_log                | 74.5 ms                                                                | 68.9 ms: 1.08x faster                                                  |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.40 ms: 1.08x faster                                                  |
| float                      | 76.7 ms                                                                | 71.4 ms: 1.08x faster                                                  |
| pyflate                    | 449 ms                                                                 | 420 ms: 1.07x faster                                                   |
| telco                      | 7.77 ms                                                                | 7.29 ms: 1.07x faster                                                  |
| regex_v8                   | 23.2 ms                                                                | 22.1 ms: 1.05x faster                                                  |
| xml_etree_parse            | 136 ms                                                                 | 130 ms: 1.05x faster                                                   |
| regex_dna                  | 189 ms                                                                 | 181 ms: 1.04x faster                                                   |
| coverage                   | 82.5 ms                                                                | 79.9 ms: 1.03x faster                                                  |
| scimark_monte_carlo        | 65.8 ms                                                                | 63.8 ms: 1.03x faster                                                  |
| sqlite_synth               | 2.25 us                                                                | 2.18 us: 1.03x faster                                                  |
| bpe_tokeniser              | 4.46 sec                                                               | 4.35 sec: 1.02x faster                                                 |
| 2to3                       | 259 ms                                                                 | 255 ms: 1.02x faster                                                   |
| docutils                   | 2.63 sec                                                               | 2.58 sec: 1.02x faster                                                 |
| tomli_loads                | 2.01 sec                                                               | 1.99 sec: 1.01x faster                                                 |
| regex_compile              | 131 ms                                                                 | 130 ms: 1.01x faster                                                   |
| meteor_contest             | 101 ms                                                                 | 101 ms: 1.01x faster                                                   |
| sympy_integrate            | 19.7 ms                                                                | 19.6 ms: 1.01x faster                                                  |
| xml_etree_iterparse        | 94.4 ms                                                                | 93.7 ms: 1.01x faster                                                  |
| chaos                      | 56.3 ms                                                                | 55.9 ms: 1.01x faster                                                  |
| genshi_text                | 21.7 ms                                                                | 22.0 ms: 1.01x slower                                                  |
| json_loads                 | 27.3 us                                                                | 27.7 us: 1.01x slower                                                  |
| logging_simple             | 6.14 us                                                                | 6.24 us: 1.02x slower                                                  |
| pprint_safe_repr           | 719 ms                                                                 | 732 ms: 1.02x slower                                                   |
| pathlib                    | 19.3 ms                                                                | 19.7 ms: 1.02x slower                                                  |
| crypto_pyaes               | 68.2 ms                                                                | 69.7 ms: 1.02x slower                                                  |
| xml_etree_process          | 59.2 ms                                                                | 60.6 ms: 1.02x slower                                                  |
| generators                 | 28.5 ms                                                                | 29.2 ms: 1.02x slower                                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.49 sec: 1.02x slower                                                 |
| logging_silent             | 98.2 ns                                                                | 101 ns: 1.02x slower                                                   |
| sympy_str                  | 274 ms                                                                 | 281 ms: 1.02x slower                                                   |
| hexiom                     | 5.95 ms                                                                | 6.12 ms: 1.03x slower                                                  |
| genshi_xml                 | 49.1 ms                                                                | 50.5 ms: 1.03x slower                                                  |
| sympy_sum                  | 154 ms                                                                 | 159 ms: 1.03x slower                                                   |
| sympy_expand               | 454 ms                                                                 | 471 ms: 1.04x slower                                                   |
| nqueens                    | 77.7 ms                                                                | 80.8 ms: 1.04x slower                                                  |
| raytrace                   | 250 ms                                                                 | 260 ms: 1.04x slower                                                   |
| scimark_lu                 | 112 ms                                                                 | 117 ms: 1.04x slower                                                   |
| pycparser                  | 1.12 sec                                                               | 1.17 sec: 1.04x slower                                                 |
| comprehensions             | 16.6 us                                                                | 17.3 us: 1.04x slower                                                  |
| typing_runtime_protocols   | 156 us                                                                 | 162 us: 1.04x slower                                                   |
| coroutines                 | 23.3 ms                                                                | 24.5 ms: 1.05x slower                                                  |
| fannkuch                   | 376 ms                                                                 | 396 ms: 1.05x slower                                                   |
| json_dumps                 | 10.6 ms                                                                | 11.2 ms: 1.06x slower                                                  |
| unpickle_pure_python       | 208 us                                                                 | 222 us: 1.07x slower                                                   |
| django_template            | 34.2 ms                                                                | 36.6 ms: 1.07x slower                                                  |
| deltablue                  | 3.10 ms                                                                | 3.36 ms: 1.08x slower                                                  |
| nbody                      | 85.3 ms                                                                | 92.6 ms: 1.09x slower                                                  |
| mako                       | 11.2 ms                                                                | 12.2 ms: 1.09x slower                                                  |
| pickle_pure_python         | 292 us                                                                 | 322 us: 1.10x slower                                                   |
| bench_thread_pool          | 924 us                                                                 | 1.06 ms: 1.14x slower                                                  |
| python_startup_no_site     | 7.41 ms                                                                | 8.64 ms: 1.17x slower                                                  |
| gc_traversal               | 3.32 ms                                                                | 4.26 ms: 1.28x slower                                                  |
| python_startup             | 11.0 ms                                                                | 15.1 ms: 1.37x slower                                                  |
| create_gc_cycles           | 1.33 ms                                                                | 1.84 ms: 1.38x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                                | 88.9 ms: 8.08x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (6): json, xml_etree_generate, richards_super, asyncio_websockets, logging_format, richards
Ignored benchmarks (20) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250407-3.14.0a6+-f0dcb29/bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.039x faster

# HPT report

- Reliability score: 96.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.12x