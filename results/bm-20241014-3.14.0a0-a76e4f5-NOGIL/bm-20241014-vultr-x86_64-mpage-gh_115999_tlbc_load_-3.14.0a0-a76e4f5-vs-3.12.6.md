# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_tlbc_load_
- machine: linux-x86_64
- commit hash: a76e4f5
- commit date: 2024-10-14
- overall geometric mean: 1.54x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.38x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-a76e4f5 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 419 ms: 1.59x slower                                                 |
| docutils       | 2.64 sec                                               | 3.37 sec: 1.28x slower                                               |
| html5lib       | 63.6 ms                                                | 106 ms: 1.66x slower                                                 |
| tornado_http   | 119 ms                                                 | 165 ms: 1.39x slower                                                 |
| Geometric mean | (ref)                                                  | 1.47x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-a76e4f5 |
|--------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| asyncio_websockets | 517 ms                                                 | 520 ms: 1.01x slower                                                 |
| asyncio_tcp        | 519 ms                                                 | 580 ms: 1.12x slower                                                 |
| asyncio_tcp_ssl    | 1.51 sec                                               | 1.83 sec: 1.21x slower                                               |
| async_generators   | 384 ms                                                 | 495 ms: 1.29x slower                                                 |
| coroutines         | 23.9 ms                                                | 31.2 ms: 1.30x slower                                                |
| Geometric mean     | (ref)                                                  | 1.18x slower                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-a76e4f5 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 151 ms: 1.87x slower                                                 |
| nbody          | 89.3 ms                                                | 196 ms: 2.19x slower                                                 |
| Geometric mean | (ref)                                                  | 1.60x slower                                                         |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-a76e4f5 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 3.20 ms: 1.01x slower                                                |
| regex_dna      | 168 ms                                                 | 191 ms: 1.14x slower                                                 |
| regex_v8       | 20.6 ms                                                | 25.9 ms: 1.26x slower                                                |
| regex_compile  | 142 ms                                                 | 233 ms: 1.63x slower                                                 |
| Geometric mean | (ref)                                                  | 1.24x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-a76e4f5 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 133 ms: 1.04x faster                                                 |
| pickle               | 10.9 us                                                | 10.7 us: 1.02x faster                                                |
| pickle_dict          | 31.8 us                                                | 32.6 us: 1.03x slower                                                |
| pickle_list          | 4.77 us                                                | 4.93 us: 1.03x slower                                                |
| unpickle             | 14.1 us                                                | 14.9 us: 1.06x slower                                                |
| json_loads           | 26.5 us                                                | 28.7 us: 1.08x slower                                                |
| unpickle_list        | 4.67 us                                                | 5.11 us: 1.09x slower                                                |
| xml_etree_iterparse  | 96.7 ms                                                | 109 ms: 1.13x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 114 ms: 1.34x slower                                                 |
| json_dumps           | 10.4 ms                                                | 15.3 ms: 1.48x slower                                                |
| tomli_loads          | 2.11 sec                                               | 3.27 sec: 1.55x slower                                               |
| xml_etree_process    | 59.0 ms                                                | 93.1 ms: 1.58x slower                                                |
| unpickle_pure_python | 221 us                                                 | 425 us: 1.93x slower                                                 |
| pickle_pure_python   | 308 us                                                 | 623 us: 2.02x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.26x slower                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-a76e4f5 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.2 ms: 1.43x slower                                                |
| python_startup         | 9.93 ms                                                | 15.7 ms: 1.58x slower                                                |
| Geometric mean         | (ref)                                                  | 1.50x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-a76e4f5 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 83.5 ms: 1.66x slower                                                |
| genshi_text     | 22.8 ms                                                | 40.4 ms: 1.77x slower                                                |
| django_template | 34.7 ms                                                | 65.4 ms: 1.89x slower                                                |
| mako            | 11.0 ms                                                | 21.1 ms: 1.91x slower                                                |
| Geometric mean  | (ref)                                                  | 1.81x slower                                                         |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-a76e4f5 |
|--------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| gc_traversal             | 3.46 ms                                                | 2.46 ms: 1.40x faster                                                |
| xml_etree_parse          | 139 ms                                                 | 133 ms: 1.04x faster                                                 |
| pickle                   | 10.9 us                                                | 10.7 us: 1.02x faster                                                |
| asyncio_websockets       | 517 ms                                                 | 520 ms: 1.01x slower                                                 |
| regex_effbot             | 3.17 ms                                                | 3.20 ms: 1.01x slower                                                |
| pickle_dict              | 31.8 us                                                | 32.6 us: 1.03x slower                                                |
| create_gc_cycles         | 1.09 ms                                                | 1.13 ms: 1.03x slower                                                |
| pickle_list              | 4.77 us                                                | 4.93 us: 1.03x slower                                                |
| pathlib                  | 21.5 ms                                                | 22.3 ms: 1.04x slower                                                |
| json                     | 5.02 ms                                                | 5.31 ms: 1.06x slower                                                |
| unpickle                 | 14.1 us                                                | 14.9 us: 1.06x slower                                                |
| json_loads               | 26.5 us                                                | 28.7 us: 1.08x slower                                                |
| unpickle_list            | 4.67 us                                                | 5.11 us: 1.09x slower                                                |
| asyncio_tcp              | 519 ms                                                 | 580 ms: 1.12x slower                                                 |
| xml_etree_iterparse      | 96.7 ms                                                | 109 ms: 1.13x slower                                                 |
| regex_dna                | 168 ms                                                 | 191 ms: 1.14x slower                                                 |
| sqlite_synth             | 2.20 us                                                | 2.50 us: 1.14x slower                                                |
| scimark_fft              | 342 ms                                                 | 404 ms: 1.18x slower                                                 |
| asyncio_tcp_ssl          | 1.51 sec                                               | 1.83 sec: 1.21x slower                                               |
| scimark_sparse_mat_mult  | 4.39 ms                                                | 5.35 ms: 1.22x slower                                                |
| regex_v8                 | 20.6 ms                                                | 25.9 ms: 1.26x slower                                                |
| deepcopy                 | 352 us                                                 | 445 us: 1.26x slower                                                 |
| docutils                 | 2.64 sec                                               | 3.37 sec: 1.28x slower                                               |
| async_generators         | 384 ms                                                 | 495 ms: 1.29x slower                                                 |
| generators               | 32.2 ms                                                | 42.1 ms: 1.30x slower                                                |
| coroutines               | 23.9 ms                                                | 31.2 ms: 1.30x slower                                                |
| bpe_tokeniser            | 4.74 sec                                               | 6.22 sec: 1.31x slower                                               |
| mdp                      | 2.42 sec                                               | 3.18 sec: 1.31x slower                                               |
| dulwich_log              | 78.9 ms                                                | 104 ms: 1.32x slower                                                 |
| pylint                   | 319 ms                                                 | 422 ms: 1.32x slower                                                 |
| xml_etree_generate       | 85.2 ms                                                | 114 ms: 1.34x slower                                                 |
| deepcopy_memo            | 40.3 us                                                | 54.3 us: 1.35x slower                                                |
| meteor_contest           | 104 ms                                                 | 141 ms: 1.37x slower                                                 |
| tornado_http             | 119 ms                                                 | 165 ms: 1.39x slower                                                 |
| spectral_norm            | 110 ms                                                 | 156 ms: 1.42x slower                                                 |
| python_startup_no_site   | 7.16 ms                                                | 10.2 ms: 1.43x slower                                                |
| crypto_pyaes             | 76.6 ms                                                | 110 ms: 1.43x slower                                                 |
| nqueens                  | 80.1 ms                                                | 115 ms: 1.44x slower                                                 |
| coverage                 | 71.4 ms                                                | 103 ms: 1.44x slower                                                 |
| telco                    | 6.53 ms                                                | 9.57 ms: 1.47x slower                                                |
| pycparser                | 1.17 sec                                               | 1.73 sec: 1.48x slower                                               |
| json_dumps               | 10.4 ms                                                | 15.3 ms: 1.48x slower                                                |
| deepcopy_reduce          | 3.08 us                                                | 4.67 us: 1.52x slower                                                |
| typing_runtime_protocols | 163 us                                                 | 248 us: 1.52x slower                                                 |
| fannkuch                 | 372 ms                                                 | 570 ms: 1.53x slower                                                 |
| comprehensions           | 19.8 us                                                | 30.6 us: 1.54x slower                                                |
| tomli_loads              | 2.11 sec                                               | 3.27 sec: 1.55x slower                                               |
| xml_etree_process        | 59.0 ms                                                | 93.1 ms: 1.58x slower                                                |
| python_startup           | 9.93 ms                                                | 15.7 ms: 1.58x slower                                                |
| 2to3                     | 264 ms                                                 | 419 ms: 1.59x slower                                                 |
| sympy_integrate          | 20.5 ms                                                | 33.2 ms: 1.62x slower                                                |
| regex_compile            | 142 ms                                                 | 233 ms: 1.63x slower                                                 |
| thrift                   | 791 us                                                 | 1.30 ms: 1.64x slower                                                |
| html5lib                 | 63.6 ms                                                | 106 ms: 1.66x slower                                                 |
| genshi_xml               | 50.2 ms                                                | 83.5 ms: 1.66x slower                                                |
| sqlglot_normalize        | 107 ms                                                 | 183 ms: 1.71x slower                                                 |
| sqlglot_optimize         | 53.3 ms                                                | 91.5 ms: 1.72x slower                                                |
| pyflate                  | 448 ms                                                 | 785 ms: 1.75x slower                                                 |
| genshi_text              | 22.8 ms                                                | 40.4 ms: 1.77x slower                                                |
| pprint_safe_repr         | 743 ms                                                 | 1.36 sec: 1.83x slower                                               |
| logging_format           | 7.35 us                                                | 13.5 us: 1.84x slower                                                |
| scimark_monte_carlo      | 68.4 ms                                                | 126 ms: 1.84x slower                                                 |
| logging_simple           | 6.63 us                                                | 12.3 us: 1.85x slower                                                |
| pprint_pformat           | 1.52 sec                                               | 2.83 sec: 1.86x slower                                               |
| sympy_str                | 292 ms                                                 | 543 ms: 1.86x slower                                                 |
| float                    | 80.8 ms                                                | 151 ms: 1.87x slower                                                 |
| django_template          | 34.7 ms                                                | 65.4 ms: 1.89x slower                                                |
| mako                     | 11.0 ms                                                | 21.1 ms: 1.91x slower                                                |
| unpickle_pure_python     | 221 us                                                 | 425 us: 1.93x slower                                                 |
| chaos                    | 62.8 ms                                                | 122 ms: 1.94x slower                                                 |
| richards                 | 45.9 ms                                                | 89.4 ms: 1.95x slower                                                |
| logging_silent           | 109 ns                                                 | 219 ns: 2.01x slower                                                 |
| sqlglot_transpile        | 1.67 ms                                                | 3.37 ms: 2.02x slower                                                |
| pickle_pure_python       | 308 us                                                 | 623 us: 2.02x slower                                                 |
| hexiom                   | 6.17 ms                                                | 12.6 ms: 2.04x slower                                                |
| scimark_sor              | 130 ms                                                 | 268 ms: 2.07x slower                                                 |
| richards_super           | 51.9 ms                                                | 108 ms: 2.08x slower                                                 |
| raytrace                 | 299 ms                                                 | 627 ms: 2.10x slower                                                 |
| scimark_lu               | 114 ms                                                 | 240 ms: 2.10x slower                                                 |
| sqlglot_parse            | 1.36 ms                                                | 2.91 ms: 2.15x slower                                                |
| go                       | 139 ms                                                 | 302 ms: 2.17x slower                                                 |
| nbody                    | 89.3 ms                                                | 196 ms: 2.19x slower                                                 |
| sympy_expand             | 468 ms                                                 | 1.06 sec: 2.27x slower                                               |
| sympy_sum                | 166 ms                                                 | 382 ms: 2.30x slower                                                 |
| deltablue                | 3.45 ms                                                | 9.10 ms: 2.64x slower                                                |
| unpack_sequence          | 52.1 ns                                                | 138 ns: 2.65x slower                                                 |
| bench_thread_pool        | 941 us                                                 | 3.48 ms: 3.69x slower                                                |
| bench_mp_pool            | 10.8 ms                                                | 71.9 ms: 6.66x slower                                                |
| Geometric mean           | (ref)                                                  | 1.54x slower                                                         |

Benchmark hidden because not significant (1): pidigits
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.45x
- 95% likely to have a slowdown of 1.43x
- 99% likely to have a slowdown of 1.38x

# Memory
- memory change: 1.22x