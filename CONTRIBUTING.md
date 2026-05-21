# Contributing / Вклад в проект

English version below ↓

---

## Русский

Спасибо, что хотите улучшить библиотеку! Любые вклады приветствуются — баг-репорты, предложения, PR.

### Подготовка окружения

```bash
git clone https://github.com/artemydottech/daterly.git
cd daterly
npm install
```

Репозиторий — npm-workspace: корень (библиотека) и `docs/` (сайт документации на Next.js).

### Команды

```bash
npm run dev            # watch-сборка библиотеки → dist/
npm run test           # тесты (vitest)
npm run test:watch     # тесты в watch-режиме
npm run test:coverage  # тесты с покрытием
npm run test:e2e       # e2e-тесты компонентов (playwright)
npm run build          # production-сборка → dist/
npm run size           # замер размера бандла (size-limit)
npm -w docs run dev    # локальный сайт документации
```

### Процесс отправки PR

1. Форкните репозиторий и создайте ветку от `main`:
   ```bash
   git checkout -b fix/my-bug-fix
   ```
2. Внесите изменения. Новую функциональность покройте тестами; при изменении API обновите документацию в `docs/`.
3. Убедитесь, что тесты проходят: `npm run test` (и `npm run test:e2e`, если затронуты компоненты).
4. Откройте Pull Request с описанием что и зачем изменено.

### Стиль коммитов

Используем [Conventional Commits](https://www.conventionalcommits.org/):

```
feat(DatePicker): add customInput prop
fix(mask): handle backspace at separator position
docs: update README examples
```

### Релиз

Релизами занимается мейнтейнер. Если ваш PR влечёт изменение версии, опишите это в теле PR — мейнтейнер создаст changeset сам.

---

## English

Thank you for your interest in contributing! Bug reports, suggestions, and pull requests are all welcome.

### Setup

```bash
git clone https://github.com/artemydottech/daterly.git
cd daterly
npm install
```

The repository is an npm workspace: the root (library) and `docs/` (the Next.js documentation site).

### Scripts

```bash
npm run dev            # library watch build → dist/
npm run test           # run tests (vitest)
npm run test:watch     # tests in watch mode
npm run test:coverage  # tests with coverage
npm run test:e2e       # component e2e tests (playwright)
npm run build          # production build → dist/
npm run size           # bundle size check (size-limit)
npm -w docs run dev    # documentation site locally
```

### Submitting a PR

1. Fork the repository and create a branch from `main`:
   ```bash
   git checkout -b fix/my-bug-fix
   ```
2. Make your changes. Cover new features with tests; update the docs in `docs/` when the API changes.
3. Make sure tests pass: `npm run test` (and `npm run test:e2e` if components are affected).
4. Open a Pull Request describing what changed and why.

### Commit style

We use [Conventional Commits](https://www.conventionalcommits.org/):

```
feat(DatePicker): add customInput prop
fix(mask): handle backspace at separator position
docs: update README examples
```

### Releases

Releases are managed by the maintainer. If your PR warrants a version bump, describe the nature of the change in the PR body — the maintainer will create the changeset.
