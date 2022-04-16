# Gentoo specific Nagios/Icinga/Monitoring plugins

[![perlcritic](https://github.com/antonfischl1980/monitoring-plugins-gentoo/actions/workflows/perlcritic.yml/badge.svg)](https://github.com/antonfischl1980/monitoring-plugins-gentoo/actions/workflows/perlcritic.yml)
![GitHub all releases](https://img.shields.io/github/downloads/antonfischl1980/monitoring-plugins-gentoo/total)

This repository started as an import of 2 checks from https://github.com/Flameeyes/nagios-plugins-flameeyes .

I will maintain these check-plugins and add new gentoo-specific checks when the need arises.

Please feel free to fork and send pull request for any enhancement or fix you come up with.

### License

Each plugin will provide its own license header to make it clear under which license it's released under. Most of them you'll see having a MIT license, which basically is an all-permissive license. If different licenses are used, it's usually because the plugin is derived from another one that was published under a different license.

### Dependencies
All Perl-based plugins will require Monitoring::Plugin at the very least, as that implements the basic Nagios API in a flexible way.

    check_openrc.pl
        openrc itself ( sys-apps/openrc )
        Monitoring::Plugin ( dev-perl/Monitoring-Plugin )
    check_portage_age.pl
        Date::Parse ( dev-perl/TimeDate )
        Time::Duration ( dev-perl/Time-Duration )
        Monitoring::Plugin ( dev-perl/Monitoring-Plugin )

### Installation
the newest ebuild will be published in my [icinga-Overlay](https://github.com/antonfischl1980/icinga/)

    emerge app-eselect/eselect-repository
    eselect repository enable icinga
    emerge --sync
    emerge net-analyzer/monitoring-plugins-gentoo

If you insist on installing it manually:
- make sure to have the dependencies installed


      cp -a *.pl /usr/lib64/nagios/plugins/
      cp -a *.conf /usr/share/icinga2/include/plugins-contrib.d/

### Thanks
[@Flameeyes](https://github.com/Flameeyes) for writing these checks almost 10 years ago
