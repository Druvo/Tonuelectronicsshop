

   --------------------------------------------------------------------------------
               README file for Bundle Transformer: Autoprefixer v1.12.1

   --------------------------------------------------------------------------------

           Copyright (c) 2012-2019 Andrey Taritsyn - http://www.taritsyn.ru


   ===========
   DESCRIPTION
   ===========
   BundleTransformer.Autoprefixer contains one postprocessor-adapter for
   postprocessing of CSS code - `AutoprefixCssPostProcessor`.
   This adapter makes actualization of vendor prefixes in CSS code by using the
   Autoprefixer Host for .NET (https://github.com/Taritsyn/AutoprefixerHost)
   version 1.0.2 (supports the Andrey Sitnik's Autoprefixer
   (https://github.com/postcss/autoprefixer) version 9.6.1.1).

   As a JS engine is used the JavaScript Engine Switcher library
   (https://github.com/Taritsyn/JavaScriptEngineSwitcher).

   =============
   RELEASE NOTES
   =============
   Added support of the Autoprefixer version 9.6.1.1.

   ====================
   POST-INSTALL ACTIONS
   ====================
   For correct working of this module, you need to install one of the following
   NuGet packages: JavaScriptEngineSwitcher.Msie (only in the Chakra JsRT modes),
   JavaScriptEngineSwitcher.V8 or JavaScriptEngineSwitcher.ChakraCore.
   After package is installed and JS engine is registered
   (https://github.com/Taritsyn/JavaScriptEngineSwitcher/wiki/Registration-of-JS-engines),
   need set a name of JS engine (for example, `MsieJsEngine`) to the `name`
   attribute of `/configuration/bundleTransformer/autoprefixer/jsEngine`
   configuration element in the `Web.config` file.

   To make `AutoprefixCssPostProcessor` is one of the default CSS postprocessors,
   you need to make changes to the `Web.config` file. 
   In the `defaultPostProcessors` attribute of
   `/configuration/bundleTransformer/core/css` element must be add
   `AutoprefixCssPostProcessor` to end of comma-separated list (for example,
   `UrlRewritingCssPostProcessor,AutoprefixCssPostProcessor`).

   =============
   DOCUMENTATION
   =============
   See documentation on GitHub - https://github.com/Taritsyn/BundleTransformer/wiki