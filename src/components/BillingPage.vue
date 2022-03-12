<template>
<!-- Sidebar Section-->
<input type="checkbox" id="nav-toggle">
    <div class="sidebar">
        <div class="sidebar-brand">
           <h2>bOnline</h2>
        </div>
        <div class="sidebar-menu">
            <ul>
                <li>
                    <a href="">
                        <fa icon="home" /><span>Home</span>
                    </a>
                </li>
                <li>
                    <a href="" class="active">
                        <fa icon="credit-card" /><span>Billing</span>
                    </a>
                </li>
            </ul>
        </div> 
    </div>
    <!--MAIN CONTENT -->
    <div class="main-content">
        <header>
          <h2>
              <label for="nav-toggle">
                  <fa icon="bars"/>
                      
              </label>
              
          </h2>
      <div class="bell">
          <fa icon="bell" />
      </div>
      <!-- USER WRAPPER -->
      <div class="user-wrapper">
          <fa icon="circle-user" width="30px" height="30px" class="circle"/> 
          <div>
              <h4>Kelvin Kayamba</h4>
              <small>kelkayamba@gmail.com</small>
          </div>
      </div>
        </header>
        <!--SECOND BAR -->
        <div id="title">
            <h2>Billing</h2>
            <small>Overview of your account</small>
        </div>
        <main>
            <!-- CARDS -->
            <div class="cards">
               <div class="card-single">
                   <div>
                       <h1>macrotel phone</h1>
                       <span>Account ID: 47000</span>
                   </div>   
                   <div>
                       <h6>active</h6>
                   </div>
               </div>

               <div class="card-single">
                   <div>
                       <h1>mobis valium</h1>
                       <span>Account ID: 90789</span>
                   </div>   
                   <div>
                       <h6>active</h6>
                   </div>
               </div>

               <div class="card-single">
                   <div>
                       <h1>jereme Hunt 3 </h1>
                       <span>Account ID: 47789</span>
                   </div>   
                   <div>
                       <h6>active</h6>
                   </div>
               </div>
            </div><!--END CARD -->
            <!--PAYMENT DETAILS -->
            <div class="recent-grid">
                 <div class="project">
                    <div class="card">
                        <div class="card-header">
                            <h2>Payment details</h2><br>
                        </div>
                        <p>View details of your next invoice and payment method</p>
                        <hr>
                        <div class="card-body">
                           <h6>Next invoice:10 March 2022</h6>
                           <div class="details">
                            <div class="card-balance"><br>
                                <h5>Current Balance</h5><br>
                                <h2>$59.00</h2>
                                <p><fa icon="lock"/> This is a secure 256-bit SSL encrypted payment.You're safe
                                </p><br>
                              <button>Pay Now</button><br><br>
                            </div>
                            <div class="card-method"><br>
                                <h5>Payment method</h5><br>
                                <p><fa icon="lightbulb"/>  Guide:To manage your payments
                                                            more easily.
                                                            We recommend Switching 
                                                            to direct debit</p><br>
                             <button>Switch to direct debit</button>
                            </div>
                           </div><!--details added by me -->
                           <br><br>
                        </div>
                    </div>
                 </div>

                 <div class="product">
                     <div class="card">
                        <div class="card-header">
                             <h2>My products</h2>  
                        </div>
                        <p>All your product at a glance</p><hr>
                        <div class="card-body ">
                         <p><fa icon="phone"/><span>Volp-987666</span></p><br><hr>
                           <br> <p><fa icon="share-nodes"/><span>Fibire-SW12RT</span></p><br><hr>
                           <br> <p><fa icon="book"/><span>www.kel.com</span></p><br><hr>
                        </div>
                     </div>
                 </div>
            </div><!-- END PAYMENT DETAILS -->
            <!-- TABLE -->
            <div class="table-responsive">
            <div class="card-table">
                <div class="card-head"><br>
                            <h2>Billing History</h2><br>
                            <p>Customers Information</p>
                        </div><hr>
                        <table width="100">
                            <thead>
                                <tr>
                                    <td>ACC ID</td>
                                    <td>Firstname</td>
                                    <td>Lastname</td>
                                    <td>Email</td>
                                    <td>BusinessName</td>
                                    <td>Address1</td>
                                    <td>Address2</td>
                                    <td>MobileNo</td>
                                </tr>
                            </thead>
                            <tbody v-for="item in data" :key="item.id">
                                <tr>
                                    <td>{{item.account_id}}</td>
                                    <td>{{item.first_name}}</td>
                                    <td>{{item.last_name}}</td>
                                    <td>{{item.email_address}}</td>
                                    <td>{{item.business_name}}</td>
                                    <td>{{item.address_line_one}}</td>
                                    <td>{{item.address_line_two}}</td>
                                    <td>{{item.mobile_number}}</td>
                                </tr>
                            </tbody>
                        </table>
                        
            </div>
            </div>
        </main>
    </div>
</template>
<script>
import Data from './/Data.json'
export  default{
    data(){
        return{
            data:Data
        }
    }
}
</script>