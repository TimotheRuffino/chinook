# README

* Nombre d'albums : 347

* Auteur de la chanson White Room : Eric Clapton

* Chason qui dure 188133 milliseconds : Perfect de Alanis Morissette

* Quel groupe a sorti l'album "Use Your Illusion II" : Guns N Roses

* Combien y a t'il d'albums dont le titre contient "Great" ? : 13

* Combien y a t'il d'albums écrits par AC/DC ? : 2

* Combien de chanson durent exactement 158589 millisecondes ? : 0

* puts en console tous les titres de AC/DC :
Track.where(artist: "AC/DC").each do |track|
puts track.title
end

* Calcule le prix total de cet album ainsi que sa durée totale.
total_duration = 0
total_price = 0

Track.where(album: "Let There Be Rock").each do |track|
total_duration += track.duration
total_price += track.price
end

puts total_duration
puts total_price


* Calcule le coût de l'intégralité de la discographie de "Deep Purple".
total_price = 0

Track.where(artist: "Deep Purple").each do |track|
total_price += track.price
end

puts total_price


* Modifie (via une boucle) tous les titres de "Eric Clapton" afin qu'ils soient affichés avec "Britney Spears" en artist.
Track.where(artist: "Eric Clapton").each do |track|
track.update(artist: "Britney Spears")
end