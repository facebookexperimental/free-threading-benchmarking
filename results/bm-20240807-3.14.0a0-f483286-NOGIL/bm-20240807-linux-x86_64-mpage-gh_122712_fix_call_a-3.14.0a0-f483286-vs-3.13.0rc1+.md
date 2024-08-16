# Results vs. 3.13.0rc1+

- fork: mpage
- ref: gh_122712_fix_call_a
- machine: linux-x86_64
- commit hash: f483286
- commit date: 2024-08-07
- overall geometric mean: 1.42x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.29x slower
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------|:-------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 442 ms                                                  | 646 ms: 1.46x slower                                                 |
| docutils       | 4.01 sec                                                | 5.06 sec: 1.26x slower                                               |
| html5lib       | 98.1 ms                                                 | 140 ms: 1.43x slower                                                 |
| tornado_http   | 248 ms                                                  | 367 ms: 1.48x slower                                                 |
| Geometric mean | (ref)                                                   | 1.41x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|--------------------|:-------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg   | 1.46 sec                                                | 1.15 sec: 1.27x faster                                               |
| async_tree_io      | 1.38 sec                                                | 1.25 sec: 1.10x faster                                               |
| async_tree_none_tg | 521 ms                                                  | 491 ms: 1.06x faster                                                 |
| asyncio_tcp        | 985 ms                                                  | 1.12 sec: 1.13x slower                                               |
| asyncio_tcp_ssl    | 2.79 sec                                                | 3.36 sec: 1.20x slower                                               |
| async_generators   | 592 ms                                                  | 753 ms: 1.27x slower                                                 |
| coroutines         | 29.2 ms                                                 | 42.1 ms: 1.44x slower                                                |
| Geometric mean     | (ref)                                                   | 1.04x slower                                                         |

Benchmark hidden because not significant (6): async_tree_cpu_io_mixed_tg, asyncio_websockets, async_tree_memoization_tg, async_tree_memoization, async_tree_none, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------|:-------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 115 ms                                                  | 196 ms: 1.70x slower                                                 |
| nbody          | 124 ms                                                  | 284 ms: 2.29x slower                                                 |
| Geometric mean | (ref)                                                   | 1.56x slower                                                         |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------|:-------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_dna      | 288 ms                                                  | 301 ms: 1.05x slower                                                 |
| regex_v8       | 32.4 ms                                                 | 39.2 ms: 1.21x slower                                                |
| regex_compile  | 177 ms                                                  | 295 ms: 1.66x slower                                                 |
| Geometric mean | (ref)                                                   | 1.20x slower                                                         |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------------|:-------------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle               | 15.4 us                                                 | 14.1 us: 1.09x faster                                                |
| pickle_dict          | 46.5 us                                                 | 43.9 us: 1.06x faster                                                |
| json_dumps           | 14.9 ms                                                 | 17.7 ms: 1.19x slower                                                |
| unpickle_list        | 6.67 us                                                 | 7.94 us: 1.19x slower                                                |
| json_loads           | 36.1 us                                                 | 45.4 us: 1.26x slower                                                |
| xml_etree_generate   | 129 ms                                                  | 164 ms: 1.27x slower                                                 |
| tomli_loads          | 2.80 sec                                                | 4.20 sec: 1.50x slower                                               |
| xml_etree_process    | 86.5 ms                                                 | 135 ms: 1.56x slower                                                 |
| pickle_pure_python   | 417 us                                                  | 778 us: 1.87x slower                                                 |
| unpickle_pure_python | 296 us                                                  | 567 us: 1.92x slower                                                 |
| Geometric mean       | (ref)                                                   | 1.22x slower                                                         |

Benchmark hidden because not significant (4): xml_etree_parse, pickle_list, xml_etree_iterparse, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|------------------------|:-------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 22.0 ms                                                 | 29.3 ms: 1.33x slower                                                |
| python_startup_no_site | 14.6 ms                                                 | 20.7 ms: 1.41x slower                                                |
| Geometric mean         | (ref)                                                   | 1.37x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|-----------------|:-------------------------------------------------------:|:--------------------------------------------------------------------:|
| django_template | 46.9 ms                                                 | 77.1 ms: 1.64x slower                                                |
| genshi_text     | 31.7 ms                                                 | 54.2 ms: 1.71x slower                                                |
| genshi_xml      | 68.3 ms                                                 | 118 ms: 1.73x slower                                                 |
| mako            | 16.1 ms                                                 | 32.1 ms: 2.00x slower                                                |
| Geometric mean  | (ref)                                                   | 1.76x slower                                                         |

All benchmarks:
===============

| Benchmark                | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|--------------------------|:-------------------------------------------------------:|:--------------------------------------------------------------------:|
| create_gc_cycles         | 2.46 ms                                                 | 1.92 ms: 1.28x faster                                                |
| gc_traversal             | 5.91 ms                                                 | 4.63 ms: 1.28x faster                                                |
| async_tree_io_tg         | 1.46 sec                                                | 1.15 sec: 1.27x faster                                               |
| bench_mp_pool            | 19.4 ms                                                 | 16.8 ms: 1.15x faster                                                |
| async_tree_io            | 1.38 sec                                                | 1.25 sec: 1.10x faster                                               |
| pickle                   | 15.4 us                                                 | 14.1 us: 1.09x faster                                                |
| async_tree_none_tg       | 521 ms                                                  | 491 ms: 1.06x faster                                                 |
| pickle_dict              | 46.5 us                                                 | 43.9 us: 1.06x faster                                                |
| regex_dna                | 288 ms                                                  | 301 ms: 1.05x slower                                                 |
| sqlite_synth             | 4.07 us                                                 | 4.44 us: 1.09x slower                                                |
| asyncio_tcp              | 985 ms                                                  | 1.12 sec: 1.13x slower                                               |
| deepcopy                 | 484 us                                                  | 556 us: 1.15x slower                                                 |
| json_dumps               | 14.9 ms                                                 | 17.7 ms: 1.19x slower                                                |
| unpickle_list            | 6.67 us                                                 | 7.94 us: 1.19x slower                                                |
| asyncio_tcp_ssl          | 2.79 sec                                                | 3.36 sec: 1.20x slower                                               |
| regex_v8                 | 32.4 ms                                                 | 39.2 ms: 1.21x slower                                                |
| telco                    | 11.4 ms                                                 | 13.8 ms: 1.21x slower                                                |
| pathlib                  | 29.3 ms                                                 | 35.6 ms: 1.21x slower                                                |
| meteor_contest           | 157 ms                                                  | 194 ms: 1.24x slower                                                 |
| pylint                   | 472 ms                                                  | 590 ms: 1.25x slower                                                 |
| json                     | 6.55 ms                                                 | 8.22 ms: 1.26x slower                                                |
| json_loads               | 36.1 us                                                 | 45.4 us: 1.26x slower                                                |
| docutils                 | 4.01 sec                                                | 5.06 sec: 1.26x slower                                               |
| xml_etree_generate       | 129 ms                                                  | 164 ms: 1.27x slower                                                 |
| async_generators         | 592 ms                                                  | 753 ms: 1.27x slower                                                 |
| scimark_sparse_mat_mult  | 6.98 ms                                                 | 9.23 ms: 1.32x slower                                                |
| coverage                 | 110 ms                                                  | 146 ms: 1.32x slower                                                 |
| python_startup           | 22.0 ms                                                 | 29.3 ms: 1.33x slower                                                |
| scimark_fft              | 477 ms                                                  | 635 ms: 1.33x slower                                                 |
| deepcopy_memo            | 51.7 us                                                 | 69.7 us: 1.35x slower                                                |
| mdp                      | 3.80 sec                                                | 5.16 sec: 1.36x slower                                               |
| deepcopy_reduce          | 4.27 us                                                 | 5.84 us: 1.37x slower                                                |
| bench_thread_pool        | 3.06 ms                                                 | 4.33 ms: 1.41x slower                                                |
| python_startup_no_site   | 14.6 ms                                                 | 20.7 ms: 1.41x slower                                                |
| html5lib                 | 98.1 ms                                                 | 140 ms: 1.43x slower                                                 |
| fannkuch                 | 543 ms                                                  | 776 ms: 1.43x slower                                                 |
| coroutines               | 29.2 ms                                                 | 42.1 ms: 1.44x slower                                                |
| pycparser                | 1.57 sec                                                | 2.29 sec: 1.46x slower                                               |
| 2to3                     | 442 ms                                                  | 646 ms: 1.46x slower                                                 |
| generators               | 39.2 ms                                                 | 57.5 ms: 1.47x slower                                                |
| tornado_http             | 248 ms                                                  | 367 ms: 1.48x slower                                                 |
| nqueens                  | 108 ms                                                  | 161 ms: 1.49x slower                                                 |
| sympy_integrate          | 29.7 ms                                                 | 44.3 ms: 1.49x slower                                                |
| tomli_loads              | 2.80 sec                                                | 4.20 sec: 1.50x slower                                               |
| crypto_pyaes             | 99.8 ms                                                 | 152 ms: 1.53x slower                                                 |
| xml_etree_process        | 86.5 ms                                                 | 135 ms: 1.56x slower                                                 |
| spectral_norm            | 159 ms                                                  | 253 ms: 1.59x slower                                                 |
| thrift                   | 1.11 ms                                                 | 1.77 ms: 1.59x slower                                                |
| richards_super           | 76.3 ms                                                 | 124 ms: 1.63x slower                                                 |
| bpe_tokeniser            | 6.25 sec                                                | 10.3 sec: 1.64x slower                                               |
| django_template          | 46.9 ms                                                 | 77.1 ms: 1.64x slower                                                |
| typing_runtime_protocols | 216 us                                                  | 356 us: 1.65x slower                                                 |
| pyflate                  | 661 ms                                                  | 1.09 sec: 1.65x slower                                               |
| sqlglot_normalize        | 146 ms                                                  | 242 ms: 1.66x slower                                                 |
| regex_compile            | 177 ms                                                  | 295 ms: 1.66x slower                                                 |
| richards                 | 65.8 ms                                                 | 110 ms: 1.67x slower                                                 |
| logging_simple           | 8.98 us                                                 | 15.0 us: 1.68x slower                                                |
| float                    | 115 ms                                                  | 196 ms: 1.70x slower                                                 |
| genshi_text              | 31.7 ms                                                 | 54.2 ms: 1.71x slower                                                |
| pprint_safe_repr         | 959 ms                                                  | 1.64 sec: 1.71x slower                                               |
| genshi_xml               | 68.3 ms                                                 | 118 ms: 1.73x slower                                                 |
| pprint_pformat           | 2.00 sec                                                | 3.45 sec: 1.73x slower                                               |
| scimark_monte_carlo      | 89.9 ms                                                 | 160 ms: 1.78x slower                                                 |
| comprehensions           | 20.9 us                                                 | 38.3 us: 1.83x slower                                                |
| sympy_str                | 367 ms                                                  | 673 ms: 1.83x slower                                                 |
| pickle_pure_python       | 417 us                                                  | 778 us: 1.87x slower                                                 |
| sqlglot_optimize         | 76.2 ms                                                 | 143 ms: 1.88x slower                                                 |
| unpickle_pure_python     | 296 us                                                  | 567 us: 1.92x slower                                                 |
| logging_format           | 9.48 us                                                 | 18.5 us: 1.96x slower                                                |
| logging_silent           | 130 ns                                                  | 254 ns: 1.96x slower                                                 |
| scimark_lu               | 154 ms                                                  | 303 ms: 1.97x slower                                                 |
| scimark_sor              | 172 ms                                                  | 342 ms: 1.98x slower                                                 |
| chaos                    | 84.7 ms                                                 | 169 ms: 1.99x slower                                                 |
| mako                     | 16.1 ms                                                 | 32.1 ms: 2.00x slower                                                |
| sympy_expand             | 631 ms                                                  | 1.26 sec: 2.00x slower                                               |
| sqlglot_transpile        | 2.30 ms                                                 | 4.62 ms: 2.01x slower                                                |
| hexiom                   | 8.35 ms                                                 | 17.2 ms: 2.05x slower                                                |
| sympy_sum                | 213 ms                                                  | 465 ms: 2.18x slower                                                 |
| raytrace                 | 350 ms                                                  | 765 ms: 2.19x slower                                                 |
| go                       | 195 ms                                                  | 446 ms: 2.28x slower                                                 |
| nbody                    | 124 ms                                                  | 284 ms: 2.29x slower                                                 |
| sqlglot_parse            | 1.80 ms                                                 | 4.43 ms: 2.46x slower                                                |
| deltablue                | 4.56 ms                                                 | 11.3 ms: 2.49x slower                                                |
| unpack_sequence          | 73.9 ns                                                 | 211 ns: 2.85x slower                                                 |
| Geometric mean           | (ref)                                                   | 1.42x slower                                                         |

Benchmark hidden because not significant (12): async_tree_cpu_io_mixed_tg, asyncio_websockets, pidigits, xml_etree_parse, async_tree_memoization_tg, regex_effbot, async_tree_memoization, pickle_list, xml_etree_iterparse, async_tree_none, unpickle, async_tree_cpu_io_mixed
Ignored benchmarks (6) of results/bm-20240814-3.13.0rc1+-79452b1/bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.36x
- 95% likely to have a slowdown of 1.34x
- 99% likely to have a slowdown of 1.29x

# Memory
- memory change: 1.14x