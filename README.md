Änderungen in der gcode_macro.cfg
Überblick

Dieses Repository enthält Fehlerbehbungen der gcode_macro.cfg-Datei, Diese Änderungen betreffen vor allem die Anpassung von Beschleunigungswerten.


Voraussetzungen:

Bevor Sie diese Änderungen vornehmen, stellen Sie sicher, dass Sie Zugriff auf die gcode_macro.cfg-Datei Ihres 3D-Druckers haben und mit der Syntax von G-Code vertraut sind.
Schritte zur Modifikation

    Öffnen Sie die gcode_macro.cfg-Datei in Ihrem bevorzugten Texteditor.

    Suchen Sie nach dem Makro gcode_macro Qmode. Die genaue Zeilennummer kann variieren, in diesem Beispiel befindet es sich in Zeile 78.

    Fügen Sie unterhalb von gcode_macro Qmode folgende Zeilen hinzu:

    yaml

variable_max_accel: 5000  # Diese Zeile hinzufügen mit einem angemessenen Wert
variable_max_accel_to_decel: 5000 # Diese Variable hinzufügen

Beispielhaft sieht der Abschnitt dann wie folgt aus:



    variable_flag: 0
    variable_max_accel: 5000
    variable_max_accel_to_decel: 5000
    variable_accel: 0
    variable_accel_to_decel: 0
    variable_velocity: 0
    variable_square_corner_velocity: 0
    variable_pressure_advance:0.0
    variable_fan0_value: 0.00
    variable_fan1_value: 0.00
    variable_fan2_value: 0.00
    variable_speed_factor: 0

    Speichern Sie die Änderungen an der gcode_macro.cfg-Datei.

Wichtig

    Stellen Sie sicher, dass Sie die Werte von variable_max_accel und variable_max_accel_to_decel entsprechend den Spezifikationen und Grenzen Ihres Druckers anpassen.
    Der weitere G-Code bleibt unverändert. (wenn sie ein drucker der K1 reie haben können sie die Einstellung so lassen)

Unterstützung

Für weitere Unterstützung oder Fragen, eröffnen Sie bitte ein Issue in diesem Repository.


