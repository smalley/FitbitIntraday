FitbitIntraday
==============

Notes
-----

This utility is not currently mature and as such its interface may change dramatically between versions. This interface should stabilize within a few days and this not will be updated accordingly. Users are further advised that this utility does not yet implement many data checks or exception handlers and thus may not be sufficiently robust.

Sample Usage
------------
    from datetime import datetime
    from FitbitIntraday import FitbitIntraday
    
    fbi = FitbitIntraday()
    
    fbi.login('example_fitbitemail@example.com','example_password')
    
    start_day = datetime(2013,5,1)
    end_day = start_day + timedelta(days=7)
    folder_path = '/my/path/here'
    
    fbi.fetch_range_to_folder('calories',folder_path,start_day,end_day)
    fbi.fetch_range_to_folder('steps',folder_path,start_day,end_day)
    fbi.fetch_range_to_folder('floors',folder_path,start_day,end_day)
    fbi.fetch_range_to_folder('time_active',folder_path,start_day,end_day)
