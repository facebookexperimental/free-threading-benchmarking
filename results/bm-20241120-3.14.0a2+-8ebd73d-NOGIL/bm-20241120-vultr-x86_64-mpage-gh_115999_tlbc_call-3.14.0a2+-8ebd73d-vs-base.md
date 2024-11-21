# Results vs. base

- fork: mpage
- ref: gh_115999_tlbc_call
- machine: linux-x86_64
- commit hash: 8ebd73d
- commit date: 2024-11-20
- overall geometric mean: 1.03x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2+-32428cf | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 414 ms                                                                 | 410 ms: 1.01x faster                                                 |
| docutils       | 3.35 sec                                                               | 3.28 sec: 1.02x faster                                               |
| html5lib       | 106 ms                                                                 | 104 ms: 1.02x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2+-32428cf | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|--------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| coroutines         | 30.4 ms                                                                | 28.6 ms: 1.06x faster                                                |
| asyncio_websockets | 520 ms                                                                 | 523 ms: 1.00x slower                                                 |
| Geometric mean     | (ref)                                                                  | 1.01x faster                                                         |

Benchmark hidden because not significant (3): asyncio_tcp_ssl, asyncio_tcp, async_generators

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2+-32428cf | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 187 ms                                                                 | 182 ms: 1.03x faster                                                 |
| float          | 150 ms                                                                 | 148 ms: 1.01x faster                                                 |
| nbody          | 195 ms                                                                 | 199 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2+-32428cf | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_compile  | 230 ms                                                                 | 213 ms: 1.08x faster                                                 |
| regex_dna      | 193 ms                                                                 | 186 ms: 1.04x faster                                                 |
| regex_v8       | 25.5 ms                                                                | 24.9 ms: 1.03x faster                                                |
| regex_effbot   | 2.88 ms                                                                | 2.82 ms: 1.02x faster                                                |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2+-32428cf | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| unpickle_pure_python | 421 us                                                                 | 390 us: 1.08x faster                                                 |
| pickle_pure_python   | 616 us                                                                 | 586 us: 1.05x faster                                                 |
| pickle_list          | 5.15 us                                                                | 4.93 us: 1.04x faster                                                |
| xml_etree_process    | 93.4 ms                                                                | 89.6 ms: 1.04x faster                                                |
| xml_etree_generate   | 114 ms                                                                 | 109 ms: 1.04x faster                                                 |
| xml_etree_iterparse  | 109 ms                                                                 | 105 ms: 1.04x faster                                                 |
| tomli_loads          | 3.20 sec                                                               | 3.12 sec: 1.03x faster                                               |
| xml_etree_parse      | 133 ms                                                                 | 132 ms: 1.01x faster                                                 |
| json_loads           | 28.7 us                                                                | 28.4 us: 1.01x faster                                                |
| json_dumps           | 15.0 ms                                                                | 15.0 ms: 1.00x faster                                                |
| pickle_dict          | 31.9 us                                                                | 31.9 us: 1.00x faster                                                |
| unpickle_list        | 5.02 us                                                                | 5.11 us: 1.02x slower                                                |
| Geometric mean       | (ref)                                                                  | 1.02x faster                                                         |

Benchmark hidden because not significant (2): unpickle, pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2+-32428cf | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 15.8 ms                                                                | 15.8 ms: 1.00x slower                                                |
| python_startup_no_site | 10.3 ms                                                                | 10.3 ms: 1.00x slower                                                |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2+-32428cf | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 20.7 ms                                                                | 18.9 ms: 1.10x faster                                                |
| django_template | 64.6 ms                                                                | 61.4 ms: 1.05x faster                                                |
| genshi_xml      | 82.6 ms                                                                | 79.6 ms: 1.04x faster                                                |
| genshi_text     | 40.6 ms                                                                | 39.2 ms: 1.04x faster                                                |
| Geometric mean  | (ref)                                                                  | 1.06x faster                                                         |

All benchmarks:
===============

| Benchmark                | bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2+-32428cf | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|--------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako                     | 20.7 ms                                                                | 18.9 ms: 1.10x faster                                                |
| raytrace                 | 632 ms                                                                 | 581 ms: 1.09x faster                                                 |
| deepcopy_memo            | 53.0 us                                                                | 48.9 us: 1.09x faster                                                |
| bpe_tokeniser            | 6.16 sec                                                               | 5.68 sec: 1.08x faster                                               |
| unpickle_pure_python     | 421 us                                                                 | 390 us: 1.08x faster                                                 |
| regex_compile            | 230 ms                                                                 | 213 ms: 1.08x faster                                                 |
| sqlglot_normalize        | 183 ms                                                                 | 171 ms: 1.07x faster                                                 |
| chaos                    | 122 ms                                                                 | 114 ms: 1.07x faster                                                 |
| pprint_safe_repr         | 1.32 sec                                                               | 1.24 sec: 1.07x faster                                               |
| coroutines               | 30.4 ms                                                                | 28.6 ms: 1.06x faster                                                |
| pprint_pformat           | 2.74 sec                                                               | 2.57 sec: 1.06x faster                                               |
| spectral_norm            | 163 ms                                                                 | 153 ms: 1.06x faster                                                 |
| sqlglot_optimize         | 90.5 ms                                                                | 85.4 ms: 1.06x faster                                                |
| hexiom                   | 12.3 ms                                                                | 11.7 ms: 1.06x faster                                                |
| fannkuch                 | 573 ms                                                                 | 544 ms: 1.05x faster                                                 |
| django_template          | 64.6 ms                                                                | 61.4 ms: 1.05x faster                                                |
| pyflate                  | 772 ms                                                                 | 734 ms: 1.05x faster                                                 |
| typing_runtime_protocols | 252 us                                                                 | 239 us: 1.05x faster                                                 |
| pickle_pure_python       | 616 us                                                                 | 586 us: 1.05x faster                                                 |
| deepcopy                 | 431 us                                                                 | 410 us: 1.05x faster                                                 |
| comprehensions           | 30.6 us                                                                | 29.2 us: 1.05x faster                                                |
| pickle_list              | 5.15 us                                                                | 4.93 us: 1.04x faster                                                |
| richards_super           | 108 ms                                                                 | 104 ms: 1.04x faster                                                 |
| xml_etree_process        | 93.4 ms                                                                | 89.6 ms: 1.04x faster                                                |
| scimark_lu               | 245 ms                                                                 | 235 ms: 1.04x faster                                                 |
| xml_etree_generate       | 114 ms                                                                 | 109 ms: 1.04x faster                                                 |
| xml_etree_iterparse      | 109 ms                                                                 | 105 ms: 1.04x faster                                                 |
| deepcopy_reduce          | 4.50 us                                                                | 4.33 us: 1.04x faster                                                |
| genshi_xml               | 82.6 ms                                                                | 79.6 ms: 1.04x faster                                                |
| regex_dna                | 193 ms                                                                 | 186 ms: 1.04x faster                                                 |
| genshi_text              | 40.6 ms                                                                | 39.2 ms: 1.04x faster                                                |
| deltablue                | 9.13 ms                                                                | 8.82 ms: 1.04x faster                                                |
| richards                 | 89.7 ms                                                                | 86.7 ms: 1.03x faster                                                |
| nqueens                  | 116 ms                                                                 | 113 ms: 1.03x faster                                                 |
| meteor_contest           | 139 ms                                                                 | 135 ms: 1.03x faster                                                 |
| logging_simple           | 12.1 us                                                                | 11.8 us: 1.03x faster                                                |
| pycparser                | 1.71 sec                                                               | 1.66 sec: 1.03x faster                                               |
| scimark_fft              | 415 ms                                                                 | 404 ms: 1.03x faster                                                 |
| tomli_loads              | 3.20 sec                                                               | 3.12 sec: 1.03x faster                                               |
| regex_v8                 | 25.5 ms                                                                | 24.9 ms: 1.03x faster                                                |
| pidigits                 | 187 ms                                                                 | 182 ms: 1.03x faster                                                 |
| sympy_integrate          | 33.1 ms                                                                | 32.2 ms: 1.03x faster                                                |
| crypto_pyaes             | 108 ms                                                                 | 105 ms: 1.03x faster                                                 |
| docutils                 | 3.35 sec                                                               | 3.28 sec: 1.02x faster                                               |
| coverage                 | 102 ms                                                                 | 99.9 ms: 1.02x faster                                                |
| regex_effbot             | 2.88 ms                                                                | 2.82 ms: 1.02x faster                                                |
| sympy_expand             | 1.06 sec                                                               | 1.04 sec: 1.02x faster                                               |
| sympy_str                | 540 ms                                                                 | 530 ms: 1.02x faster                                                 |
| scimark_monte_carlo      | 126 ms                                                                 | 124 ms: 1.02x faster                                                 |
| sqlite_synth             | 2.44 us                                                                | 2.39 us: 1.02x faster                                                |
| logging_format           | 13.4 us                                                                | 13.1 us: 1.02x faster                                                |
| html5lib                 | 106 ms                                                                 | 104 ms: 1.02x faster                                                 |
| xml_etree_parse          | 133 ms                                                                 | 132 ms: 1.01x faster                                                 |
| sqlglot_transpile        | 3.33 ms                                                                | 3.29 ms: 1.01x faster                                                |
| scimark_sor              | 269 ms                                                                 | 266 ms: 1.01x faster                                                 |
| sqlglot_parse            | 2.86 ms                                                                | 2.83 ms: 1.01x faster                                                |
| mdp                      | 3.16 sec                                                               | 3.12 sec: 1.01x faster                                               |
| float                    | 150 ms                                                                 | 148 ms: 1.01x faster                                                 |
| json_loads               | 28.7 us                                                                | 28.4 us: 1.01x faster                                                |
| 2to3                     | 414 ms                                                                 | 410 ms: 1.01x faster                                                 |
| go                       | 298 ms                                                                 | 295 ms: 1.01x faster                                                 |
| sympy_sum                | 381 ms                                                                 | 377 ms: 1.01x faster                                                 |
| logging_silent           | 212 ns                                                                 | 210 ns: 1.01x faster                                                 |
| dulwich_log              | 104 ms                                                                 | 103 ms: 1.01x faster                                                 |
| bench_mp_pool            | 70.2 ms                                                                | 69.7 ms: 1.01x faster                                                |
| bench_thread_pool        | 3.49 ms                                                                | 3.47 ms: 1.01x faster                                                |
| pathlib                  | 22.1 ms                                                                | 22.0 ms: 1.01x faster                                                |
| json_dumps               | 15.0 ms                                                                | 15.0 ms: 1.00x faster                                                |
| pickle_dict              | 31.9 us                                                                | 31.9 us: 1.00x faster                                                |
| python_startup           | 15.8 ms                                                                | 15.8 ms: 1.00x slower                                                |
| python_startup_no_site   | 10.3 ms                                                                | 10.3 ms: 1.00x slower                                                |
| asyncio_websockets       | 520 ms                                                                 | 523 ms: 1.00x slower                                                 |
| scimark_sparse_mat_mult  | 5.81 ms                                                                | 5.85 ms: 1.01x slower                                                |
| unpickle_list            | 5.02 us                                                                | 5.11 us: 1.02x slower                                                |
| nbody                    | 195 ms                                                                 | 199 ms: 1.02x slower                                                 |
| generators               | 40.8 ms                                                                | 42.0 ms: 1.03x slower                                                |
| unpack_sequence          | 136 ns                                                                 | 152 ns: 1.12x slower                                                 |
| Geometric mean           | (ref)                                                                  | 1.03x faster                                                         |

Benchmark hidden because not significant (11): pylint, unpickle, thrift, asyncio_tcp_ssl, telco, create_gc_cycles, asyncio_tcp, async_generators, json, gc_traversal, pickle

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.00x