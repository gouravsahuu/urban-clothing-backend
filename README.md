# Urban Clothing Backend

This is a backend repository for a fashion ecommerce website "Urban Clothing".

Urban Clothing is a luxury fashion e-commerce website. It currently designs and distributes ready to wear apparels, including trench coats (for which it is most famous), leather accessories, and footwear.

Backend deployed link - https://lucky-ruby-puffer.cyclic.app/

Frontend deployed link - https://fluffy-kelpie-9b2a37.netlify.app/

## Routes

### API's

    User Routes

        /user/register

            method : POST
            body :  {
                        name : string,
                        email : string (unique),
                        password : string,
                        gender : string,
                        phone_number : number
                    }
            success-response : "User registered Successfully"

        /user/login

            method : POST
            body :  {    
                        email : string,
                        password : string
                    }
            success-response : "Login Success", token

        /user/all

            method : "GET"
            success-response : returns all users that are registered

        /user/id/:id

            method : "GET"
            success-response : returns user with a particular ID provided


    Product Routes

        /product/all

            method : "GET"
            success-response : returns all products that are in inventory

        /product/add

            method : "POST"
            body :  {
                        title : string,
                        price : string,
                        image : string,
                        colour : string,
                        category : string,
                        inStock : boolean,
                        rating : number
                    }
            success-response : "Product successfully added"

        /product/delete/:id

            method : "DELETE"
            success-response : deletes product with a particular ID provided
            message : "Product Deleted"