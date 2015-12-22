# buffy
A reporting tool for the Bacula backup program.

buffy generates Bacula reports in a highly flexible manner.  In addition,
some values can be expressed in Nagios performance data format.

	Usage:buffy [date] [query target] [query type] [extra]

		Where:[date] is one or more of: 	
		--date=(is the 24 hours within given date)
		--sdate= Dates in month/day/year format
		--edate= Dates in month/day/year format
		--sdate_days= Start in terms of "days" ago
		--edate_days= End in terms of "days" ago
		--since_full(for host only)
		Date is optional for the host query target.  If there 
		is no date specified status will be based on data since
		the beginning of TODAY.

		Where:[query target] is one of:
		--group= Name of catalogue, default is ECI
		--host=

		Where:[query type] is one or more of:
		--report
		--failures=days	Displays a listing of hosts that have failed for 
			'days' number or greater days.
		--status - Provides stat_last, stat_last_full, and stat_successrate
		  --stat_last_full(for host only)
		  --stat_list_fulls(for host only)
		  --stat_last(for host only) 
       		  --stat_successrate A percentage of successful backups done specified
			time frame.  Supports Nagios output.
 		--expansion(default all below)
       		  --excount Growth rate of the file count for date range specified
			Supports Nagios output
       		  --exsize Growth rate of the file size for date range specified
			Supports Nagios output
 		--files(default all below)
		  --no_fulls Don't include fulls in calculations for options below
       		  --fcount File count. Supports Nagios output
       		  --fsize File size.  Supports Nagios output
       		  --faverage_count Average file count across backups
       		  --faverage_size Average file size across backups
       		  --frank(host only, both count and size, for ranking in group)
       		  --frank_count(host only, for ranking in group)
       		  --frank_size(host only, for ranking in group)
       		  --fpercent_count(host only, percentage of group total)
       		  --fpercent_size(host only, percentage of group total)
		
		Where:[extra] is one of:
		--debug
		--nagios 	Spits out data in Nagios performance data friendly format
		--nagiosW 	Nagios warn level, reports in performance data friendly format
		--nagiosC 	Nagios critical level, reports in performance data friendly format

