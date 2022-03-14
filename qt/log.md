- use [QLoggingCategory](https://doc.qt.io/qt-5/qloggingcategory.html)
- example :
- in header files :
- `src/serialbus/qmodbusrtuserialserver_p.h`
- `src/serialbus/qmodbusrtuserialclient_p.h`
- `src/serialbus/qmodbustcpserver_p.h`
- `src/serialbus/qmodbustcpclient_p.h`
```
Q_DECLARE_LOGGING_CATEGORY(QT_MODBUS)
Q_DECLARE_LOGGING_CATEGORY(QT_MODBUS_LOW)
```
- in source file or in main :
- `qtserialbus/src/serialbus/qmodbusdevice.cpp`
```
Q_LOGGING_CATEGORY(QT_MODBUS, "qt.modbus")
Q_LOGGING_CATEGORY(QT_MODBUS_LOW, "qt.modbus.lowlevel")
```

- usage `qCDebug`
```
qCDebug(QT_MODBUS_LOW) << "(TCP client) Response buffer:" << responseBuffer.toHex();
```
---
- [KDAB Guidelines Debugging](https://community.kde.org/Guidelines_and_HOWTOs/Debugging/Using_Error_Messages)
- [Qt Logging Framework](https://www.kdab.com/wp-content/uploads/stories/slides/Day2/KaiKoehne_Qt%20Logging%20Framework%2016_9_0.pdf)
- [Logging Qt application events to a text file](https://evileg.com/en/post/154/)
