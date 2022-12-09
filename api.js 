const getData = async()=>{
    let response = await fetch('http://localhost:5000/api/products/');
    let data = await response.json();
console.log(data)
    return data;
}
try{
   getData();
}
catch (error) {
    console.log(error);
  }
getData().then((data)=> {data.data.forEach(element => {
    
    document.getElementById("row").innerHTML+=` <div class="col-lg-3 col-md-4 col-sm-6 pb-1">
    <div class="product-item bg-light mb-4">
        <div class="product-img position-relative overflow-hidden">
            <img class="img-fluid w-100" src="/${element.image}" alt="">
            <div class="product-action">
                <a class="btn btn-outline-dark btn-square" href=""><i class="fa fa-shopping-cart"></i></a>
                <a class="btn btn-outline-dark btn-square" href=""><i class="far fa-heart"></i></a>
                <a class="btn btn-outline-dark btn-square" href=""><i class="fa fa-sync-alt"></i></a>
                <a class="btn btn-outline-dark btn-square" href=""><i class="fa fa-search"></i></a>
            </div>
        </div>
        <div class="text-center py-4">
            <a class="h6 text-decoration-none text-truncate" href="">${element.name}</a>
            <div class="d-flex align-items-center justify-content-center mt-2">
                <h5>${element.price}</h5> <h6 class="text-muted ml-2"><del>${element.price-(element.price*element.discount)}</del></h6>
            </div>
            <div class="d-flex align-items-center justify-content-center mb-1">
                <small class="fa fa-star text-primary mr-1"></small>
                <small class="fa fa-star text-primary mr-1"></small>
                <small class="fa fa-star text-primary mr-1"></small>
                <small class="fa fa-star text-primary mr-1"></small>
                <small class="fa fa-star text-primary mr-1"></small>
                <small>(${element.rating_count})</small>
            </div>
        </div>
    </div>
</div>`
})
});
  async function getToken(){
    try{
    let res =fetch('http://localhost:5000/api/users/login/',{
  method:"POST",
  headers:{
    'Authorization':'Basic '+btoa('ramymibrahim@yahoo.com:123456'),
    'Content-Type': 'application/json',
  },


 });
let data=await res.json();
return data;
  }
  catch(err){
    console.log("error")
    return err;}
}
getToken();