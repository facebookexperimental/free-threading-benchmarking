# Results vs. 3.13.0rc2

- fork: colesbury
- ref: gh_128421_frame
- machine: linux-x86_64
- commit hash: 44f8c85
- commit date: 2025-03-19
- overall geometric mean: 1.081x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250319-vultr-x86_64-colesbury-gh_128421_frame-3.14.0a6+-44f8c85 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 299 ms: 1.15x slower                                                 |
| docutils       | 2.63 sec                                                               | 2.78 sec: 1.06x slower                                               |
| html5lib       | 68.6 ms                                                                | 72.6 ms: 1.06x slower                                                |
| Geometric mean | (ref)                                                                  | 1.09x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250319-vultr-x86_64-colesbury-gh_128421_frame-3.14.0a6+-44f8c85 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 551 ms: 1.64x faster                                                 |
| async_tree_io              | 881 ms                                                                 | 581 ms: 1.52x faster                                                 |
| async_tree_none_tg         | 333 ms                                                                 | 238 ms: 1.40x faster                                                 |
| async_tree_memoization     | 459 ms                                                                 | 338 ms: 1.36x faster                                                 |
| async_tree_memoization_tg  | 410 ms                                                                 | 307 ms: 1.34x faster                                                 |
| async_tree_none            | 353 ms                                                                 | 276 ms: 1.28x faster                                                 |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 575 ms: 1.10x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 605 ms: 1.10x faster                                                 |
| Geometric mean             | (ref)                                                                  | 1.23x faster                                                         |

Benchmark hidden because not significant (3): asyncio_websockets, coroutines, async_generators

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250319-vultr-x86_64-colesbury-gh_128421_frame-3.14.0a6+-44f8c85 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 76.7 ms                                                                | 77.6 ms: 1.01x slower                                                |
| pidigits       | 216 ms                                                                 | 222 ms: 1.02x slower                                                 |
| nbody          | 85.3 ms                                                                | 133 ms: 1.56x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.17x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250319-vultr-x86_64-colesbury-gh_128421_frame-3.14.0a6+-44f8c85 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.69 ms: 1.19x faster                                                |
| regex_v8       | 23.2 ms                                                                | 21.7 ms: 1.07x faster                                                |
| regex_dna      | 189 ms                                                                 | 182 ms: 1.04x faster                                                 |
| regex_compile  | 131 ms                                                                 | 158 ms: 1.20x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250319-vultr-x86_64-colesbury-gh_128421_frame-3.14.0a6+-44f8c85 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 88.7 ms: 1.06x faster                                                |
| xml_etree_parse      | 136 ms                                                                 | 129 ms: 1.05x faster                                                 |
| json_loads           | 27.3 us                                                                | 29.0 us: 1.06x slower                                                |
| xml_etree_generate   | 85.4 ms                                                                | 96.3 ms: 1.13x slower                                                |
| tomli_loads          | 2.01 sec                                                               | 2.36 sec: 1.17x slower                                               |
| xml_etree_process    | 59.2 ms                                                                | 70.3 ms: 1.19x slower                                                |
| json_dumps           | 10.6 ms                                                                | 12.9 ms: 1.21x slower                                                |
| unpickle_pure_python | 208 us                                                                 | 258 us: 1.24x slower                                                 |
| pickle_pure_python   | 292 us                                                                 | 364 us: 1.25x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.12x slower                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250319-vultr-x86_64-colesbury-gh_128421_frame-3.14.0a6+-44f8c85 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 15.7 ms: 1.43x slower                                                |
| python_startup_no_site | 7.41 ms                                                                | 11.1 ms: 1.50x slower                                                |
| Geometric mean         | (ref)                                                                  | 1.46x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250319-vultr-x86_64-colesbury-gh_128421_frame-3.14.0a6+-44f8c85 |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 60.0 ms: 1.22x slower                                                |
| django_template | 34.2 ms                                                                | 43.3 ms: 1.27x slower                                                |
| genshi_text     | 21.7 ms                                                                | 28.3 ms: 1.30x slower                                                |
| mako            | 11.2 ms                                                                | 15.9 ms: 1.42x slower                                                |
| Geometric mean  | (ref)                                                                  | 1.30x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250319-vultr-x86_64-colesbury-gh_128421_frame-3.14.0a6+-44f8c85 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.78 ms: 1.86x faster                                                |
| async_tree_io_tg           | 901 ms                                                                 | 551 ms: 1.64x faster                                                 |
| async_tree_io              | 881 ms                                                                 | 581 ms: 1.52x faster                                                 |
| async_tree_none_tg         | 333 ms                                                                 | 238 ms: 1.40x faster                                                 |
| async_tree_memoization     | 459 ms                                                                 | 338 ms: 1.36x faster                                                 |
| async_tree_memoization_tg  | 410 ms                                                                 | 307 ms: 1.34x faster                                                 |
| async_tree_none            | 353 ms                                                                 | 276 ms: 1.28x faster                                                 |
| regex_effbot               | 3.21 ms                                                                | 2.69 ms: 1.19x faster                                                |
| deepcopy                   | 357 us                                                                 | 313 us: 1.14x faster                                                 |
| sqlite_synth               | 2.25 us                                                                | 2.01 us: 1.12x faster                                                |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 575 ms: 1.10x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 605 ms: 1.10x faster                                                 |
| regex_v8                   | 23.2 ms                                                                | 21.7 ms: 1.07x faster                                                |
| xml_etree_iterparse        | 94.4 ms                                                                | 88.7 ms: 1.06x faster                                                |
| xml_etree_parse            | 136 ms                                                                 | 129 ms: 1.05x faster                                                 |
| regex_dna                  | 189 ms                                                                 | 182 ms: 1.04x faster                                                 |
| dulwich_log                | 74.5 ms                                                                | 73.7 ms: 1.01x faster                                                |
| float                      | 76.7 ms                                                                | 77.6 ms: 1.01x slower                                                |
| json                       | 4.98 ms                                                                | 5.06 ms: 1.01x slower                                                |
| pidigits                   | 216 ms                                                                 | 222 ms: 1.02x slower                                                 |
| pathlib                    | 19.3 ms                                                                | 19.8 ms: 1.03x slower                                                |
| deepcopy_reduce            | 3.12 us                                                                | 3.22 us: 1.03x slower                                                |
| go                         | 141 ms                                                                 | 145 ms: 1.03x slower                                                 |
| deepcopy_memo              | 38.1 us                                                                | 39.3 us: 1.03x slower                                                |
| spectral_norm              | 108 ms                                                                 | 111 ms: 1.04x slower                                                 |
| scimark_sor                | 134 ms                                                                 | 139 ms: 1.04x slower                                                 |
| html5lib                   | 68.6 ms                                                                | 72.6 ms: 1.06x slower                                                |
| docutils                   | 2.63 sec                                                               | 2.78 sec: 1.06x slower                                               |
| json_loads                 | 27.3 us                                                                | 29.0 us: 1.06x slower                                                |
| pycparser                  | 1.12 sec                                                               | 1.20 sec: 1.07x slower                                               |
| bpe_tokeniser              | 4.46 sec                                                               | 4.84 sec: 1.09x slower                                               |
| thrift                     | 772 us                                                                 | 866 us: 1.12x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                                | 96.3 ms: 1.13x slower                                                |
| pyflate                    | 449 ms                                                                 | 507 ms: 1.13x slower                                                 |
| mdp                        | 2.34 sec                                                               | 2.68 sec: 1.15x slower                                               |
| telco                      | 7.77 ms                                                                | 8.91 ms: 1.15x slower                                                |
| 2to3                       | 259 ms                                                                 | 299 ms: 1.15x slower                                                 |
| scimark_fft                | 348 ms                                                                 | 402 ms: 1.15x slower                                                 |
| pprint_safe_repr           | 719 ms                                                                 | 829 ms: 1.15x slower                                                 |
| generators                 | 28.5 ms                                                                | 33.1 ms: 1.16x slower                                                |
| tomli_loads                | 2.01 sec                                                               | 2.36 sec: 1.17x slower                                               |
| pprint_pformat             | 1.46 sec                                                               | 1.71 sec: 1.18x slower                                               |
| logging_simple             | 6.14 us                                                                | 7.27 us: 1.18x slower                                                |
| xml_etree_process          | 59.2 ms                                                                | 70.3 ms: 1.19x slower                                                |
| logging_format             | 6.92 us                                                                | 8.24 us: 1.19x slower                                                |
| regex_compile              | 131 ms                                                                 | 158 ms: 1.20x slower                                                 |
| logging_silent             | 98.2 ns                                                                | 118 ns: 1.20x slower                                                 |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.73 ms: 1.21x slower                                                |
| json_dumps                 | 10.6 ms                                                                | 12.9 ms: 1.21x slower                                                |
| sympy_sum                  | 154 ms                                                                 | 187 ms: 1.21x slower                                                 |
| sympy_expand               | 454 ms                                                                 | 555 ms: 1.22x slower                                                 |
| genshi_xml                 | 49.1 ms                                                                | 60.0 ms: 1.22x slower                                                |
| sympy_integrate            | 19.7 ms                                                                | 24.3 ms: 1.23x slower                                                |
| sympy_str                  | 274 ms                                                                 | 338 ms: 1.23x slower                                                 |
| unpickle_pure_python       | 208 us                                                                 | 258 us: 1.24x slower                                                 |
| chaos                      | 56.3 ms                                                                | 70.1 ms: 1.25x slower                                                |
| pickle_pure_python         | 292 us                                                                 | 364 us: 1.25x slower                                                 |
| comprehensions             | 16.6 us                                                                | 20.8 us: 1.25x slower                                                |
| deltablue                  | 3.10 ms                                                                | 3.89 ms: 1.26x slower                                                |
| coverage                   | 82.5 ms                                                                | 104 ms: 1.26x slower                                                 |
| richards                   | 44.4 ms                                                                | 56.1 ms: 1.26x slower                                                |
| django_template            | 34.2 ms                                                                | 43.3 ms: 1.27x slower                                                |
| scimark_monte_carlo        | 65.8 ms                                                                | 83.9 ms: 1.27x slower                                                |
| meteor_contest             | 101 ms                                                                 | 129 ms: 1.28x slower                                                 |
| typing_runtime_protocols   | 156 us                                                                 | 199 us: 1.28x slower                                                 |
| nqueens                    | 77.7 ms                                                                | 99.8 ms: 1.28x slower                                                |
| hexiom                     | 5.95 ms                                                                | 7.67 ms: 1.29x slower                                                |
| scimark_lu                 | 112 ms                                                                 | 146 ms: 1.30x slower                                                 |
| crypto_pyaes               | 68.2 ms                                                                | 88.4 ms: 1.30x slower                                                |
| richards_super             | 50.4 ms                                                                | 65.5 ms: 1.30x slower                                                |
| genshi_text                | 21.7 ms                                                                | 28.3 ms: 1.30x slower                                                |
| raytrace                   | 250 ms                                                                 | 330 ms: 1.32x slower                                                 |
| fannkuch                   | 376 ms                                                                 | 499 ms: 1.33x slower                                                 |
| mako                       | 11.2 ms                                                                | 15.9 ms: 1.42x slower                                                |
| python_startup             | 11.0 ms                                                                | 15.7 ms: 1.43x slower                                                |
| python_startup_no_site     | 7.41 ms                                                                | 11.1 ms: 1.50x slower                                                |
| nbody                      | 85.3 ms                                                                | 133 ms: 1.56x slower                                                 |
| bench_thread_pool          | 924 us                                                                 | 3.16 ms: 3.42x slower                                                |
| bench_mp_pool              | 11.0 ms                                                                | 97.2 ms: 8.84x slower                                                |
| Geometric mean             | (ref)                                                                  | 1.13x slower                                                         |

Benchmark hidden because not significant (5): pylint, asyncio_websockets, coroutines, async_generators, create_gc_cycles
Ignored benchmarks (18) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250319-3.14.0a6+-44f8c85-NOGIL/bm-20250319-vultr-x86_64-colesbury-gh_128421_frame-3.14.0a6+-44f8c85.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.081x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.35x