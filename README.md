MVC4-ValidateJsonAntiForgeryToken
=================================

Validates Html.AntiForgeryToken from header of AJAX request.

    @Html.AntiForgeryToken()

    //Set up Ajax request
    var headers = {};
    headers["__RequestVerificationToken"] = $('[name=__RequestVerificationToken]').val();
    $.ajax({
        type: "POST", //Type must be POST
        url: url,
        dataType: "json",
        headers: headers,
