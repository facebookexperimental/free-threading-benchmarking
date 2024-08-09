# Results vs. base

- fork: python
- ref: e73e7a7abdc3fed252af
- machine: linux-x86_64
- commit hash: e73e7a7
- commit date: 2024-08-07
- overall geometric mean: 1.39x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.27x slower
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20240807-3.14.0a0-e73e7a7/bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7.json | results/bm-20240807-3.14.0a0-e73e7a7-NOGIL/bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 447 ms                                                                                                          | 651 ms: 1.45x slower                                                                                                  |
| docutils       | 4.14 sec                                                                                                        | 4.92 sec: 1.19x slower                                                                                                |
| html5lib       | 94.3 ms                                                                                                         | 137 ms: 1.45x slower                                                                                                  |
| tornado_http   | 260 ms                                                                                                          | 319 ms: 1.23x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.32x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20240807-3.14.0a0-e73e7a7/bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7.json | results/bm-20240807-3.14.0a0-e73e7a7-NOGIL/bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.30 sec                                                                                                        | 1.12 sec: 1.16x faster                                                                                                |
| async_tree_cpu_io_mixed_tg | 829 ms                                                                                                          | 874 ms: 1.05x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 856 ms                                                                                                          | 951 ms: 1.11x slower                                                                                                  |
| asyncio_tcp                | 940 ms                                                                                                          | 1.09 sec: 1.16x slower                                                                                                |
| async_tree_none            | 501 ms                                                                                                          | 584 ms: 1.17x slower                                                                                                  |
| asyncio_tcp_ssl            | 2.78 sec                                                                                                        | 3.34 sec: 1.20x slower                                                                                                |
| async_generators           | 579 ms                                                                                                          | 747 ms: 1.29x slower                                                                                                  |
| coroutines                 | 32.6 ms                                                                                                         | 42.7 ms: 1.31x slower                                                                                                 |
| Geometric mean             | (ref)                                                                                                           | 1.08x slower                                                                                                          |

Benchmark hidden because not significant (5): async_tree_memoization_tg, async_tree_io, asyncio_websockets, async_tree_none_tg, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20240807-3.14.0a0-e73e7a7/bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7.json | results/bm-20240807-3.14.0a0-e73e7a7-NOGIL/bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| float          | 119 ms                                                                                                          | 194 ms: 1.63x slower                                                                                                  |
| nbody          | 121 ms                                                                                                          | 281 ms: 2.33x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.55x slower                                                                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20240807-3.14.0a0-e73e7a7/bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7.json | results/bm-20240807-3.14.0a0-e73e7a7-NOGIL/bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_effbot   | 5.47 ms                                                                                                         | 4.84 ms: 1.13x faster                                                                                                 |
| regex_v8       | 38.1 ms                                                                                                         | 35.6 ms: 1.07x faster                                                                                                 |
| regex_dna      | 300 ms                                                                                                          | 290 ms: 1.03x faster                                                                                                  |
| regex_compile  | 192 ms                                                                                                          | 296 ms: 1.54x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.05x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20240807-3.14.0a0-e73e7a7/bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7.json | results/bm-20240807-3.14.0a0-e73e7a7-NOGIL/bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pickle_dict          | 46.2 us                                                                                                         | 43.1 us: 1.07x faster                                                                                                 |
| pickle               | 15.4 us                                                                                                         | 14.5 us: 1.06x faster                                                                                                 |
| xml_etree_parse      | 226 ms                                                                                                          | 218 ms: 1.04x faster                                                                                                  |
| json_loads           | 37.5 us                                                                                                         | 41.2 us: 1.10x slower                                                                                                 |
| unpickle_list        | 6.83 us                                                                                                         | 7.70 us: 1.13x slower                                                                                                 |
| json_dumps           | 14.5 ms                                                                                                         | 18.0 ms: 1.24x slower                                                                                                 |
| xml_etree_generate   | 123 ms                                                                                                          | 159 ms: 1.29x slower                                                                                                  |
| xml_etree_process    | 86.9 ms                                                                                                         | 127 ms: 1.46x slower                                                                                                  |
| tomli_loads          | 2.66 sec                                                                                                        | 4.14 sec: 1.55x slower                                                                                                |
| unpickle_pure_python | 295 us                                                                                                          | 544 us: 1.85x slower                                                                                                  |
| pickle_pure_python   | 436 us                                                                                                          | 846 us: 1.94x slower                                                                                                  |
| Geometric mean       | (ref)                                                                                                           | 1.21x slower                                                                                                          |

Benchmark hidden because not significant (3): xml_etree_iterparse, pickle_list, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20240807-3.14.0a0-e73e7a7/bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7.json | results/bm-20240807-3.14.0a0-e73e7a7-NOGIL/bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 23.8 ms                                                                                                         | 28.9 ms: 1.21x slower                                                                                                 |
| python_startup_no_site | 14.9 ms                                                                                                         | 19.4 ms: 1.30x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.25x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20240807-3.14.0a0-e73e7a7/bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7.json | results/bm-20240807-3.14.0a0-e73e7a7-NOGIL/bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| genshi_xml      | 72.0 ms                                                                                                         | 111 ms: 1.54x slower                                                                                                  |
| django_template | 48.3 ms                                                                                                         | 79.6 ms: 1.65x slower                                                                                                 |
| genshi_text     | 32.0 ms                                                                                                         | 53.4 ms: 1.67x slower                                                                                                 |
| mako            | 18.3 ms                                                                                                         | 31.0 ms: 1.70x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.64x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20240807-3.14.0a0-e73e7a7/bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7.json | results/bm-20240807-3.14.0a0-e73e7a7-NOGIL/bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| create_gc_cycles           | 2.41 ms                                                                                                         | 1.80 ms: 1.34x faster                                                                                                 |
| gc_traversal               | 5.59 ms                                                                                                         | 4.19 ms: 1.33x faster                                                                                                 |
| async_tree_io_tg           | 1.30 sec                                                                                                        | 1.12 sec: 1.16x faster                                                                                                |
| bench_mp_pool              | 21.4 ms                                                                                                         | 18.8 ms: 1.14x faster                                                                                                 |
| regex_effbot               | 5.47 ms                                                                                                         | 4.84 ms: 1.13x faster                                                                                                 |
| pickle_dict                | 46.2 us                                                                                                         | 43.1 us: 1.07x faster                                                                                                 |
| regex_v8                   | 38.1 ms                                                                                                         | 35.6 ms: 1.07x faster                                                                                                 |
| pickle                     | 15.4 us                                                                                                         | 14.5 us: 1.06x faster                                                                                                 |
| xml_etree_parse            | 226 ms                                                                                                          | 218 ms: 1.04x faster                                                                                                  |
| regex_dna                  | 300 ms                                                                                                          | 290 ms: 1.03x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 829 ms                                                                                                          | 874 ms: 1.05x slower                                                                                                  |
| sqlite_synth               | 4.10 us                                                                                                         | 4.42 us: 1.08x slower                                                                                                 |
| json_loads                 | 37.5 us                                                                                                         | 41.2 us: 1.10x slower                                                                                                 |
| async_tree_cpu_io_mixed    | 856 ms                                                                                                          | 951 ms: 1.11x slower                                                                                                  |
| pathlib                    | 29.7 ms                                                                                                         | 33.0 ms: 1.11x slower                                                                                                 |
| unpickle_list              | 6.83 us                                                                                                         | 7.70 us: 1.13x slower                                                                                                 |
| asyncio_tcp                | 940 ms                                                                                                          | 1.09 sec: 1.16x slower                                                                                                |
| async_tree_none            | 501 ms                                                                                                          | 584 ms: 1.17x slower                                                                                                  |
| docutils                   | 4.14 sec                                                                                                        | 4.92 sec: 1.19x slower                                                                                                |
| json                       | 6.76 ms                                                                                                         | 8.10 ms: 1.20x slower                                                                                                 |
| asyncio_tcp_ssl            | 2.78 sec                                                                                                        | 3.34 sec: 1.20x slower                                                                                                |
| python_startup             | 23.8 ms                                                                                                         | 28.9 ms: 1.21x slower                                                                                                 |
| pylint                     | 477 ms                                                                                                          | 579 ms: 1.21x slower                                                                                                  |
| telco                      | 11.5 ms                                                                                                         | 14.0 ms: 1.22x slower                                                                                                 |
| tornado_http               | 260 ms                                                                                                          | 319 ms: 1.23x slower                                                                                                  |
| json_dumps                 | 14.5 ms                                                                                                         | 18.0 ms: 1.24x slower                                                                                                 |
| coverage                   | 117 ms                                                                                                          | 146 ms: 1.24x slower                                                                                                  |
| async_generators           | 579 ms                                                                                                          | 747 ms: 1.29x slower                                                                                                  |
| xml_etree_generate         | 123 ms                                                                                                          | 159 ms: 1.29x slower                                                                                                  |
| python_startup_no_site     | 14.9 ms                                                                                                         | 19.4 ms: 1.30x slower                                                                                                 |
| coroutines                 | 32.6 ms                                                                                                         | 42.7 ms: 1.31x slower                                                                                                 |
| scimark_fft                | 476 ms                                                                                                          | 624 ms: 1.31x slower                                                                                                  |
| bench_thread_pool          | 3.44 ms                                                                                                         | 4.52 ms: 1.32x slower                                                                                                 |
| pycparser                  | 1.67 sec                                                                                                        | 2.21 sec: 1.32x slower                                                                                                |
| generators                 | 41.5 ms                                                                                                         | 55.0 ms: 1.33x slower                                                                                                 |
| scimark_sparse_mat_mult    | 6.59 ms                                                                                                         | 8.91 ms: 1.35x slower                                                                                                 |
| meteor_contest             | 139 ms                                                                                                          | 192 ms: 1.38x slower                                                                                                  |
| mdp                        | 3.71 sec                                                                                                        | 5.13 sec: 1.38x slower                                                                                                |
| fannkuch                   | 534 ms                                                                                                          | 762 ms: 1.43x slower                                                                                                  |
| richards                   | 69.2 ms                                                                                                         | 99.2 ms: 1.43x slower                                                                                                 |
| sqlglot_optimize           | 83.9 ms                                                                                                         | 121 ms: 1.44x slower                                                                                                  |
| html5lib                   | 94.3 ms                                                                                                         | 137 ms: 1.45x slower                                                                                                  |
| 2to3                       | 447 ms                                                                                                          | 651 ms: 1.45x slower                                                                                                  |
| thrift                     | 1.15 ms                                                                                                         | 1.67 ms: 1.46x slower                                                                                                 |
| xml_etree_process          | 86.9 ms                                                                                                         | 127 ms: 1.46x slower                                                                                                  |
| nqueens                    | 105 ms                                                                                                          | 155 ms: 1.47x slower                                                                                                  |
| crypto_pyaes               | 105 ms                                                                                                          | 156 ms: 1.49x slower                                                                                                  |
| typing_runtime_protocols   | 218 us                                                                                                          | 327 us: 1.50x slower                                                                                                  |
| regex_compile              | 192 ms                                                                                                          | 296 ms: 1.54x slower                                                                                                  |
| genshi_xml                 | 72.0 ms                                                                                                         | 111 ms: 1.54x slower                                                                                                  |
| tomli_loads                | 2.66 sec                                                                                                        | 4.14 sec: 1.55x slower                                                                                                |
| deepcopy                   | 359 us                                                                                                          | 560 us: 1.56x slower                                                                                                  |
| sqlglot_normalize          | 146 ms                                                                                                          | 229 ms: 1.56x slower                                                                                                  |
| pyflate                    | 682 ms                                                                                                          | 1.07 sec: 1.56x slower                                                                                                |
| deepcopy_reduce            | 3.63 us                                                                                                         | 5.70 us: 1.57x slower                                                                                                 |
| spectral_norm              | 157 ms                                                                                                          | 247 ms: 1.57x slower                                                                                                  |
| sympy_integrate            | 28.1 ms                                                                                                         | 44.9 ms: 1.60x slower                                                                                                 |
| logging_format             | 10.2 us                                                                                                         | 16.4 us: 1.60x slower                                                                                                 |
| comprehensions             | 24.0 us                                                                                                         | 38.7 us: 1.61x slower                                                                                                 |
| float                      | 119 ms                                                                                                          | 194 ms: 1.63x slower                                                                                                  |
| django_template            | 48.3 ms                                                                                                         | 79.6 ms: 1.65x slower                                                                                                 |
| pprint_safe_repr           | 995 ms                                                                                                          | 1.65 sec: 1.66x slower                                                                                                |
| richards_super             | 76.3 ms                                                                                                         | 127 ms: 1.66x slower                                                                                                  |
| bpe_tokeniser              | 6.08 sec                                                                                                        | 10.1 sec: 1.67x slower                                                                                                |
| deepcopy_memo              | 40.2 us                                                                                                         | 67.1 us: 1.67x slower                                                                                                 |
| genshi_text                | 32.0 ms                                                                                                         | 53.4 ms: 1.67x slower                                                                                                 |
| mako                       | 18.3 ms                                                                                                         | 31.0 ms: 1.70x slower                                                                                                 |
| pprint_pformat             | 1.94 sec                                                                                                        | 3.39 sec: 1.75x slower                                                                                                |
| scimark_monte_carlo        | 89.4 ms                                                                                                         | 159 ms: 1.78x slower                                                                                                  |
| logging_silent             | 139 ns                                                                                                          | 249 ns: 1.80x slower                                                                                                  |
| sympy_str                  | 372 ms                                                                                                          | 675 ms: 1.81x slower                                                                                                  |
| logging_simple             | 8.46 us                                                                                                         | 15.4 us: 1.82x slower                                                                                                 |
| sqlglot_transpile          | 2.37 ms                                                                                                         | 4.32 ms: 1.82x slower                                                                                                 |
| unpickle_pure_python       | 295 us                                                                                                          | 544 us: 1.85x slower                                                                                                  |
| hexiom                     | 8.52 ms                                                                                                         | 16.3 ms: 1.91x slower                                                                                                 |
| chaos                      | 88.2 ms                                                                                                         | 170 ms: 1.93x slower                                                                                                  |
| pickle_pure_python         | 436 us                                                                                                          | 846 us: 1.94x slower                                                                                                  |
| sympy_sum                  | 226 ms                                                                                                          | 443 ms: 1.96x slower                                                                                                  |
| scimark_lu                 | 158 ms                                                                                                          | 313 ms: 1.99x slower                                                                                                  |
| sqlglot_parse              | 1.89 ms                                                                                                         | 3.76 ms: 1.99x slower                                                                                                 |
| scimark_sor                | 171 ms                                                                                                          | 340 ms: 1.99x slower                                                                                                  |
| sympy_expand               | 606 ms                                                                                                          | 1.29 sec: 2.12x slower                                                                                                |
| go                         | 198 ms                                                                                                          | 434 ms: 2.19x slower                                                                                                  |
| nbody                      | 121 ms                                                                                                          | 281 ms: 2.33x slower                                                                                                  |
| raytrace                   | 340 ms                                                                                                          | 801 ms: 2.36x slower                                                                                                  |
| deltablue                  | 4.43 ms                                                                                                         | 11.6 ms: 2.61x slower                                                                                                 |
| unpack_sequence            | 61.3 ns                                                                                                         | 190 ns: 3.10x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.39x slower                                                                                                          |

Benchmark hidden because not significant (9): async_tree_memoization_tg, async_tree_io, pidigits, asyncio_websockets, xml_etree_iterparse, async_tree_none_tg, pickle_list, unpickle, async_tree_memoization

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.32x
- 95% likely to have a slowdown of 1.31x
- 99% likely to have a slowdown of 1.27x

# Memory
- memory change: 1.14x