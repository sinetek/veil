Veil version 1.0.0.0 is now available from:

  <https://veil-project.com/get-started/>

This is a new major version release, including new features, various bugfixes
and performance improvements, as well as updated translations.

Please report bugs using the issue tracker at GitHub:

  <https://github.com/Veil-Project/veil/issues>


Notable changes
===============


1.0.0.0 change log
===================

XXX change log
==============

`listtransactions` label support
--------------------------------

The `listtransactions` RPC `account` parameter which was deprecated in 0.17.0
and renamed to `dummy` has been un-deprecated and renamed again to `label`.

When bitcoin is configured with the `-deprecatedrpc=accounts` setting, specifying
a label/account/dummy argument will return both outgoing and incoming
transactions. Without the `-deprecatedrpc=accounts` setting, it will only return
incoming transactions (because it used to be possible to create transactions
spending from specific accounts, but this is no longer possible with labels).

When `-deprecatedrpc=accounts` is set, it's possible to pass the empty string ""
to list transactions that don't have any label. Without
`-deprecatedrpc=accounts`, passing the empty string is an error because returning
only non-labeled transactions is not generally useful behavior and can cause
confusion.

Credits
=======


