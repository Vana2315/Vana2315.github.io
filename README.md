
<!DOCTYPE html>
<html lang="en">
 <head>
    <meta charset="UTF-8">
    <link rel="stylesheet" href="style.css">
    <title>Знайомство з JS</title>
 
<script>
    var photosCount = 8
    var currentPhotoIndex = 1
    function showNextPhoto () {
        currentPhotoIndex++
        if (currentPhotoIndex > photosCount) currentPhotoIndex = 1
     
        var elem = document.getElementById("currentPhoto")
        elem.src = "images/photo" + currentPhotoIndex + ".jpg"
    }
    function addNextPhoto () {
        var newImage = document.createElement("img")

        currentPhotoIndex++
        if (currentPhotoIndex > photosCount) currentPhotoIndex= 1
        
        newImage.src="images/photo"+currentPhotoIndex+".jpg"
        var containerElem = document.getElementById("gallery")
        containerElem.appendchild(newImage)
}
 function addimage() { 
          var img = document.createElement("img");
          currentPhotoIndex++
          if (currentPhotoIndex > photosCount) currentPhotoIndex= 1
          img.src = "images/photo"+currentPhotoIndex+".jpg"; 
      
          img.height = 300; 
          img.width = 300;

        
         var class_name = "foo";
          img.setAttribute("class", class_name);

          document.body.appendChild(img);
        } 
</script>

</head>

<body>
   
    <div  id="gallery">
    <img id="currentPhoto"  src="images/photo1.jpg"  width="300" height="300"  >
    </div>

<button class="baton" onclick="showNextPhoto ()" style="vertical-align:middle"><span>Наступне </span></button>
<button class="button" onclick="addimage ()" style="vertical-align:middle"><span>Додати</span></button>
</body> 
</html>
     

