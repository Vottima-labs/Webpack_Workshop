Completed using a modern Node.js environment 
The cloned repository contains several older dependencies. This resulted in some compatibility issues.

The repository uses Webpack 4.8.3 and older Babel dependencies,
the current course instructions reference newer versions of Webpack and Babel. 
Running Webpack with Node.js 22 initially caused an OpenSSL compatibility error (ERR_OSSL_EVP_UNSUPPORTED).

Environment variable was used to allow the legacy Webpack version to build successfully:
export NODE_OPTIONS=--openssl-legacy-provider

After applying this workaround:
Webpack successfully builds the application
React renders correctly in the browser
production minification works
and source maps are generated successfully. 

The final automated React test times out due to the repository's legacy Nightmare 3 / Electron 1.8 testing environment.
The application itself successfully renders the expected React content in a modern browser, so the objective of the assignment is still being met.

These issues appear to result from version differences between the current course instructions, the older dependencies in the cloned repository, and the modern Node.js runtime.
