# Results vs. 3.13.0rc2

- fork: python
- ref: 0dbaeb94a8b39972ebda
- machine: linux-x86_64
- commit hash: 0dbaeb9
- commit date: 2025-04-03
- overall geometric mean: 1.032x faster
- HPT reliability: 89.93%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250403-vultr-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 255 ms: 1.02x faster                                                   |
| docutils       | 2.63 sec                                                               | 2.60 sec: 1.01x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250403-vultr-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 630 ms: 1.43x faster                                                   |
| async_tree_memoization     | 459 ms                                                                 | 327 ms: 1.40x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 638 ms: 1.38x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 516 ms: 1.29x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 510 ms: 1.24x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 332 ms: 1.24x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 287 ms: 1.23x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 271 ms: 1.23x faster                                                   |
| async_generators           | 375 ms                                                                 | 336 ms: 1.11x faster                                                   |
| coroutines                 | 23.3 ms                                                                | 24.0 ms: 1.03x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.22x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250403-vultr-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 191 ms: 1.13x faster                                                   |
| float          | 76.7 ms                                                                | 72.0 ms: 1.07x faster                                                  |
| nbody          | 85.3 ms                                                                | 92.5 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250403-vultr-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.78 ms: 1.16x faster                                                  |
| regex_dna      | 189 ms                                                                 | 176 ms: 1.07x faster                                                   |
| regex_v8       | 23.2 ms                                                                | 22.0 ms: 1.05x faster                                                  |
| regex_compile  | 131 ms                                                                 | 131 ms: 1.00x faster                                                   |
| Geometric mean | (ref)                                                                  | 1.07x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250403-vultr-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                                 | 131 ms: 1.03x faster                                                   |
| json_loads           | 27.3 us                                                                | 27.5 us: 1.00x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                                | 86.9 ms: 1.02x slower                                                  |
| xml_etree_process    | 59.2 ms                                                                | 61.4 ms: 1.04x slower                                                  |
| json_dumps           | 10.6 ms                                                                | 11.2 ms: 1.05x slower                                                  |
| unpickle_pure_python | 208 us                                                                 | 223 us: 1.07x slower                                                   |
| pickle_pure_python   | 292 us                                                                 | 321 us: 1.10x slower                                                   |
| Geometric mean       | (ref)                                                                  | 1.03x slower                                                           |

Benchmark hidden because not significant (2): tomli_loads, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250403-vultr-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 8.72 ms: 1.18x slower                                                  |
| python_startup         | 11.0 ms                                                                | 15.2 ms: 1.38x slower                                                  |
| Geometric mean         | (ref)                                                                  | 1.27x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250403-vultr-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 21.7 ms                                                                | 22.2 ms: 1.02x slower                                                  |
| genshi_xml      | 49.1 ms                                                                | 50.7 ms: 1.03x slower                                                  |
| django_template | 34.2 ms                                                                | 36.8 ms: 1.08x slower                                                  |
| mako            | 11.2 ms                                                                | 12.2 ms: 1.09x slower                                                  |
| Geometric mean  | (ref)                                                                  | 1.05x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250403-vultr-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.34 sec                                                               | 1.18 sec: 1.98x faster                                                 |
| async_tree_io_tg           | 901 ms                                                                 | 630 ms: 1.43x faster                                                   |
| async_tree_memoization     | 459 ms                                                                 | 327 ms: 1.40x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 638 ms: 1.38x faster                                                   |
| deepcopy                   | 357 us                                                                 | 262 us: 1.36x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 516 ms: 1.29x faster                                                   |
| deepcopy_memo              | 38.1 us                                                                | 29.9 us: 1.27x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 510 ms: 1.24x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 332 ms: 1.24x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 287 ms: 1.23x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 271 ms: 1.23x faster                                                   |
| go                         | 141 ms                                                                 | 115 ms: 1.22x faster                                                   |
| scimark_sor                | 134 ms                                                                 | 114 ms: 1.17x faster                                                   |
| deepcopy_reduce            | 3.12 us                                                                | 2.70 us: 1.16x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.78 ms: 1.16x faster                                                  |
| pidigits                   | 216 ms                                                                 | 191 ms: 1.13x faster                                                   |
| async_generators           | 375 ms                                                                 | 336 ms: 1.11x faster                                                   |
| pylint                     | 317 ms                                                                 | 289 ms: 1.10x faster                                                   |
| spectral_norm              | 108 ms                                                                 | 98.5 ms: 1.09x faster                                                  |
| dulwich_log                | 74.5 ms                                                                | 68.6 ms: 1.08x faster                                                  |
| scimark_fft                | 348 ms                                                                 | 325 ms: 1.07x faster                                                   |
| regex_dna                  | 189 ms                                                                 | 176 ms: 1.07x faster                                                   |
| pyflate                    | 449 ms                                                                 | 419 ms: 1.07x faster                                                   |
| float                      | 76.7 ms                                                                | 72.0 ms: 1.07x faster                                                  |
| regex_v8                   | 23.2 ms                                                                | 22.0 ms: 1.05x faster                                                  |
| telco                      | 7.77 ms                                                                | 7.45 ms: 1.04x faster                                                  |
| scimark_monte_carlo        | 65.8 ms                                                                | 63.4 ms: 1.04x faster                                                  |
| xml_etree_parse            | 136 ms                                                                 | 131 ms: 1.03x faster                                                   |
| sqlite_synth               | 2.25 us                                                                | 2.19 us: 1.03x faster                                                  |
| coverage                   | 82.5 ms                                                                | 80.3 ms: 1.03x faster                                                  |
| json                       | 4.98 ms                                                                | 4.90 ms: 1.02x faster                                                  |
| 2to3                       | 259 ms                                                                 | 255 ms: 1.02x faster                                                   |
| bpe_tokeniser              | 4.46 sec                                                               | 4.40 sec: 1.01x faster                                                 |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.69 ms: 1.01x faster                                                  |
| docutils                   | 2.63 sec                                                               | 2.60 sec: 1.01x faster                                                 |
| richards                   | 44.4 ms                                                                | 44.1 ms: 1.01x faster                                                  |
| regex_compile              | 131 ms                                                                 | 131 ms: 1.00x faster                                                   |
| sympy_integrate            | 19.7 ms                                                                | 19.8 ms: 1.00x slower                                                  |
| json_loads                 | 27.3 us                                                                | 27.5 us: 1.00x slower                                                  |
| pathlib                    | 19.3 ms                                                                | 19.4 ms: 1.01x slower                                                  |
| logging_simple             | 6.14 us                                                                | 6.21 us: 1.01x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                                | 86.9 ms: 1.02x slower                                                  |
| genshi_text                | 21.7 ms                                                                | 22.2 ms: 1.02x slower                                                  |
| pycparser                  | 1.12 sec                                                               | 1.15 sec: 1.02x slower                                                 |
| raytrace                   | 250 ms                                                                 | 257 ms: 1.03x slower                                                   |
| coroutines                 | 23.3 ms                                                                | 24.0 ms: 1.03x slower                                                  |
| sympy_str                  | 274 ms                                                                 | 283 ms: 1.03x slower                                                   |
| pprint_safe_repr           | 719 ms                                                                 | 742 ms: 1.03x slower                                                   |
| genshi_xml                 | 49.1 ms                                                                | 50.7 ms: 1.03x slower                                                  |
| xml_etree_process          | 59.2 ms                                                                | 61.4 ms: 1.04x slower                                                  |
| hexiom                     | 5.95 ms                                                                | 6.18 ms: 1.04x slower                                                  |
| typing_runtime_protocols   | 156 us                                                                 | 162 us: 1.04x slower                                                   |
| logging_silent             | 98.2 ns                                                                | 102 ns: 1.04x slower                                                   |
| sympy_sum                  | 154 ms                                                                 | 160 ms: 1.04x slower                                                   |
| comprehensions             | 16.6 us                                                                | 17.2 us: 1.04x slower                                                  |
| crypto_pyaes               | 68.2 ms                                                                | 70.9 ms: 1.04x slower                                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.52 sec: 1.05x slower                                                 |
| fannkuch                   | 376 ms                                                                 | 395 ms: 1.05x slower                                                   |
| scimark_lu                 | 112 ms                                                                 | 118 ms: 1.05x slower                                                   |
| nqueens                    | 77.7 ms                                                                | 81.7 ms: 1.05x slower                                                  |
| json_dumps                 | 10.6 ms                                                                | 11.2 ms: 1.05x slower                                                  |
| sympy_expand               | 454 ms                                                                 | 479 ms: 1.06x slower                                                   |
| unpickle_pure_python       | 208 us                                                                 | 223 us: 1.07x slower                                                   |
| django_template            | 34.2 ms                                                                | 36.8 ms: 1.08x slower                                                  |
| nbody                      | 85.3 ms                                                                | 92.5 ms: 1.08x slower                                                  |
| deltablue                  | 3.10 ms                                                                | 3.36 ms: 1.09x slower                                                  |
| generators                 | 28.5 ms                                                                | 31.1 ms: 1.09x slower                                                  |
| mako                       | 11.2 ms                                                                | 12.2 ms: 1.09x slower                                                  |
| pickle_pure_python         | 292 us                                                                 | 321 us: 1.10x slower                                                   |
| bench_thread_pool          | 924 us                                                                 | 1.06 ms: 1.15x slower                                                  |
| python_startup_no_site     | 7.41 ms                                                                | 8.72 ms: 1.18x slower                                                  |
| python_startup             | 11.0 ms                                                                | 15.2 ms: 1.38x slower                                                  |
| create_gc_cycles           | 1.33 ms                                                                | 1.86 ms: 1.39x slower                                                  |
| gc_traversal               | 3.32 ms                                                                | 4.64 ms: 1.40x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                                | 89.7 ms: 8.15x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                           |

Benchmark hidden because not significant (7): tomli_loads, chaos, xml_etree_iterparse, asyncio_websockets, richards_super, logging_format, meteor_contest
Ignored benchmarks (20) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250403-3.14.0a6+-0dbaeb9/bm-20250403-vultr-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.032x faster

# HPT report

- Reliability score: 89.93% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.13x