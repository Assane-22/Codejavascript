# Codejavascript
var distance = msg.payload.distance; // Assurez-vous que la charge utile (payload) contient un champ "distance"
var newMsg = {}; // Créez un nouvel objet de message

newMsg.topic = "distance capteur"; // Définissez le sujet du message

if (distance > 10) {
    newMsg.payload = "Embouteillage detecté sur l'autoroute A 34, veuillez changer d'itinéraire";
} else {
    newMsg.payload = "";
}

return newMsg;

