LOG_FILE ?= output.log

.PHONY: file_exists
file_exists:
	test ! -f $(LOG_FILE) && touch $(LOG_FILE)

.PHONY: log
log: start_log file_exists
	echo "error" > $(LOG_FILE)

.PHONY: start_log
start_log:
	echo "Start logging"