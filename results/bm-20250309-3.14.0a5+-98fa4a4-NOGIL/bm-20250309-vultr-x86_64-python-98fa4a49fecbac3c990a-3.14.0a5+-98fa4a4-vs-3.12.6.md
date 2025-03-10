# Results vs. 3.12.6

- fork: python
- ref: 98fa4a49fecbac3c990a
- machine: linux-x86_64
- commit hash: 98fa4a4
- commit date: 2025-03-09
- overall geometric mean: 1.046x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250309-vultr-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 299 ms: 1.13x slower                                                   |
| docutils       | 2.64 sec                                               | 2.83 sec: 1.07x slower                                                 |
| html5lib       | 63.6 ms                                                | 73.5 ms: 1.16x slower                                                  |
| Geometric mean | (ref)                                                  | 1.12x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250309-vultr-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 552 ms: 2.01x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 239 ms: 1.87x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 582 ms: 1.86x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 308 ms: 1.82x faster                                                   |
| async_tree_none            | 464 ms                                                 | 276 ms: 1.68x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 343 ms: 1.62x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 499 ms: 1.45x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 531 ms: 1.35x faster                                                   |
| async_generators           | 384 ms                                                 | 377 ms: 1.02x faster                                                   |
| coroutines                 | 23.9 ms                                                | 23.7 ms: 1.01x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.47x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250309-vultr-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 76.9 ms: 1.05x faster                                                  |
| pidigits       | 184 ms                                                 | 194 ms: 1.05x slower                                                   |
| nbody          | 89.3 ms                                                | 129 ms: 1.44x slower                                                   |
| Geometric mean | (ref)                                                  | 1.13x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250309-vultr-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.84 ms: 1.11x faster                                                  |
| regex_dna      | 168 ms                                                 | 176 ms: 1.05x slower                                                   |
| regex_compile  | 142 ms                                                 | 156 ms: 1.10x slower                                                   |
| regex_v8       | 20.6 ms                                                | 23.0 ms: 1.12x slower                                                  |
| Geometric mean | (ref)                                                  | 1.04x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250309-vultr-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.0 ms: 1.10x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.08x faster                                                   |
| json_loads           | 26.5 us                                                | 29.3 us: 1.10x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 96.2 ms: 1.13x slower                                                  |
| tomli_loads          | 2.11 sec                                               | 2.40 sec: 1.14x slower                                                 |
| unpickle_pure_python | 221 us                                                 | 254 us: 1.15x slower                                                   |
| pickle_pure_python   | 308 us                                                 | 362 us: 1.18x slower                                                   |
| xml_etree_process    | 59.0 ms                                                | 70.1 ms: 1.19x slower                                                  |
| json_dumps           | 10.4 ms                                                | 12.8 ms: 1.24x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.10x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250309-vultr-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 11.1 ms: 1.55x slower                                                  |
| python_startup         | 9.93 ms                                                | 15.7 ms: 1.59x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.57x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250309-vultr-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 60.0 ms: 1.20x slower                                                  |
| genshi_text     | 22.8 ms                                                | 28.0 ms: 1.23x slower                                                  |
| django_template | 34.7 ms                                                | 42.6 ms: 1.23x slower                                                  |
| mako            | 11.0 ms                                                | 15.7 ms: 1.43x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.27x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250309-vultr-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 552 ms: 2.01x faster                                                   |
| gc_traversal               | 3.46 ms                                                | 1.74 ms: 1.99x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 239 ms: 1.87x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 582 ms: 1.86x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 308 ms: 1.82x faster                                                   |
| async_tree_none            | 464 ms                                                 | 276 ms: 1.68x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 343 ms: 1.62x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 499 ms: 1.45x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 531 ms: 1.35x faster                                                   |
| deepcopy                   | 352 us                                                 | 313 us: 1.12x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.84 ms: 1.11x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 88.0 ms: 1.10x faster                                                  |
| pathlib                    | 21.5 ms                                                | 19.7 ms: 1.09x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 2.03 us: 1.09x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                                   |
| dulwich_log                | 78.9 ms                                                | 73.0 ms: 1.08x faster                                                  |
| float                      | 80.8 ms                                                | 76.9 ms: 1.05x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 38.7 us: 1.04x faster                                                  |
| async_generators           | 384 ms                                                 | 377 ms: 1.02x faster                                                   |
| coroutines                 | 23.9 ms                                                | 23.7 ms: 1.01x faster                                                  |
| generators                 | 32.2 ms                                                | 32.4 ms: 1.01x slower                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.77 sec: 1.01x slower                                                 |
| json                       | 5.02 ms                                                | 5.07 ms: 1.01x slower                                                  |
| pycparser                  | 1.17 sec                                               | 1.19 sec: 1.02x slower                                                 |
| go                         | 139 ms                                                 | 142 ms: 1.02x slower                                                   |
| deepcopy_reduce            | 3.08 us                                                | 3.19 us: 1.04x slower                                                  |
| spectral_norm              | 110 ms                                                 | 114 ms: 1.04x slower                                                   |
| regex_dna                  | 168 ms                                                 | 176 ms: 1.05x slower                                                   |
| pidigits                   | 184 ms                                                 | 194 ms: 1.05x slower                                                   |
| logging_silent             | 109 ns                                                 | 115 ns: 1.06x slower                                                   |
| scimark_sor                | 130 ms                                                 | 138 ms: 1.07x slower                                                   |
| docutils                   | 2.64 sec                                               | 2.83 sec: 1.07x slower                                                 |
| mdp                        | 2.42 sec                                               | 2.62 sec: 1.08x slower                                                 |
| regex_compile              | 142 ms                                                 | 156 ms: 1.10x slower                                                   |
| raytrace                   | 299 ms                                                 | 328 ms: 1.10x slower                                                   |
| sqlalchemy_declarative     | 143 ms                                                 | 157 ms: 1.10x slower                                                   |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.0 ms: 1.10x slower                                                  |
| logging_simple             | 6.63 us                                                | 7.31 us: 1.10x slower                                                  |
| json_loads                 | 26.5 us                                                | 29.3 us: 1.10x slower                                                  |
| deltablue                  | 3.45 ms                                                | 3.82 ms: 1.11x slower                                                  |
| chaos                      | 62.8 ms                                                | 69.7 ms: 1.11x slower                                                  |
| logging_format             | 7.35 us                                                | 8.17 us: 1.11x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 23.0 ms: 1.12x slower                                                  |
| pyflate                    | 448 ms                                                 | 503 ms: 1.12x slower                                                   |
| thrift                     | 791 us                                                 | 891 us: 1.13x slower                                                   |
| xml_etree_generate         | 85.2 ms                                                | 96.2 ms: 1.13x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 188 ms: 1.13x slower                                                   |
| pprint_safe_repr           | 743 ms                                                 | 841 ms: 1.13x slower                                                   |
| 2to3                       | 264 ms                                                 | 299 ms: 1.13x slower                                                   |
| tomli_loads                | 2.11 sec                                               | 2.40 sec: 1.14x slower                                                 |
| crypto_pyaes               | 76.6 ms                                                | 87.5 ms: 1.14x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.74 sec: 1.14x slower                                                 |
| sympy_str                  | 292 ms                                                 | 335 ms: 1.15x slower                                                   |
| unpickle_pure_python       | 221 us                                                 | 254 us: 1.15x slower                                                   |
| sqlglot_normalize          | 107 ms                                                 | 123 ms: 1.15x slower                                                   |
| sqlglot_transpile          | 1.67 ms                                                | 1.92 ms: 1.15x slower                                                  |
| html5lib                   | 63.6 ms                                                | 73.5 ms: 1.16x slower                                                  |
| sqlglot_optimize           | 53.3 ms                                                | 61.7 ms: 1.16x slower                                                  |
| scimark_fft                | 342 ms                                                 | 396 ms: 1.16x slower                                                   |
| sympy_integrate            | 20.5 ms                                                | 24.1 ms: 1.17x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 362 us: 1.18x slower                                                   |
| sympy_expand               | 468 ms                                                 | 552 ms: 1.18x slower                                                   |
| sqlglot_parse              | 1.36 ms                                                | 1.60 ms: 1.18x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 70.1 ms: 1.19x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 60.0 ms: 1.20x slower                                                  |
| typing_runtime_protocols   | 163 us                                                 | 195 us: 1.20x slower                                                   |
| nqueens                    | 80.1 ms                                                | 96.8 ms: 1.21x slower                                                  |
| richards                   | 45.9 ms                                                | 55.6 ms: 1.21x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.33 ms: 1.22x slower                                                  |
| hexiom                     | 6.17 ms                                                | 7.51 ms: 1.22x slower                                                  |
| genshi_text                | 22.8 ms                                                | 28.0 ms: 1.23x slower                                                  |
| django_template            | 34.7 ms                                                | 42.6 ms: 1.23x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 84.5 ms: 1.23x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 12.8 ms: 1.24x slower                                                  |
| richards_super             | 51.9 ms                                                | 64.4 ms: 1.24x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 142 ms: 1.25x slower                                                   |
| meteor_contest             | 104 ms                                                 | 129 ms: 1.25x slower                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.67 ms: 1.29x slower                                                  |
| fannkuch                   | 372 ms                                                 | 499 ms: 1.34x slower                                                   |
| telco                      | 6.53 ms                                                | 8.87 ms: 1.36x slower                                                  |
| coverage                   | 71.4 ms                                                | 97.1 ms: 1.36x slower                                                  |
| mako                       | 11.0 ms                                                | 15.7 ms: 1.43x slower                                                  |
| nbody                      | 89.3 ms                                                | 129 ms: 1.44x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 11.1 ms: 1.55x slower                                                  |
| python_startup             | 9.93 ms                                                | 15.7 ms: 1.59x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 3.17 ms: 3.37x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 95.7 ms: 8.86x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.09x slower                                                           |

Benchmark hidden because not significant (3): pylint, asyncio_websockets, comprehensions
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250309-3.14.0a5+-98fa4a4-NOGIL/bm-20250309-vultr-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.046x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.36x