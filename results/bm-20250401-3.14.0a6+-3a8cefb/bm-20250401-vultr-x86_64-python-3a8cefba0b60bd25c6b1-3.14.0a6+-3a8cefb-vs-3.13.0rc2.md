# Results vs. 3.13.0rc2

- fork: python
- ref: 3a8cefba0b60bd25c6b1
- machine: linux-x86_64
- commit hash: 3a8cefb
- commit date: 2025-04-01
- overall geometric mean: 1.034x faster
- HPT reliability: 88.74%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 256 ms: 1.01x faster                                                   |
| docutils       | 2.63 sec                                                               | 2.61 sec: 1.01x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_memoization     | 459 ms                                                                 | 327 ms: 1.41x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 638 ms: 1.38x faster                                                   |
| async_tree_io_tg           | 901 ms                                                                 | 653 ms: 1.38x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 518 ms: 1.29x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 325 ms: 1.26x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 266 ms: 1.25x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 508 ms: 1.25x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 284 ms: 1.24x faster                                                   |
| async_generators           | 375 ms                                                                 | 340 ms: 1.10x faster                                                   |
| coroutines                 | 23.3 ms                                                                | 24.0 ms: 1.03x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.22x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 197 ms: 1.10x faster                                                   |
| float          | 76.7 ms                                                                | 73.2 ms: 1.05x faster                                                  |
| nbody          | 85.3 ms                                                                | 94.6 ms: 1.11x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.82 ms: 1.14x faster                                                  |
| regex_dna      | 189 ms                                                                 | 179 ms: 1.06x faster                                                   |
| regex_v8       | 23.2 ms                                                                | 22.2 ms: 1.04x faster                                                  |
| regex_compile  | 131 ms                                                                 | 132 ms: 1.00x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                                 | 130 ms: 1.04x faster                                                   |
| json_loads           | 27.3 us                                                                | 27.1 us: 1.01x faster                                                  |
| xml_etree_generate   | 85.4 ms                                                                | 86.2 ms: 1.01x slower                                                  |
| xml_etree_process    | 59.2 ms                                                                | 61.3 ms: 1.04x slower                                                  |
| json_dumps           | 10.6 ms                                                                | 11.3 ms: 1.07x slower                                                  |
| unpickle_pure_python | 208 us                                                                 | 223 us: 1.07x slower                                                   |
| pickle_pure_python   | 292 us                                                                 | 320 us: 1.10x slower                                                   |
| Geometric mean       | (ref)                                                                  | 1.02x slower                                                           |

Benchmark hidden because not significant (2): xml_etree_iterparse, tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 8.65 ms: 1.17x slower                                                  |
| python_startup         | 11.0 ms                                                                | 15.1 ms: 1.37x slower                                                  |
| Geometric mean         | (ref)                                                                  | 1.27x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 50.3 ms: 1.03x slower                                                  |
| django_template | 34.2 ms                                                                | 36.6 ms: 1.07x slower                                                  |
| mako            | 11.2 ms                                                                | 12.2 ms: 1.09x slower                                                  |
| Geometric mean  | (ref)                                                                  | 1.05x slower                                                           |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.34 sec                                                               | 1.18 sec: 1.98x faster                                                 |
| async_tree_memoization     | 459 ms                                                                 | 327 ms: 1.41x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 638 ms: 1.38x faster                                                   |
| async_tree_io_tg           | 901 ms                                                                 | 653 ms: 1.38x faster                                                   |
| deepcopy                   | 357 us                                                                 | 260 us: 1.37x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 518 ms: 1.29x faster                                                   |
| deepcopy_memo              | 38.1 us                                                                | 29.9 us: 1.27x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 325 ms: 1.26x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 266 ms: 1.25x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 508 ms: 1.25x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 284 ms: 1.24x faster                                                   |
| go                         | 141 ms                                                                 | 114 ms: 1.23x faster                                                   |
| scimark_sor                | 134 ms                                                                 | 114 ms: 1.17x faster                                                   |
| deepcopy_reduce            | 3.12 us                                                                | 2.71 us: 1.15x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.82 ms: 1.14x faster                                                  |
| async_generators           | 375 ms                                                                 | 340 ms: 1.10x faster                                                   |
| pylint                     | 317 ms                                                                 | 288 ms: 1.10x faster                                                   |
| pidigits                   | 216 ms                                                                 | 197 ms: 1.10x faster                                                   |
| spectral_norm              | 108 ms                                                                 | 99.1 ms: 1.09x faster                                                  |
| scimark_fft                | 348 ms                                                                 | 321 ms: 1.08x faster                                                   |
| dulwich_log                | 74.5 ms                                                                | 68.7 ms: 1.08x faster                                                  |
| pyflate                    | 449 ms                                                                 | 417 ms: 1.08x faster                                                   |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.46 ms: 1.07x faster                                                  |
| regex_dna                  | 189 ms                                                                 | 179 ms: 1.06x faster                                                   |
| float                      | 76.7 ms                                                                | 73.2 ms: 1.05x faster                                                  |
| telco                      | 7.77 ms                                                                | 7.41 ms: 1.05x faster                                                  |
| xml_etree_parse            | 136 ms                                                                 | 130 ms: 1.04x faster                                                   |
| regex_v8                   | 23.2 ms                                                                | 22.2 ms: 1.04x faster                                                  |
| coverage                   | 82.5 ms                                                                | 79.4 ms: 1.04x faster                                                  |
| scimark_monte_carlo        | 65.8 ms                                                                | 63.4 ms: 1.04x faster                                                  |
| bpe_tokeniser              | 4.46 sec                                                               | 4.36 sec: 1.02x faster                                                 |
| sqlite_synth               | 2.25 us                                                                | 2.21 us: 1.02x faster                                                  |
| richards                   | 44.4 ms                                                                | 43.7 ms: 1.02x faster                                                  |
| json                       | 4.98 ms                                                                | 4.91 ms: 1.01x faster                                                  |
| 2to3                       | 259 ms                                                                 | 256 ms: 1.01x faster                                                   |
| richards_super             | 50.4 ms                                                                | 49.8 ms: 1.01x faster                                                  |
| docutils                   | 2.63 sec                                                               | 2.61 sec: 1.01x faster                                                 |
| json_loads                 | 27.3 us                                                                | 27.1 us: 1.01x faster                                                  |
| chaos                      | 56.3 ms                                                                | 56.0 ms: 1.00x faster                                                  |
| regex_compile              | 131 ms                                                                 | 132 ms: 1.00x slower                                                   |
| pathlib                    | 19.3 ms                                                                | 19.4 ms: 1.01x slower                                                  |
| sympy_integrate            | 19.7 ms                                                                | 19.9 ms: 1.01x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                                | 86.2 ms: 1.01x slower                                                  |
| logging_format             | 6.92 us                                                                | 7.01 us: 1.01x slower                                                  |
| logging_simple             | 6.14 us                                                                | 6.26 us: 1.02x slower                                                  |
| genshi_xml                 | 49.1 ms                                                                | 50.3 ms: 1.03x slower                                                  |
| pprint_safe_repr           | 719 ms                                                                 | 737 ms: 1.03x slower                                                   |
| logging_silent             | 98.2 ns                                                                | 101 ns: 1.03x slower                                                   |
| pycparser                  | 1.12 sec                                                               | 1.15 sec: 1.03x slower                                                 |
| coroutines                 | 23.3 ms                                                                | 24.0 ms: 1.03x slower                                                  |
| typing_runtime_protocols   | 156 us                                                                 | 161 us: 1.03x slower                                                   |
| crypto_pyaes               | 68.2 ms                                                                | 70.5 ms: 1.03x slower                                                  |
| sympy_str                  | 274 ms                                                                 | 283 ms: 1.03x slower                                                   |
| xml_etree_process          | 59.2 ms                                                                | 61.3 ms: 1.04x slower                                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.51 sec: 1.04x slower                                                 |
| hexiom                     | 5.95 ms                                                                | 6.18 ms: 1.04x slower                                                  |
| raytrace                   | 250 ms                                                                 | 260 ms: 1.04x slower                                                   |
| comprehensions             | 16.6 us                                                                | 17.3 us: 1.05x slower                                                  |
| fannkuch                   | 376 ms                                                                 | 394 ms: 1.05x slower                                                   |
| nqueens                    | 77.7 ms                                                                | 81.8 ms: 1.05x slower                                                  |
| sympy_sum                  | 154 ms                                                                 | 162 ms: 1.05x slower                                                   |
| scimark_lu                 | 112 ms                                                                 | 118 ms: 1.05x slower                                                   |
| sympy_expand               | 454 ms                                                                 | 480 ms: 1.06x slower                                                   |
| json_dumps                 | 10.6 ms                                                                | 11.3 ms: 1.07x slower                                                  |
| django_template            | 34.2 ms                                                                | 36.6 ms: 1.07x slower                                                  |
| unpickle_pure_python       | 208 us                                                                 | 223 us: 1.07x slower                                                   |
| deltablue                  | 3.10 ms                                                                | 3.36 ms: 1.09x slower                                                  |
| mako                       | 11.2 ms                                                                | 12.2 ms: 1.09x slower                                                  |
| generators                 | 28.5 ms                                                                | 31.2 ms: 1.09x slower                                                  |
| pickle_pure_python         | 292 us                                                                 | 320 us: 1.10x slower                                                   |
| nbody                      | 85.3 ms                                                                | 94.6 ms: 1.11x slower                                                  |
| bench_thread_pool          | 924 us                                                                 | 1.06 ms: 1.15x slower                                                  |
| python_startup_no_site     | 7.41 ms                                                                | 8.65 ms: 1.17x slower                                                  |
| gc_traversal               | 3.32 ms                                                                | 4.19 ms: 1.26x slower                                                  |
| python_startup             | 11.0 ms                                                                | 15.1 ms: 1.37x slower                                                  |
| create_gc_cycles           | 1.33 ms                                                                | 1.84 ms: 1.38x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                                | 90.1 ms: 8.19x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (5): asyncio_websockets, xml_etree_iterparse, tomli_loads, meteor_contest, genshi_text
Ignored benchmarks (20) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250401-3.14.0a6+-3a8cefb/bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.034x faster

# HPT report

- Reliability score: 88.74% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.13x