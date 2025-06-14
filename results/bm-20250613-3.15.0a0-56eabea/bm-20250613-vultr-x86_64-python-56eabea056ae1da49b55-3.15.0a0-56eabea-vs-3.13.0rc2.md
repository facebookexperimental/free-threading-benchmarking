# Results vs. 3.13.0rc2

- fork: python
- ref: 56eabea056ae1da49b55
- machine: linux-x86_64
- commit hash: 56eabea
- commit date: 2025-06-13
- overall geometric mean: 1.074x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250613-vultr-x86_64-python-56eabea056ae1da49b55-3.15.0a0-56eabea |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 248 ms: 1.05x faster                                                  |
| docutils       | 2.63 sec                                                               | 2.52 sec: 1.04x faster                                                |
| html5lib       | 68.6 ms                                                                | 61.3 ms: 1.12x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.07x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250613-vultr-x86_64-python-56eabea056ae1da49b55-3.15.0a0-56eabea |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization     | 459 ms                                                                 | 305 ms: 1.50x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 619 ms: 1.46x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 606 ms: 1.45x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 498 ms: 1.34x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 308 ms: 1.33x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 251 ms: 1.33x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 267 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 497 ms: 1.28x faster                                                  |
| async_generators           | 375 ms                                                                 | 336 ms: 1.12x faster                                                  |
| Geometric mean             | (ref)                                                                  | 1.27x faster                                                          |

Benchmark hidden because not significant (2): asyncio_websockets, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250613-vultr-x86_64-python-56eabea056ae1da49b55-3.15.0a0-56eabea |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 76.7 ms                                                                | 71.0 ms: 1.08x faster                                                 |
| pidigits       | 216 ms                                                                 | 206 ms: 1.05x faster                                                  |
| nbody          | 85.3 ms                                                                | 88.0 ms: 1.03x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250613-vultr-x86_64-python-56eabea056ae1da49b55-3.15.0a0-56eabea |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.63 ms: 1.22x faster                                                 |
| regex_dna      | 189 ms                                                                 | 171 ms: 1.10x faster                                                  |
| regex_v8       | 23.2 ms                                                                | 21.6 ms: 1.08x faster                                                 |
| regex_compile  | 131 ms                                                                 | 123 ms: 1.07x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.12x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250613-vultr-x86_64-python-56eabea056ae1da49b55-3.15.0a0-56eabea |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                               | 1.91 sec: 1.05x faster                                                |
| xml_etree_generate   | 85.4 ms                                                                | 82.6 ms: 1.03x faster                                                 |
| xml_etree_parse      | 136 ms                                                                 | 132 ms: 1.03x faster                                                  |
| xml_etree_iterparse  | 94.4 ms                                                                | 92.1 ms: 1.03x faster                                                 |
| xml_etree_process    | 59.2 ms                                                                | 58.5 ms: 1.01x faster                                                 |
| unpickle_pure_python | 208 us                                                                 | 208 us: 1.00x faster                                                  |
| json_dumps           | 10.6 ms                                                                | 10.8 ms: 1.01x slower                                                 |
| pickle_pure_python   | 292 us                                                                 | 304 us: 1.04x slower                                                  |
| json_loads           | 27.3 us                                                                | 28.6 us: 1.05x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250613-vultr-x86_64-python-56eabea056ae1da49b55-3.15.0a0-56eabea |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 7.27 ms: 1.02x faster                                                 |
| python_startup         | 11.0 ms                                                                | 12.5 ms: 1.14x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.06x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250613-vultr-x86_64-python-56eabea056ae1da49b55-3.15.0a0-56eabea |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text    | 21.7 ms                                                                | 20.0 ms: 1.09x faster                                                 |
| genshi_xml     | 49.1 ms                                                                | 47.2 ms: 1.04x faster                                                 |
| mako           | 11.2 ms                                                                | 11.8 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250613-vultr-x86_64-python-56eabea056ae1da49b55-3.15.0a0-56eabea |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.34 sec                                                               | 1.15 sec: 2.04x faster                                                |
| async_tree_memoization     | 459 ms                                                                 | 305 ms: 1.50x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 619 ms: 1.46x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 606 ms: 1.45x faster                                                  |
| deepcopy                   | 357 us                                                                 | 250 us: 1.43x faster                                                  |
| go                         | 141 ms                                                                 | 105 ms: 1.34x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 498 ms: 1.34x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 308 ms: 1.33x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 251 ms: 1.33x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 267 ms: 1.32x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 28.9 us: 1.32x faster                                                 |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 497 ms: 1.28x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.63 ms: 1.22x faster                                                 |
| scimark_sor                | 134 ms                                                                 | 111 ms: 1.21x faster                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 2.65 us: 1.18x faster                                                 |
| pylint                     | 317 ms                                                                 | 279 ms: 1.14x faster                                                  |
| pyflate                    | 449 ms                                                                 | 398 ms: 1.13x faster                                                  |
| html5lib                   | 68.6 ms                                                                | 61.3 ms: 1.12x faster                                                 |
| async_generators           | 375 ms                                                                 | 336 ms: 1.12x faster                                                  |
| dulwich_log                | 74.5 ms                                                                | 66.7 ms: 1.12x faster                                                 |
| spectral_norm              | 108 ms                                                                 | 97.4 ms: 1.10x faster                                                 |
| regex_dna                  | 189 ms                                                                 | 171 ms: 1.10x faster                                                  |
| genshi_text                | 21.7 ms                                                                | 20.0 ms: 1.09x faster                                                 |
| float                      | 76.7 ms                                                                | 71.0 ms: 1.08x faster                                                 |
| bpe_tokeniser              | 4.46 sec                                                               | 4.13 sec: 1.08x faster                                                |
| richards                   | 44.4 ms                                                                | 41.2 ms: 1.08x faster                                                 |
| richards_super             | 50.4 ms                                                                | 46.8 ms: 1.08x faster                                                 |
| regex_v8                   | 23.2 ms                                                                | 21.6 ms: 1.08x faster                                                 |
| telco                      | 7.77 ms                                                                | 7.23 ms: 1.08x faster                                                 |
| hexiom                     | 5.95 ms                                                                | 5.54 ms: 1.08x faster                                                 |
| scimark_monte_carlo        | 65.8 ms                                                                | 61.3 ms: 1.07x faster                                                 |
| regex_compile              | 131 ms                                                                 | 123 ms: 1.07x faster                                                  |
| scimark_fft                | 348 ms                                                                 | 328 ms: 1.06x faster                                                  |
| comprehensions             | 16.6 us                                                                | 15.6 us: 1.06x faster                                                 |
| thrift                     | 772 us                                                                 | 729 us: 1.06x faster                                                  |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.49 ms: 1.06x faster                                                 |
| sympy_integrate            | 19.7 ms                                                                | 18.7 ms: 1.05x faster                                                 |
| tomli_loads                | 2.01 sec                                                               | 1.91 sec: 1.05x faster                                                |
| pidigits                   | 216 ms                                                                 | 206 ms: 1.05x faster                                                  |
| 2to3                       | 259 ms                                                                 | 248 ms: 1.05x faster                                                  |
| generators                 | 28.5 ms                                                                | 27.3 ms: 1.05x faster                                                 |
| docutils                   | 2.63 sec                                                               | 2.52 sec: 1.04x faster                                                |
| genshi_xml                 | 49.1 ms                                                                | 47.2 ms: 1.04x faster                                                 |
| nqueens                    | 77.7 ms                                                                | 74.9 ms: 1.04x faster                                                 |
| xml_etree_generate         | 85.4 ms                                                                | 82.6 ms: 1.03x faster                                                 |
| sympy_str                  | 274 ms                                                                 | 265 ms: 1.03x faster                                                  |
| xml_etree_parse            | 136 ms                                                                 | 132 ms: 1.03x faster                                                  |
| pycparser                  | 1.12 sec                                                               | 1.09 sec: 1.03x faster                                                |
| meteor_contest             | 101 ms                                                                 | 98.7 ms: 1.03x faster                                                 |
| xml_etree_iterparse        | 94.4 ms                                                                | 92.1 ms: 1.03x faster                                                 |
| scimark_lu                 | 112 ms                                                                 | 110 ms: 1.02x faster                                                  |
| typing_runtime_protocols   | 156 us                                                                 | 152 us: 1.02x faster                                                  |
| sympy_expand               | 454 ms                                                                 | 444 ms: 1.02x faster                                                  |
| python_startup_no_site     | 7.41 ms                                                                | 7.27 ms: 1.02x faster                                                 |
| sympy_sum                  | 154 ms                                                                 | 152 ms: 1.02x faster                                                  |
| coverage                   | 82.5 ms                                                                | 81.2 ms: 1.02x faster                                                 |
| xml_etree_process          | 59.2 ms                                                                | 58.5 ms: 1.01x faster                                                 |
| chaos                      | 56.3 ms                                                                | 55.8 ms: 1.01x faster                                                 |
| crypto_pyaes               | 68.2 ms                                                                | 67.6 ms: 1.01x faster                                                 |
| unpickle_pure_python       | 208 us                                                                 | 208 us: 1.00x faster                                                  |
| raytrace                   | 250 ms                                                                 | 249 ms: 1.00x faster                                                  |
| fannkuch                   | 376 ms                                                                 | 378 ms: 1.01x slower                                                  |
| json_dumps                 | 10.6 ms                                                                | 10.8 ms: 1.01x slower                                                 |
| json                       | 4.98 ms                                                                | 5.10 ms: 1.02x slower                                                 |
| nbody                      | 85.3 ms                                                                | 88.0 ms: 1.03x slower                                                 |
| pickle_pure_python         | 292 us                                                                 | 304 us: 1.04x slower                                                  |
| json_loads                 | 27.3 us                                                                | 28.6 us: 1.05x slower                                                 |
| deltablue                  | 3.10 ms                                                                | 3.24 ms: 1.05x slower                                                 |
| mako                       | 11.2 ms                                                                | 11.8 ms: 1.05x slower                                                 |
| pprint_safe_repr           | 719 ms                                                                 | 764 ms: 1.06x slower                                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.56 sec: 1.07x slower                                                |
| logging_format             | 6.92 us                                                                | 7.44 us: 1.08x slower                                                 |
| logging_simple             | 6.14 us                                                                | 6.71 us: 1.09x slower                                                 |
| bench_thread_pool          | 924 us                                                                 | 1.04 ms: 1.12x slower                                                 |
| python_startup             | 11.0 ms                                                                | 12.5 ms: 1.14x slower                                                 |
| gc_traversal               | 3.32 ms                                                                | 4.40 ms: 1.33x slower                                                 |
| create_gc_cycles           | 1.33 ms                                                                | 1.89 ms: 1.42x slower                                                 |
| logging_silent             | 98.2 ns                                                                | 469 ns: 4.78x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                                | 98.3 ms: 8.93x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (5): asyncio_websockets, pathlib, coroutines, django_template, sqlite_synth
Ignored benchmarks (18) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250613-3.15.0a0-56eabea/bm-20250613-vultr-x86_64-python-56eabea056ae1da49b55-3.15.0a0-56eabea.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.074x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.15x