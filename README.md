# nagios-plugins-cmadams

These are some useful Nagios monitoring plugins I've written.

## Description

* check_cert: 
    This plugin makes an SSL/TLS connection to the specified server/port,
    validates the cert, and warns/errors on the number of days until the
    cert expires. It can be set to check an RSA or ECDSA cert, and can check
    some types of connections using STARTTLS.

    Required perl modules:
    - Monitoring::Plugin
    - IO::Socket::SSL
    - Socket
    - POSIX

    Optional perl modules (needed for specific protocols):
    - Net::FTP
    - Mail::IMAPClient
    - Net::LDAP
    - Net::POP3
    - Net::SMTP


* check_chrony: 
    This plugin checks the selected chrony NTP server using the
    "chronyc" command line client.

    Required perl modules:
    - Monitoring::Plugin


* check_smtp_msg:
    This plugin makes a connection to an SMTP server, sends a message, and
    checks the result.

    Required perl modules:
    - Monitoring::Plugin
    - Net::SMTP
    - Time::HiRes
    - Sys::Hostname
    - Socket
    - POSIX

    Optional perl modules:
    - Authen::SASL (for authentication)
    - IO::Socket::SSL (for SSL/STARTTLS)


## Notes

These plugins need at least perl 5.16.

## License

This project is licensed under the GNU General Public License (v3.0 only).
