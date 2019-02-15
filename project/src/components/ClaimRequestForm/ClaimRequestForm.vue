<template>
  <div class="hello">
    <el-form ref="form" :model="form" label-width="120px">
      <el-form-item label="First name">
        <el-input placeholder="First name" v-model="input10" clearable></el-input>
      </el-form-item>
      <el-form-item label="Last name">
        <el-input placeholder="Last name" v-model="input11" clearable></el-input>
      </el-form-item>
      <el-form-item label="Email">
        <el-input placeholder="Email address" v-model="input12" clearable></el-input>
      </el-form-item>
      <el-form-item label="Subject">
        <el-input type="textarea" autosize placeholder="Subject" v-model="textarea2"></el-input>
      </el-form-item>
      <div style="margin: 20px 0;"></div>
      <el-form-item>
        <el-input
          type="textarea"
          :autosize="{ minRows: 2, maxRows: 4}"
          placeholder="Input content"
          v-model="textarea3"
        ></el-input>
      </el-form-item>
      <!-- `checked` should be true or false -->
      <el-checkbox v-model="checked">Agreement</el-checkbox>
      <el-row>
        <el-button type="primary" @click="dialogVisible = true
        ">Submit</el-button>
      </el-row>
      <el-dialog
        title="Confirm information"
        :visible.sync="dialogVisible"
        width="30%"
        :before-close="handleClose"
      >
        <div class="confirmation">First name: {{input10}}</div>
        <div class="confirmation">Last name: {{input11}}</div>
        <div class="confirmation">Email: {{input12}}</div>
        <div class="confirmation">Subject: {{textarea2}}</div>
        <div class="confirmation">Content: {{textarea3}}</div>
        <span slot="footer" class="dialog-footer">
          <el-button @click="dialogVisible = false">Cancel</el-button>
          <el-button type="primary" @click="dialogVisible = false">Confirm</el-button>
        </span>
      </el-dialog>
    </el-form>
  </div>
</template>

<script src='./ClaimRequestForm.js'>
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style  src='./ClaimRequestForm.css' scoped>
</style>
