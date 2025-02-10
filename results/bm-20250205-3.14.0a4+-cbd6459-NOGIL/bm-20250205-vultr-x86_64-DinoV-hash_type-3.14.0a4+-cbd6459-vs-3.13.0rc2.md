# Results vs. 3.13.0rc2

- fork: DinoV
- ref: hash_type
- machine: linux-x86_64
- commit hash: cbd6459
- commit date: 2025-02-05
- overall geometric mean: 1.080x slower
- HPT reliability: 99.98%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4+-cbd6459 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 302 ms: 1.16x slower                                       |
| docutils       | 2.63 sec                                                               | 2.85 sec: 1.08x slower                                     |
| html5lib       | 68.6 ms                                                                | 70.7 ms: 1.03x slower                                      |
| Geometric mean | (ref)                                                                  | 1.09x slower                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4+-cbd6459 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 580 ms: 1.55x faster                                       |
| async_tree_io              | 881 ms                                                                 | 613 ms: 1.44x faster                                       |
| async_tree_none_tg         | 333 ms                                                                 | 251 ms: 1.33x faster                                       |
| async_tree_memoization     | 459 ms                                                                 | 361 ms: 1.27x faster                                       |
| async_tree_memoization_tg  | 410 ms                                                                 | 323 ms: 1.27x faster                                       |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 516 ms: 1.23x faster                                       |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 552 ms: 1.21x faster                                       |
| async_tree_none            | 353 ms                                                                 | 293 ms: 1.21x faster                                       |
| Geometric mean             | (ref)                                                                  | 1.22x faster                                               |

Benchmark hidden because not significant (3): async_generators, asyncio_websockets, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4+-cbd6459 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 193 ms: 1.12x faster                                       |
| float          | 76.7 ms                                                                | 75.6 ms: 1.02x faster                                      |
| nbody          | 85.3 ms                                                                | 134 ms: 1.57x slower                                       |
| Geometric mean | (ref)                                                                  | 1.11x slower                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4+-cbd6459 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.77 ms: 1.16x faster                                      |
| regex_dna      | 189 ms                                                                 | 177 ms: 1.07x faster                                       |
| regex_v8       | 23.2 ms                                                                | 23.7 ms: 1.02x slower                                      |
| regex_compile  | 131 ms                                                                 | 149 ms: 1.13x slower                                       |
| Geometric mean | (ref)                                                                  | 1.02x faster                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4+-cbd6459 |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 87.5 ms: 1.08x faster                                      |
| xml_etree_parse      | 136 ms                                                                 | 127 ms: 1.07x faster                                       |
| xml_etree_generate   | 85.4 ms                                                                | 96.7 ms: 1.13x slower                                      |
| json_loads           | 27.3 us                                                                | 31.0 us: 1.13x slower                                      |
| tomli_loads          | 2.01 sec                                                               | 2.29 sec: 1.14x slower                                     |
| xml_etree_process    | 59.2 ms                                                                | 69.1 ms: 1.17x slower                                      |
| unpickle_pure_python | 208 us                                                                 | 245 us: 1.18x slower                                       |
| json_dumps           | 10.6 ms                                                                | 12.9 ms: 1.21x slower                                      |
| pickle_pure_python   | 292 us                                                                 | 376 us: 1.29x slower                                       |
| Geometric mean       | (ref)                                                                  | 1.12x slower                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4+-cbd6459 |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.63 ms: 1.30x slower                                      |
| python_startup         | 11.0 ms                                                                | 15.3 ms: 1.39x slower                                      |
| Geometric mean         | (ref)                                                                  | 1.34x slower                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4+-cbd6459 |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 59.9 ms: 1.22x slower                                      |
| django_template | 34.2 ms                                                                | 42.6 ms: 1.25x slower                                      |
| genshi_text     | 21.7 ms                                                                | 27.4 ms: 1.26x slower                                      |
| mako            | 11.2 ms                                                                | 16.0 ms: 1.43x slower                                      |
| Geometric mean  | (ref)                                                                  | 1.29x slower                                               |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4+-cbd6459 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.76 ms: 1.89x faster                                      |
| async_tree_io_tg           | 901 ms                                                                 | 580 ms: 1.55x faster                                       |
| async_tree_io              | 881 ms                                                                 | 613 ms: 1.44x faster                                       |
| async_tree_none_tg         | 333 ms                                                                 | 251 ms: 1.33x faster                                       |
| async_tree_memoization     | 459 ms                                                                 | 361 ms: 1.27x faster                                       |
| async_tree_memoization_tg  | 410 ms                                                                 | 323 ms: 1.27x faster                                       |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 516 ms: 1.23x faster                                       |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 552 ms: 1.21x faster                                       |
| async_tree_none            | 353 ms                                                                 | 293 ms: 1.21x faster                                       |
| regex_effbot               | 3.21 ms                                                                | 2.77 ms: 1.16x faster                                      |
| deepcopy                   | 357 us                                                                 | 314 us: 1.14x faster                                       |
| pidigits                   | 216 ms                                                                 | 193 ms: 1.12x faster                                       |
| sqlite_synth               | 2.25 us                                                                | 2.07 us: 1.09x faster                                      |
| xml_etree_iterparse        | 94.4 ms                                                                | 87.5 ms: 1.08x faster                                      |
| xml_etree_parse            | 136 ms                                                                 | 127 ms: 1.07x faster                                       |
| regex_dna                  | 189 ms                                                                 | 177 ms: 1.07x faster                                       |
| go                         | 141 ms                                                                 | 135 ms: 1.04x faster                                       |
| pathlib                    | 19.3 ms                                                                | 18.8 ms: 1.02x faster                                      |
| float                      | 76.7 ms                                                                | 75.6 ms: 1.02x faster                                      |
| deepcopy_memo              | 38.1 us                                                                | 38.2 us: 1.00x slower                                      |
| regex_v8                   | 23.2 ms                                                                | 23.7 ms: 1.02x slower                                      |
| deepcopy_reduce            | 3.12 us                                                                | 3.21 us: 1.03x slower                                      |
| html5lib                   | 68.6 ms                                                                | 70.7 ms: 1.03x slower                                      |
| bpe_tokeniser              | 4.46 sec                                                               | 4.66 sec: 1.05x slower                                     |
| create_gc_cycles           | 1.33 ms                                                                | 1.40 ms: 1.05x slower                                      |
| pycparser                  | 1.12 sec                                                               | 1.18 sec: 1.05x slower                                     |
| json                       | 4.98 ms                                                                | 5.39 ms: 1.08x slower                                      |
| docutils                   | 2.63 sec                                                               | 2.85 sec: 1.08x slower                                     |
| scimark_fft                | 348 ms                                                                 | 380 ms: 1.09x slower                                       |
| telco                      | 7.77 ms                                                                | 8.55 ms: 1.10x slower                                      |
| dulwich_log                | 74.5 ms                                                                | 82.0 ms: 1.10x slower                                      |
| mdp                        | 2.34 sec                                                               | 2.58 sec: 1.10x slower                                     |
| logging_silent             | 98.2 ns                                                                | 109 ns: 1.11x slower                                       |
| pyflate                    | 449 ms                                                                 | 497 ms: 1.11x slower                                       |
| pprint_safe_repr           | 719 ms                                                                 | 808 ms: 1.12x slower                                       |
| regex_compile              | 131 ms                                                                 | 149 ms: 1.13x slower                                       |
| xml_etree_generate         | 85.4 ms                                                                | 96.7 ms: 1.13x slower                                      |
| json_loads                 | 27.3 us                                                                | 31.0 us: 1.13x slower                                      |
| tomli_loads                | 2.01 sec                                                               | 2.29 sec: 1.14x slower                                     |
| pprint_pformat             | 1.46 sec                                                               | 1.67 sec: 1.15x slower                                     |
| 2to3                       | 259 ms                                                                 | 302 ms: 1.16x slower                                       |
| xml_etree_process          | 59.2 ms                                                                | 69.1 ms: 1.17x slower                                      |
| sqlglot_normalize          | 106 ms                                                                 | 123 ms: 1.17x slower                                       |
| generators                 | 28.5 ms                                                                | 33.5 ms: 1.17x slower                                      |
| coverage                   | 82.5 ms                                                                | 96.9 ms: 1.18x slower                                      |
| sqlglot_optimize           | 52.7 ms                                                                | 61.9 ms: 1.18x slower                                      |
| thrift                     | 772 us                                                                 | 909 us: 1.18x slower                                       |
| unpickle_pure_python       | 208 us                                                                 | 245 us: 1.18x slower                                       |
| logging_simple             | 6.14 us                                                                | 7.27 us: 1.18x slower                                      |
| comprehensions             | 16.6 us                                                                | 19.8 us: 1.19x slower                                      |
| logging_format             | 6.92 us                                                                | 8.25 us: 1.19x slower                                      |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.74 ms: 1.21x slower                                      |
| sympy_expand               | 454 ms                                                                 | 548 ms: 1.21x slower                                       |
| json_dumps                 | 10.6 ms                                                                | 12.9 ms: 1.21x slower                                      |
| sympy_sum                  | 154 ms                                                                 | 187 ms: 1.21x slower                                       |
| scimark_lu                 | 112 ms                                                                 | 137 ms: 1.22x slower                                       |
| genshi_xml                 | 49.1 ms                                                                | 59.9 ms: 1.22x slower                                      |
| chaos                      | 56.3 ms                                                                | 68.7 ms: 1.22x slower                                      |
| sympy_str                  | 274 ms                                                                 | 336 ms: 1.23x slower                                       |
| hexiom                     | 5.95 ms                                                                | 7.31 ms: 1.23x slower                                      |
| sqlglot_transpile          | 1.55 ms                                                                | 1.91 ms: 1.23x slower                                      |
| sympy_integrate            | 19.7 ms                                                                | 24.3 ms: 1.23x slower                                      |
| nqueens                    | 77.7 ms                                                                | 96.5 ms: 1.24x slower                                      |
| scimark_monte_carlo        | 65.8 ms                                                                | 82.1 ms: 1.25x slower                                      |
| django_template            | 34.2 ms                                                                | 42.6 ms: 1.25x slower                                      |
| genshi_text                | 21.7 ms                                                                | 27.4 ms: 1.26x slower                                      |
| sqlglot_parse              | 1.25 ms                                                                | 1.58 ms: 1.27x slower                                      |
| typing_runtime_protocols   | 156 us                                                                 | 198 us: 1.27x slower                                       |
| meteor_contest             | 101 ms                                                                 | 129 ms: 1.27x slower                                       |
| richards                   | 44.4 ms                                                                | 57.0 ms: 1.28x slower                                      |
| pickle_pure_python         | 292 us                                                                 | 376 us: 1.29x slower                                       |
| raytrace                   | 250 ms                                                                 | 323 ms: 1.29x slower                                       |
| crypto_pyaes               | 68.2 ms                                                                | 88.3 ms: 1.29x slower                                      |
| fannkuch                   | 376 ms                                                                 | 487 ms: 1.29x slower                                       |
| python_startup_no_site     | 7.41 ms                                                                | 9.63 ms: 1.30x slower                                      |
| richards_super             | 50.4 ms                                                                | 65.8 ms: 1.30x slower                                      |
| python_startup             | 11.0 ms                                                                | 15.3 ms: 1.39x slower                                      |
| mako                       | 11.2 ms                                                                | 16.0 ms: 1.43x slower                                      |
| deltablue                  | 3.10 ms                                                                | 4.63 ms: 1.50x slower                                      |
| nbody                      | 85.3 ms                                                                | 134 ms: 1.57x slower                                       |
| bench_thread_pool          | 924 us                                                                 | 3.31 ms: 3.58x slower                                      |
| bench_mp_pool              | 11.0 ms                                                                | 94.8 ms: 8.62x slower                                      |
| Geometric mean             | (ref)                                                                  | 1.13x slower                                               |

Benchmark hidden because not significant (6): scimark_sor, async_generators, asyncio_websockets, spectral_norm, coroutines, pylint
Ignored benchmarks (14) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250205-3.14.0a4+-cbd6459-NOGIL/bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4+-cbd6459.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.080x slower

# HPT report

- Reliability score: 99.98% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.35x