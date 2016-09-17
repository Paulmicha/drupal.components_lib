Components Library
==================

Allows declaring Drupal templates anywhere. For each template, its (default) corresponding hook and theme_hook_suggestions priority must be specified in one of the following formats : .info file (7.x only), [planned] .yml (7.x: with 'parse_yaml' contrib module), or [discuss] .json.

Generic (reusable) components templates should reside in libraries, and specific ones will be scanned for in active theme(s) and/or paths possibly added via hook_components_lib_paths_alter().

See [planned] example component and its documentation for settings and file structure + https://github.com/Paulmicha/css-organization (section "individual components").

**Early work in progress** : data mapping (variables correspondance) still under discussion.

Goals:

- Ease styleguide-based Drupal theming by attempting to use its components directly
- [planned] attached JS integration
- [discuss] ability to require modular CSS or Sass assets from custom themes and/or modules
- [discuss] ability to combine components ? Seems difficult, as it could lead to support or design an entire "parallel" rendering system, on top of Drupal's own render arrays - or : see https://www.drupal.org/node/2702061 (8.x only).

Currently planned complementary (or sub-) modules could offer additional convenient ways to use this :

- [planned] admin UI to override templates settings : match templates to hooks + specify corresponding theme_hook_suggestions priority
- [planned] variables correspondance for reusable components (~'presenter' in Model–view–presenter pattern)
- [planned] UI to select template per field
- [planned] Panel layout preset(s)
- [discuss] Form alter to select template for a single entity
- [discuss] Form alter to select template (+ field formatter settings ?) for a single entity field

Inspired by the following modules :

- Drupal 8 : https://www.drupal.org/project/components
- Drupal 7 : https://www.drupal.org/sandbox/JamesOakley/1976492 (library_templates)
- Drupal 7 : https://www.drupal.org/project/template_picker

Note on potential future 8.x work :
If these functionnalities aren't already implemented in other modules, each might be designed as separate modules depending on the existing 'components' contrib module.
