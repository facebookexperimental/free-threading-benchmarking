# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_tlbc_integ
- machine: linux-x86_64
- commit hash: 0a68813
- commit date: 2024-10-31
- overall geometric mean: 1.45x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.32x slower
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241031-vultr-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 407 ms: 1.55x slower                                                 |
| docutils       | 2.64 sec                                               | 3.20 sec: 1.21x slower                                               |
| html5lib       | 63.6 ms                                                | 101 ms: 1.58x slower                                                 |
| tornado_http   | 119 ms                                                 | 159 ms: 1.33x slower                                                 |
| Geometric mean | (ref)                                                  | 1.41x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241031-vultr-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| asyncio_tcp      | 519 ms                                                 | 582 ms: 1.12x slower                                                 |
| coroutines       | 23.9 ms                                                | 26.9 ms: 1.12x slower                                                |
| asyncio_tcp_ssl  | 1.51 sec                                               | 1.80 sec: 1.20x slower                                               |
| async_generators | 384 ms                                                 | 489 ms: 1.27x slower                                                 |
| Geometric mean   | (ref)                                                  | 1.14x slower                                                         |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241031-vultr-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 183 ms: 1.01x faster                                                 |
| float          | 80.8 ms                                                | 144 ms: 1.78x slower                                                 |
| nbody          | 89.3 ms                                                | 191 ms: 2.14x slower                                                 |
| Geometric mean | (ref)                                                  | 1.56x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241031-vultr-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 3.15 ms: 1.01x faster                                                |
| regex_dna      | 168 ms                                                 | 188 ms: 1.12x slower                                                 |
| regex_v8       | 20.6 ms                                                | 25.9 ms: 1.26x slower                                                |
| regex_compile  | 142 ms                                                 | 201 ms: 1.41x slower                                                 |
| Geometric mean | (ref)                                                  | 1.19x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241031-vultr-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle               | 10.9 us                                                | 10.4 us: 1.05x faster                                                |
| xml_etree_parse      | 139 ms                                                 | 133 ms: 1.04x faster                                                 |
| pickle_dict          | 31.8 us                                                | 31.1 us: 1.02x faster                                                |
| pickle_list          | 4.77 us                                                | 4.79 us: 1.01x slower                                                |
| xml_etree_iterparse  | 96.7 ms                                                | 100 ms: 1.04x slower                                                 |
| unpickle             | 14.1 us                                                | 15.0 us: 1.07x slower                                                |
| json_loads           | 26.5 us                                                | 28.7 us: 1.08x slower                                                |
| unpickle_list        | 4.67 us                                                | 5.16 us: 1.10x slower                                                |
| xml_etree_generate   | 85.2 ms                                                | 104 ms: 1.22x slower                                                 |
| json_dumps           | 10.4 ms                                                | 14.6 ms: 1.41x slower                                                |
| xml_etree_process    | 59.0 ms                                                | 85.2 ms: 1.44x slower                                                |
| tomli_loads          | 2.11 sec                                               | 3.07 sec: 1.46x slower                                               |
| unpickle_pure_python | 221 us                                                 | 353 us: 1.60x slower                                                 |
| pickle_pure_python   | 308 us                                                 | 530 us: 1.72x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.19x slower                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241031-vultr-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.3 ms: 1.44x slower                                                |
| python_startup         | 9.93 ms                                                | 15.8 ms: 1.59x slower                                                |
| Geometric mean         | (ref)                                                  | 1.51x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241031-vultr-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 73.3 ms: 1.46x slower                                                |
| genshi_text     | 22.8 ms                                                | 35.6 ms: 1.56x slower                                                |
| django_template | 34.7 ms                                                | 56.5 ms: 1.63x slower                                                |
| mako            | 11.0 ms                                                | 18.6 ms: 1.69x slower                                                |
| Geometric mean  | (ref)                                                  | 1.58x slower                                                         |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241031-vultr-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|--------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| gc_traversal             | 3.46 ms                                                | 2.48 ms: 1.40x faster                                                |
| pickle                   | 10.9 us                                                | 10.4 us: 1.05x faster                                                |
| xml_etree_parse          | 139 ms                                                 | 133 ms: 1.04x faster                                                 |
| pickle_dict              | 31.8 us                                                | 31.1 us: 1.02x faster                                                |
| pathlib                  | 21.5 ms                                                | 21.1 ms: 1.02x faster                                                |
| pidigits                 | 184 ms                                                 | 183 ms: 1.01x faster                                                 |
| regex_effbot             | 3.17 ms                                                | 3.15 ms: 1.01x faster                                                |
| pickle_list              | 4.77 us                                                | 4.79 us: 1.01x slower                                                |
| deepcopy                 | 352 us                                                 | 362 us: 1.03x slower                                                 |
| create_gc_cycles         | 1.09 ms                                                | 1.13 ms: 1.03x slower                                                |
| xml_etree_iterparse      | 96.7 ms                                                | 100 ms: 1.04x slower                                                 |
| json                     | 5.02 ms                                                | 5.22 ms: 1.04x slower                                                |
| deepcopy_memo            | 40.3 us                                                | 42.7 us: 1.06x slower                                                |
| unpickle                 | 14.1 us                                                | 15.0 us: 1.07x slower                                                |
| sqlite_synth             | 2.20 us                                                | 2.36 us: 1.07x slower                                                |
| json_loads               | 26.5 us                                                | 28.7 us: 1.08x slower                                                |
| unpickle_list            | 4.67 us                                                | 5.16 us: 1.10x slower                                                |
| regex_dna                | 168 ms                                                 | 188 ms: 1.12x slower                                                 |
| asyncio_tcp              | 519 ms                                                 | 582 ms: 1.12x slower                                                 |
| coroutines               | 23.9 ms                                                | 26.9 ms: 1.12x slower                                                |
| bpe_tokeniser            | 4.74 sec                                               | 5.38 sec: 1.14x slower                                               |
| scimark_fft              | 342 ms                                                 | 400 ms: 1.17x slower                                                 |
| asyncio_tcp_ssl          | 1.51 sec                                               | 1.80 sec: 1.20x slower                                               |
| docutils                 | 2.64 sec                                               | 3.20 sec: 1.21x slower                                               |
| xml_etree_generate       | 85.2 ms                                                | 104 ms: 1.22x slower                                                 |
| deepcopy_reduce          | 3.08 us                                                | 3.77 us: 1.22x slower                                                |
| pylint                   | 319 ms                                                 | 400 ms: 1.26x slower                                                 |
| regex_v8                 | 20.6 ms                                                | 25.9 ms: 1.26x slower                                                |
| scimark_sparse_mat_mult  | 4.39 ms                                                | 5.54 ms: 1.26x slower                                                |
| typing_runtime_protocols | 163 us                                                 | 207 us: 1.26x slower                                                 |
| async_generators         | 384 ms                                                 | 489 ms: 1.27x slower                                                 |
| dulwich_log              | 78.9 ms                                                | 100 ms: 1.27x slower                                                 |
| meteor_contest           | 104 ms                                                 | 133 ms: 1.28x slower                                                 |
| mdp                      | 2.42 sec                                               | 3.15 sec: 1.30x slower                                               |
| generators               | 32.2 ms                                                | 42.5 ms: 1.32x slower                                                |
| tornado_http             | 119 ms                                                 | 159 ms: 1.33x slower                                                 |
| spectral_norm            | 110 ms                                                 | 147 ms: 1.34x slower                                                 |
| nqueens                  | 80.1 ms                                                | 110 ms: 1.37x slower                                                 |
| coverage                 | 71.4 ms                                                | 99.8 ms: 1.40x slower                                                |
| pycparser                | 1.17 sec                                               | 1.64 sec: 1.40x slower                                               |
| crypto_pyaes             | 76.6 ms                                                | 107 ms: 1.40x slower                                                 |
| json_dumps               | 10.4 ms                                                | 14.6 ms: 1.41x slower                                                |
| regex_compile            | 142 ms                                                 | 201 ms: 1.41x slower                                                 |
| sqlglot_normalize        | 107 ms                                                 | 152 ms: 1.43x slower                                                 |
| python_startup_no_site   | 7.16 ms                                                | 10.3 ms: 1.44x slower                                                |
| sqlglot_optimize         | 53.3 ms                                                | 76.9 ms: 1.44x slower                                                |
| xml_etree_process        | 59.0 ms                                                | 85.2 ms: 1.44x slower                                                |
| comprehensions           | 19.8 us                                                | 28.8 us: 1.45x slower                                                |
| tomli_loads              | 2.11 sec                                               | 3.07 sec: 1.46x slower                                               |
| telco                    | 6.53 ms                                                | 9.52 ms: 1.46x slower                                                |
| genshi_xml               | 50.2 ms                                                | 73.3 ms: 1.46x slower                                                |
| pprint_safe_repr         | 743 ms                                                 | 1.09 sec: 1.47x slower                                               |
| pprint_pformat           | 1.52 sec                                               | 2.28 sec: 1.50x slower                                               |
| fannkuch                 | 372 ms                                                 | 561 ms: 1.51x slower                                                 |
| sympy_integrate          | 20.5 ms                                                | 31.3 ms: 1.52x slower                                                |
| thrift                   | 791 us                                                 | 1.22 ms: 1.54x slower                                                |
| 2to3                     | 264 ms                                                 | 407 ms: 1.55x slower                                                 |
| genshi_text              | 22.8 ms                                                | 35.6 ms: 1.56x slower                                                |
| html5lib                 | 63.6 ms                                                | 101 ms: 1.58x slower                                                 |
| python_startup           | 9.93 ms                                                | 15.8 ms: 1.59x slower                                                |
| unpickle_pure_python     | 221 us                                                 | 353 us: 1.60x slower                                                 |
| django_template          | 34.7 ms                                                | 56.5 ms: 1.63x slower                                                |
| pyflate                  | 448 ms                                                 | 741 ms: 1.66x slower                                                 |
| mako                     | 11.0 ms                                                | 18.6 ms: 1.69x slower                                                |
| logging_format           | 7.35 us                                                | 12.5 us: 1.70x slower                                                |
| logging_simple           | 6.63 us                                                | 11.4 us: 1.72x slower                                                |
| pickle_pure_python       | 308 us                                                 | 530 us: 1.72x slower                                                 |
| scimark_monte_carlo      | 68.4 ms                                                | 120 ms: 1.76x slower                                                 |
| sympy_str                | 292 ms                                                 | 513 ms: 1.76x slower                                                 |
| scimark_lu               | 114 ms                                                 | 202 ms: 1.77x slower                                                 |
| chaos                    | 62.8 ms                                                | 112 ms: 1.78x slower                                                 |
| float                    | 80.8 ms                                                | 144 ms: 1.78x slower                                                 |
| richards                 | 45.9 ms                                                | 82.6 ms: 1.80x slower                                                |
| hexiom                   | 6.17 ms                                                | 11.2 ms: 1.81x slower                                                |
| logging_silent           | 109 ns                                                 | 199 ns: 1.83x slower                                                 |
| sqlglot_transpile        | 1.67 ms                                                | 3.20 ms: 1.91x slower                                                |
| richards_super           | 51.9 ms                                                | 99.7 ms: 1.92x slower                                                |
| raytrace                 | 299 ms                                                 | 577 ms: 1.93x slower                                                 |
| scimark_sor              | 130 ms                                                 | 264 ms: 2.03x slower                                                 |
| sqlglot_parse            | 1.36 ms                                                | 2.78 ms: 2.05x slower                                                |
| go                       | 139 ms                                                 | 288 ms: 2.07x slower                                                 |
| nbody                    | 89.3 ms                                                | 191 ms: 2.14x slower                                                 |
| sympy_expand             | 468 ms                                                 | 1.01 sec: 2.16x slower                                               |
| sympy_sum                | 166 ms                                                 | 367 ms: 2.21x slower                                                 |
| deltablue                | 3.45 ms                                                | 8.43 ms: 2.45x slower                                                |
| unpack_sequence          | 52.1 ns                                                | 142 ns: 2.72x slower                                                 |
| bench_thread_pool        | 941 us                                                 | 3.44 ms: 3.65x slower                                                |
| bench_mp_pool            | 10.8 ms                                                | 71.7 ms: 6.64x slower                                                |
| Geometric mean           | (ref)                                                  | 1.45x slower                                                         |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.38x
- 95% likely to have a slowdown of 1.36x
- 99% likely to have a slowdown of 1.32x

# Memory
- memory change: 1.23x