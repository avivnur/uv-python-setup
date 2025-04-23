# `uv` python setup
`uv` `python` setup for data science project. Untuk dokumentasi pribadi.

## First Setup
Pada terminal, initialisasi project menggunakan command berikut:

```
$ uv init <nama-folder>
```

contoh:

```
$ uv init first-project
```

Selanjutnya, silahkan berpindah ke folder `first-project`, dengan menggunakan command berikut:

```
$ cd first-project
```

## Using `uv` with Jupyter

Direkomendasikan untuk membuat kernel terlebih dahulu sebelum menggunakan `jupyter notebook` agar setiap package yang digunakan terdokumentasi dengan baik pada uv environment.
Untuk membuat kernel, install `ipykernel` dengan comman berikut:

```
$ uv add --dev ipykernel
```

Untuk membuat kernel untuk `first-project`, gunakan command berikut:

```
$ uv run ipython kernel install --user --env VIRTUAL_ENV $(pwd)/.venv --name=first-project
```
Catatan: nama kernel bebas, tidak harus sesuai dengan nama folder project.

Selanjutnya, mulai server dengan:

```
$ uv run --with jupyter jupyter lab
```

## Install `python`

Untuk menginstall versi `python` yang terbaru:

```
$ uv python install
```

Untuk menginstall versi `python` yang spesifik:

```
$ uv python install 3.10
```

Untuk melihat versi `python` yang tersedia dan telah terinstall:

```
$ uv python list
```

## Menambahkan dependency

Untuk menambahkan dependency, gunakan command berikut:

```
$ uv add pandas numpy matplotlib scikit-learn
```

Untuk mengimpor dependency dalam sebuah file `requirements.txt`

```
$ uv add -r requirements.txt
```

Thank You.
