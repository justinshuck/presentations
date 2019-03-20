# monorepos

> presented by: **justin shuck**

> **justin.shuck@walmartlabs.com**

3/20/2019


---

### what are they?

---

### what are they?
> A collection of packages all stored in a single repo

```
my-mono-repo
├─ .git/
├─ packages/
│  ├─ project-a
│  │    └─ package.json
│  ├─ project-b
│  │    └─ package.json
│  ├─ project-c
│       └─ package.json
├─ package.json
```


---

## examining advantages and disadvantages of monorepos
---

### advantages 💁

* code reuse
* dependency reuse
* organization
* cross-cutting changes
    * ex: FE & BE could work on same feature branch
* uniformity across tooling, including
    * publishing/releasing
    * commiting
* collaboration

---

### disadvantages 🤦‍

* scalability
* potential coupling of packages
* upkeep in CI/CD pipeline


---

### mitigating disadvantages

* scalability
    * **can break down pipeline to focus on specific sub-packages**
* potential coupling of packages
    * **architecture review on new packages**
* upkeep in CI/CD pipeline
    * **tools exist to assist in the upkeep**

---

### tools 🛠 and packages 📦

---
## bazel

`> Build and test software of any size, quickly and reliably`



* https://github.com/bazelbuild/bazel
* developed by Google
* cross-platform
* multi-language support
    * JavaScript, Java, C++, android, iOS, Go

---
## lerna
`> A tool for managing JavaScript projects with multiple packages.`
* https://github.com/lerna/lerna/
* cross-dependency management
    * available in top level `node_modules`
* cross-project execution
    * ex: can run `yarn test` in each package
* release & publishing support
* simple configuration

---
### usuage and opportunity for your projects