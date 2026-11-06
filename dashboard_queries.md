# Ghost Trace SOC Dashboard

## Total Failed Logins

index=main status=failed
| stats count

## Failed Logins by Source IP

index=main status=failed
| stats count by src_ip
| sort - count

## Failed Logins by Username

index=main status=failed
| stats count by username

## Successful vs Failed Logins

index=main
| stats count by status

## Login Activity Over Time

index=main
| timechart count by status
