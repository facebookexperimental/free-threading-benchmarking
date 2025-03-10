# Results vs. 3.13.0rc2

- fork: python
- ref: 98fa4a49fecbac3c990a
- machine: linux-x86_64
- commit hash: 98fa4a4
- commit date: 2025-03-09
- overall geometric mean: 1.078x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.05x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250309-vultr-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 299 ms: 1.15x slower                                                   |
| docutils       | 2.63 sec                                                               | 2.83 sec: 1.08x slower                                                 |
| html5lib       | 68.6 ms                                                                | 73.5 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.10x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250309-vultr-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 552 ms: 1.63x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 582 ms: 1.51x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 239 ms: 1.40x faster                                                   |
| async_tree_memoization     | 459 ms                                                                 | 343 ms: 1.34x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 308 ms: 1.33x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 276 ms: 1.28x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 499 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 531 ms: 1.25x faster                                                   |
| async_generators           | 375 ms                                                                 | 377 ms: 1.01x slower                                                   |
| coroutines                 | 23.3 ms                                                                | 23.7 ms: 1.02x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.26x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250309-vultr-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 194 ms: 1.12x faster                                                   |
| nbody          | 85.3 ms                                                                | 129 ms: 1.51x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.11x slower                                                           |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250309-vultr-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.84 ms: 1.13x faster                                                  |
| regex_dna      | 189 ms                                                                 | 176 ms: 1.07x faster                                                   |
| regex_v8       | 23.2 ms                                                                | 23.0 ms: 1.01x faster                                                  |
| regex_compile  | 131 ms                                                                 | 156 ms: 1.19x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250309-vultr-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 88.0 ms: 1.07x faster                                                  |
| xml_etree_parse      | 136 ms                                                                 | 128 ms: 1.06x faster                                                   |
| json_loads           | 27.3 us                                                                | 29.3 us: 1.07x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                                | 96.2 ms: 1.13x slower                                                  |
| xml_etree_process    | 59.2 ms                                                                | 70.1 ms: 1.18x slower                                                  |
| tomli_loads          | 2.01 sec                                                               | 2.40 sec: 1.19x slower                                                 |
| json_dumps           | 10.6 ms                                                                | 12.8 ms: 1.20x slower                                                  |
| unpickle_pure_python | 208 us                                                                 | 254 us: 1.22x slower                                                   |
| pickle_pure_python   | 292 us                                                                 | 362 us: 1.24x slower                                                   |
| Geometric mean       | (ref)                                                                  | 1.12x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250309-vultr-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 15.7 ms: 1.43x slower                                                  |
| python_startup_no_site | 7.41 ms                                                                | 11.1 ms: 1.50x slower                                                  |
| Geometric mean         | (ref)                                                                  | 1.46x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250309-vultr-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 60.0 ms: 1.22x slower                                                  |
| django_template | 34.2 ms                                                                | 42.6 ms: 1.25x slower                                                  |
| genshi_text     | 21.7 ms                                                                | 28.0 ms: 1.29x slower                                                  |
| mako            | 11.2 ms                                                                | 15.7 ms: 1.40x slower                                                  |
| Geometric mean  | (ref)                                                                  | 1.29x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250309-vultr-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.74 ms: 1.91x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 552 ms: 1.63x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 582 ms: 1.51x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 239 ms: 1.40x faster                                                   |
| async_tree_memoization     | 459 ms                                                                 | 343 ms: 1.34x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 308 ms: 1.33x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 276 ms: 1.28x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 499 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 531 ms: 1.25x faster                                                   |
| deepcopy                   | 357 us                                                                 | 313 us: 1.14x faster                                                   |
| regex_effbot               | 3.21 ms                                                                | 2.84 ms: 1.13x faster                                                  |
| pidigits                   | 216 ms                                                                 | 194 ms: 1.12x faster                                                   |
| sqlite_synth               | 2.25 us                                                                | 2.03 us: 1.11x faster                                                  |
| regex_dna                  | 189 ms                                                                 | 176 ms: 1.07x faster                                                   |
| xml_etree_iterparse        | 94.4 ms                                                                | 88.0 ms: 1.07x faster                                                  |
| xml_etree_parse            | 136 ms                                                                 | 128 ms: 1.06x faster                                                   |
| dulwich_log                | 74.5 ms                                                                | 73.0 ms: 1.02x faster                                                  |
| regex_v8                   | 23.2 ms                                                                | 23.0 ms: 1.01x faster                                                  |
| async_generators           | 375 ms                                                                 | 377 ms: 1.01x slower                                                   |
| go                         | 141 ms                                                                 | 142 ms: 1.01x slower                                                   |
| coroutines                 | 23.3 ms                                                                | 23.7 ms: 1.02x slower                                                  |
| deepcopy_memo              | 38.1 us                                                                | 38.7 us: 1.02x slower                                                  |
| json                       | 4.98 ms                                                                | 5.07 ms: 1.02x slower                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 3.19 us: 1.02x slower                                                  |
| pathlib                    | 19.3 ms                                                                | 19.7 ms: 1.02x slower                                                  |
| scimark_sor                | 134 ms                                                                 | 138 ms: 1.04x slower                                                   |
| pycparser                  | 1.12 sec                                                               | 1.19 sec: 1.06x slower                                                 |
| spectral_norm              | 108 ms                                                                 | 114 ms: 1.06x slower                                                   |
| bpe_tokeniser              | 4.46 sec                                                               | 4.77 sec: 1.07x slower                                                 |
| json_loads                 | 27.3 us                                                                | 29.3 us: 1.07x slower                                                  |
| html5lib                   | 68.6 ms                                                                | 73.5 ms: 1.07x slower                                                  |
| docutils                   | 2.63 sec                                                               | 2.83 sec: 1.08x slower                                                 |
| mdp                        | 2.34 sec                                                               | 2.62 sec: 1.12x slower                                                 |
| pyflate                    | 449 ms                                                                 | 503 ms: 1.12x slower                                                   |
| xml_etree_generate         | 85.4 ms                                                                | 96.2 ms: 1.13x slower                                                  |
| generators                 | 28.5 ms                                                                | 32.4 ms: 1.14x slower                                                  |
| scimark_fft                | 348 ms                                                                 | 396 ms: 1.14x slower                                                   |
| telco                      | 7.77 ms                                                                | 8.87 ms: 1.14x slower                                                  |
| 2to3                       | 259 ms                                                                 | 299 ms: 1.15x slower                                                   |
| thrift                     | 772 us                                                                 | 891 us: 1.16x slower                                                   |
| sqlglot_normalize          | 106 ms                                                                 | 123 ms: 1.16x slower                                                   |
| pprint_safe_repr           | 719 ms                                                                 | 841 ms: 1.17x slower                                                   |
| logging_silent             | 98.2 ns                                                                | 115 ns: 1.17x slower                                                   |
| sqlglot_optimize           | 52.7 ms                                                                | 61.7 ms: 1.17x slower                                                  |
| coverage                   | 82.5 ms                                                                | 97.1 ms: 1.18x slower                                                  |
| logging_format             | 6.92 us                                                                | 8.17 us: 1.18x slower                                                  |
| xml_etree_process          | 59.2 ms                                                                | 70.1 ms: 1.18x slower                                                  |
| regex_compile              | 131 ms                                                                 | 156 ms: 1.19x slower                                                   |
| logging_simple             | 6.14 us                                                                | 7.31 us: 1.19x slower                                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.74 sec: 1.19x slower                                                 |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.67 ms: 1.19x slower                                                  |
| tomli_loads                | 2.01 sec                                                               | 2.40 sec: 1.19x slower                                                 |
| comprehensions             | 16.6 us                                                                | 19.8 us: 1.20x slower                                                  |
| json_dumps                 | 10.6 ms                                                                | 12.8 ms: 1.20x slower                                                  |
| sympy_expand               | 454 ms                                                                 | 552 ms: 1.22x slower                                                   |
| sympy_sum                  | 154 ms                                                                 | 188 ms: 1.22x slower                                                   |
| unpickle_pure_python       | 208 us                                                                 | 254 us: 1.22x slower                                                   |
| sympy_integrate            | 19.7 ms                                                                | 24.1 ms: 1.22x slower                                                  |
| genshi_xml                 | 49.1 ms                                                                | 60.0 ms: 1.22x slower                                                  |
| sympy_str                  | 274 ms                                                                 | 335 ms: 1.22x slower                                                   |
| deltablue                  | 3.10 ms                                                                | 3.82 ms: 1.24x slower                                                  |
| sqlglot_transpile          | 1.55 ms                                                                | 1.92 ms: 1.24x slower                                                  |
| chaos                      | 56.3 ms                                                                | 69.7 ms: 1.24x slower                                                  |
| pickle_pure_python         | 292 us                                                                 | 362 us: 1.24x slower                                                   |
| nqueens                    | 77.7 ms                                                                | 96.8 ms: 1.25x slower                                                  |
| django_template            | 34.2 ms                                                                | 42.6 ms: 1.25x slower                                                  |
| richards                   | 44.4 ms                                                                | 55.6 ms: 1.25x slower                                                  |
| typing_runtime_protocols   | 156 us                                                                 | 195 us: 1.25x slower                                                   |
| hexiom                     | 5.95 ms                                                                | 7.51 ms: 1.26x slower                                                  |
| scimark_lu                 | 112 ms                                                                 | 142 ms: 1.26x slower                                                   |
| meteor_contest             | 101 ms                                                                 | 129 ms: 1.28x slower                                                   |
| richards_super             | 50.4 ms                                                                | 64.4 ms: 1.28x slower                                                  |
| crypto_pyaes               | 68.2 ms                                                                | 87.5 ms: 1.28x slower                                                  |
| scimark_monte_carlo        | 65.8 ms                                                                | 84.5 ms: 1.28x slower                                                  |
| sqlglot_parse              | 1.25 ms                                                                | 1.60 ms: 1.29x slower                                                  |
| genshi_text                | 21.7 ms                                                                | 28.0 ms: 1.29x slower                                                  |
| raytrace                   | 250 ms                                                                 | 328 ms: 1.31x slower                                                   |
| fannkuch                   | 376 ms                                                                 | 499 ms: 1.33x slower                                                   |
| mako                       | 11.2 ms                                                                | 15.7 ms: 1.40x slower                                                  |
| python_startup             | 11.0 ms                                                                | 15.7 ms: 1.43x slower                                                  |
| python_startup_no_site     | 7.41 ms                                                                | 11.1 ms: 1.50x slower                                                  |
| nbody                      | 85.3 ms                                                                | 129 ms: 1.51x slower                                                   |
| bench_thread_pool          | 924 us                                                                 | 3.17 ms: 3.43x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                                | 95.7 ms: 8.70x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.13x slower                                                           |

Benchmark hidden because not significant (4): create_gc_cycles, pylint, asyncio_websockets, float
Ignored benchmarks (14) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250309-3.14.0a5+-98fa4a4-NOGIL/bm-20250309-vultr-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.078x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: 1.34x