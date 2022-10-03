# udemy-iot-kichen-garden
leaning iot, rasp pi, python on udemy

Required modules:
smbus
rpi.gpio
spidev
gspread
oauth2client
schedule

Google service account Email address:
kitchen-garden@kitchen-garden-350821.iam.gserviceaccount.com

Target Spread sheet:
1lGQIrw1g-gUXwMIa5tgxdcHHONggn8_zoQIayy-cmrM

Spread sheet URL:
https://docs.google.com/spreadsheets/d/1lGQIrw1g-gUXwMIa5tgxdcHHONggn8_zoQIayy-cmrM/edit?hl=JA#gid

Usage of spread_sheet.py
$ python3 spread_sheet.py -s [Target Spread sheet] -t [Value]

Usage of handler.py
$ python3 handler.py -s [Target Spread sheet] -i [Interval]

Usage of bme280_sample_th_only.py
$ python3 bme280_sample_th_only.py (気温と湿度を表示、なぜ2回表示か謎)
temp : 30.78  ℃
hum :  46.11 ％
temp : 30.78  ℃
hum :  46.11 ％

Usage of append_row_to_gs_dt.py
$ python3 append_row_to_gs_dt.py (gspreadへ日時の書き込み)
['2022-10-03 08:46:10']

Usage of append_row_to_gs_dt_th.py
$ python3 append_row_to_gs_dt_th.py (gspreadへ日付と温湿度の書き込み)

Work memo:
2022.10.3：append_row_to_gs_dt_th.pyで日付と温湿度のGS書き込みに成功
　残課題
　　・気圧の読み込み
　　・スケジューリング
　　・他のセンサー追加
