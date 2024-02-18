+++
date = 2022-08-15T12:26:00Z
description = ""
draft = false
slug = "nostr-fur-marktkommunikation"
title = "Nostr für Marktkommunikation"

+++


### AS/4 statt Email ist ein Fortschritt, jedoch unnötig komplex.



Die deutsche Energiewirtschaft wird durch eine stetig wachsende Anzahl an Marktpartnern gebildet. Diese tauschen sich in vielen Fällen automatisiert über die sogenannte Marktkommunikation aus. Dies sind typischerweise speziell formatierte Textdateien, welche per verschlüsselter Email zwischen den verschiedenen Akteuren ausgetauscht werden.

{{< figure src="https://images.unsplash.com/photo-1563762270340-3f5fde3243cd?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=MnwzMDAzMzh8MHwxfHNlYXJjaHw1M3x8ZW1haWx8ZW58MHx8fHwxNjYwNTcxMTk5&ixlib=rb-1.2.1&q=80&w=1080" >}}

Email als Transportmechanismus ist nicht mehr optimal, da bei komplizierten Geschäftsprozessen beispielsweise die Reihenfolge von Nachrichten relevant ist. Dies kann jedoch beim Emailtransport nicht spezifiziert werden, sodass dies im Backend eines Marktteilnehmers abgefangen beziehungsweise in eine Warteschlange überführt werden muss.

Um dies zu verbessern, ist 2024 die verpflichtende Einführung von AS/4 durch die Bundesnetzagentur vorgesehen. Dies stellt eine Verbesserung dar, da AS/4 als Transportmechanismus modernere Web-Service Architekturen erlaubt. Leider ist die Technologie auch relativ komplex und sieht weiterhin die Verwendung von speziellen SMIME Zertifikaten vor, welche kryptographisch unnötig sind.

Eine einfachere und gleichzeitig funktionale Alternative ist das offene Nostr Protokoll: Nostr[1](#footnote-1) basiert auf einer föderierten Client-Server Architektur, kombiniert mit Public-Key-Kryptographie. Jeder Netzwerkteilnehmer betreibt einen Client, um Nachrichten zu senden und zu empfangen. Nachrichten werden von Clients signiert & validiert und von Servern - sogenannten Relays - verteilt. Relays kann jeder betreiben und jeder Client kann festlegen, über welche Relays er kommuniziert. Das erlaubt z.B. das Betreiben von privaten Netzwerken, basierend auf öffentlichen Schlüsseln auf Allowlists.

Die Community ist zur Zeit vor allem auf Telegram aktiv und besteht Großteils aus P2P und Bitcoin Software Ingenieuren. Es hat sich bereits ein buntes Sammelsurium[2](#footnote-2) an Projekten und Tools entwickelt. Das Protokoll ist absichtlich minimalistisch, sodass auch die Implementierung von M2M-Kommunikation denkbar ist. Der Nachrichteninhalt und Struktur sind nicht auf Protokollebene festgelegt.

Das bedeutet, dass die bekannten EDI@Energy und XML-basierten Formate direkt übernommen werden könnten. Die Implementierung des Protokolls bei den jeweiligen Marktteilnehmern kann aufgrund der breiten Verfügbarkeit von Open-Source Code und der schlanken Architektur erheblich schneller ablaufen, als bei AS/4.

Der BDEW könnte dann zentrale Relay Server betreiben, die direkt ein Adressbuch (Allowlist) und weitere Validierung mitbringen. Gleichzeitig könnte das Nostr Key-Pair direkt bei der Registrierung einer BDEW Nummer vergeben werden. Das lästige und teure Einholen von SMIME Zertifikaten entfällt. Auch die Teilnahme von Geräten am Netzwerk ist denkbar. Jedes Gerät entspricht mindestens einem Nostr Client, welcher entsprechend durch einen Public Key identifizierbar ist.

Schreib mir gerne was du darüber denkst per [Mail](mailto:phil@philippnagel.com) oder Nostr!

Meine Nostr ID lautet: npub1uhqal6z002p7wcrdm3hqaqsfxpx0skfsflf457whrh4465tnqyxq3tvzmw. Empfehlenswert ist [Branle](https://branle.netlify.app/) im Browser oder [Damus](https://damus.io/) für iOS. Die Fußnote Zwei enthält weitere Implementierungen.

---

[1](#footnote-anchor-1) https://github.com/nostr-protocol/nostr

[2](#footnote-anchor-2) https://github.com/aljazceru/awesome-nostr


