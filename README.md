
<div id="app">
    <div class="header">
      <img src="logo.png" alt="logo" class="logo">
      <div class="title">湖南信息职业技术学院选课系统</div>
      <img src="logo1.png" alt="logo1" class="logo1">
    </div>

    <div class="form">
      <div class="title">退选课程</div>
      <form @submit.prevent="submitWithdrawForm">
        <label for="courseScope">课程范围：</label>
        <select v-model="courseScope" name="courseScope" id="courseScope">
          <option value="major">主修</option>
          <option value="minor">辅修</option>
        </select>

        <label for="classSelection">班级选择：</label>
        <select v-model="classSelection" name="classSelection" id="classSelection">
          <option value="software01">软件01班</option>
          <option value="software02">软件02班</option>
          <option value="mobile01">移动01班</option>
        </select>

        <label for="courseSelection">课程选择：</label>
        <select v-model="courseSelection" name="courseSelection" id="courseSelection">
          <option value="h5">H5移动端开发</option>
          <option value="java">JAVA开发</option>
          <option value="softwareTest">软件测试</option>
        </select>

        <button type="submit">提交退选申请</button>
      </form>

      <div v-if="withdrawFormSubmitted">
        <p>课程（{{ courseSelection }}）退选成功。</p>
      </div>
    </div>

    <div class="form">
      <div class="title">重修课程</div>
      <form @submit.prevent="submitRetakeForm">
        <label for="courseScopeRetake">课程范围：</label>
        <select v-model="courseScopeRetake" name="courseScopeRetake" id="courseScopeRetake">
          <option value="major">主修</option>
          <option value="minor">辅修</option>
        </select>
