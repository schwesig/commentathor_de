+++
date = '2026-04-02T00:00:00+02:00'
draft = false
title = "Verantwortung by Design: Wie Haftung unsichtbar wird — Plausible Deniability by Design"
tags = ['AI', 'Verantwortung', 'Kommentar']
categories = ['Gesellschaft', 'Tech']
+++

*[Read this in English](/posts/plausible-deniability-by-design)*

### Human in the Loop ist das neue "Ich habe die Terms and Conditions gelesen."

Es gibt ein kleines Ritual, das sich am Ende fast jeder Software-Installation und jeder Web-Registrierung wiederholt. Fast jeder hat daran teilgenommen. Fast niemand hat es ehrlich vollzogen. Du setzt den Haken. Du klickst auf Akzeptieren. Irgendwo in einer Rechtsabteilung gilt ein Kästchen als abgehakt. Verantwortung wurde übertragen. Du hast zugestimmt. Was danach passiert, ist, in einem sehr spezifischen und sehr nützlichen Sinne, dein Problem.

Niemand liest wirklich die Terms and Conditions. Das ist kein Geheimnis. Die Unternehmen, die sie schreiben, wissen es. Die Regulatoren, die sie als rechtsgültig akzeptieren, wissen es. Die Nutzer, die sich durchklicken, wissen es. Aber das System hängt davon ab, dass die Fiktion aufrechterhalten wird, denn sobald du zugibst, dass die Zustimmung hohl ist, musst du fragen, was die Vereinbarung eigentlich geschützt hat. Und für wen.

Ich denke seit einer Weile in einem anderen Zusammenhang darüber nach. Ein anderes Ritual, aber mit einer erkennbaren Form.

---

Die ursprüngliche Idee hinter "Human in the Loop" war nicht unvernünftig. Sie war, genau genommen, vernünftig und bescheiden: AI erledigt die Arbeit, der Mensch prüft die Arbeit, der Mensch entscheidet. Die Maschine beschleunigt. Die Person bleibt verantwortlich. Das Urteilsvermögen bleibt bei der Spezies, die Urteilsvermögen besitzt. Das klang plausibel, und es klingt noch immer vernünftig, wenn man es laut ausspricht. Das Problem ist: Es wurde für eine Welt entworfen, in der das Ausgabevolumen überschaubar war. In der ein Mensch tatsächlich lesen konnte, was er genehmigt. In der "Review" eine echte Tätigkeit war, kein Label.

### Diese Welt verschwindet. Und nicht langsam.

Die Zahlen sind nicht schwer zu finden. KI-gestützte Entwicklung hat den Code-Output in manchen Teams um Größenordnungen erhöht. Wo ein Entwickler früher vielleicht ein paar hundert Zeilen bedeutungsvollen Code pro Tag produziert hat, liefert dieselbe Person heute Pull Requests mit mehreren tausend Zeilen, oft in Minuten generiert. Der Code funktioniert. Oder besteht zumindest die Tests, die ebenfalls zum Teil generiert wurden. Der PR wird geöffnet. Jemand muss ihn reviewen.

### Und hier beginnt das Ritual.

---

Fünftausend Zeilen sind keine Zahl, die ein Mensch in der Zeit eines Sprints sorgfältig reviewen kann. Es ist eine Zahl, durch die man scrollen kann. Man kann nach offensichtlichen Problemen suchen. Man kann prüfen, ob es kompiliert, ob die Tests durchlaufen, ob die Namenskonventionen eingehalten wurden. Was man nicht wirklich kann, ist es zu verstehen, in dem Sinne, der einen befähigen würde, mit Überzeugung zu sagen: Ich weiß, was dieses System in Produktion tun wird. In Edge Cases. Unter Last. Wenn es missbraucht wird. Dieses Verständnis braucht Zeit, Tiefe und meistens jene Vertrautheit mit der Codebase, die nur entsteht, wenn man Teile davon selbst gebaut hat.

Also tun Menschen das, was Menschen tun, wenn ihnen Verantwortung übertragen wird, die sie innerhalb ihrer gegebenen Rahmenbedingungen nicht erfüllen können. Sie passen sich an. Sie entwickeln einen geübten Blick für die Oberfläche. Sie suchen nach Red Flags. Sie vertrauen den Tests. Sie vertrauen der CI Pipeline. Sie vertrauen dem Agenten, der den Output des Agenten geprüft hat. Und dann klicken sie auf Approve.

Ich beschreibe keine Fahrlässigkeit. Ich beschreibe eine strukturelle Bedingung. Der einzelne Entwickler, der diesen PR reviewt, ist nicht faul. Er handelt rational. Die Menge des Outputs hat skaliert. Die Zeit für den Review nicht. Die formale Anforderung, dass ein Mensch genehmigt, bleibt bestehen. Was sich ändert, ist, was diese Genehmigung tatsächlich enthält.

### Die Menge des Outputs hat skaliert. Die Zeit für den Review nicht.

---

Dieses Muster hat einen Namen, auch wenn er meistens auf eine andere Branche angewendet wird. 2015 wurde der Abgasskandal von Volkswagen unter dem Begriff Dieselgate bekannt. Das Interessante daran, das, was ihn strukturell interessant und nicht nur zu einer Geschichte von Unternehmenskorruption machte, war die Art, wie das Fehlverhalten organisiert war. Niemand, soweit wir wissen, hat ein Memo verschickt. Niemand hat den Ingenieuren explizit die Anweisung gegeben, Abschalteinrichtungen zu programmieren. Was passiert ist, war eher etwas Atmosphärisches: Eine Organisation hat Ziele gesetzt, die sich gegenseitig ausschlossen: den Abgastest bestehen, sich wie ein echtes Auto verhalten, den Preispunkt halten. Dann ließ man die Teams damit allein, alle drei gleichzeitig zu erfüllen. Die Lösung hat sich selbst gefunden. Die Menschen, die sie gebaut haben, wussten, was sie tat. Die Menschen über ihnen hatten plausible Deniability. Die Struktur hat die Täuschung absorbiert — und die Struktur wurde von Menschen geführt, die die Arbeit in einem formalen Sinne auf dem ganzen Weg nach oben geprüft und genehmigt hatten.

Ich denke immer wieder an diese Struktur, wenn ich sehe, wie Verantwortung in der KI-Entwicklung gerade organisiert wird. Das Unternehmen sagt: Du musst alles reviewen, was ein Mensch in Produktion bringt. Das Unternehmen sagt auch: Wir müssen zehnmal schneller liefern als letztes Jahr. Das Tooling sagt: Hier sind fünftausend Zeilen, agent-generiert, agent-reviewed, bereit für deine Genehmigung. Die KI sagt, auf ihre weiche und selbstsichere Art: Ich habe das geprüft. Sieht gut aus.

### Der Mensch ist noch im Loop. Formal. In welchem Loop er sich tatsächlich befindet, ist eine andere Frage.

---

Die Haftungsarchitektur hier ist fast elegant, wenn man sie kalt betrachtet. "Ein Mensch hat es genehmigt" ist ein Satz, der die meisten Untersuchungen beendet, bevor sie beginnen. Er verteilt Verantwortung nach unten, weg vom System und hin zum Individuum. Er bewahrt die KI als Werkzeug, und Werkzeuge haben historisch gesehen keine Haftung. Er erlaubt der Organisation, den Standpunkt zu vertreten, dass die Richtlinien klar waren und der Prozess eingehalten wurde, selbst wenn die Richtlinien praktisch nicht durchsetzbar waren und der Prozess eine Simulation seiner selbst.

Das ist nicht neu in der Geschichte von Organisationen. Was neu ist, ist die Geschwindigkeit und das Ausmaß, mit dem die Lücke zwischen formaler und realer Verantwortung sich jetzt öffnen kann. KI skaliert Output. Sie skaliert nicht die Kapazität des Menschen, der diesen Output prüft. Verantwortung skaliert nicht. Sie bleibt beim Individuum, genau dort, wo sie war, während alles um sie herum in einem Tempo wächst, das das Individuum nicht mithalten kann.

### KI skaliert Output. Aber sie skaliert keine Verantwortung.

![AI scales output. But it does not scale responsibility.](/images/ai-scales-output-not-responsibility.png)

Das System wird wirklich instabil, wenn drei Dinge zusammenfallen: Output überschreitet die Review-Kapazität, Zeitdruck überschreitet die Toleranz für echte Sorgfalt, und individuelle Verantwortung bleibt rechtlich intakt. Diese Kombination ist kein hypothetisches Zukunftsszenario. Es ist die Situation, auf die sich viele Engineering-Organisationen gerade zubewegen, oft mit Enthusiasmus, oft mit sorgfältig verfasster Prozessdokumentation, die einen Review-Prozess beschreibt, den niemand so wie beschrieben tatsächlich durchführen kann.

### Compliance wird zur Simulation.

---

### Human in the Loop wird zur Haftungsillusion.

Der Vergleich mit den Terms and Conditions ist kein Witz. Es ist eine strukturelle Beobachtung. Das ToS-Regime hat uns gezeigt, was passiert, wenn Zustimmung formalisiert, aber ausgehöhlt wird: Man schafft eine Klasse von Vereinbarungen, die rechtlich bindend und praktisch bedeutungslos sind. Die Bedeutungslosigkeit ist kein Bug, sondern ein architektonisches Merkmal. Weil sie eine Partei schützt, ohne der anderen wirklich etwas abzuverlangen. Klick auf Akzeptieren, und wir sind hier fertig.

Wir bauen etwas Ähnliches in das Fundament dessen ein, wie Software gemacht wird. Human in the Loop ist in seiner aktuellen Umsetzung oft weniger ein Sicherheitsmechanismus als eine Haftungszuweisung. Es erlaubt dem System, in jeder Phase auf einen Menschen zu zeigen: der Entwickler hat es genehmigt, der Tech Lead hat es gemergt, der Manager hat den Sprint abgezeichnet. Ohne dass einer dieser Menschen eine echte Chance hatte, das Urteilsvermögen auszuüben, für das er verantwortlich gemacht wird.

### Wir zeichnen Verantwortung für Dinge ab, die wir nicht mehr verstehen können.

Wir zeichnen Verantwortung für Dinge ab, die wir nicht mehr verstehen können. Die Maschine trifft die Entscheidung nicht, genau genommen. Aber sie bringt uns in die Position, sie abzustempeln: unter Zeitdruck, in Mengen, die wir nicht bewältigen können, mit Review-Tooling, das selbst automatisiert ist, und mit der formalen Anforderung einer Genehmigung, die nach wie vor fest an unseren Namen hängt.

---

Was daran unangenehm ist, ist nicht, dass es passiert. Unangenehme Dinge passieren ständig, und Organisationen navigieren sie. Was unangenehm ist, ist die Ähnlichkeit mit jeder Vor-Skandal-Struktur im Rückblick: Offiziell alles sauber. Inoffiziell weiß jeder Beteiligte, dass der Prozess nicht so funktioniert, wie beschrieben. Niemand möchte derjenige sein, der es laut ausspricht, denn laut aussprechen macht dich verantwortlich für die Lücke, die du gerade benannt hast. Also bleibt die Lücke unbenannt. Das Ritual geht weiter. Die Kästchen werden abgehakt.

Plausible Deniability by Design ist ein Satz, der absichtlich bedrohlich klingt, aber er braucht keine absichtlich böse Absicht. Er braucht nur, dass die Anreize in eine Richtung zeigen und die Kontrollmechanismen irgendwo anders hin, und dass niemand Beteiligtes ein besonderes Interesse daran hat, beides in Einklang zu bringen.

Die ursprüngliche Idee von Human in the Loop war nicht falsch. Menschen in bedeutungsvollem Kontakt mit folgenreichen Entscheidungen zu halten ist ein echter Wert, und ein vertretbarer. Das Problem ist, dass "in the loop" still zu einer positionalen Beschreibung geworden ist, nicht zu einer funktionalen. Der Mensch ist da. Der Loop existiert. Was der Mensch darin tatsächlich tun kann, was er realistischerweise prüfen, verstehen, erkennen oder verweigern kann, diese Frage wird nicht laut genug gestellt.

Und das Ding mit Ritualen, das, was sie dauerhaft macht, auch wenn sie ihre ursprüngliche Bedeutung verloren haben: Von außen sehen sie genau gleich aus, egal ob noch jemand zu Hause ist oder nicht.

### Wir verwandeln Verantwortung in ein Ritual.

---

Die autonome Fahrzeugindustrie kreist seit Jahren um eine Version dieser Frage. Wenn ein selbstfahrendes Auto einen Unfall verursacht, wer ist verantwortlich? Der Hersteller? Der Software-Anbieter? Der Eigentümer? Der Passagier, der nicht eingegriffen hat? Regulatoren und Versicherer haben das nicht gelöst. Was sie in den meisten Jurisdiktionen getan haben, ist die Mehrdeutigkeit zu bewahren, weil ihre Auflösung erfordern würde, dass jemand eine Haftung akzeptiert, die niemand akzeptieren will. Die Frage, wer im Loop ist, und was es von dieser Person tatsächlich verlangt, darin zu sein, ist überraschend schwer zu beantworten, wenn die Antwort Konsequenzen hat.

### Wer ist im Loop? Frag nochmal, wenn etwas schiefgeht.
