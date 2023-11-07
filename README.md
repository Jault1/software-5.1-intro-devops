# software-5.1-intro-devops
Describe Angular (NG) Message Format
(i18n)
This feature is available since Angular 1.4

Pluralization, localization, and Gender Selection

Pluralization exapmple:
<ng-pluralize count="numberOfMessages"
              when="{'1': 'You have one new message.',
                     'other': 'You have {} new messages.'}">
</ng-pluralize>
=======================
$ npm install angular-message-format
Once installed and included in our HTML document, we can add it as a module dependency and start using it right away!

angular.module('myApp', ['ngMessageFormat']);
========================
{{EXPRESSION, TYPE,
     =VALUE { MESSAGE }
     ...
}}
========================
{{numberOfMessages, plural,
    =0 { You have no new messages }
    =1 { You have one new message }
    other { You have # new messages }
}}
========================
Gender selection with ngMessageFormat

Gender selection uses the exact same syntax. All we have to do is to change the selection type and define messages for each gender:

{{genderExpression, select,
    male { Send him a message. }
    female { Send her a message. }
    other { Send them a message. }
}}