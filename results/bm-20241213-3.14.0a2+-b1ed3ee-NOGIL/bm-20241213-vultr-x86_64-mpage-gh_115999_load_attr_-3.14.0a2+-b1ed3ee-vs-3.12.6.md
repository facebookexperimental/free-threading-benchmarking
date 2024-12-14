# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: b1ed3ee
- commit date: 2024-12-13
- overall geometric mean: 1.115x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.09x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 323 ms: 1.23x slower                                                  |
| docutils       | 2.64 sec                                               | 2.87 sec: 1.09x slower                                                |
| html5lib       | 63.6 ms                                                | 80.4 ms: 1.26x slower                                                 |
| Geometric mean | (ref)                                                  | 1.19x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 618 ms: 1.80x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 266 ms: 1.68x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 337 ms: 1.66x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 653 ms: 1.66x faster                                                  |
| async_tree_none            | 464 ms                                                 | 306 ms: 1.52x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 375 ms: 1.48x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 512 ms: 1.41x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 544 ms: 1.31x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 521 ms: 1.01x slower                                                  |
| coroutines                 | 23.9 ms                                                | 24.6 ms: 1.03x slower                                                 |
| async_generators           | 384 ms                                                 | 415 ms: 1.08x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.37x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 181 ms: 1.02x faster                                                  |
| float          | 80.8 ms                                                | 103 ms: 1.27x slower                                                  |
| nbody          | 89.3 ms                                                | 130 ms: 1.46x slower                                                  |
| Geometric mean | (ref)                                                  | 1.22x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.76 ms: 1.15x faster                                                 |
| regex_dna      | 168 ms                                                 | 176 ms: 1.05x slower                                                  |
| regex_compile  | 142 ms                                                 | 157 ms: 1.10x slower                                                  |
| regex_v8       | 20.6 ms                                                | 23.2 ms: 1.12x slower                                                 |
| Geometric mean | (ref)                                                  | 1.03x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.7 ms: 1.10x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.07x faster                                                  |
| json_loads           | 26.5 us                                                | 28.1 us: 1.06x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 95.5 ms: 1.12x slower                                                 |
| unpickle_pure_python | 221 us                                                 | 254 us: 1.15x slower                                                  |
| tomli_loads          | 2.11 sec                                               | 2.52 sec: 1.20x slower                                                |
| pickle_pure_python   | 308 us                                                 | 370 us: 1.20x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 71.6 ms: 1.21x slower                                                 |
| json_dumps           | 10.4 ms                                                | 13.2 ms: 1.27x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.11x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.2 ms: 1.43x slower                                                 |
| python_startup         | 9.93 ms                                                | 17.1 ms: 1.72x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.57x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 27.7 ms: 1.21x slower                                                 |
| genshi_xml      | 50.2 ms                                                | 60.8 ms: 1.21x slower                                                 |
| django_template | 34.7 ms                                                | 44.0 ms: 1.27x slower                                                 |
| mako            | 11.0 ms                                                | 15.6 ms: 1.42x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.28x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 618 ms: 1.80x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 266 ms: 1.68x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 337 ms: 1.66x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 653 ms: 1.66x faster                                                  |
| async_tree_none            | 464 ms                                                 | 306 ms: 1.52x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 375 ms: 1.48x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 512 ms: 1.41x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 544 ms: 1.31x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.76 ms: 1.15x faster                                                 |
| deepcopy                   | 352 us                                                 | 307 us: 1.15x faster                                                  |
| pathlib                    | 21.5 ms                                                | 19.4 ms: 1.11x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 87.7 ms: 1.10x faster                                                 |
| gc_traversal               | 3.46 ms                                                | 3.16 ms: 1.09x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.07x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 38.0 us: 1.06x faster                                                 |
| generators                 | 32.2 ms                                                | 30.7 ms: 1.05x faster                                                 |
| sqlite_synth               | 2.20 us                                                | 2.16 us: 1.02x faster                                                 |
| pidigits                   | 184 ms                                                 | 181 ms: 1.02x faster                                                  |
| json                       | 5.02 ms                                                | 4.95 ms: 1.02x faster                                                 |
| spectral_norm              | 110 ms                                                 | 110 ms: 1.00x slower                                                  |
| asyncio_websockets         | 517 ms                                                 | 521 ms: 1.01x slower                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.78 sec: 1.01x slower                                                |
| coroutines                 | 23.9 ms                                                | 24.6 ms: 1.03x slower                                                 |
| logging_silent             | 109 ns                                                 | 114 ns: 1.05x slower                                                  |
| regex_dna                  | 168 ms                                                 | 176 ms: 1.05x slower                                                  |
| deepcopy_reduce            | 3.08 us                                                | 3.25 us: 1.06x slower                                                 |
| json_loads                 | 26.5 us                                                | 28.1 us: 1.06x slower                                                 |
| comprehensions             | 19.8 us                                                | 21.2 us: 1.07x slower                                                 |
| async_generators           | 384 ms                                                 | 415 ms: 1.08x slower                                                  |
| dulwich_log                | 78.9 ms                                                | 85.2 ms: 1.08x slower                                                 |
| docutils                   | 2.64 sec                                               | 2.87 sec: 1.09x slower                                                |
| scimark_fft                | 342 ms                                                 | 373 ms: 1.09x slower                                                  |
| pylint                     | 319 ms                                                 | 349 ms: 1.10x slower                                                  |
| regex_compile              | 142 ms                                                 | 157 ms: 1.10x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 95.5 ms: 1.12x slower                                                 |
| sqlglot_normalize          | 107 ms                                                 | 119 ms: 1.12x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 23.2 ms: 1.12x slower                                                 |
| mdp                        | 2.42 sec                                               | 2.72 sec: 1.13x slower                                                |
| crypto_pyaes               | 76.6 ms                                                | 86.7 ms: 1.13x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 844 ms: 1.14x slower                                                  |
| sqlglot_optimize           | 53.3 ms                                                | 61.0 ms: 1.15x slower                                                 |
| sqlalchemy_imperative      | 21.8 ms                                                | 25.0 ms: 1.15x slower                                                 |
| pprint_pformat             | 1.52 sec                                               | 1.75 sec: 1.15x slower                                                |
| unpickle_pure_python       | 221 us                                                 | 254 us: 1.15x slower                                                  |
| pycparser                  | 1.17 sec                                               | 1.35 sec: 1.16x slower                                                |
| pyflate                    | 448 ms                                                 | 519 ms: 1.16x slower                                                  |
| go                         | 139 ms                                                 | 165 ms: 1.19x slower                                                  |
| tomli_loads                | 2.11 sec                                               | 2.52 sec: 1.20x slower                                                |
| pickle_pure_python         | 308 us                                                 | 370 us: 1.20x slower                                                  |
| typing_runtime_protocols   | 163 us                                                 | 197 us: 1.21x slower                                                  |
| genshi_text                | 22.8 ms                                                | 27.7 ms: 1.21x slower                                                 |
| genshi_xml                 | 50.2 ms                                                | 60.8 ms: 1.21x slower                                                 |
| nqueens                    | 80.1 ms                                                | 97.2 ms: 1.21x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 71.6 ms: 1.21x slower                                                 |
| 2to3                       | 264 ms                                                 | 323 ms: 1.23x slower                                                  |
| logging_simple             | 6.63 us                                                | 8.14 us: 1.23x slower                                                 |
| raytrace                   | 299 ms                                                 | 372 ms: 1.24x slower                                                  |
| meteor_contest             | 104 ms                                                 | 129 ms: 1.24x slower                                                  |
| logging_format             | 7.35 us                                                | 9.20 us: 1.25x slower                                                 |
| hexiom                     | 6.17 ms                                                | 7.73 ms: 1.25x slower                                                 |
| chaos                      | 62.8 ms                                                | 79.1 ms: 1.26x slower                                                 |
| html5lib                   | 63.6 ms                                                | 80.4 ms: 1.26x slower                                                 |
| sqlalchemy_declarative     | 143 ms                                                 | 181 ms: 1.27x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 13.2 ms: 1.27x slower                                                 |
| django_template            | 34.7 ms                                                | 44.0 ms: 1.27x slower                                                 |
| float                      | 80.8 ms                                                | 103 ms: 1.27x slower                                                  |
| thrift                     | 791 us                                                 | 1.02 ms: 1.28x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.68 ms: 1.29x slower                                                 |
| sqlglot_transpile          | 1.67 ms                                                | 2.18 ms: 1.30x slower                                                 |
| telco                      | 6.53 ms                                                | 8.52 ms: 1.31x slower                                                 |
| fannkuch                   | 372 ms                                                 | 490 ms: 1.32x slower                                                  |
| sqlglot_parse              | 1.36 ms                                                | 1.85 ms: 1.37x slower                                                 |
| scimark_sor                | 130 ms                                                 | 178 ms: 1.37x slower                                                  |
| coverage                   | 71.4 ms                                                | 98.4 ms: 1.38x slower                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 94.6 ms: 1.38x slower                                                 |
| sympy_integrate            | 20.5 ms                                                | 28.6 ms: 1.39x slower                                                 |
| richards                   | 45.9 ms                                                | 64.9 ms: 1.41x slower                                                 |
| mako                       | 11.0 ms                                                | 15.6 ms: 1.42x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 10.2 ms: 1.43x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 163 ms: 1.43x slower                                                  |
| richards_super             | 51.9 ms                                                | 74.8 ms: 1.44x slower                                                 |
| nbody                      | 89.3 ms                                                | 130 ms: 1.46x slower                                                  |
| deltablue                  | 3.45 ms                                                | 5.36 ms: 1.55x slower                                                 |
| sympy_str                  | 292 ms                                                 | 458 ms: 1.57x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.78 ms: 1.63x slower                                                 |
| python_startup             | 9.93 ms                                                | 17.1 ms: 1.72x slower                                                 |
| sympy_expand               | 468 ms                                                 | 928 ms: 1.98x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 340 ms: 2.05x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 3.34 ms: 3.55x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 106 ms: 9.82x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.17x slower                                                          |
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241213-3.14.0a2+-b1ed3ee-NOGIL/bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.115x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.12x
- 95% likely to have a slowdown of 1.11x
- 99% likely to have a slowdown of 1.09x

# Memory
- memory change: 1.35x