const rotateRightButton = document.getElementById("rotate-right");
const rotateLeftButton = document.getElementById("rotate-left");
const scaleXButton = document.getElementById("scale-X-button");
const scaleYButton = document.getElementById("scale-Y-button");
const options = document.querySelector(".options-btn");
const filterValue = document.querySelector(".filter-info .value");
const filterSlider = document.querySelector(".slider input");
const resetFilterBtn = document.querySelector(".reset-filter");
const filterOptions = document.querySelectorAll(".crop button, .ratio button");
const dropArea = document.querySelector(".image-container");
const dragText = dropArea.querySelector("h6");
const button = dropArea.querySelector("button");
let fileInput = document.getElementById("file");
let image = document.getElementById("image");
let downloadButton = document.getElementById("download");
let RatioBtns = document.querySelectorAll(".ratio button");
let CropBtns = document.querySelectorAll(".crop button");
let cropper = "";
let fileName = "";
let scaleXClick = false,
  scaleYClick = false;
let rotateRightValue = 45,
  rotateLeftValue = -45;
let initialValue = 0;
var slider = document.querySelector('.margins');

button.onclick = ()=>{
  fileInput.click(); 
}

fileInput.onchange = () => {
  let reader = new FileReader();
  reader.readAsDataURL(fileInput.files[0]);
  reader.onload = () => {
    image.setAttribute("src", reader.result);
    if (cropper) {
      cropper.destroy();
    }
    cropper = new Cropper(image, {
      responsive: true,
      restore: true,
      scalable: true,
      wheelZoomRatio: 0.01,
      cropBoxResizable: true,
      cropBoxMovable: true,
      dragMode: 'move',
      toggleDragModeOnDblclick: true,
      zoomOnTouch: true,
      zoomOnWheel: true,
      autoCropArea : 1,
    });
  };
  fileName = fileInput.files[0].name.split(".")[0];
  document.querySelector(".drag-image").hidden = true;
  document.querySelector(".container").classList.remove("disable");
};

dropArea.addEventListener("dragover", (event)=>{
  event.preventDefault();
  dropArea.classList.add("active");
  dragText.textContent = "Release to Upload File";
});

dropArea.addEventListener("dragleave", ()=>{
  dropArea.classList.remove("active");
  dragText.textContent = "Drag & Drop to Upload File";
}); 

dropArea.addEventListener("drop", (event)=>{
  let reader = new FileReader();
  reader.readAsDataURL(fileInput.files[0]);
  reader.onload = () => {
    image.setAttribute("src", reader.result);
    if (cropper) {
      cropper.destroy();
    }
    cropper = new Cropper(image, {
      responsive: true,
      restore: true,
      scalable: true,
      wheelZoomRatio: 0.1,
      cropBoxResizable: true,
      cropBoxMovable: true,
      dragMode: 'move',
      toggleDragModeOnDblclick: true,
      zoomOnTouch: true,
      zoomOnWheel: true,
      autoCropArea : 1,
    });
  };
  fileName = fileInput.files[0].name.split(".")[0];
  document.querySelector(".drag-image").hidden = true;
  document.querySelector(".container").classList.remove("disable");
});

//reste à régler le drop//

filterOptions.forEach(option => {
  option.addEventListener("click", () => {
    document.querySelector(".active").classList.remove("active");
    option.classList.add("active");
  });
});

rotateRightButton.addEventListener("click", () => {
  cropper.rotate(rotateRightValue);
});

rotateLeftButton.addEventListener("click", () => {
  cropper.rotate(rotateLeftValue);
});

scaleXButton.addEventListener("click", () => {
  if (scaleXClick) {
    cropper.scaleX(1);
    scaleXClick = false;
  } else {
    cropper.scaleX(-1);
    scaleXClick = true;
  }
});

scaleYButton.addEventListener("click", () => {
  if (scaleYClick) {
    cropper.scaleY(1);
    scaleYClick = false;
  } else {
    cropper.scaleY(-1);
    scaleYClick = true;
  }
});

RatioBtns.forEach((element) => {
  element.addEventListener("click", () => {
    if (element.innerText == "Free") {
      cropper.setAspectRatio(NaN);
    } else {
      cropper.setAspectRatio(eval(element.innerText.replace(":", "/")));
    }
  });
});

CropBtns.forEach((element) => {
  element.addEventListener("click", () => {

    if (element.innerText == "Auto-Crop") {
    } else {
    }
  });
});

//reste à faire l'auto-crop et le manual-crop//

const updateFilter =() => {
  filterValue.innerText = `${filterSlider.value}%`;
  let margins = filterSlider.value;
}
filterSlider.addEventListener("input",updateFilter);
filterSlider.onchange = () => {
  const currentValue = Number(filterSlider.value);
    cropper.zoom(0.01 * (initialValue - currentValue));
    initialValue = currentValue;
};

downloadButton.addEventListener("click", (e) => {
  let imgSrc = cropper.getCroppedCanvas({}).toDataURL();
  downloadButton.download = `cropped_${fileName}.png`;
  downloadButton.setAttribute("href", imgSrc);
});

const resetFilter = () => {
  cropper.zoom(0.01 * (filterSlider.value));
  cropper.setAspectRatio(NaN);
  document.querySelector(".active").classList.remove("active");
  document.getElementById("Free").classList.add("active");
  cropper.scaleX(1);
  cropper.scaleY(1);
  cropper.rotate();
  initialValue = 0;
  filterSlider.value = 0;
  filterValue.innerText = `${filterSlider.value}%`;
}
resetFilterBtn.addEventListener("click", resetFilter);

//reste à reset les rotations//
