# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: gh_115999_tlbc_call
- machine: linux-x86_64
- commit hash: 8ebd73d
- commit date: 2024-11-20
- overall geometric mean: 1.49x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.35x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2+-32428cf | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 256 ms                                                                 | 410 ms: 1.60x slower                                                 |
| docutils       | 2.63 sec                                                               | 3.28 sec: 1.25x slower                                               |
| html5lib       | 66.9 ms                                                                | 104 ms: 1.55x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.46x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2+-32428cf | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|--------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| asyncio_websockets | 521 ms                                                                 | 523 ms: 1.00x slower                                                 |
| asyncio_tcp        | 506 ms                                                                 | 584 ms: 1.15x slower                                                 |
| asyncio_tcp_ssl    | 1.53 sec                                                               | 1.84 sec: 1.20x slower                                               |
| coroutines         | 22.6 ms                                                                | 28.6 ms: 1.27x slower                                                |
| async_generators   | 378 ms                                                                 | 485 ms: 1.28x slower                                                 |
| Geometric mean     | (ref)                                                                  | 1.18x slower                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2+-32428cf | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 217 ms                                                                 | 182 ms: 1.19x faster                                                 |
| float          | 78.8 ms                                                                | 148 ms: 1.88x slower                                                 |
| nbody          | 95.9 ms                                                                | 199 ms: 2.08x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.49x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2+-32428cf | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 2.86 ms                                                                | 2.82 ms: 1.01x faster                                                |
| regex_dna      | 177 ms                                                                 | 186 ms: 1.05x slower                                                 |
| regex_v8       | 23.6 ms                                                                | 24.9 ms: 1.05x slower                                                |
| regex_compile  | 135 ms                                                                 | 213 ms: 1.59x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.15x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2+-32428cf | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle_list          | 5.29 us                                                                | 4.93 us: 1.07x faster                                                |
| xml_etree_parse      | 137 ms                                                                 | 132 ms: 1.04x faster                                                 |
| pickle_dict          | 32.3 us                                                                | 31.9 us: 1.01x faster                                                |
| pickle               | 12.3 us                                                                | 12.7 us: 1.04x slower                                                |
| unpickle             | 13.5 us                                                                | 14.2 us: 1.06x slower                                                |
| unpickle_list        | 4.81 us                                                                | 5.11 us: 1.06x slower                                                |
| xml_etree_iterparse  | 96.1 ms                                                                | 105 ms: 1.09x slower                                                 |
| json_loads           | 25.0 us                                                                | 28.4 us: 1.13x slower                                                |
| xml_etree_generate   | 86.2 ms                                                                | 109 ms: 1.27x slower                                                 |
| json_dumps           | 11.3 ms                                                                | 15.0 ms: 1.32x slower                                                |
| tomli_loads          | 2.15 sec                                                               | 3.12 sec: 1.45x slower                                               |
| xml_etree_process    | 60.2 ms                                                                | 89.6 ms: 1.49x slower                                                |
| unpickle_pure_python | 217 us                                                                 | 390 us: 1.80x slower                                                 |
| pickle_pure_python   | 320 us                                                                 | 586 us: 1.83x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.21x slower                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2+-32428cf | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 10.3 ms: 1.39x slower                                                |
| python_startup         | 11.1 ms                                                                | 15.8 ms: 1.43x slower                                                |
| Geometric mean         | (ref)                                                                  | 1.41x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2+-32428cf | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 12.0 ms                                                                | 18.9 ms: 1.58x slower                                                |
| genshi_xml      | 50.3 ms                                                                | 79.6 ms: 1.58x slower                                                |
| django_template | 35.7 ms                                                                | 61.4 ms: 1.72x slower                                                |
| genshi_text     | 21.9 ms                                                                | 39.2 ms: 1.79x slower                                                |
| Geometric mean  | (ref)                                                                  | 1.66x slower                                                         |

All benchmarks:
===============

| Benchmark                | bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2+-32428cf | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|--------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| gc_traversal             | 3.63 ms                                                                | 2.68 ms: 1.35x faster                                                |
| pidigits                 | 217 ms                                                                 | 182 ms: 1.19x faster                                                 |
| create_gc_cycles         | 1.34 ms                                                                | 1.19 ms: 1.13x faster                                                |
| pickle_list              | 5.29 us                                                                | 4.93 us: 1.07x faster                                                |
| xml_etree_parse          | 137 ms                                                                 | 132 ms: 1.04x faster                                                 |
| pickle_dict              | 32.3 us                                                                | 31.9 us: 1.01x faster                                                |
| regex_effbot             | 2.86 ms                                                                | 2.82 ms: 1.01x faster                                                |
| asyncio_websockets       | 521 ms                                                                 | 523 ms: 1.00x slower                                                 |
| pickle                   | 12.3 us                                                                | 12.7 us: 1.04x slower                                                |
| regex_dna                | 177 ms                                                                 | 186 ms: 1.05x slower                                                 |
| regex_v8                 | 23.6 ms                                                                | 24.9 ms: 1.05x slower                                                |
| unpickle                 | 13.5 us                                                                | 14.2 us: 1.06x slower                                                |
| unpickle_list            | 4.81 us                                                                | 5.11 us: 1.06x slower                                                |
| sqlite_synth             | 2.24 us                                                                | 2.39 us: 1.07x slower                                                |
| xml_etree_iterparse      | 96.1 ms                                                                | 105 ms: 1.09x slower                                                 |
| bench_mp_pool            | 63.6 ms                                                                | 69.7 ms: 1.10x slower                                                |
| json_loads               | 25.0 us                                                                | 28.4 us: 1.13x slower                                                |
| json                     | 4.61 ms                                                                | 5.22 ms: 1.13x slower                                                |
| asyncio_tcp              | 506 ms                                                                 | 584 ms: 1.15x slower                                                 |
| pathlib                  | 18.6 ms                                                                | 22.0 ms: 1.18x slower                                                |
| scimark_fft              | 337 ms                                                                 | 404 ms: 1.20x slower                                                 |
| asyncio_tcp_ssl          | 1.53 sec                                                               | 1.84 sec: 1.20x slower                                               |
| coverage                 | 80.2 ms                                                                | 99.9 ms: 1.25x slower                                                |
| docutils                 | 2.63 sec                                                               | 3.28 sec: 1.25x slower                                               |
| xml_etree_generate       | 86.2 ms                                                                | 109 ms: 1.27x slower                                                 |
| coroutines               | 22.6 ms                                                                | 28.6 ms: 1.27x slower                                                |
| async_generators         | 378 ms                                                                 | 485 ms: 1.28x slower                                                 |
| telco                    | 7.22 ms                                                                | 9.33 ms: 1.29x slower                                                |
| scimark_sparse_mat_mult  | 4.48 ms                                                                | 5.85 ms: 1.31x slower                                                |
| bpe_tokeniser            | 4.34 sec                                                               | 5.68 sec: 1.31x slower                                               |
| mdp                      | 2.36 sec                                                               | 3.12 sec: 1.32x slower                                               |
| json_dumps               | 11.3 ms                                                                | 15.0 ms: 1.32x slower                                                |
| meteor_contest           | 100 ms                                                                 | 135 ms: 1.35x slower                                                 |
| spectral_norm            | 113 ms                                                                 | 153 ms: 1.35x slower                                                 |
| dulwich_log              | 75.9 ms                                                                | 103 ms: 1.36x slower                                                 |
| python_startup_no_site   | 7.41 ms                                                                | 10.3 ms: 1.39x slower                                                |
| nqueens                  | 79.2 ms                                                                | 113 ms: 1.42x slower                                                 |
| python_startup           | 11.1 ms                                                                | 15.8 ms: 1.43x slower                                                |
| generators               | 29.2 ms                                                                | 42.0 ms: 1.44x slower                                                |
| tomli_loads              | 2.15 sec                                                               | 3.12 sec: 1.45x slower                                               |
| pycparser                | 1.14 sec                                                               | 1.66 sec: 1.46x slower                                               |
| fannkuch                 | 371 ms                                                                 | 544 ms: 1.47x slower                                                 |
| xml_etree_process        | 60.2 ms                                                                | 89.6 ms: 1.49x slower                                                |
| typing_runtime_protocols | 160 us                                                                 | 239 us: 1.49x slower                                                 |
| pylint                   | 272 ms                                                                 | 412 ms: 1.52x slower                                                 |
| deepcopy                 | 266 us                                                                 | 410 us: 1.54x slower                                                 |
| crypto_pyaes             | 67.9 ms                                                                | 105 ms: 1.55x slower                                                 |
| html5lib                 | 66.9 ms                                                                | 104 ms: 1.55x slower                                                 |
| mako                     | 12.0 ms                                                                | 18.9 ms: 1.58x slower                                                |
| genshi_xml               | 50.3 ms                                                                | 79.6 ms: 1.58x slower                                                |
| sqlglot_optimize         | 53.9 ms                                                                | 85.4 ms: 1.59x slower                                                |
| regex_compile            | 135 ms                                                                 | 213 ms: 1.59x slower                                                 |
| sqlglot_normalize        | 108 ms                                                                 | 171 ms: 1.59x slower                                                 |
| 2to3                     | 256 ms                                                                 | 410 ms: 1.60x slower                                                 |
| deepcopy_memo            | 30.3 us                                                                | 48.9 us: 1.61x slower                                                |
| sympy_integrate          | 20.0 ms                                                                | 32.2 ms: 1.61x slower                                                |
| deepcopy_reduce          | 2.65 us                                                                | 4.33 us: 1.63x slower                                                |
| pyflate                  | 448 ms                                                                 | 734 ms: 1.64x slower                                                 |
| comprehensions           | 17.3 us                                                                | 29.2 us: 1.69x slower                                                |
| thrift                   | 752 us                                                                 | 1.28 ms: 1.70x slower                                                |
| django_template          | 35.7 ms                                                                | 61.4 ms: 1.72x slower                                                |
| pprint_safe_repr         | 716 ms                                                                 | 1.24 sec: 1.73x slower                                               |
| pprint_pformat           | 1.48 sec                                                               | 2.57 sec: 1.74x slower                                               |
| genshi_text              | 21.9 ms                                                                | 39.2 ms: 1.79x slower                                                |
| unpickle_pure_python     | 217 us                                                                 | 390 us: 1.80x slower                                                 |
| pickle_pure_python       | 320 us                                                                 | 586 us: 1.83x slower                                                 |
| logging_simple           | 6.30 us                                                                | 11.8 us: 1.87x slower                                                |
| logging_format           | 6.99 us                                                                | 13.1 us: 1.88x slower                                                |
| float                    | 78.8 ms                                                                | 148 ms: 1.88x slower                                                 |
| richards                 | 45.9 ms                                                                | 86.7 ms: 1.89x slower                                                |
| scimark_monte_carlo      | 65.4 ms                                                                | 124 ms: 1.89x slower                                                 |
| logging_silent           | 109 ns                                                                 | 210 ns: 1.92x slower                                                 |
| sympy_str                | 275 ms                                                                 | 530 ms: 1.93x slower                                                 |
| chaos                    | 59.0 ms                                                                | 114 ms: 1.93x slower                                                 |
| hexiom                   | 5.96 ms                                                                | 11.7 ms: 1.96x slower                                                |
| scimark_sor              | 136 ms                                                                 | 266 ms: 1.96x slower                                                 |
| richards_super           | 52.0 ms                                                                | 104 ms: 2.00x slower                                                 |
| sqlglot_transpile        | 1.59 ms                                                                | 3.29 ms: 2.06x slower                                                |
| nbody                    | 95.9 ms                                                                | 199 ms: 2.08x slower                                                 |
| scimark_lu               | 113 ms                                                                 | 235 ms: 2.08x slower                                                 |
| sqlglot_parse            | 1.30 ms                                                                | 2.83 ms: 2.17x slower                                                |
| raytrace                 | 264 ms                                                                 | 581 ms: 2.20x slower                                                 |
| sympy_expand             | 460 ms                                                                 | 1.04 sec: 2.26x slower                                               |
| go                       | 122 ms                                                                 | 295 ms: 2.43x slower                                                 |
| sympy_sum                | 153 ms                                                                 | 377 ms: 2.46x slower                                                 |
| deltablue                | 3.25 ms                                                                | 8.82 ms: 2.71x slower                                                |
| unpack_sequence          | 47.0 ns                                                                | 152 ns: 3.24x slower                                                 |
| bench_thread_pool        | 1.02 ms                                                                | 3.47 ms: 3.41x slower                                                |
| Geometric mean           | (ref)                                                                  | 1.49x slower                                                         |

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.42x
- 95% likely to have a slowdown of 1.40x
- 99% likely to have a slowdown of 1.35x

# Memory
- memory change: 1.21x