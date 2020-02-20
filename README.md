# TimezoneAwareTimedRotatingFileHandler
For python logging, a TimedRotatingFileHandler that obeys time zones.  If the added tzinfo parameter is specified (as a pytz.timezone), the utc parameter is ignored.  The atTime parameter can be specified and is obeyed in the specified time zone.

Usage:

    import pytz
    from timezoneawarefilehandler import TimezoneAwareTimedRotatingFileHandler
    central = pytz.timezone("America/Chicago")
    central_handler = TimezoneAwareTimedRotatingFileHandler('mylog', when='midnight',
                                                        backupCount=30, tzinfo=central)
