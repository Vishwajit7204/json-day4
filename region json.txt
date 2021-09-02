var request=new XMLHttpRequest();
request.open('GET','https://restcountries.eu/rest/v2/all',true);
request.send();
request.onload=function()
{
    var data=JSON.parse(request.response);
    console.log(data);
for (var i in data)
console.log(data [i].name,data [i].region,data [i].subregion,data [i].regionblock);
}