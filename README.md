JavaScript Deck of Cards
Setup

Create a new local project directory called "js-deck-of-cards".
Add a local git repository.
Create a remote repository on Github.
Add/commit to your local git repo, and then push your changes to Github.
Steps

Within the main.js file-

Make sure you understand the current code. Add comments. Read the code aloud!
Finish the newDeck() function so that it returns a deck of cards as an array of objects - e.g., [{card: "j"suit: "s"}, {card: "q"suit: "d"}, ...]
Write a function called shuffleCards() that takes the created card deck and returns the it shuffled.
Review the following code, making certain you understand the DOM manipulation:

showCards.onclick = function(){
  var cardContainer = document.getElementById('container');
  cardContainer.innerHTML = "";
  displayCards();
};

function displayCards(){
  var deck = newDeck();
  var shuffledCards = shuffleCards(deck);

  for(var i=0; i < deck.length; i++){
    var card = document.createElement('div');
    card.className = "card";
    var cardContainer = document.getElementById('container');
    cardContainer.appendChild(card);
    card.style.backgroundImage = "url(images/" + shuffledCards[i].suit + "-" + shuffledCards[i].card + ".png" + ")";

  }
}
Within the index.html file-

Add a another button called "Reset!", which clears all cards from the DOM. Think about what needs to happen, if anything, within the JavaScript file.
Make sure this button is only displayed after the end user clicks the "Deal!" button.
After the "Reset!" button is clicked remove or hide it from the DOM.
Resources

Normalize CSS - Make sure you understand normalize.css!
Creating your own Grid system
