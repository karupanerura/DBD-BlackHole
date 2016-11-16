# NAME

DBD::BlackHole - NULL database driver for DBI

# SYNOPSIS

    use DBI;

    my $dbh = DBI->connect('dbi:BlackHole:', undef, undef); # always successful

    $dbh->do('INSERT INTO my_table (val) VALUES (?)', undef, 'value'); # always successful

    my $rows = $dbh->selectall_arrayref('SELECT * FROM my_table'); # always returns empty arrayref

# DESCRIPTION

DBD::BlackHole is a null database driver for DBI.

This module dosen't parse/execute any query, and it fetches a empty result always.

# LICENSE

Copyright (C) karupanerura.

This library is free software; you can redistribute it and/or modify
it under the same terms as Perl itself.

# AUTHOR

karupanerura <karupa@cpan.org>
