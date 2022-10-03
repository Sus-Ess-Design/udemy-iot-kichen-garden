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
$ python3 append_row_to_gs_dt.py (gspreadへ日時の書き込み、ラズパイのみ)
['2022-10-03 08:46:10']

Usage of append_row_to_gs_all_in_one.py
$ python3 append_row_to_gs_all_in_one.py (gspreadへ日付と温湿度の書き込み)

Work memo:
append_row_to_gs_all_in_one.pyで温度湿度計測とgspreadへの日付書き込みを同時に記述するが、温度湿度計測の部分が動かない
おそらく、温度湿度計測の部分をClass化する必要がある。
BME280の記述をSH31と同様に変更する作業が必要と思われる
