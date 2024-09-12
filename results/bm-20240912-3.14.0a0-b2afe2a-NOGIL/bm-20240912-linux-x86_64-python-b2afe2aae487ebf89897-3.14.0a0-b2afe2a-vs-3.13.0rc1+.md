# Results vs. 3.13.0rc1+

- fork: python
- ref: b2afe2aae487ebf89897
- machine: linux-x86_64
- commit hash: b2afe2a
- commit date: 2024-09-12
- overall geometric mean: 1.43x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.30x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240912-linux-x86_64-python-b2afe2aae487ebf89897-3.14.0a0-b2afe2a |
|----------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 442 ms                                                  | 721 ms: 1.63x slower                                                  |
| docutils       | 4.01 sec                                                | 5.09 sec: 1.27x slower                                                |
| html5lib       | 98.1 ms                                                 | 141 ms: 1.44x slower                                                  |
| tornado_http   | 248 ms                                                  | 369 ms: 1.49x slower                                                  |
| Geometric mean | (ref)                                                   | 1.45x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240912-linux-x86_64-python-b2afe2aae487ebf89897-3.14.0a0-b2afe2a |
|----------------------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.46 sec                                                | 1.26 sec: 1.16x faster                                                |
| async_tree_none_tg         | 521 ms                                                  | 491 ms: 1.06x faster                                                  |
| async_tree_cpu_io_mixed_tg | 849 ms                                                  | 906 ms: 1.07x slower                                                  |
| asyncio_tcp_ssl            | 2.79 sec                                                | 3.12 sec: 1.12x slower                                                |
| async_tree_none            | 576 ms                                                  | 647 ms: 1.12x slower                                                  |
| asyncio_tcp                | 985 ms                                                  | 1.19 sec: 1.21x slower                                                |
| async_generators           | 592 ms                                                  | 726 ms: 1.23x slower                                                  |
| coroutines                 | 29.2 ms                                                 | 44.1 ms: 1.51x slower                                                 |
| Geometric mean             | (ref)                                                   | 1.07x slower                                                          |

Benchmark hidden because not significant (5): async_tree_memoization_tg, async_tree_io, async_tree_memoization, async_tree_cpu_io_mixed, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240912-linux-x86_64-python-b2afe2aae487ebf89897-3.14.0a0-b2afe2a |
|----------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 115 ms                                                  | 202 ms: 1.76x slower                                                  |
| nbody          | 124 ms                                                  | 286 ms: 2.31x slower                                                  |
| Geometric mean | (ref)                                                   | 1.62x slower                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240912-linux-x86_64-python-b2afe2aae487ebf89897-3.14.0a0-b2afe2a |
|----------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 32.4 ms                                                 | 36.2 ms: 1.12x slower                                                 |
| regex_compile  | 177 ms                                                  | 301 ms: 1.70x slower                                                  |
| Geometric mean | (ref)                                                   | 1.18x slower                                                          |

Benchmark hidden because not significant (2): regex_dna, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240912-linux-x86_64-python-b2afe2aae487ebf89897-3.14.0a0-b2afe2a |
|----------------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle               | 15.4 us                                                 | 14.5 us: 1.06x faster                                                 |
| unpickle             | 21.4 us                                                 | 24.2 us: 1.13x slower                                                 |
| unpickle_list        | 6.67 us                                                 | 7.76 us: 1.16x slower                                                 |
| json_loads           | 36.1 us                                                 | 42.8 us: 1.18x slower                                                 |
| json_dumps           | 14.9 ms                                                 | 18.0 ms: 1.21x slower                                                 |
| xml_etree_generate   | 129 ms                                                  | 165 ms: 1.28x slower                                                  |
| xml_etree_process    | 86.5 ms                                                 | 128 ms: 1.48x slower                                                  |
| tomli_loads          | 2.80 sec                                                | 4.26 sec: 1.52x slower                                                |
| unpickle_pure_python | 296 us                                                  | 581 us: 1.96x slower                                                  |
| pickle_pure_python   | 417 us                                                  | 835 us: 2.00x slower                                                  |
| Geometric mean       | (ref)                                                   | 1.23x slower                                                          |

Benchmark hidden because not significant (4): xml_etree_iterparse, xml_etree_parse, pickle_dict, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240912-linux-x86_64-python-b2afe2aae487ebf89897-3.14.0a0-b2afe2a |
|------------------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 22.0 ms                                                 | 35.1 ms: 1.59x slower                                                 |
| python_startup_no_site | 14.6 ms                                                 | 23.8 ms: 1.63x slower                                                 |
| Geometric mean         | (ref)                                                   | 1.61x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240912-linux-x86_64-python-b2afe2aae487ebf89897-3.14.0a0-b2afe2a |
|-----------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 68.3 ms                                                 | 114 ms: 1.67x slower                                                  |
| django_template | 46.9 ms                                                 | 82.9 ms: 1.77x slower                                                 |
| mako            | 16.1 ms                                                 | 30.3 ms: 1.89x slower                                                 |
| genshi_text     | 31.7 ms                                                 | 61.0 ms: 1.92x slower                                                 |
| Geometric mean  | (ref)                                                   | 1.81x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240912-linux-x86_64-python-b2afe2aae487ebf89897-3.14.0a0-b2afe2a |
|----------------------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| create_gc_cycles           | 2.46 ms                                                 | 1.83 ms: 1.34x faster                                                 |
| gc_traversal               | 5.91 ms                                                 | 4.51 ms: 1.31x faster                                                 |
| bench_mp_pool              | 19.4 ms                                                 | 16.5 ms: 1.17x faster                                                 |
| async_tree_io_tg           | 1.46 sec                                                | 1.26 sec: 1.16x faster                                                |
| pickle                     | 15.4 us                                                 | 14.5 us: 1.06x faster                                                 |
| async_tree_none_tg         | 521 ms                                                  | 491 ms: 1.06x faster                                                  |
| async_tree_cpu_io_mixed_tg | 849 ms                                                  | 906 ms: 1.07x slower                                                  |
| sqlite_synth               | 4.07 us                                                 | 4.43 us: 1.09x slower                                                 |
| asyncio_tcp_ssl            | 2.79 sec                                                | 3.12 sec: 1.12x slower                                                |
| regex_v8                   | 32.4 ms                                                 | 36.2 ms: 1.12x slower                                                 |
| async_tree_none            | 576 ms                                                  | 647 ms: 1.12x slower                                                  |
| unpickle                   | 21.4 us                                                 | 24.2 us: 1.13x slower                                                 |
| unpickle_list              | 6.67 us                                                 | 7.76 us: 1.16x slower                                                 |
| json_loads                 | 36.1 us                                                 | 42.8 us: 1.18x slower                                                 |
| asyncio_tcp                | 985 ms                                                  | 1.19 sec: 1.21x slower                                                |
| json_dumps                 | 14.9 ms                                                 | 18.0 ms: 1.21x slower                                                 |
| async_generators           | 592 ms                                                  | 726 ms: 1.23x slower                                                  |
| deepcopy                   | 484 us                                                  | 595 us: 1.23x slower                                                  |
| pathlib                    | 29.3 ms                                                 | 36.3 ms: 1.24x slower                                                 |
| json                       | 6.55 ms                                                 | 8.13 ms: 1.24x slower                                                 |
| dulwich_log                | 100.0 ms                                                | 125 ms: 1.25x slower                                                  |
| docutils                   | 4.01 sec                                                | 5.09 sec: 1.27x slower                                                |
| meteor_contest             | 157 ms                                                  | 199 ms: 1.27x slower                                                  |
| telco                      | 11.4 ms                                                 | 14.6 ms: 1.28x slower                                                 |
| xml_etree_generate         | 129 ms                                                  | 165 ms: 1.28x slower                                                  |
| scimark_sparse_mat_mult    | 6.98 ms                                                 | 8.99 ms: 1.29x slower                                                 |
| deepcopy_reduce            | 4.27 us                                                 | 5.61 us: 1.32x slower                                                 |
| pylint                     | 472 ms                                                  | 627 ms: 1.33x slower                                                  |
| scimark_fft                | 477 ms                                                  | 636 ms: 1.33x slower                                                  |
| mdp                        | 3.80 sec                                                | 5.18 sec: 1.37x slower                                                |
| deepcopy_memo              | 51.7 us                                                 | 71.2 us: 1.38x slower                                                 |
| bench_thread_pool          | 3.06 ms                                                 | 4.27 ms: 1.39x slower                                                 |
| coverage                   | 110 ms                                                  | 154 ms: 1.40x slower                                                  |
| generators                 | 39.2 ms                                                 | 56.1 ms: 1.43x slower                                                 |
| html5lib                   | 98.1 ms                                                 | 141 ms: 1.44x slower                                                  |
| fannkuch                   | 543 ms                                                  | 786 ms: 1.45x slower                                                  |
| thrift                     | 1.11 ms                                                 | 1.61 ms: 1.45x slower                                                 |
| xml_etree_process          | 86.5 ms                                                 | 128 ms: 1.48x slower                                                  |
| tornado_http               | 248 ms                                                  | 369 ms: 1.49x slower                                                  |
| coroutines                 | 29.2 ms                                                 | 44.1 ms: 1.51x slower                                                 |
| sympy_integrate            | 29.7 ms                                                 | 44.8 ms: 1.51x slower                                                 |
| tomli_loads                | 2.80 sec                                                | 4.26 sec: 1.52x slower                                                |
| crypto_pyaes               | 99.8 ms                                                 | 153 ms: 1.53x slower                                                  |
| typing_runtime_protocols   | 216 us                                                  | 334 us: 1.55x slower                                                  |
| pycparser                  | 1.57 sec                                                | 2.43 sec: 1.55x slower                                                |
| python_startup             | 22.0 ms                                                 | 35.1 ms: 1.59x slower                                                 |
| pyflate                    | 661 ms                                                  | 1.06 sec: 1.60x slower                                                |
| python_startup_no_site     | 14.6 ms                                                 | 23.8 ms: 1.63x slower                                                 |
| richards                   | 65.8 ms                                                 | 107 ms: 1.63x slower                                                  |
| 2to3                       | 442 ms                                                  | 721 ms: 1.63x slower                                                  |
| nqueens                    | 108 ms                                                  | 177 ms: 1.63x slower                                                  |
| spectral_norm              | 159 ms                                                  | 260 ms: 1.64x slower                                                  |
| bpe_tokeniser              | 6.25 sec                                                | 10.4 sec: 1.66x slower                                                |
| genshi_xml                 | 68.3 ms                                                 | 114 ms: 1.67x slower                                                  |
| sqlglot_normalize          | 146 ms                                                  | 245 ms: 1.68x slower                                                  |
| regex_compile              | 177 ms                                                  | 301 ms: 1.70x slower                                                  |
| float                      | 115 ms                                                  | 202 ms: 1.76x slower                                                  |
| sqlglot_optimize           | 76.2 ms                                                 | 134 ms: 1.76x slower                                                  |
| django_template            | 46.9 ms                                                 | 82.9 ms: 1.77x slower                                                 |
| pprint_safe_repr           | 959 ms                                                  | 1.70 sec: 1.77x slower                                                |
| richards_super             | 76.3 ms                                                 | 137 ms: 1.79x slower                                                  |
| pprint_pformat             | 2.00 sec                                                | 3.58 sec: 1.79x slower                                                |
| scimark_monte_carlo        | 89.9 ms                                                 | 164 ms: 1.82x slower                                                  |
| logging_simple             | 8.98 us                                                 | 16.7 us: 1.85x slower                                                 |
| go                         | 195 ms                                                  | 363 ms: 1.86x slower                                                  |
| logging_format             | 9.48 us                                                 | 17.9 us: 1.88x slower                                                 |
| mako                       | 16.1 ms                                                 | 30.3 ms: 1.89x slower                                                 |
| genshi_text                | 31.7 ms                                                 | 61.0 ms: 1.92x slower                                                 |
| comprehensions             | 20.9 us                                                 | 40.4 us: 1.93x slower                                                 |
| scimark_lu                 | 154 ms                                                  | 302 ms: 1.96x slower                                                  |
| sympy_str                  | 367 ms                                                  | 721 ms: 1.96x slower                                                  |
| unpickle_pure_python       | 296 us                                                  | 581 us: 1.96x slower                                                  |
| pickle_pure_python         | 417 us                                                  | 835 us: 2.00x slower                                                  |
| logging_silent             | 130 ns                                                  | 262 ns: 2.02x slower                                                  |
| hexiom                     | 8.35 ms                                                 | 16.9 ms: 2.02x slower                                                 |
| sqlglot_transpile          | 2.30 ms                                                 | 4.66 ms: 2.03x slower                                                 |
| chaos                      | 84.7 ms                                                 | 172 ms: 2.03x slower                                                  |
| sympy_expand               | 631 ms                                                  | 1.31 sec: 2.08x slower                                                |
| sqlglot_parse              | 1.80 ms                                                 | 3.75 ms: 2.09x slower                                                 |
| scimark_sor                | 172 ms                                                  | 367 ms: 2.13x slower                                                  |
| sympy_sum                  | 213 ms                                                  | 460 ms: 2.16x slower                                                  |
| raytrace                   | 350 ms                                                  | 764 ms: 2.18x slower                                                  |
| nbody                      | 124 ms                                                  | 286 ms: 2.31x slower                                                  |
| deltablue                  | 4.56 ms                                                 | 11.4 ms: 2.49x slower                                                 |
| unpack_sequence            | 73.9 ns                                                 | 220 ns: 2.97x slower                                                  |
| Geometric mean             | (ref)                                                   | 1.43x slower                                                          |

Benchmark hidden because not significant (12): async_tree_memoization_tg, xml_etree_iterparse, xml_etree_parse, async_tree_io, pickle_dict, pickle_list, regex_dna, async_tree_memoization, regex_effbot, async_tree_cpu_io_mixed, asyncio_websockets, pidigits
Ignored benchmarks (5) of results/bm-20240814-3.13.0rc1+-79452b1/bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1.json: aiohttp, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.37x
- 95% likely to have a slowdown of 1.35x
- 99% likely to have a slowdown of 1.30x

# Memory
- memory change: 1.15x