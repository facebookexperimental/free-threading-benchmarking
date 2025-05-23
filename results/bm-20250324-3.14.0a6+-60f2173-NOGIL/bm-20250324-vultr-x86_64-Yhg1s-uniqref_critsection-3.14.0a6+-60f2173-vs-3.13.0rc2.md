# Results vs. 3.13.0rc2

- fork: Yhg1s
- ref: uniqref_critsection
- machine: linux-x86_64
- commit hash: 60f2173
- commit date: 2025-03-24
- overall geometric mean: 1.073x slower
- HPT reliability: 99.98%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.37x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250324-vultr-x86_64-Yhg1s-uniqref_critsection-3.14.0a6+-60f2173 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 297 ms: 1.14x slower                                                 |
| docutils       | 2.63 sec                                                               | 2.78 sec: 1.06x slower                                               |
| html5lib       | 68.6 ms                                                                | 70.4 ms: 1.03x slower                                                |
| Geometric mean | (ref)                                                                  | 1.07x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250324-vultr-x86_64-Yhg1s-uniqref_critsection-3.14.0a6+-60f2173 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 555 ms: 1.62x faster                                                 |
| async_tree_io              | 881 ms                                                                 | 588 ms: 1.50x faster                                                 |
| async_tree_none_tg         | 333 ms                                                                 | 239 ms: 1.39x faster                                                 |
| async_tree_memoization     | 459 ms                                                                 | 334 ms: 1.37x faster                                                 |
| async_tree_memoization_tg  | 410 ms                                                                 | 302 ms: 1.36x faster                                                 |
| async_tree_none            | 353 ms                                                                 | 278 ms: 1.27x faster                                                 |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 537 ms: 1.18x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 572 ms: 1.16x faster                                                 |
| coroutines                 | 23.3 ms                                                                | 23.0 ms: 1.01x faster                                                |
| Geometric mean             | (ref)                                                                  | 1.25x faster                                                         |

Benchmark hidden because not significant (2): asyncio_websockets, async_generators

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250324-vultr-x86_64-Yhg1s-uniqref_critsection-3.14.0a6+-60f2173 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 76.7 ms                                                                | 76.4 ms: 1.00x faster                                                |
| pidigits       | 216 ms                                                                 | 223 ms: 1.03x slower                                                 |
| nbody          | 85.3 ms                                                                | 131 ms: 1.53x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.16x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250324-vultr-x86_64-Yhg1s-uniqref_critsection-3.14.0a6+-60f2173 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.77 ms: 1.16x faster                                                |
| regex_v8       | 23.2 ms                                                                | 20.7 ms: 1.12x faster                                                |
| regex_dna      | 189 ms                                                                 | 174 ms: 1.08x faster                                                 |
| regex_compile  | 131 ms                                                                 | 152 ms: 1.16x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250324-vultr-x86_64-Yhg1s-uniqref_critsection-3.14.0a6+-60f2173 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                                 | 127 ms: 1.07x faster                                                 |
| xml_etree_iterparse  | 94.4 ms                                                                | 88.5 ms: 1.07x faster                                                |
| json_loads           | 27.3 us                                                                | 29.8 us: 1.09x slower                                                |
| xml_etree_generate   | 85.4 ms                                                                | 95.5 ms: 1.12x slower                                                |
| tomli_loads          | 2.01 sec                                                               | 2.29 sec: 1.14x slower                                               |
| xml_etree_process    | 59.2 ms                                                                | 69.6 ms: 1.17x slower                                                |
| unpickle_pure_python | 208 us                                                                 | 252 us: 1.21x slower                                                 |
| json_dumps           | 10.6 ms                                                                | 12.9 ms: 1.21x slower                                                |
| pickle_pure_python   | 292 us                                                                 | 358 us: 1.23x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.11x slower                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250324-vultr-x86_64-Yhg1s-uniqref_critsection-3.14.0a6+-60f2173 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 15.7 ms: 1.43x slower                                                |
| python_startup_no_site | 7.41 ms                                                                | 11.1 ms: 1.49x slower                                                |
| Geometric mean         | (ref)                                                                  | 1.46x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250324-vultr-x86_64-Yhg1s-uniqref_critsection-3.14.0a6+-60f2173 |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 58.7 ms: 1.20x slower                                                |
| django_template | 34.2 ms                                                                | 43.3 ms: 1.27x slower                                                |
| genshi_text     | 21.7 ms                                                                | 28.2 ms: 1.30x slower                                                |
| mako            | 11.2 ms                                                                | 15.9 ms: 1.42x slower                                                |
| Geometric mean  | (ref)                                                                  | 1.29x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250324-vultr-x86_64-Yhg1s-uniqref_critsection-3.14.0a6+-60f2173 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.81 ms: 1.83x faster                                                |
| async_tree_io_tg           | 901 ms                                                                 | 555 ms: 1.62x faster                                                 |
| async_tree_io              | 881 ms                                                                 | 588 ms: 1.50x faster                                                 |
| async_tree_none_tg         | 333 ms                                                                 | 239 ms: 1.39x faster                                                 |
| async_tree_memoization     | 459 ms                                                                 | 334 ms: 1.37x faster                                                 |
| async_tree_memoization_tg  | 410 ms                                                                 | 302 ms: 1.36x faster                                                 |
| async_tree_none            | 353 ms                                                                 | 278 ms: 1.27x faster                                                 |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 537 ms: 1.18x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 572 ms: 1.16x faster                                                 |
| regex_effbot               | 3.21 ms                                                                | 2.77 ms: 1.16x faster                                                |
| deepcopy                   | 357 us                                                                 | 313 us: 1.14x faster                                                 |
| regex_v8                   | 23.2 ms                                                                | 20.7 ms: 1.12x faster                                                |
| sqlite_synth               | 2.25 us                                                                | 2.03 us: 1.11x faster                                                |
| regex_dna                  | 189 ms                                                                 | 174 ms: 1.08x faster                                                 |
| xml_etree_parse            | 136 ms                                                                 | 127 ms: 1.07x faster                                                 |
| xml_etree_iterparse        | 94.4 ms                                                                | 88.5 ms: 1.07x faster                                                |
| dulwich_log                | 74.5 ms                                                                | 72.2 ms: 1.03x faster                                                |
| coroutines                 | 23.3 ms                                                                | 23.0 ms: 1.01x faster                                                |
| scimark_sor                | 134 ms                                                                 | 132 ms: 1.01x faster                                                 |
| float                      | 76.7 ms                                                                | 76.4 ms: 1.00x faster                                                |
| html5lib                   | 68.6 ms                                                                | 70.4 ms: 1.03x slower                                                |
| deepcopy_memo              | 38.1 us                                                                | 39.2 us: 1.03x slower                                                |
| pidigits                   | 216 ms                                                                 | 223 ms: 1.03x slower                                                 |
| json                       | 4.98 ms                                                                | 5.13 ms: 1.03x slower                                                |
| create_gc_cycles           | 1.33 ms                                                                | 1.38 ms: 1.04x slower                                                |
| pathlib                    | 19.3 ms                                                                | 20.0 ms: 1.04x slower                                                |
| spectral_norm              | 108 ms                                                                 | 112 ms: 1.04x slower                                                 |
| pycparser                  | 1.12 sec                                                               | 1.18 sec: 1.06x slower                                               |
| docutils                   | 2.63 sec                                                               | 2.78 sec: 1.06x slower                                               |
| deepcopy_reduce            | 3.12 us                                                                | 3.35 us: 1.07x slower                                                |
| bpe_tokeniser              | 4.46 sec                                                               | 4.85 sec: 1.09x slower                                               |
| json_loads                 | 27.3 us                                                                | 29.8 us: 1.09x slower                                                |
| pyflate                    | 449 ms                                                                 | 491 ms: 1.09x slower                                                 |
| scimark_fft                | 348 ms                                                                 | 388 ms: 1.11x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                                | 95.5 ms: 1.12x slower                                                |
| thrift                     | 772 us                                                                 | 872 us: 1.13x slower                                                 |
| tomli_loads                | 2.01 sec                                                               | 2.29 sec: 1.14x slower                                               |
| 2to3                       | 259 ms                                                                 | 297 ms: 1.14x slower                                                 |
| logging_silent             | 98.2 ns                                                                | 113 ns: 1.15x slower                                                 |
| mdp                        | 2.34 sec                                                               | 2.70 sec: 1.15x slower                                               |
| regex_compile              | 131 ms                                                                 | 152 ms: 1.16x slower                                                 |
| telco                      | 7.77 ms                                                                | 9.03 ms: 1.16x slower                                                |
| generators                 | 28.5 ms                                                                | 33.3 ms: 1.17x slower                                                |
| pprint_safe_repr           | 719 ms                                                                 | 842 ms: 1.17x slower                                                 |
| xml_etree_process          | 59.2 ms                                                                | 69.6 ms: 1.17x slower                                                |
| pprint_pformat             | 1.46 sec                                                               | 1.73 sec: 1.19x slower                                               |
| logging_simple             | 6.14 us                                                                | 7.32 us: 1.19x slower                                                |
| sympy_integrate            | 19.7 ms                                                                | 23.5 ms: 1.19x slower                                                |
| logging_format             | 6.92 us                                                                | 8.27 us: 1.20x slower                                                |
| genshi_xml                 | 49.1 ms                                                                | 58.7 ms: 1.20x slower                                                |
| chaos                      | 56.3 ms                                                                | 67.4 ms: 1.20x slower                                                |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.69 ms: 1.20x slower                                                |
| sympy_sum                  | 154 ms                                                                 | 185 ms: 1.20x slower                                                 |
| sympy_expand               | 454 ms                                                                 | 547 ms: 1.21x slower                                                 |
| unpickle_pure_python       | 208 us                                                                 | 252 us: 1.21x slower                                                 |
| sympy_str                  | 274 ms                                                                 | 332 ms: 1.21x slower                                                 |
| json_dumps                 | 10.6 ms                                                                | 12.9 ms: 1.21x slower                                                |
| comprehensions             | 16.6 us                                                                | 20.3 us: 1.23x slower                                                |
| richards                   | 44.4 ms                                                                | 54.5 ms: 1.23x slower                                                |
| pickle_pure_python         | 292 us                                                                 | 358 us: 1.23x slower                                                 |
| scimark_lu                 | 112 ms                                                                 | 139 ms: 1.23x slower                                                 |
| hexiom                     | 5.95 ms                                                                | 7.37 ms: 1.24x slower                                                |
| deltablue                  | 3.10 ms                                                                | 3.85 ms: 1.24x slower                                                |
| scimark_monte_carlo        | 65.8 ms                                                                | 82.3 ms: 1.25x slower                                                |
| typing_runtime_protocols   | 156 us                                                                 | 195 us: 1.25x slower                                                 |
| richards_super             | 50.4 ms                                                                | 63.8 ms: 1.27x slower                                                |
| django_template            | 34.2 ms                                                                | 43.3 ms: 1.27x slower                                                |
| meteor_contest             | 101 ms                                                                 | 129 ms: 1.27x slower                                                 |
| nqueens                    | 77.7 ms                                                                | 99.1 ms: 1.28x slower                                                |
| raytrace                   | 250 ms                                                                 | 320 ms: 1.28x slower                                                 |
| crypto_pyaes               | 68.2 ms                                                                | 88.1 ms: 1.29x slower                                                |
| genshi_text                | 21.7 ms                                                                | 28.2 ms: 1.30x slower                                                |
| coverage                   | 82.5 ms                                                                | 108 ms: 1.30x slower                                                 |
| fannkuch                   | 376 ms                                                                 | 492 ms: 1.31x slower                                                 |
| mako                       | 11.2 ms                                                                | 15.9 ms: 1.42x slower                                                |
| python_startup             | 11.0 ms                                                                | 15.7 ms: 1.43x slower                                                |
| python_startup_no_site     | 7.41 ms                                                                | 11.1 ms: 1.49x slower                                                |
| nbody                      | 85.3 ms                                                                | 131 ms: 1.53x slower                                                 |
| bench_thread_pool          | 924 us                                                                 | 3.15 ms: 3.41x slower                                                |
| bench_mp_pool              | 11.0 ms                                                                | 96.6 ms: 8.78x slower                                                |
| Geometric mean             | (ref)                                                                  | 1.12x slower                                                         |

Benchmark hidden because not significant (4): pylint, go, asyncio_websockets, async_generators
Ignored benchmarks (18) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250324-3.14.0a6+-60f2173-NOGIL/bm-20250324-vultr-x86_64-Yhg1s-uniqref_critsection-3.14.0a6+-60f2173.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.073x slower

# HPT report

- Reliability score: 99.98% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.37x