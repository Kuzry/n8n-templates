# Shoper - ActiveCampaign

## Wymagane kroki
1. Skopiuj szablon z pliku `add-client.json` do swojej instalacji n8n.
1. Otwórz node o nazwie `Shoper - Auth`. Kliknij w `Basic Auth` a następnie `Create new credential`. W nowym oknie w polu `user` oraz `password` wpisz dane swojego konta Shoper i kliknij `Zapisz`.
1. Otwórz node o nazawie `Pobranie użytkowników ActiveCampaign o przesłanym adresie e-mail z Shoper`. Kliknij w `ActiveCampaign API` a następnie `Create new credential`. W nowym oknie wpisz dane z ActiveCampaign.
1. Otwórz node o nazwie `Dodanie kontaktu ActiveCampaign`. Kliknij w `ActiveCampaign API` a następnie wybierz konto, które dodałeś w punkcie powyżej.
1. Otwórz node o nazwie `Webhook - Shoper - Zamówienie`.
1. Kliknij w `Production URL` i skopiuj adres url.
1. Zaloguj się do swojego sklepu Shoper i przejdź do: `Dodatki i integracje → Webhooki → Dodaj webhook`.
1. W polu `Adres URL` wklej wcześniej skopiowany url z n8n.
1. W polu `Klucz` umieść losowy klucz, który będzie służył za potwierdzenie, że zapytania przychodzą z Twojego sklepu Shoper.
Skopiuj ten klucz, będzie potrzebny za chwilę gdy wrócisz do instalacji n8n.
Losowy klucz najlepiej wygenerować na stronie https://onlinehashtools.com/generate-random-sha256-hash.
1. W polu `Zdarzenia` wybierz `order.create`, pole `Format` powinno mieć wartość `JSON` a pole `Aktywność` ustaw na aktywny.
1. Wróć do instalacji n8n, otwórz node `Zmienne` i skopiowany wcześniej klucz wklej do pola `shoper_webhook_key`.
1. Uzupełnij pozostałe zmienne w node `Zmienne`. `shoper_base_url` to adres Twojego sklepu np.: `https://shop-123.shoparena.pl`.
`active_campaign_base_url` to adres Twojego konta ActiveCampaign np.: `https://johnatan.activehosted.com`.

---
Krzysztof Kuzara

krzysztof@automatly.pl

https://automatly.pl/
