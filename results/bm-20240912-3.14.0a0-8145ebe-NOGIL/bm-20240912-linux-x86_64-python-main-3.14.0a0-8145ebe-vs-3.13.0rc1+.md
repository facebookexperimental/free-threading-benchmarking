# Results vs. 3.13.0rc1+

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 8145ebe
- commit date: 2024-09-12
- overall geometric mean: 1.41x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.30x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe |
|----------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 442 ms                                                  | 669 ms: 1.51x slower                                  |
| docutils       | 4.01 sec                                                | 4.89 sec: 1.22x slower                                |
| html5lib       | 98.1 ms                                                 | 133 ms: 1.36x slower                                  |
| tornado_http   | 248 ms                                                  | 374 ms: 1.51x slower                                  |
| Geometric mean | (ref)                                                   | 1.39x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe |
|-------------------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg        | 1.46 sec                                                | 1.17 sec: 1.25x faster                                |
| async_tree_io           | 1.38 sec                                                | 1.24 sec: 1.11x faster                                |
| async_tree_none_tg      | 521 ms                                                  | 497 ms: 1.05x faster                                  |
| asyncio_websockets      | 772 ms                                                  | 802 ms: 1.04x slower                                  |
| async_tree_cpu_io_mixed | 899 ms                                                  | 948 ms: 1.06x slower                                  |
| async_tree_none         | 576 ms                                                  | 609 ms: 1.06x slower                                  |
| asyncio_tcp             | 985 ms                                                  | 1.10 sec: 1.12x slower                                |
| asyncio_tcp_ssl         | 2.79 sec                                                | 3.36 sec: 1.20x slower                                |
| async_generators        | 592 ms                                                  | 742 ms: 1.25x slower                                  |
| coroutines              | 29.2 ms                                                 | 44.4 ms: 1.52x slower                                 |
| Geometric mean          | (ref)                                                   | 1.05x slower                                          |

Benchmark hidden because not significant (3): async_tree_memoization_tg, async_tree_cpu_io_mixed_tg, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe |
|----------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| float          | 115 ms                                                  | 196 ms: 1.71x slower                                  |
| nbody          | 124 ms                                                  | 281 ms: 2.27x slower                                  |
| Geometric mean | (ref)                                                   | 1.57x slower                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe |
|----------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| regex_effbot   | 4.84 ms                                                 | 4.42 ms: 1.09x faster                                 |
| regex_v8       | 32.4 ms                                                 | 37.2 ms: 1.15x slower                                 |
| regex_compile  | 177 ms                                                  | 288 ms: 1.62x slower                                  |
| Geometric mean | (ref)                                                   | 1.14x slower                                          |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe |
|----------------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| xml_etree_parse      | 236 ms                                                  | 224 ms: 1.05x faster                                  |
| unpickle_list        | 6.67 us                                                 | 7.64 us: 1.15x slower                                 |
| json_loads           | 36.1 us                                                 | 41.7 us: 1.15x slower                                 |
| json_dumps           | 14.9 ms                                                 | 17.8 ms: 1.20x slower                                 |
| xml_etree_generate   | 129 ms                                                  | 170 ms: 1.31x slower                                  |
| xml_etree_process    | 86.5 ms                                                 | 126 ms: 1.46x slower                                  |
| tomli_loads          | 2.80 sec                                                | 4.34 sec: 1.55x slower                                |
| unpickle_pure_python | 296 us                                                  | 516 us: 1.75x slower                                  |
| pickle_pure_python   | 417 us                                                  | 847 us: 2.03x slower                                  |
| Geometric mean       | (ref)                                                   | 1.22x slower                                          |

Benchmark hidden because not significant (5): pickle, pickle_dict, xml_etree_iterparse, pickle_list, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe |
|------------------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 14.6 ms                                                 | 21.3 ms: 1.46x slower                                 |
| python_startup         | 22.0 ms                                                 | 32.2 ms: 1.46x slower                                 |
| Geometric mean         | (ref)                                                   | 1.46x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe |
|-----------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_xml      | 68.3 ms                                                 | 118 ms: 1.73x slower                                  |
| django_template | 46.9 ms                                                 | 85.0 ms: 1.81x slower                                 |
| genshi_text     | 31.7 ms                                                 | 60.8 ms: 1.92x slower                                 |
| mako            | 16.1 ms                                                 | 31.6 ms: 1.97x slower                                 |
| Geometric mean  | (ref)                                                   | 1.85x slower                                          |

All benchmarks:
===============

| Benchmark                | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe |
|--------------------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg         | 1.46 sec                                                | 1.17 sec: 1.25x faster                                |
| create_gc_cycles         | 2.46 ms                                                 | 2.04 ms: 1.21x faster                                 |
| gc_traversal             | 5.91 ms                                                 | 4.89 ms: 1.21x faster                                 |
| async_tree_io            | 1.38 sec                                                | 1.24 sec: 1.11x faster                                |
| regex_effbot             | 4.84 ms                                                 | 4.42 ms: 1.09x faster                                 |
| xml_etree_parse          | 236 ms                                                  | 224 ms: 1.05x faster                                  |
| async_tree_none_tg       | 521 ms                                                  | 497 ms: 1.05x faster                                  |
| asyncio_websockets       | 772 ms                                                  | 802 ms: 1.04x slower                                  |
| async_tree_cpu_io_mixed  | 899 ms                                                  | 948 ms: 1.06x slower                                  |
| async_tree_none          | 576 ms                                                  | 609 ms: 1.06x slower                                  |
| sqlite_synth             | 4.07 us                                                 | 4.43 us: 1.09x slower                                 |
| asyncio_tcp              | 985 ms                                                  | 1.10 sec: 1.12x slower                                |
| unpickle_list            | 6.67 us                                                 | 7.64 us: 1.15x slower                                 |
| regex_v8                 | 32.4 ms                                                 | 37.2 ms: 1.15x slower                                 |
| json_loads               | 36.1 us                                                 | 41.7 us: 1.15x slower                                 |
| json_dumps               | 14.9 ms                                                 | 17.8 ms: 1.20x slower                                 |
| deepcopy                 | 484 us                                                  | 581 us: 1.20x slower                                  |
| asyncio_tcp_ssl          | 2.79 sec                                                | 3.36 sec: 1.20x slower                                |
| pathlib                  | 29.3 ms                                                 | 35.3 ms: 1.20x slower                                 |
| telco                    | 11.4 ms                                                 | 13.9 ms: 1.22x slower                                 |
| json                     | 6.55 ms                                                 | 8.00 ms: 1.22x slower                                 |
| docutils                 | 4.01 sec                                                | 4.89 sec: 1.22x slower                                |
| async_generators         | 592 ms                                                  | 742 ms: 1.25x slower                                  |
| scimark_sparse_mat_mult  | 6.98 ms                                                 | 8.92 ms: 1.28x slower                                 |
| pylint                   | 472 ms                                                  | 610 ms: 1.29x slower                                  |
| xml_etree_generate       | 129 ms                                                  | 170 ms: 1.31x slower                                  |
| meteor_contest           | 157 ms                                                  | 208 ms: 1.32x slower                                  |
| scimark_fft              | 477 ms                                                  | 631 ms: 1.32x slower                                  |
| deepcopy_memo            | 51.7 us                                                 | 68.8 us: 1.33x slower                                 |
| generators               | 39.2 ms                                                 | 52.8 ms: 1.35x slower                                 |
| html5lib                 | 98.1 ms                                                 | 133 ms: 1.36x slower                                  |
| mdp                      | 3.80 sec                                                | 5.21 sec: 1.37x slower                                |
| deepcopy_reduce          | 4.27 us                                                 | 5.91 us: 1.38x slower                                 |
| fannkuch                 | 543 ms                                                  | 767 ms: 1.41x slower                                  |
| coverage                 | 110 ms                                                  | 156 ms: 1.42x slower                                  |
| pycparser                | 1.57 sec                                                | 2.24 sec: 1.43x slower                                |
| nqueens                  | 108 ms                                                  | 155 ms: 1.44x slower                                  |
| python_startup_no_site   | 14.6 ms                                                 | 21.3 ms: 1.46x slower                                 |
| xml_etree_process        | 86.5 ms                                                 | 126 ms: 1.46x slower                                  |
| python_startup           | 22.0 ms                                                 | 32.2 ms: 1.46x slower                                 |
| tornado_http             | 248 ms                                                  | 374 ms: 1.51x slower                                  |
| crypto_pyaes             | 99.8 ms                                                 | 151 ms: 1.51x slower                                  |
| 2to3                     | 442 ms                                                  | 669 ms: 1.51x slower                                  |
| coroutines               | 29.2 ms                                                 | 44.4 ms: 1.52x slower                                 |
| thrift                   | 1.11 ms                                                 | 1.71 ms: 1.53x slower                                 |
| sqlglot_optimize         | 76.2 ms                                                 | 117 ms: 1.54x slower                                  |
| spectral_norm            | 159 ms                                                  | 245 ms: 1.54x slower                                  |
| typing_runtime_protocols | 216 us                                                  | 334 us: 1.55x slower                                  |
| bench_thread_pool        | 3.06 ms                                                 | 4.74 ms: 1.55x slower                                 |
| tomli_loads              | 2.80 sec                                                | 4.34 sec: 1.55x slower                                |
| sympy_integrate          | 29.7 ms                                                 | 46.3 ms: 1.56x slower                                 |
| pyflate                  | 661 ms                                                  | 1.04 sec: 1.57x slower                                |
| dulwich_log              | 100.0 ms                                                | 159 ms: 1.59x slower                                  |
| richards_super           | 76.3 ms                                                 | 123 ms: 1.61x slower                                  |
| regex_compile            | 177 ms                                                  | 288 ms: 1.62x slower                                  |
| bpe_tokeniser            | 6.25 sec                                                | 10.2 sec: 1.64x slower                                |
| richards                 | 65.8 ms                                                 | 108 ms: 1.64x slower                                  |
| logging_simple           | 8.98 us                                                 | 15.2 us: 1.69x slower                                 |
| float                    | 115 ms                                                  | 196 ms: 1.71x slower                                  |
| sqlglot_normalize        | 146 ms                                                  | 250 ms: 1.71x slower                                  |
| logging_format           | 9.48 us                                                 | 16.3 us: 1.72x slower                                 |
| genshi_xml               | 68.3 ms                                                 | 118 ms: 1.73x slower                                  |
| unpickle_pure_python     | 296 us                                                  | 516 us: 1.75x slower                                  |
| pprint_safe_repr         | 959 ms                                                  | 1.69 sec: 1.76x slower                                |
| pprint_pformat           | 2.00 sec                                                | 3.52 sec: 1.76x slower                                |
| comprehensions           | 20.9 us                                                 | 37.2 us: 1.78x slower                                 |
| django_template          | 46.9 ms                                                 | 85.0 ms: 1.81x slower                                 |
| go                       | 195 ms                                                  | 361 ms: 1.85x slower                                  |
| scimark_monte_carlo      | 89.9 ms                                                 | 166 ms: 1.85x slower                                  |
| sympy_str                | 367 ms                                                  | 687 ms: 1.87x slower                                  |
| chaos                    | 84.7 ms                                                 | 159 ms: 1.88x slower                                  |
| hexiom                   | 8.35 ms                                                 | 16.0 ms: 1.91x slower                                 |
| genshi_text              | 31.7 ms                                                 | 60.8 ms: 1.92x slower                                 |
| sqlglot_transpile        | 2.30 ms                                                 | 4.40 ms: 1.92x slower                                 |
| mako                     | 16.1 ms                                                 | 31.6 ms: 1.97x slower                                 |
| logging_silent           | 130 ns                                                  | 256 ns: 1.97x slower                                  |
| scimark_lu               | 154 ms                                                  | 307 ms: 1.99x slower                                  |
| scimark_sor              | 172 ms                                                  | 345 ms: 2.00x slower                                  |
| pickle_pure_python       | 417 us                                                  | 847 us: 2.03x slower                                  |
| sympy_expand             | 631 ms                                                  | 1.33 sec: 2.10x slower                                |
| sqlglot_parse            | 1.80 ms                                                 | 3.90 ms: 2.16x slower                                 |
| raytrace                 | 350 ms                                                  | 766 ms: 2.19x slower                                  |
| nbody                    | 124 ms                                                  | 281 ms: 2.27x slower                                  |
| sympy_sum                | 213 ms                                                  | 491 ms: 2.30x slower                                  |
| deltablue                | 4.56 ms                                                 | 11.6 ms: 2.55x slower                                 |
| unpack_sequence          | 73.9 ns                                                 | 201 ns: 2.72x slower                                  |
| Geometric mean           | (ref)                                                   | 1.41x slower                                          |

Benchmark hidden because not significant (11): bench_mp_pool, async_tree_memoization_tg, pickle, pickle_dict, regex_dna, async_tree_cpu_io_mixed_tg, xml_etree_iterparse, pidigits, pickle_list, async_tree_memoization, unpickle
Ignored benchmarks (5) of results/bm-20240814-3.13.0rc1+-79452b1/bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1.json: aiohttp, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.36x
- 95% likely to have a slowdown of 1.34x
- 99% likely to have a slowdown of 1.30x

# Memory
- memory change: 1.15x