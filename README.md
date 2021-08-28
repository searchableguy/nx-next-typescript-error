# Nx Next Typescript Error

When running pnpm build, the generated package.json for web at `./dist/apps/web` doesn't include typescript in dependencies even though it seems to be required for running the app by @nrwl/next package.

## Reproduction Steps

1. Clone the repo.

```sh
git clone git@github.com:searchableguy/nx-next-typescript-error.git
```

2. Go inside the repo and run install.

```sh
cd nx-next-typescript-error
pnpm install
```

3. Build.

```sh
pnpm build
```

4. Use docker to generate image and run it

```sh
docker build -f ./apps/web/Dockerfile . -t nx-next-typescript-error
docker run nx-next-typescript-error
```

This should result in an error posted in error.log file inside this repo.
