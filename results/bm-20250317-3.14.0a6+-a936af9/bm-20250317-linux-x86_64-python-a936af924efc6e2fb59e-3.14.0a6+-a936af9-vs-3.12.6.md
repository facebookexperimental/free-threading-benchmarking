# Results vs. 3.12.6

- fork: python
- ref: a936af924efc6e2fb59e
- machine: linux-x86_64
- commit hash: a936af9
- commit date: 2025-03-17
- overall geometric mean: 1.080x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 494 ms: 1.08x slower                                                   |
| docutils       | 4.00 sec                                               | 3.82 sec: 1.05x faster                                                 |
| Geometric mean | (ref)                                                  | 1.02x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 963 ms: 2.01x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 921 ms: 2.01x faster                                                   |
| async_tree_none            | 741 ms                                                 | 373 ms: 1.99x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 523 ms: 1.87x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 389 ms: 1.81x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 528 ms: 1.76x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 717 ms: 1.53x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 712 ms: 1.51x faster                                                   |
| async_generators           | 589 ms                                                 | 531 ms: 1.11x faster                                                   |
| coroutines                 | 29.5 ms                                                | 31.6 ms: 1.07x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.54x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 111 ms: 1.11x faster                                                   |
| nbody          | 119 ms                                                 | 136 ms: 1.14x slower                                                   |
| Geometric mean | (ref)                                                  | 1.00x slower                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 3.88 ms: 1.32x faster                                                  |
| regex_compile  | 187 ms                                                 | 161 ms: 1.16x faster                                                   |
| Geometric mean | (ref)                                                  | 1.11x faster                                                           |

Benchmark hidden because not significant (2): regex_v8, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 241 ms                                                 | 208 ms: 1.16x faster                                                   |
| tomli_loads          | 2.88 sec                                               | 2.55 sec: 1.13x faster                                                 |
| xml_etree_generate   | 127 ms                                                 | 118 ms: 1.08x faster                                                   |
| unpickle_pure_python | 300 us                                                 | 284 us: 1.05x faster                                                   |
| json_loads           | 37.9 us                                                | 40.2 us: 1.06x slower                                                  |
| json_dumps           | 14.3 ms                                                | 15.5 ms: 1.08x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.04x faster                                                           |

Benchmark hidden because not significant (3): xml_etree_iterparse, pickle_pure_python, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 19.7 ms: 1.12x slower                                                  |
| python_startup         | 23.7 ms                                                | 32.1 ms: 1.35x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.23x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 30.2 ms                                                | 28.6 ms: 1.06x faster                                                  |
| django_template | 44.9 ms                                                | 48.2 ms: 1.07x slower                                                  |
| mako            | 15.7 ms                                                | 18.9 ms: 1.20x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.05x slower                                                           |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 963 ms: 2.01x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 921 ms: 2.01x faster                                                   |
| async_tree_none            | 741 ms                                                 | 373 ms: 1.99x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 523 ms: 1.87x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 389 ms: 1.81x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 528 ms: 1.76x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 717 ms: 1.53x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 712 ms: 1.51x faster                                                   |
| deepcopy_memo              | 52.4 us                                                | 37.9 us: 1.38x faster                                                  |
| deepcopy                   | 468 us                                                 | 354 us: 1.32x faster                                                   |
| regex_effbot               | 5.13 ms                                                | 3.88 ms: 1.32x faster                                                  |
| comprehensions             | 27.1 us                                                | 21.9 us: 1.24x faster                                                  |
| dulwich_log                | 100 ms                                                 | 81.5 ms: 1.23x faster                                                  |
| sqlalchemy_declarative     | 218 ms                                                 | 181 ms: 1.20x faster                                                   |
| deepcopy_reduce            | 4.04 us                                                | 3.37 us: 1.20x faster                                                  |
| spectral_norm              | 156 ms                                                 | 130 ms: 1.19x faster                                                   |
| pycparser                  | 1.79 sec                                               | 1.54 sec: 1.16x faster                                                 |
| regex_compile              | 187 ms                                                 | 161 ms: 1.16x faster                                                   |
| pathlib                    | 31.6 ms                                                | 27.3 ms: 1.16x faster                                                  |
| xml_etree_parse            | 241 ms                                                 | 208 ms: 1.16x faster                                                   |
| tomli_loads                | 2.88 sec                                               | 2.55 sec: 1.13x faster                                                 |
| raytrace                   | 408 ms                                                 | 362 ms: 1.13x faster                                                   |
| scimark_fft                | 500 ms                                                 | 445 ms: 1.12x faster                                                   |
| sympy_sum                  | 222 ms                                                 | 200 ms: 1.11x faster                                                   |
| nqueens                    | 117 ms                                                 | 105 ms: 1.11x faster                                                   |
| async_generators           | 589 ms                                                 | 531 ms: 1.11x faster                                                   |
| float                      | 123 ms                                                 | 111 ms: 1.11x faster                                                   |
| sympy_str                  | 385 ms                                                 | 351 ms: 1.10x faster                                                   |
| scimark_sor                | 167 ms                                                 | 152 ms: 1.09x faster                                                   |
| sqlglot_normalize          | 157 ms                                                 | 144 ms: 1.09x faster                                                   |
| pylint                     | 465 ms                                                 | 428 ms: 1.09x faster                                                   |
| scimark_monte_carlo        | 96.4 ms                                                | 88.8 ms: 1.09x faster                                                  |
| xml_etree_generate         | 127 ms                                                 | 118 ms: 1.08x faster                                                   |
| sqlglot_transpile          | 2.34 ms                                                | 2.17 ms: 1.08x faster                                                  |
| crypto_pyaes               | 107 ms                                                 | 99.7 ms: 1.08x faster                                                  |
| mdp                        | 3.97 sec                                               | 3.70 sec: 1.07x faster                                                 |
| pyflate                    | 727 ms                                                 | 679 ms: 1.07x faster                                                   |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 6.31 ms: 1.06x faster                                                  |
| go                         | 172 ms                                                 | 162 ms: 1.06x faster                                                   |
| genshi_text                | 30.2 ms                                                | 28.6 ms: 1.06x faster                                                  |
| sqlite_synth               | 3.87 us                                                | 3.67 us: 1.05x faster                                                  |
| unpickle_pure_python       | 300 us                                                 | 284 us: 1.05x faster                                                   |
| scimark_lu                 | 152 ms                                                 | 145 ms: 1.05x faster                                                   |
| docutils                   | 4.00 sec                                               | 3.82 sec: 1.05x faster                                                 |
| typing_runtime_protocols   | 224 us                                                 | 216 us: 1.04x faster                                                   |
| pprint_pformat             | 1.98 sec                                               | 1.93 sec: 1.03x faster                                                 |
| hexiom                     | 8.27 ms                                                | 8.66 ms: 1.05x slower                                                  |
| deltablue                  | 4.27 ms                                                | 4.49 ms: 1.05x slower                                                  |
| json_loads                 | 37.9 us                                                | 40.2 us: 1.06x slower                                                  |
| coroutines                 | 29.5 ms                                                | 31.6 ms: 1.07x slower                                                  |
| django_template            | 44.9 ms                                                | 48.2 ms: 1.07x slower                                                  |
| json                       | 6.85 ms                                                | 7.36 ms: 1.08x slower                                                  |
| 2to3                       | 456 ms                                                 | 494 ms: 1.08x slower                                                   |
| json_dumps                 | 14.3 ms                                                | 15.5 ms: 1.08x slower                                                  |
| python_startup_no_site     | 17.6 ms                                                | 19.7 ms: 1.12x slower                                                  |
| nbody                      | 119 ms                                                 | 136 ms: 1.14x slower                                                   |
| mako                       | 15.7 ms                                                | 18.9 ms: 1.20x slower                                                  |
| coverage                   | 95.4 ms                                                | 119 ms: 1.25x slower                                                   |
| bench_thread_pool          | 3.48 ms                                                | 4.39 ms: 1.26x slower                                                  |
| python_startup             | 23.7 ms                                                | 32.1 ms: 1.35x slower                                                  |
| gc_traversal               | 5.86 ms                                                | 9.00 ms: 1.54x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 4.91 ms: 2.53x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 109 ms: 5.26x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.05x faster                                                           |

Benchmark hidden because not significant (26): logging_silent, logging_simple, xml_etree_iterparse, pickle_pure_python, richards_super, pidigits, sqlalchemy_imperative, sqlglot_optimize, bpe_tokeniser, pprint_safe_repr, sympy_integrate, thrift, generators, asyncio_websockets, xml_etree_process, richards, regex_v8, regex_dna, genshi_xml, fannkuch, logging_format, sympy_expand, meteor_contest, telco, sqlglot_parse, chaos
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250317-3.14.0a6+-a936af9/bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.080x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.14x