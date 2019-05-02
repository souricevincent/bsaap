---
title: Contact
slug: contact
form:
    name: contact
    fields:
        name:
            classes: uk-input
            outerclasses: uk-margin
            label: Name
            placeholder: 'Enter your name'
            autocomplete: 'on'
            type: text
            class: super
            validate:
                required: true
        email:
            classes: uk-input
            outerclasses: uk-margin
            label: Email
            placeholder: 'Enter your email address'
            type: email
            validate:
                required: true
        message:
            classes: uk-textarea
            outerclasses: uk-margin
            label: Message
            placeholder: 'Enter your message'
            type: textarea
            validate:
                required: true
    buttons:
        reset:
            classes: 'uk-button uk-button-secondary'
            type: reset
            value: Reset
        submit:
            classes: 'uk-button uk-button-default uk-margin-left'
            type: submit
            value: Submit
    process:
        save:
            fileprefix: contact-
            dateformat: Ymd-His-u
            extension: txt
            body: '{% include ''forms/data.txt.twig'' %}'
        email:
            subject: '[Site Contact Form] {{ form.value.name|e }}'
            body: '{% include ''forms/data.html.twig'' %}'
        message: 'Merci pour votre message !'
        display: thankyou
---

Information de contact ici
