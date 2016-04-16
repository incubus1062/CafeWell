set {StartDate, EndDate, amt} to {"1/1/2016", "3/22/2016", 1}

set dd to ((date EndDate) - (date StartDate)) div days

repeat with n from 0 to dd
	set dt to (date StartDate) + (n * days)
	set dth to day of dt & "/" & (month of dt as integer) & "/" & year of dt
	set dtv to (month of dt as integer) & "/" & day of dt & "/" & year of dt
	
	tell application "Safari" to tell document 1
		do JavaScript "document.getElementsByName('user_challenge_progress[activity_date]')[0].value ='" & dth & "'
		document.getElementsByName('display_activity_date')[0].value ='" & dtv & "'
		document.getElementsByName('user_challenge_progress[reported_value]')[0].value ='" & amt & "'
		document.getElementsByName('button')[0].click()"
	end tell
	
	delay 1
	
end repeat
