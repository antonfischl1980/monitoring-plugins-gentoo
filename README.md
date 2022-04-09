# Gentoo specific Nagios/Icinga/Monitoring plugins

This repository started as an import of 2 checks from https://github.com/Flameeyes/nagios-plugins-flameeyes .

I will maintain these check-plugins and add new gentoo-specific checks when the need arises.

Please feel free to fork and send pull request for any enhacement or fix you come up with.

### License

Each plugin will provide its own license header to make it clear under which license it's released under. Most of them you'll see having a MIT license, which basically is an all-permissive license. If different licenses are used, it's usually because the plugin is derived from another one that was published under a different license.
Dependencies

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

### Thanks
[@Flameeyes](https://github.com/Flameeyes) for writing these checks almost 10 years ago
