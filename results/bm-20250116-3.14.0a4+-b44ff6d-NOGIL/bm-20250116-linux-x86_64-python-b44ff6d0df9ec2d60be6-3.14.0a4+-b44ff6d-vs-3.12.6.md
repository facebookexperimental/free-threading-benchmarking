# Results vs. 3.12.6

- fork: python
- ref: b44ff6d0df9ec2d60be6
- machine: linux-x86_64
- commit hash: b44ff6d
- commit date: 2025-01-16
- overall geometric mean: 1.062x slower
- HPT reliability: 99.98%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-linux-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 603 ms: 1.32x slower                                                   |
| docutils       | 4.00 sec                                               | 4.11 sec: 1.03x slower                                                 |
| html5lib       | 88.9 ms                                                | 107 ms: 1.20x slower                                                   |
| Geometric mean | (ref)                                                  | 1.18x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-linux-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 775 ms: 2.49x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 835 ms: 2.21x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 347 ms: 2.03x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 468 ms: 1.99x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 534 ms: 1.83x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 673 ms: 1.64x faster                                                   |
| async_tree_none            | 741 ms                                                 | 456 ms: 1.63x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 776 ms: 1.39x faster                                                   |
| coroutines                 | 29.5 ms                                                | 34.0 ms: 1.15x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.55x faster                                                           |

Benchmark hidden because not significant (2): async_generators, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-linux-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 104 ms: 1.18x faster                                                   |
| pidigits       | 250 ms                                                 | 227 ms: 1.10x faster                                                   |
| nbody          | 119 ms                                                 | 176 ms: 1.48x slower                                                   |
| Geometric mean | (ref)                                                  | 1.05x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-linux-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.65 ms: 1.10x faster                                                  |
| regex_compile  | 187 ms                                                 | 196 ms: 1.05x slower                                                   |
| regex_v8       | 32.5 ms                                                | 35.3 ms: 1.09x slower                                                  |
| regex_dna      | 278 ms                                                 | 304 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                  | 1.03x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-linux-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 169 ms                                                 | 144 ms: 1.18x faster                                                   |
| xml_etree_parse      | 241 ms                                                 | 225 ms: 1.07x faster                                                   |
| tomli_loads          | 2.88 sec                                               | 2.99 sec: 1.04x slower                                                 |
| xml_etree_generate   | 127 ms                                                 | 140 ms: 1.10x slower                                                   |
| unpickle_pure_python | 300 us                                                 | 341 us: 1.14x slower                                                   |
| json_loads           | 37.9 us                                                | 44.7 us: 1.18x slower                                                  |
| json_dumps           | 14.3 ms                                                | 17.2 ms: 1.20x slower                                                  |
| pickle_pure_python   | 436 us                                                 | 527 us: 1.21x slower                                                   |
| xml_etree_process    | 83.7 ms                                                | 110 ms: 1.31x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.10x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-linux-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 24.2 ms: 1.38x slower                                                  |
| python_startup         | 23.7 ms                                                | 37.0 ms: 1.56x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.46x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-linux-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 30.2 ms                                                | 38.5 ms: 1.28x slower                                                  |
| django_template | 44.9 ms                                                | 58.6 ms: 1.30x slower                                                  |
| genshi_xml      | 67.6 ms                                                | 96.8 ms: 1.43x slower                                                  |
| mako            | 15.7 ms                                                | 24.8 ms: 1.58x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.39x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-linux-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 775 ms: 2.49x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 835 ms: 2.21x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 347 ms: 2.03x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 468 ms: 1.99x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 534 ms: 1.83x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 673 ms: 1.64x faster                                                   |
| async_tree_none            | 741 ms                                                 | 456 ms: 1.63x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 776 ms: 1.39x faster                                                   |
| float                      | 123 ms                                                 | 104 ms: 1.18x faster                                                   |
| xml_etree_iterparse        | 169 ms                                                 | 144 ms: 1.18x faster                                                   |
| pycparser                  | 1.79 sec                                               | 1.61 sec: 1.12x faster                                                 |
| sqlite_synth               | 3.87 us                                                | 3.48 us: 1.11x faster                                                  |
| regex_effbot               | 5.13 ms                                                | 4.65 ms: 1.10x faster                                                  |
| pidigits                   | 250 ms                                                 | 227 ms: 1.10x faster                                                   |
| xml_etree_parse            | 241 ms                                                 | 225 ms: 1.07x faster                                                   |
| deepcopy                   | 468 us                                                 | 443 us: 1.06x faster                                                   |
| docutils                   | 4.00 sec                                               | 4.11 sec: 1.03x slower                                                 |
| tomli_loads                | 2.88 sec                                               | 2.99 sec: 1.04x slower                                                 |
| nqueens                    | 117 ms                                                 | 122 ms: 1.05x slower                                                   |
| regex_compile              | 187 ms                                                 | 196 ms: 1.05x slower                                                   |
| sqlglot_transpile          | 2.34 ms                                                | 2.49 ms: 1.07x slower                                                  |
| raytrace                   | 408 ms                                                 | 435 ms: 1.07x slower                                                   |
| sqlalchemy_declarative     | 218 ms                                                 | 233 ms: 1.07x slower                                                   |
| go                         | 172 ms                                                 | 186 ms: 1.08x slower                                                   |
| mdp                        | 3.97 sec                                               | 4.29 sec: 1.08x slower                                                 |
| deepcopy_reduce            | 4.04 us                                                | 4.37 us: 1.08x slower                                                  |
| regex_v8                   | 32.5 ms                                                | 35.3 ms: 1.09x slower                                                  |
| regex_dna                  | 278 ms                                                 | 304 ms: 1.09x slower                                                   |
| sympy_str                  | 385 ms                                                 | 422 ms: 1.10x slower                                                   |
| sympy_sum                  | 222 ms                                                 | 244 ms: 1.10x slower                                                   |
| xml_etree_generate         | 127 ms                                                 | 140 ms: 1.10x slower                                                   |
| scimark_sor                | 167 ms                                                 | 185 ms: 1.11x slower                                                   |
| scimark_fft                | 500 ms                                                 | 556 ms: 1.11x slower                                                   |
| sqlglot_normalize          | 157 ms                                                 | 175 ms: 1.11x slower                                                   |
| sqlglot_optimize           | 76.0 ms                                                | 84.7 ms: 1.12x slower                                                  |
| generators                 | 41.1 ms                                                | 46.0 ms: 1.12x slower                                                  |
| logging_silent             | 139 ns                                                 | 156 ns: 1.12x slower                                                   |
| crypto_pyaes               | 107 ms                                                 | 121 ms: 1.13x slower                                                   |
| deepcopy_memo              | 52.4 us                                                | 59.2 us: 1.13x slower                                                  |
| unpickle_pure_python       | 300 us                                                 | 341 us: 1.14x slower                                                   |
| sympy_integrate            | 29.8 ms                                                | 34.1 ms: 1.14x slower                                                  |
| fannkuch                   | 540 ms                                                 | 622 ms: 1.15x slower                                                   |
| coroutines                 | 29.5 ms                                                | 34.0 ms: 1.15x slower                                                  |
| scimark_lu                 | 152 ms                                                 | 177 ms: 1.16x slower                                                   |
| pprint_safe_repr           | 967 ms                                                 | 1.14 sec: 1.18x slower                                                 |
| dulwich_log                | 100 ms                                                 | 118 ms: 1.18x slower                                                   |
| json_loads                 | 37.9 us                                                | 44.7 us: 1.18x slower                                                  |
| pprint_pformat             | 1.98 sec                                               | 2.35 sec: 1.19x slower                                                 |
| meteor_contest             | 146 ms                                                 | 175 ms: 1.20x slower                                                   |
| html5lib                   | 88.9 ms                                                | 107 ms: 1.20x slower                                                   |
| bpe_tokeniser              | 6.59 sec                                               | 7.91 sec: 1.20x slower                                                 |
| json_dumps                 | 14.3 ms                                                | 17.2 ms: 1.20x slower                                                  |
| pickle_pure_python         | 436 us                                                 | 527 us: 1.21x slower                                                   |
| json                       | 6.85 ms                                                | 8.31 ms: 1.21x slower                                                  |
| chaos                      | 84.9 ms                                                | 103 ms: 1.22x slower                                                   |
| sqlglot_parse              | 1.79 ms                                                | 2.21 ms: 1.23x slower                                                  |
| telco                      | 9.59 ms                                                | 11.9 ms: 1.24x slower                                                  |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 8.38 ms: 1.25x slower                                                  |
| thrift                     | 1.06 ms                                                | 1.34 ms: 1.26x slower                                                  |
| genshi_text                | 30.2 ms                                                | 38.5 ms: 1.28x slower                                                  |
| hexiom                     | 8.27 ms                                                | 10.7 ms: 1.29x slower                                                  |
| scimark_monte_carlo        | 96.4 ms                                                | 125 ms: 1.30x slower                                                   |
| django_template            | 44.9 ms                                                | 58.6 ms: 1.30x slower                                                  |
| richards                   | 60.3 ms                                                | 78.9 ms: 1.31x slower                                                  |
| xml_etree_process          | 83.7 ms                                                | 110 ms: 1.31x slower                                                   |
| sympy_expand               | 582 ms                                                 | 763 ms: 1.31x slower                                                   |
| richards_super             | 72.8 ms                                                | 95.5 ms: 1.31x slower                                                  |
| 2to3                       | 456 ms                                                 | 603 ms: 1.32x slower                                                   |
| typing_runtime_protocols   | 224 us                                                 | 298 us: 1.33x slower                                                   |
| gc_traversal               | 5.86 ms                                                | 7.85 ms: 1.34x slower                                                  |
| sqlalchemy_imperative      | 24.7 ms                                                | 33.1 ms: 1.34x slower                                                  |
| logging_format             | 9.59 us                                                | 13.0 us: 1.36x slower                                                  |
| python_startup_no_site     | 17.6 ms                                                | 24.2 ms: 1.38x slower                                                  |
| coverage                   | 95.4 ms                                                | 132 ms: 1.38x slower                                                   |
| genshi_xml                 | 67.6 ms                                                | 96.8 ms: 1.43x slower                                                  |
| nbody                      | 119 ms                                                 | 176 ms: 1.48x slower                                                   |
| create_gc_cycles           | 1.94 ms                                                | 2.98 ms: 1.54x slower                                                  |
| python_startup             | 23.7 ms                                                | 37.0 ms: 1.56x slower                                                  |
| deltablue                  | 4.27 ms                                                | 6.72 ms: 1.57x slower                                                  |
| bench_thread_pool          | 3.48 ms                                                | 5.49 ms: 1.58x slower                                                  |
| mako                       | 15.7 ms                                                | 24.8 ms: 1.58x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 97.1 ms: 4.69x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.10x slower                                                           |

Benchmark hidden because not significant (8): pathlib, logging_simple, spectral_norm, comprehensions, pyflate, async_generators, pylint, asyncio_websockets
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250116-3.14.0a4+-b44ff6d-NOGIL/bm-20250116-linux-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4+-b44ff6d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.062x slower

# HPT report

- Reliability score: 99.98% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.35x