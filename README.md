# Alien::patch

Find or build patch

# SYNOPSIS

    use Alien::patch;
    # patch should now be in your PATH if it wasn't already

# DESCRIPTION

Many environments provide the patch command, but a few do not.
Using this module in your `Build.PL` (or elsewhere) you can
make sure that patch will be available.  If the system provides
it, then great, this module is a no-op.  If it does not, then
it will download and install it into a private location so that
it can be added to the `PATH` when this module is used.

# METHODS

## exe

    my $exe = Alien::patch->exe;

Returns the command to run patch on your system.  For now it simply
adds the `--binary` option on Windows (`MSWin32` but not `cygwin`)
which is usually what you want.

# AUTHOR

Graham Ollis <plicease@cpan.org>

# COPYRIGHT AND LICENSE

This software is copyright (c) 2014 by Graham Ollis.

This is free software; you can redistribute it and/or modify it under
the same terms as the Perl 5 programming language system itself.
