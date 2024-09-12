# Results vs. 3.13.0rc1+

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 3bd942f
- commit date: 2024-09-11
- overall geometric mean: 1.40x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f |
|----------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 442 ms                                                  | 626 ms: 1.42x slower                                  |
| docutils       | 4.01 sec                                                | 4.76 sec: 1.19x slower                                |
| html5lib       | 98.1 ms                                                 | 141 ms: 1.44x slower                                  |
| tornado_http   | 248 ms                                                  | 352 ms: 1.42x slower                                  |
| Geometric mean | (ref)                                                   | 1.36x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f |
|-------------------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg        | 1.46 sec                                                | 1.13 sec: 1.29x faster                                |
| async_tree_none_tg      | 521 ms                                                  | 495 ms: 1.05x faster                                  |
| async_tree_io           | 1.38 sec                                                | 1.31 sec: 1.05x faster                                |
| asyncio_websockets      | 772 ms                                                  | 738 ms: 1.05x faster                                  |
| async_tree_cpu_io_mixed | 899 ms                                                  | 980 ms: 1.09x slower                                  |
| asyncio_tcp             | 985 ms                                                  | 1.09 sec: 1.11x slower                                |
| asyncio_tcp_ssl         | 2.79 sec                                                | 3.27 sec: 1.17x slower                                |
| async_generators        | 592 ms                                                  | 712 ms: 1.20x slower                                  |
| coroutines              | 29.2 ms                                                 | 45.1 ms: 1.55x slower                                 |
| Geometric mean          | (ref)                                                   | 1.04x slower                                          |

Benchmark hidden because not significant (4): async_tree_memoization_tg, async_tree_cpu_io_mixed_tg, async_tree_none, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f |
|----------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| float          | 115 ms                                                  | 201 ms: 1.75x slower                                  |
| nbody          | 124 ms                                                  | 312 ms: 2.52x slower                                  |
| Geometric mean | (ref)                                                   | 1.63x slower                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f |
|----------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| regex_effbot   | 4.84 ms                                                 | 4.56 ms: 1.06x faster                                 |
| regex_v8       | 32.4 ms                                                 | 36.1 ms: 1.11x slower                                 |
| regex_compile  | 177 ms                                                  | 290 ms: 1.63x slower                                  |
| Geometric mean | (ref)                                                   | 1.14x slower                                          |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f |
|----------------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| pickle_list          | 6.82 us                                                 | 6.36 us: 1.07x faster                                 |
| pickle_dict          | 46.5 us                                                 | 43.5 us: 1.07x faster                                 |
| unpickle             | 21.4 us                                                 | 22.7 us: 1.06x slower                                 |
| unpickle_list        | 6.67 us                                                 | 7.59 us: 1.14x slower                                 |
| json_loads           | 36.1 us                                                 | 42.8 us: 1.19x slower                                 |
| xml_etree_generate   | 129 ms                                                  | 157 ms: 1.21x slower                                  |
| json_dumps           | 14.9 ms                                                 | 18.9 ms: 1.27x slower                                 |
| xml_etree_process    | 86.5 ms                                                 | 121 ms: 1.40x slower                                  |
| tomli_loads          | 2.80 sec                                                | 4.35 sec: 1.55x slower                                |
| unpickle_pure_python | 296 us                                                  | 547 us: 1.85x slower                                  |
| pickle_pure_python   | 417 us                                                  | 804 us: 1.93x slower                                  |
| Geometric mean       | (ref)                                                   | 1.21x slower                                          |

Benchmark hidden because not significant (3): pickle, xml_etree_iterparse, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f |
|------------------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup         | 22.0 ms                                                 | 30.9 ms: 1.40x slower                                 |
| python_startup_no_site | 14.6 ms                                                 | 21.2 ms: 1.45x slower                                 |
| Geometric mean         | (ref)                                                   | 1.42x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f |
|-----------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_xml      | 68.3 ms                                                 | 116 ms: 1.70x slower                                  |
| django_template | 46.9 ms                                                 | 83.8 ms: 1.79x slower                                 |
| genshi_text     | 31.7 ms                                                 | 58.2 ms: 1.83x slower                                 |
| mako            | 16.1 ms                                                 | 31.2 ms: 1.94x slower                                 |
| Geometric mean  | (ref)                                                   | 1.81x slower                                          |

All benchmarks:
===============

| Benchmark                | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f |
|--------------------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| create_gc_cycles         | 2.46 ms                                                 | 1.83 ms: 1.34x faster                                 |
| gc_traversal             | 5.91 ms                                                 | 4.51 ms: 1.31x faster                                 |
| async_tree_io_tg         | 1.46 sec                                                | 1.13 sec: 1.29x faster                                |
| bench_mp_pool            | 19.4 ms                                                 | 17.5 ms: 1.10x faster                                 |
| pickle_list              | 6.82 us                                                 | 6.36 us: 1.07x faster                                 |
| pickle_dict              | 46.5 us                                                 | 43.5 us: 1.07x faster                                 |
| regex_effbot             | 4.84 ms                                                 | 4.56 ms: 1.06x faster                                 |
| async_tree_none_tg       | 521 ms                                                  | 495 ms: 1.05x faster                                  |
| async_tree_io            | 1.38 sec                                                | 1.31 sec: 1.05x faster                                |
| asyncio_websockets       | 772 ms                                                  | 738 ms: 1.05x faster                                  |
| unpickle                 | 21.4 us                                                 | 22.7 us: 1.06x slower                                 |
| async_tree_cpu_io_mixed  | 899 ms                                                  | 980 ms: 1.09x slower                                  |
| asyncio_tcp              | 985 ms                                                  | 1.09 sec: 1.11x slower                                |
| regex_v8                 | 32.4 ms                                                 | 36.1 ms: 1.11x slower                                 |
| unpickle_list            | 6.67 us                                                 | 7.59 us: 1.14x slower                                 |
| asyncio_tcp_ssl          | 2.79 sec                                                | 3.27 sec: 1.17x slower                                |
| json_loads               | 36.1 us                                                 | 42.8 us: 1.19x slower                                 |
| meteor_contest           | 157 ms                                                  | 186 ms: 1.19x slower                                  |
| docutils                 | 4.01 sec                                                | 4.76 sec: 1.19x slower                                |
| deepcopy                 | 484 us                                                  | 579 us: 1.20x slower                                  |
| async_generators         | 592 ms                                                  | 712 ms: 1.20x slower                                  |
| xml_etree_generate       | 129 ms                                                  | 157 ms: 1.21x slower                                  |
| json                     | 6.55 ms                                                 | 7.97 ms: 1.22x slower                                 |
| telco                    | 11.4 ms                                                 | 14.0 ms: 1.23x slower                                 |
| scimark_fft              | 477 ms                                                  | 587 ms: 1.23x slower                                  |
| pathlib                  | 29.3 ms                                                 | 36.6 ms: 1.25x slower                                 |
| scimark_sparse_mat_mult  | 6.98 ms                                                 | 8.77 ms: 1.26x slower                                 |
| pylint                   | 472 ms                                                  | 593 ms: 1.26x slower                                  |
| json_dumps               | 14.9 ms                                                 | 18.9 ms: 1.27x slower                                 |
| dulwich_log              | 100.0 ms                                                | 130 ms: 1.30x slower                                  |
| coverage                 | 110 ms                                                  | 147 ms: 1.34x slower                                  |
| mdp                      | 3.80 sec                                                | 5.11 sec: 1.35x slower                                |
| bench_thread_pool        | 3.06 ms                                                 | 4.19 ms: 1.37x slower                                 |
| deepcopy_reduce          | 4.27 us                                                 | 5.88 us: 1.38x slower                                 |
| generators               | 39.2 ms                                                 | 54.8 ms: 1.40x slower                                 |
| python_startup           | 22.0 ms                                                 | 30.9 ms: 1.40x slower                                 |
| xml_etree_process        | 86.5 ms                                                 | 121 ms: 1.40x slower                                  |
| fannkuch                 | 543 ms                                                  | 767 ms: 1.41x slower                                  |
| 2to3                     | 442 ms                                                  | 626 ms: 1.42x slower                                  |
| tornado_http             | 248 ms                                                  | 352 ms: 1.42x slower                                  |
| deepcopy_memo            | 51.7 us                                                 | 73.7 us: 1.43x slower                                 |
| html5lib                 | 98.1 ms                                                 | 141 ms: 1.44x slower                                  |
| pycparser                | 1.57 sec                                                | 2.28 sec: 1.45x slower                                |
| python_startup_no_site   | 14.6 ms                                                 | 21.2 ms: 1.45x slower                                 |
| sympy_integrate          | 29.7 ms                                                 | 43.8 ms: 1.48x slower                                 |
| nqueens                  | 108 ms                                                  | 160 ms: 1.48x slower                                  |
| thrift                   | 1.11 ms                                                 | 1.65 ms: 1.48x slower                                 |
| crypto_pyaes             | 99.8 ms                                                 | 151 ms: 1.51x slower                                  |
| coroutines               | 29.2 ms                                                 | 45.1 ms: 1.55x slower                                 |
| tomli_loads              | 2.80 sec                                                | 4.35 sec: 1.55x slower                                |
| richards                 | 65.8 ms                                                 | 105 ms: 1.60x slower                                  |
| spectral_norm            | 159 ms                                                  | 254 ms: 1.60x slower                                  |
| bpe_tokeniser            | 6.25 sec                                                | 10.0 sec: 1.61x slower                                |
| pyflate                  | 661 ms                                                  | 1.08 sec: 1.63x slower                                |
| regex_compile            | 177 ms                                                  | 290 ms: 1.63x slower                                  |
| sqlglot_optimize         | 76.2 ms                                                 | 125 ms: 1.63x slower                                  |
| logging_simple           | 8.98 us                                                 | 15.0 us: 1.67x slower                                 |
| sqlglot_normalize        | 146 ms                                                  | 245 ms: 1.68x slower                                  |
| typing_runtime_protocols | 216 us                                                  | 364 us: 1.68x slower                                  |
| logging_format           | 9.48 us                                                 | 16.0 us: 1.69x slower                                 |
| genshi_xml               | 68.3 ms                                                 | 116 ms: 1.70x slower                                  |
| richards_super           | 76.3 ms                                                 | 130 ms: 1.71x slower                                  |
| scimark_monte_carlo      | 89.9 ms                                                 | 157 ms: 1.74x slower                                  |
| float                    | 115 ms                                                  | 201 ms: 1.75x slower                                  |
| pprint_pformat           | 2.00 sec                                                | 3.52 sec: 1.76x slower                                |
| pprint_safe_repr         | 959 ms                                                  | 1.69 sec: 1.76x slower                                |
| django_template          | 46.9 ms                                                 | 83.8 ms: 1.79x slower                                 |
| sympy_str                | 367 ms                                                  | 672 ms: 1.83x slower                                  |
| genshi_text              | 31.7 ms                                                 | 58.2 ms: 1.83x slower                                 |
| comprehensions           | 20.9 us                                                 | 38.4 us: 1.84x slower                                 |
| unpickle_pure_python     | 296 us                                                  | 547 us: 1.85x slower                                  |
| go                       | 195 ms                                                  | 369 ms: 1.89x slower                                  |
| hexiom                   | 8.35 ms                                                 | 16.0 ms: 1.92x slower                                 |
| pickle_pure_python       | 417 us                                                  | 804 us: 1.93x slower                                  |
| mako                     | 16.1 ms                                                 | 31.2 ms: 1.94x slower                                 |
| sqlglot_parse            | 1.80 ms                                                 | 3.50 ms: 1.95x slower                                 |
| scimark_sor              | 172 ms                                                  | 337 ms: 1.95x slower                                  |
| sqlglot_transpile        | 2.30 ms                                                 | 4.53 ms: 1.97x slower                                 |
| chaos                    | 84.7 ms                                                 | 168 ms: 1.98x slower                                  |
| scimark_lu               | 154 ms                                                  | 309 ms: 2.00x slower                                  |
| logging_silent           | 130 ns                                                  | 272 ns: 2.10x slower                                  |
| sympy_expand             | 631 ms                                                  | 1.36 sec: 2.15x slower                                |
| sympy_sum                | 213 ms                                                  | 464 ms: 2.18x slower                                  |
| raytrace                 | 350 ms                                                  | 791 ms: 2.26x slower                                  |
| deltablue                | 4.56 ms                                                 | 10.9 ms: 2.39x slower                                 |
| nbody                    | 124 ms                                                  | 312 ms: 2.52x slower                                  |
| unpack_sequence          | 73.9 ns                                                 | 187 ns: 2.54x slower                                  |
| Geometric mean           | (ref)                                                   | 1.40x slower                                          |

Benchmark hidden because not significant (10): async_tree_memoization_tg, pickle, async_tree_cpu_io_mixed_tg, pidigits, regex_dna, xml_etree_iterparse, xml_etree_parse, async_tree_none, async_tree_memoization, sqlite_synth
Ignored benchmarks (5) of results/bm-20240814-3.13.0rc1+-79452b1/bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1.json: aiohttp, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.35x
- 95% likely to have a slowdown of 1.32x
- 99% likely to have a slowdown of 1.25x

# Memory
- memory change: 1.15x