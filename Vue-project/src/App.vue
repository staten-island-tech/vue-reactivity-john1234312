<script >
  import card from "./components/card.vue"
  export default {
    components: {
      card
    },
    data(){
      return {
        books: [
          {
            title: "Brothers Karamzov" ,
            description: "The Brothers Karamazov is a novel with a simple plot about a murder and a complex discussion of faith, doubt, and morality. We begin with the father, Fyodor Karamazov. Fyodor is a cruel and lustful man who has fathered three sons: Dmitri, a man driven by his passions." ,
            image: "https://m.media-amazon.com/images/I/A1dNvQXVPZL._AC_UF1000,1000_QL80_.jpg" ,
          },
          {
            title: "Crime and Punishment",
            description: "Crime and Punishment follows the mental anguish and moral dilemmas of Rodion Raskolnikov, an impoverished ex-student in Saint Petersburg who plans to kill an unscrupulous pawnbroker, an old woman who stores money and valuable objects in her flat." ,
            image: "https://mybooksummaries-23.s3.eu-north-1.amazonaws.com/crime-and-punishment.jpg" ,
          },
          {
            title: "The Idiot" ,
            description: "The Idiot is a novel by Russian author Fyodor Dostoyevsky. It follows the titular character, Prince Lev Myshkin as he arrives in a corrupt St. Petersburg and attempts to navigate love and life.S" ,
            image: "https://mybooksummaries-23.s3.eu-north-1.amazonaws.com/the-idiot.jpg" ,
          },
          {
            title: "No Longer Human" ,
            description: "No Longer Human tells the poignant and fascinating story of a young man who is caught between the breakup of the traditions of a northern Japanese aristocratic family and the impact of Western ideas." ,
            image: "https://prodimage.images-bn.com/pimages/9780811204811_p0_v3_s1200x630.jpg" ,
          },
          {
            title: "The Great Gatsby" ,
            description: "The Great Gatsby, Third novel by American author F. Scott Fitzgerald, published in 1925. Set in Jazz Age New York, it tells the tragic story of Jay Gatsby, a self-made millionaire, and his pursuit of Daisy Buchanan, a wealthy young woman whom he loved in his youth" ,
            image: "https://blog.prepscholar.com/hubfs/feature_gatsbycover.jpg" ,
          },
          {
            title: "Moby Dick" ,
            description: "Moby-Dick; or, The Whale is an 1851 novel by American writer Herman Melville. The book is the sailor Ishmael's narrative of the maniacal quest of Ahab, captain of the whaling ship Pequod, for vengeance against Moby Dick, the giant white sperm whale that bit off his leg on the ship's previous voyage." ,
            image: "https://cdn11.bigcommerce.com/s-5uqrjcd/images/stencil/1280x1280/products/34425/50792/sp9243__83785.1589553930.jpg?c=2" ,
          },
          {
            title: "The Catcher in the Rye" ,
            description: "The Catcher in the Rye describes the adventures of well-off teenage boy Holden Caulfield on a weekend out alone in New York City, illuminating the struggles of young adults with existential questions of morality, identity, meaning, and connection." ,
            image: "https://cdn.britannica.com/94/181394-050-2F76F7EE/Reproduction-cover-edition-The-Catcher-in-the.jpg" ,
          },
          {
            title: "A Farewell to Arms" ,
            description: "Ernest Hemingway's A Farewell to Arms was published in 1929. It tells the story of an American expatriate who served as an ambulance driver of the Italian army during World War I. Hemingway's novel is a first person account of a wartime love story." ,
            image: "https://upload.wikimedia.org/wikipedia/en/4/48/Hemingway_farewell.png" ,
          },
          {
            title: "Slaughterhouse-Five" ,
            description: "Slaughterhouse-Five is the semi-autobiographical account of the fire bombing of Dresden, Germany by the British and American air forces in the February of 1945. The destruction of this non-military city so late in the war is still very controversial, and that controversy is central to Vonnegut's book." ,
            image: "https://i.gr-assets.com/images/S/compressed.photo.goodreads.com/books/1440319389l/4981._SY475_.jpg" ,
          },
        ],
        selectedBooks: [

        ],
      }
    },
    methods: {
      addStorage: function () {
        this.selectedBooks.push(this.books.find(book=>book.image===event.target.parentNode.id))
        console.log(this.selectedBooks)
      }
    }
    

  }
</script>

<template>
  <div class="mainPage">
      <h1 class="header">Books</h1>
      <div class="storageSpace">
        <div v-for="book in selectedBooks" :key="book">
          <h2>{{ book.title }}</h2>
        </div>
      </div>
  </div>
  <card v-for="book in books" :key="book.title" :title="book.title" :description="book.description" :image="book.image" :addStorage="addStorage"></card>
</template>

