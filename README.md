# JSProoofAssessment1
// Step 1: Create a variable to hold your NFTs
// this varibale will be an array and it will store the NFTs
const nftsDetails = [];

// Step 2: This function will take in some values as parameters, create an
// NFT object using the parameters passed to it for its metadata,
// and store it in the variable above.
// Here we created a function called mintNFT which holds all the metadata 
function mintNFT(nftName, creator, YearOfPublish, detail) {
    const nft = {
        nftName: nftName,
        creator: creator,
        YearOfPublish: YearOfPublish,
        detail: detail
    }
    nftsDetails.push(nft);
}

// Step 3: Create a "loop" that will go through an "array" of NFTs
// and print their metadata with console.log()
// Here we have created a function called listNFTS which will include a loop and that loop will print the metadata
function listNFTs() {
    let i = 0;
    do {
        if (i >= nftsDetails.length) break;
        console.log("Name; " + nftsDetails[i].nftName);
        console.log("creator: " + nftsDetails[i].creator);
        console.log("yearOFPublish: " + nftsDetails[i].YearOfPublish);
        console.log("detail: "+ nftsDetails[i].detail);
        console.log("***************************");
        i++;
    } while (i < nftsDetails.length);
}
// Step 4: Print the total number of NFTs we have minted to the console
// here we have created a function called getTotalSupply which will return the total number of NFTS using the length() function
function getTotalSupply() {
    return nftsDetails.length;
}

// Call your functions below this line
// Mint some NFTs
mintNFT("bestNFt", "Jatin Gaur", 2020, "an ape with a gun.");
mintNFT("NFT of Science", "Max Planck", 2019, "An atom inside a hat.");
mintNFT("nft of the future", "imtiaz ali", 2023, "A scenery of a beautiful waterfall.");
// List all NFTs
listNFTs();

// Print the total number of NFTs
console.log("Total number of nfts: " + getTotalSupply());
