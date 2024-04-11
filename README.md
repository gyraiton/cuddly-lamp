function main() {
    var count;
    var randomNumber;
    var searchNumber;
    var foundCount;
    var found;

    window.alert("Laten we een spel spelen! Jij noemt een getal onder 100, en we zullen zien of het in een willekeurig gegenereerde reeks van 50 cijfers komt te staan.");
    searchNumber = Number(window.prompt('Enter a value for searchNumber'));
    count = 1;
    found = false;
    foundCount = 0;
    while (count <= 50) {
        randomNumber = Math.floor(Math.random() * 100);
        window.alert(randomNumber);
        if (randomNumber == searchNumber) {
            found = true;
            foundCount = foundCount + 1;
        }
        count = count + 1;
    }
    if (found) {
        window.alert("Het getal " + searchNumber + " is " + foundCount + " keer gevonden.");
    } else {
        window.alert("Het getal " + searchNumber + " is helaas niet gevonden.");
    }
    if (searchNumber > 100) {
        window.alert("Misschien omdat je een te hoge getal in hebt gevoerd...");
    }
}
