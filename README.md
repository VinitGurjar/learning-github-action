# learning-github-action
### How I created an Automated task
To use github actions I do the following:
1. Create an folder `.github` then create another folder inside it `workflows` and create a yaml file inside it like `build.yml`.
2. Then I write this yaml code inside build.yml file:

  ```yml
   name: Build
on: [push]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - uses: actions/setup-node@v3
        with: 
          node-version: '17'
      - run: node index.js
  ```
3. After commiting the task are automated by github action, here an screenshot of this sucssesful build -

    
   ![Update build yml · VinitGurjar_learning-github-action@1f25759 - Brave 26-06-2023 16_51_54](https://github.com/VinitGurjar/learning-github-action/assets/97173586/7e3b63a1-b3ee-4003-bfe3-8dfb9b2f5e87)
