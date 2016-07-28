# Ember Components Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  Give an example of a visual hierarchy that could be modeled with components.

    ```md
    A magazine application. The nav bar could be in one component and then there could be a two main components one with the newest news articles and one with blog articles. In the blog article could be another component for comments.
    ```

1.  What is the command to generate a new component called '`my-map`'?

    ```sh
    ember g component my-map
    ```

1.  What files are edited to produce a component, and what are their
    responsibilities?

    ```md
    component.js : determines functionality of webpag, place to put javascript to interact with your webpage
    template.hbs :  determines what should be displayed in component
    ```

1.  Suppose you have a component '`my-contact`', which is loaded from
    '`app/contacts/template.hbs`' when visiting the `/contacts` path. What is
    the syntax for loading this component inside that template?

    ```html
    {{outlet}}
    ```

  4. Each contact has multiple phone numbers. Suppose you also have '`my-phone`'
    nested under '`my-contact`'. What is the code you would write in
    '`app/components/my-contact/template.hbs`' to load the nested component and
    pass it data?

    ```html
    {{outlet}}

    <h2> My Contacts </h2>
    <ul>
    {{#each model as |tel|}}

    <h4> {{#link-to 'tel' tel}} {{tel.number}}{{/link-to}}</h4>

    {{/each}}
    </ul>

    ```
