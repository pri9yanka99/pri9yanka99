// Create a variable to hold your NFTs
const NFTs = [];

// This function will take in some values as parameters, create an
// NFT object using the parameters passed to it for its metadata, 
// and store it in the variable above.
function mintNFT(title, director, actor, actress, releaseYear, type, language) {
    const NFT = {
        "title": title,
        "director": director,
        "actor": actor,
        "actress": actress,
        "releaseYear": releaseYear,
        "type": type,
        "language": language
    };
    NFTs.push(NFT);
    console.log("Minted NFT for movie: " + title);
}

// Create a "loop" that will go through an "array" of NFTs
// and print their metadata with console.log()
function listNFTs() {
    for (let i = 0; i < NFTs.length; i++) {
        console.log("\nID:\t\t" + (i + 1));
        console.log("Title: \t\t" + NFTs[i].title);
        console.log("Director: \t" + NFTs[i].director);
        console.log("Actor: \t\t" + NFTs[i].actor);
        console.log("Actress: \t" + NFTs[i].actress);
        console.log("Release Year: \t" + NFTs[i].releaseYear);
        console.log("Type: \t\t" + NFTs[i].type);
        console.log("Language: \t" + NFTs[i].language);
        console.log('------------------------');
    }
}

// Print the total number of NFTs we have minted to the console
function getTotalSupply() {
    console.log("\nTotal NFTs minted: " + NFTs.length);
}

// Call your functions below this line
mintNFT("Inception", "Christopher Nolan", "Leonardo DiCaprio", "Elliot Page", 2010, "Sci-Fi", "English");
mintNFT("The Matrix", "Lana Wachowski, Lilly Wachowski", "Keanu Reeves", "Carrie-Anne Moss", 1999, "Action", "English");
mintNFT("Interstellar", "Christopher Nolan", "Matthew McConaughey", "Anne Hathaway", 2014, "Sci-Fi", "English");
mintNFT("The Shawshank Redemption", "Frank Darabont", "Tim Robbins", "N/A", 1994, "Drama", "English");
mintNFT("The Godfather", "Francis Ford Coppola", "Marlon Brando", "Diane Keaton", 1972, "Crime", "English");

console.log("Listing all NFTs:");
listNFTs();
getTotalSupply();

