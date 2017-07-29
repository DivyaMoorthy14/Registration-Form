# Registration-Form
<html>
<head>

<script language="javascript">
   function onvalidate(){
     var fname=document.regform.fname.value;
     var userid=document.regform.userid.value;
     var pwd=document.regform.pwd.value;
     var dob=document.regform.dob.value;
     var country=document.regform.country.value;
     var zip=document.regform.zip.value;
    
    
     if(fname==null || fname==""){
       alert("First name cannot be empty");
       return false;
     }
    
     if(userid==null || userid==""){
       alert("Please mention the userid for further login to the website");
       return false;
     }

     if(pwd.length < 6 || pwd.length > 15){
       alert("Password should be greater than 6 characters and less than 15 characters");
       return false;
     }

     if(dob==null || dob==""){
       alert("Please mention your Date of Birth");
       return false;
     }

     if(country==null || country==""){
       alert("Select the country");
       return false;
     }

     if(zip==null || zip==""){
       alert("Entry the zip code");
       return false;
     }
    return true;
   
   }   
 
  
</script>
 </head>

<body>
 <h1>REGISTRATION FORM</h1>
  <form name= "regform" method="post" action="welcome.html" onsubmit ="return onvalidate()">
     <table>
       <tr>
         <td> First Name: </td>
         <td> <input type="text" name="fname"></td>
       </tr>

       <tr>
         <td> Last Name: </td>
         <td> <input type="text" name="lname"></td>
       </tr>

       <tr>
         <td> User Id: </td>
         <td> <input type="text" name="userid"></td>
       </tr>

       <tr>
         <td> Password: </td>
         <td> <input type="password" name="pwd"></td>
       </tr>

       <tr>
         <td> Gender: </td>
         <td> <input type="radio" name="female" value="Female"><span>Female</span>
         <input type="radio" name="male" value="Male"><span>Male</span></td>
       </tr>

       <tr>
         <td> Date of Birth: </td>
         <td> <input type="text" name="dob"></td>
       </tr>

       <tr>
         <td> <label for="country">Country:</label></td>
         <td>
        <select name="country">
           <option selected="" value="Default">(Please select a country)</option>
           <option value="Aus">Australia</option>
           <option value="canada">Canada</option>
           <option value="Ind">India</option>
           <option value="Indo">Indonesia</option>
           <option value="ussr">Russia</option>
           <option value="us">USA</option>
           <option value="uk">UK</option>
        </select>
         </td>
       </tr>

       <tr>
         <td> Zip Code: </td>
         <td> <input type="text" name="zip"></td>
       </tr>

       <tr>
         <td> <label>Language:</label></td>
         <td> <input type="checkbox" name="eng" value="en" checked> <span> English </span>
          <input type="checkbox" name="fre" value="french"> <span> French </span>
          <input type="checkbox" name="span" value="spanish"> <span> Spanish </span></br>
          <input type="checkbox" name="hin" value="hindi"> <span> Hindi </span>
          <input type="checkbox" name="sans" value="sanskirt"> <span> Sanskrit </span></br>
          <input type="checkbox" name="rus" value="russian"> <span> Russian </span>
          <input type="checkbox" name="jap" value="japanese"> <span> Japanese </span>
          <input type="checkbox" name="kor" value="korean"> <span> Korean </span></td>
       </tr>

       <tr>
         <td> <button type="submit" name="submit" > Register </td>
         <td> <button type="reset" name="reset"> Reset</td>
       </tr>
    </table>
  </form>

</body>
</html>
