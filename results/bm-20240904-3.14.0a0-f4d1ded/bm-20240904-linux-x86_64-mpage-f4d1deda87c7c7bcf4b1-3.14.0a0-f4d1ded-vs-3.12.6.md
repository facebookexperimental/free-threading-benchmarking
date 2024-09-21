# Results vs. 3.12.6

- fork: mpage
- ref: f4d1deda87c7c7bcf4b1
- machine: linux-x86_64
- commit hash: f4d1ded
- commit date: 2024-09-04
- overall geometric mean: 1.22x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240904-linux-x86_64-mpage-f4d1deda87c7c7bcf4b1-3.14.0a0-f4d1ded |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 546 ms: 1.20x slower                                                 |
| docutils       | 4.00 sec                                               | 4.52 sec: 1.13x slower                                               |
| html5lib       | 88.9 ms                                                | 130 ms: 1.46x slower                                                 |
| tornado_http   | 266 ms                                                 | 334 ms: 1.25x slower                                                 |
| Geometric mean | (ref)                                                  | 1.25x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240904-linux-x86_64-mpage-f4d1deda87c7c7bcf4b1-3.14.0a0-f4d1ded |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.56 sec: 1.24x faster                                               |
| async_tree_memoization_tg  | 930 ms                                                 | 760 ms: 1.22x faster                                                 |
| async_tree_memoization     | 977 ms                                                 | 809 ms: 1.21x faster                                                 |
| async_tree_io              | 1.85 sec                                               | 1.55 sec: 1.19x faster                                               |
| async_tree_none            | 741 ms                                                 | 636 ms: 1.17x faster                                                 |
| async_tree_none_tg         | 704 ms                                                 | 609 ms: 1.16x faster                                                 |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 1.01 sec: 1.09x faster                                               |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 1.01 sec: 1.07x faster                                               |
| asyncio_tcp                | 923 ms                                                 | 970 ms: 1.05x slower                                                 |
| async_generators           | 589 ms                                                 | 637 ms: 1.08x slower                                                 |
| coroutines                 | 29.5 ms                                                | 38.7 ms: 1.31x slower                                                |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                         |

Benchmark hidden because not significant (2): asyncio_tcp_ssl, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240904-linux-x86_64-mpage-f4d1deda87c7c7bcf4b1-3.14.0a0-f4d1ded |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 123 ms                                                 | 171 ms: 1.39x slower                                                 |
| nbody          | 119 ms                                                 | 226 ms: 1.90x slower                                                 |
| Geometric mean | (ref)                                                  | 1.38x slower                                                         |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240904-linux-x86_64-mpage-f4d1deda87c7c7bcf4b1-3.14.0a0-f4d1ded |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.84 ms: 1.06x faster                                                |
| regex_dna      | 278 ms                                                 | 304 ms: 1.09x slower                                                 |
| regex_v8       | 32.5 ms                                                | 38.6 ms: 1.19x slower                                                |
| regex_compile  | 187 ms                                                 | 253 ms: 1.35x slower                                                 |
| Geometric mean | (ref)                                                  | 1.13x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240904-linux-x86_64-mpage-f4d1deda87c7c7bcf4b1-3.14.0a0-f4d1ded |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle_dict          | 52.7 us                                                | 45.2 us: 1.17x faster                                                |
| unpickle             | 21.2 us                                                | 19.4 us: 1.10x faster                                                |
| pickle               | 16.4 us                                                | 15.0 us: 1.09x faster                                                |
| xml_etree_parse      | 241 ms                                                 | 223 ms: 1.08x faster                                                 |
| pickle_list          | 6.97 us                                                | 6.68 us: 1.04x faster                                                |
| json_loads           | 37.9 us                                                | 40.3 us: 1.06x slower                                                |
| unpickle_list        | 6.83 us                                                | 7.52 us: 1.10x slower                                                |
| xml_etree_generate   | 127 ms                                                 | 142 ms: 1.11x slower                                                 |
| xml_etree_iterparse  | 169 ms                                                 | 196 ms: 1.16x slower                                                 |
| json_dumps           | 14.3 ms                                                | 16.8 ms: 1.17x slower                                                |
| tomli_loads          | 2.88 sec                                               | 3.74 sec: 1.30x slower                                               |
| xml_etree_process    | 83.7 ms                                                | 110 ms: 1.31x slower                                                 |
| unpickle_pure_python | 300 us                                                 | 461 us: 1.54x slower                                                 |
| pickle_pure_python   | 436 us                                                 | 673 us: 1.54x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.11x slower                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240904-linux-x86_64-mpage-f4d1deda87c7c7bcf4b1-3.14.0a0-f4d1ded |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 16.3 ms: 1.08x faster                                                |
| Geometric mean         | (ref)                                                  | 1.04x faster                                                         |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240904-linux-x86_64-mpage-f4d1deda87c7c7bcf4b1-3.14.0a0-f4d1ded |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| django_template | 44.9 ms                                                | 64.3 ms: 1.43x slower                                                |
| mako            | 15.7 ms                                                | 22.5 ms: 1.43x slower                                                |
| genshi_text     | 30.2 ms                                                | 43.7 ms: 1.45x slower                                                |
| genshi_xml      | 67.6 ms                                                | 101 ms: 1.50x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.45x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240904-linux-x86_64-mpage-f4d1deda87c7c7bcf4b1-3.14.0a0-f4d1ded |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.56 sec: 1.24x faster                                               |
| async_tree_memoization_tg  | 930 ms                                                 | 760 ms: 1.22x faster                                                 |
| async_tree_memoization     | 977 ms                                                 | 809 ms: 1.21x faster                                                 |
| async_tree_io              | 1.85 sec                                               | 1.55 sec: 1.19x faster                                               |
| pickle_dict                | 52.7 us                                                | 45.2 us: 1.17x faster                                                |
| async_tree_none            | 741 ms                                                 | 636 ms: 1.17x faster                                                 |
| async_tree_none_tg         | 704 ms                                                 | 609 ms: 1.16x faster                                                 |
| unpickle                   | 21.2 us                                                | 19.4 us: 1.10x faster                                                |
| pickle                     | 16.4 us                                                | 15.0 us: 1.09x faster                                                |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 1.01 sec: 1.09x faster                                               |
| xml_etree_parse            | 241 ms                                                 | 223 ms: 1.08x faster                                                 |
| python_startup_no_site     | 17.6 ms                                                | 16.3 ms: 1.08x faster                                                |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 1.01 sec: 1.07x faster                                               |
| regex_effbot               | 5.13 ms                                                | 4.84 ms: 1.06x faster                                                |
| pickle_list                | 6.97 us                                                | 6.68 us: 1.04x faster                                                |
| mdp                        | 3.97 sec                                               | 4.07 sec: 1.03x slower                                               |
| asyncio_tcp                | 923 ms                                                 | 970 ms: 1.05x slower                                                 |
| json_loads                 | 37.9 us                                                | 40.3 us: 1.06x slower                                                |
| pathlib                    | 31.6 ms                                                | 33.7 ms: 1.07x slower                                                |
| scimark_fft                | 500 ms                                                 | 538 ms: 1.08x slower                                                 |
| async_generators           | 589 ms                                                 | 637 ms: 1.08x slower                                                 |
| regex_dna                  | 278 ms                                                 | 304 ms: 1.09x slower                                                 |
| unpickle_list              | 6.83 us                                                | 7.52 us: 1.10x slower                                                |
| gc_traversal               | 5.86 ms                                                | 6.46 ms: 1.10x slower                                                |
| deepcopy_reduce            | 4.04 us                                                | 4.47 us: 1.11x slower                                                |
| xml_etree_generate         | 127 ms                                                 | 142 ms: 1.11x slower                                                 |
| bench_mp_pool              | 20.7 ms                                                | 23.1 ms: 1.12x slower                                                |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 7.49 ms: 1.12x slower                                                |
| json                       | 6.85 ms                                                | 7.67 ms: 1.12x slower                                                |
| docutils                   | 4.00 sec                                               | 4.52 sec: 1.13x slower                                               |
| sqlite_synth               | 3.87 us                                                | 4.40 us: 1.14x slower                                                |
| comprehensions             | 27.1 us                                                | 31.0 us: 1.14x slower                                                |
| meteor_contest             | 146 ms                                                 | 168 ms: 1.15x slower                                                 |
| pycparser                  | 1.79 sec                                               | 2.06 sec: 1.15x slower                                               |
| bpe_tokeniser              | 6.59 sec                                               | 7.57 sec: 1.15x slower                                               |
| xml_etree_iterparse        | 169 ms                                                 | 196 ms: 1.16x slower                                                 |
| nqueens                    | 117 ms                                                 | 136 ms: 1.16x slower                                                 |
| json_dumps                 | 14.3 ms                                                | 16.8 ms: 1.17x slower                                                |
| sympy_sum                  | 222 ms                                                 | 260 ms: 1.17x slower                                                 |
| sympy_integrate            | 29.8 ms                                                | 35.0 ms: 1.18x slower                                                |
| generators                 | 41.1 ms                                                | 48.5 ms: 1.18x slower                                                |
| regex_v8                   | 32.5 ms                                                | 38.6 ms: 1.19x slower                                                |
| 2to3                       | 456 ms                                                 | 546 ms: 1.20x slower                                                 |
| coverage                   | 95.4 ms                                                | 114 ms: 1.20x slower                                                 |
| bench_thread_pool          | 3.48 ms                                                | 4.17 ms: 1.20x slower                                                |
| pylint                     | 465 ms                                                 | 563 ms: 1.21x slower                                                 |
| create_gc_cycles           | 1.94 ms                                                | 2.37 ms: 1.22x slower                                                |
| typing_runtime_protocols   | 224 us                                                 | 275 us: 1.23x slower                                                 |
| sympy_str                  | 385 ms                                                 | 480 ms: 1.25x slower                                                 |
| telco                      | 9.59 ms                                                | 12.0 ms: 1.25x slower                                                |
| tornado_http               | 266 ms                                                 | 334 ms: 1.25x slower                                                 |
| fannkuch                   | 540 ms                                                 | 688 ms: 1.27x slower                                                 |
| sympy_expand               | 582 ms                                                 | 742 ms: 1.28x slower                                                 |
| crypto_pyaes               | 107 ms                                                 | 137 ms: 1.28x slower                                                 |
| tomli_loads                | 2.88 sec                                               | 3.74 sec: 1.30x slower                                               |
| sqlglot_normalize          | 157 ms                                                 | 205 ms: 1.30x slower                                                 |
| coroutines                 | 29.5 ms                                                | 38.7 ms: 1.31x slower                                                |
| xml_etree_process          | 83.7 ms                                                | 110 ms: 1.31x slower                                                 |
| pyflate                    | 727 ms                                                 | 961 ms: 1.32x slower                                                 |
| regex_compile              | 187 ms                                                 | 253 ms: 1.35x slower                                                 |
| thrift                     | 1.06 ms                                                | 1.45 ms: 1.37x slower                                                |
| logging_simple             | 9.45 us                                                | 12.9 us: 1.37x slower                                                |
| spectral_norm              | 156 ms                                                 | 216 ms: 1.39x slower                                                 |
| float                      | 123 ms                                                 | 171 ms: 1.39x slower                                                 |
| pprint_pformat             | 1.98 sec                                               | 2.76 sec: 1.39x slower                                               |
| sqlglot_optimize           | 76.0 ms                                                | 106 ms: 1.40x slower                                                 |
| django_template            | 44.9 ms                                                | 64.3 ms: 1.43x slower                                                |
| mako                       | 15.7 ms                                                | 22.5 ms: 1.43x slower                                                |
| pprint_safe_repr           | 967 ms                                                 | 1.39 sec: 1.44x slower                                               |
| genshi_text                | 30.2 ms                                                | 43.7 ms: 1.45x slower                                                |
| html5lib                   | 88.9 ms                                                | 130 ms: 1.46x slower                                                 |
| raytrace                   | 408 ms                                                 | 608 ms: 1.49x slower                                                 |
| richards                   | 60.3 ms                                                | 90.4 ms: 1.50x slower                                                |
| genshi_xml                 | 67.6 ms                                                | 101 ms: 1.50x slower                                                 |
| chaos                      | 84.9 ms                                                | 129 ms: 1.52x slower                                                 |
| scimark_monte_carlo        | 96.4 ms                                                | 147 ms: 1.52x slower                                                 |
| richards_super             | 72.8 ms                                                | 111 ms: 1.53x slower                                                 |
| logging_silent             | 139 ns                                                 | 214 ns: 1.53x slower                                                 |
| unpickle_pure_python       | 300 us                                                 | 461 us: 1.54x slower                                                 |
| pickle_pure_python         | 436 us                                                 | 673 us: 1.54x slower                                                 |
| sqlglot_transpile          | 2.34 ms                                                | 3.66 ms: 1.57x slower                                                |
| logging_format             | 9.59 us                                                | 15.4 us: 1.60x slower                                                |
| sqlglot_parse              | 1.79 ms                                                | 2.93 ms: 1.64x slower                                                |
| hexiom                     | 8.27 ms                                                | 13.9 ms: 1.68x slower                                                |
| scimark_lu                 | 152 ms                                                 | 261 ms: 1.71x slower                                                 |
| go                         | 172 ms                                                 | 298 ms: 1.73x slower                                                 |
| scimark_sor                | 167 ms                                                 | 304 ms: 1.82x slower                                                 |
| nbody                      | 119 ms                                                 | 226 ms: 1.90x slower                                                 |
| deltablue                  | 4.27 ms                                                | 9.01 ms: 2.11x slower                                                |
| unpack_sequence            | 60.2 ns                                                | 149 ns: 2.47x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.22x slower                                                         |

Benchmark hidden because not significant (6): asyncio_tcp_ssl, python_startup, pidigits, asyncio_websockets, deepcopy_memo, deepcopy
Ignored benchmarks (9) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.15x
- 95% likely to have a slowdown of 1.13x
- 99% likely to have a slowdown of 1.11x

# Memory
- memory change: 1.00x