<template>
    <div class="container-fluid">
       
        <section class="content">
      
            <h3 class="" style="color:gray">Dashboard</h3>
         
          <br>
        <!-- Info boxes -->
        <div class="row">
          <div class="col-12 col-sm-6 col-md-3">
            <div class="info-box">
              <span class="info-box-icon bg-info elevation-1"><i class="fas fa-box-open"></i></span>

              <div class="info-box-content">
                <span class="info-box-text">Expired <br/> Domain</span>
                <span class="info-box-number">
                  {{domain}}
                  <!-- <small>%</small> -->
                </span>
              </div>
              <!-- /.info-box-content -->
            </div>
            <!-- /.info-box -->
          </div>
          <!-- /.col -->
          <div class="col-12 col-sm-6 col-md-3">
            <div class="info-box mb-3">
              <span class="info-box-icon bg-danger elevation-1"><i class="far fa-address-card"></i></i></span>

              <div class="info-box-content">
                <span class="info-box-text">Uncomplete <br/>Registration</span>
                <span class="info-box-number">{{regstatus}}</span>
              </div>
              <!-- /.info-box-content -->
            </div>
            <!-- /.info-box -->
          </div>
          <!-- /.col -->

          <!-- fix for small devices only -->
          <div class="clearfix hidden-md-up"></div>

          <div class="col-12 col-sm-6 col-md-3">
            <div class="info-box mb-3">
              <span class="info-box-icon bg-success elevation-1"><i class="fas fa-users"></i></span>

              <div class="info-box-content">
                <span class="info-box-text">Active <br/> Users</span>
                <span class="info-box-number">{{activuser}}</span>
              </div>
              <!-- /.info-box-content -->
            </div>
            <!-- /.info-box -->
          </div>
          <!-- /.col -->
          <div class="col-12 col-sm-6 col-md-3">
            <div class="info-box mb-3">
              <span class="info-box-icon bg-warning elevation-1"><i class="fas fa-users"></i></span>

              <div class="info-box-content">
                <span class="info-box-text">Total <br/> User</span>
                <span class="info-box-number">{{tuser}}</span>
              </div>
              <!-- /.info-box-content -->
            </div>
            <!-- /.info-box -->
          </div>
          <!-- /.col -->
        </div>
        <!-- /.row -->

        <div class="row">
          <div class="col-md-12">
           
            <!-- /.card -->
          </div>
          <!-- /.col -->
        </div>
        <!-- /.row -->

        <!-- Main row -->
        <div class="row">
          <!-- Left col -->
          <div class="col-md-8">
           
            <!-- /.card -->
            <div class="row">
             
              <!-- /.col -->

         
              <!-- /.col -->
            </div>
            <!-- /.row -->

            <!-- TABLE: LATEST ORDERS -->
            <div class="card">
              <div class="card-header border-transparent">
                <h3 class="card-title">Latest Orders</h3>
              </div>
              <!-- /.card-header -->
              <div class="card-body p-0">
                <div class="table-responsive">
                  <table class="table m-0">
                    <thead>
                    <tr>
                      <th>Order ID</th>
                      <th>Clint ID</th>
                      <th>Domian Name</th>
                      <th>Status</th>
                    </tr>
                    </thead>
                    <tbody>

                      <!-- badge-success
                            badge-warning
                            badge badge-danger
                            badge badge-info
                       -->
                      <tr v-for="order in orders" :key="order.id">
                      <td><a href="javascript:void(0)">{{order.orderId}}</a></td>
                      <td>{{order.generatedschoolID}}</td>
                      
                      <td>
                        <div class="sparkbar" data-color="#00a65a" data-height="20">{{order.domain}}</div>
                      </td>
                      <td><span class="badge badge-danger">{{order.status}}</span></td>
                    </tr>
                    
                    </tbody>
                  </table>
                </div>
                <!-- /.table-responsive -->
              </div>
              <!-- /.card-body -->
              <div class="card-footer clearfix">
                <!-- <a href="javascript:void(0)" class="btn btn-sm btn-info float-left">Place New Order</a> -->
                <a href="javascript:void(0)" class="btn btn-sm btn-secondary float-right">View All Orders</a>
              </div>
              <!-- /.card-footer -->
            </div>
            <!-- /.card -->
          </div>
          <!-- /.col -->

          <div class="col-md-4">
            <!-- Info Boxes Style 2 -->
            
           
            <div class="info-box mb-3 bg-info">
              <span class="info-box-icon"><i class="far fa-comment"></i></span>

              <div class="info-box-content">
                <span class="info-box-text">Direct Messages</span>
                <span class="info-box-number text-danger">6 unread</span>
              </div>
              <!-- /.info-box-content -->
            </div>
            <!-- /.info-box -->

      
            <!-- /.card -->

            <!-- PRODUCT LIST -->
       
            <!-- /.card -->
          </div>
          <!-- /.col -->
        </div>
        <!-- /.row -->
      <!--/. container-fluid -->
    </section>
    </div>
</template>

<script>
    export default {
      data(){

      },
      props:['domain','tuser','regstatus','activuser','orders'],
      methods:{
       
      },
        mounted() {
          
        }
    }
</script>
