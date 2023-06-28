[fork]: https://github.com/KitetsuK/TemplateC-Cpp/fork
[pr]: https://github.com/KitetsuK/TemplateC-Cpp/compare
[style]: https://intra.epitech.eu/file/Public/technical-documentations/C/epitech_c_coding_style.pdf
[doc-codeQL]: https://docs.github.com/en/code-security/code-scanning/using-codeql-code-scanning-with-your-existing-ci-system/about-codeql-code-scanning-in-your-ci-system

# CONTRIBUTING

Here is the instructions if you want to contribute to the project

## Submitting a pull request

1. [Fork][fork] and clone the repository
2. Create a new branch: `git checkout -b my-branch-name`
3. Make your change, add tests, and make sure the tests still pass
4. Make sure that the code is codeQL compliant
5. Make sure that you had documentation to the new added code (obviously compliant with our doc)
6. Push to your fork and [submit a pull request][pr] with correct labels added if necessary
7. Pat your self on the back and wait for your pull request to be reviewed and merged.

Here are a few things you can do that will increase the likelihood of your pull request being accepted:

- The security of your code is analysed by [codeQL][doc-codeQL] the CI might fail if it's not secure.  
  Warning ! Only cpp will be analysed
- You must see [epitech coding style][style] and respect it.  
  Warning ! If your code is not epitech coding style compliant your CI will fail and your pr will be refused.
- Write tests.
- Keep your change as focused as possible.  
  If there are multiple changes you would like to make that are not dependent upon each other, consider submitting them as separate pull requests.
- Write a commit message that respect the commit norm that you have set up.
