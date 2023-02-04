# nagios-plugins-cmadams

These are some useful Nagios monitoring plugins I've written.

## Description

* check_cert: 
	This plugin makes an SSL/TLS connection to the specified server/port,
	validates the cert, and warns/errors on the number of days until the
	cert expires. It can be set to check an RSA or ECDSA cert, and can check
	some types of connections using STARTTLS.

* check_chrony: 
	This plugin checks the selected chrony NTP server

* check_smtp_msg:
	This plugin makes a connection to an SMTP server, sends a message, and
	checks the result.

## Notes

These plugins need at least perl 5.26.

## License

This project is licensed under the GNU General Public License (v3.0 only).
