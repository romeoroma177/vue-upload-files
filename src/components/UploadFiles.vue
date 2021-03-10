<template>
<div>
    <div v-if="currentFile" class="progress">
      <div
        class="progress-bar progress-bar-info progress-bar-striped"
        role="progressbar"
        :aria-valuenow="progress"
        aria-valuemin="0"
        aria-valuemax="100"
        :style="{ width: progress + '%' }"
      >
        {{ progress }}%
      </div>
    </div>
<form>
  <div class="form-row">
    <div class="col-md-4 mb-3">
      <label for="validationDefault01">Travel ID Number</label>
      <input type="number" class="form-control" id="validationDefault01" placeholder="Travel ID Number" value="" required>
    </div>
    <div class="col-md-4 mb-3">
      <label for="validationDefault02">Route Number</label>
      <input type="number" class="form-control" id="validationDefault02" placeholder="Route Number" value="" required>
    </div>
    <div class="col-md-4 mb-3">
      <label for="validationDefault02">Segment Number</label>
      <input type="number" class="form-control" id="validationDefault02" placeholder="Segment Number" value="" required>
    </div>
  </div>
  <div class="form-row">
<div class="col-md-3 mb-3">

    <label>Route Type</label>
  <select class="custom-select my-1 mr-sm-2" id="inlineFormCustomSelectPref">
    <option selected>RSSO to CO</option>
    <option value="1">RSSO to CO
</option>
    <option value="2">RSSO to Other RSSO</option>
    <option value="3">RSSO to PSO of the same Region</option>
    <option value="3">RSSO to Provincial LGU Offices of the same Region</option>
    <option value="3">PSO to CO</option>
    <option value="3">PSO to PSO of the same Region</option>
    <option value="3">PSO to City/Municipal Hall of the same Province</option>
    <option value="3">City/Municial Hall to Other City/Municipal Hall of the same Province</option>
    <option value="3">City/Municipal Hall to Barangay Hall</option>
    <option value="3">Barangay Hall to Other Barangay Hall of the same Province</option>
  </select>


</div>
<div class="col-md-3 mb-3">

    <label>Road Type</label>
  <select class="custom-select my-1 mr-sm-2" id="inlineFormCustomSelectPref">
    <option selected>Not applicable
</option>
    <option value="1">National road
</option>
    <option value="2">Provincial road</option>
    <option value="3">City/Municipal road</option>
    <option value="3"> Barangay road</option>
    <option value="3">Trail</option>
    <option value="3">Others, specify</option>
    
  </select>


</div>

<div class="col-md-3 mb-3">

    <label>Topographical</label>
  <select class="custom-select my-1 mr-sm-2" id="inlineFormCustomSelectPref">
    <option selected>Not applicable</option>
    <option value="1">Plain
</option>
    <option value="2">Terrain</option>
    <option value="3">Mountainous</option>
    <option value="3">Hill</option>
    <option value="3">River</option>
    <option value="3">Lake</option>
    <option value="3">Sea/ocean</option>
    <option value="3">Valley</option>
    <option value="3">Others, specify</option>
    
  </select>


</div>
<div class="col-md-3 mb-3">

    <label>Mode of Travel</label>
  <select class="custom-select my-1 mr-sm-2" id="inlineFormCustomSelectPref">
    <option selected> Airplane</option>
    <option value="1">Bus
</option>
    <option value="2">Jeep</option>
    <option value="3">Van</option>
    <option value="3">Tricycle</option>
    <option value="3">Habal-habal</option>
    <option value="3">Horse</option>
    <option value="3">Pump Boat</option>
    <option value="3">Fast Craft</option>
    <option value="3">Roro</option>
    <option value="3">PNR</option>
    <option value="3">LRT/MRT</option>
    <option value="3">Walk</option>
    <option value="3">Others, specify</option>
  </select>


</div>
<label>WRITE THE CODE CORRESPONDING TO THE ANSWER.

</label>
<div class="col-md-10 mb-3">

    
  <select class="custom-select my-1 mr-sm-2" id="inlineFormCustomSelectPref">
    <option selected>1</option>
    <option value="1">1
</option>
    <option value="2">2</option>
    <option value="3">3</option>
    <option value="3">4</option>
    <option value="3">5</option>
    <option value="3">6</option>
    <option value="3">7</option>
    <option value="3">8</option>
    <option value="3">9</option>
    <option value="3">10</option>
  </select>
</div>

<div class="col-md-6 mb-3">

    <label>Origin</label>
  <select class="custom-select my-1 mr-sm-2" id="inlineFormCustomSelectPref">
    <option selected>PSA - BARMM (RSSO) - COTABATO CITY
</option>
    <option value="1">PSA - BARMM (RSSO) - COTABATO CITY

</option>
    <option value="2">PSA - BARMM (RSSO) - COTABATO CITY - COTABATO CITY
- ZAMBOANGA CITY

</option>
    <option value="3">PSA - BARMM (RSSO) - COTABATO CITY - COTABATO CITY
- ZAMBOANGA CITY
</option>
    <option value="3">PSA - BARMM (RSSO) - COTABATO CITY
 - RSSO BARMM - COTABATO CITY
 - RSSO BARMM - COTABATO CITY
</option>
    <option value="3">PSA - TAWI-TAWI (PSO)
 - BONGAO
 - ZAMBOANGA CITY
</option>
    <option value="3">PSA - TAWI-TAWI (PSO)
 - BONGAO
 -ZAMBOANGA CITY </option>
    <option value="3">PSA - PROVINCIAL OFFICE (PSO)
 - BONGAO
 - ZAMBOANGA CITY
</option>
    <option value="3">BONGAO
 - ZAMBOANGA CITY
 - MANILA
</option>
    <option value="3">PUERTO PRINCESA CITY (VIA BROOKE'S POINT)
</option>
    <option value="3">PSA - PROVINCIAL OFFICE (PSO)
</option>
<option value="3">PUERTO PRINCESA CITY (VIA BROOKE'S POINT)
</option>
<option value="3">BONGAO

</option>
<option value="3">CITY/MUNICIPAL HALL

</option>
<option value="3">SIMUNOL MUNICIPAL HALL 

</option>
<option value="3">TURTLE ISLAND MUNICIPAL HALL

</option>
<option value="3">CITY/MUNICIPAL HALL1

</option>
<option value="3">BONGAO MUNICIPAL HALL

</option>
<option value="3">IPIL BARANGAY HALL

</option>
<option value="3">LAMION BARANGAY HALL

</option>

  </select>



</div>

<div class="col-md-6 mb-3">

    <label>Destination</label>
  <select class="custom-select my-1 mr-sm-2" id="inlineFormCustomSelectPref">
    <option selected>PSA - Central Office (CO)
</option>
    <option value="1">Other PSA - RSSO IX - ZAMBOANGA CITY


</option>
    <option value="2">PSA - TAWI-TAWI (PSO)
</option>
    <option value="3">PSA - BASILAN (PSO)
</option>
    <option value="3">LANAO DEL SUR - PROVINCIAL LGU OFFICES
</option>
    <option value="3">PSA - CENTRAL OFFICE (CO)
</option>
    <option value="3">PSA - BASILAN (PSO)
</option>
    <option value="3">MAPUN MUNICIPAL HALL
</option>
    <option value="3">CITY/MUNICIPAL HALL OF THE SAME PROVINCE
</option>
    <option value="3">OTHER CITY/MUNICIPAL HALL OF THE SAME PROVINCE
</option>
    <option value="3">KAMAGONG BARANGAY HALL
</option>
  </select>



</div>


</div>
  <div class="form-row">
    <div class="col-md-4 mb-3">
      <label for="validationDefault03">Duration of Travel(mins)</label>
      <input type="number" class="form-control" id="validationDefault03" placeholder="Minutes" required>
    </div>
    <div class="col-md-3 mb-3">
      <label for="validationDefault04">Frequency of Trips</label>
      <input type="text" class="form-control" id="validationDefault04" placeholder="Day/Week" required>
    </div>
    <div class="col-md-3 mb-3">
      <label for="validationDefault05">Fare(one way)</label>
      <input type="number" class="form-control" id="validationDefault05" placeholder="Fare" required>
    </div>
    

    
  </div>
  <div class="form-group">
    <div class="form-check">
      
      <label class="form-check-label" for="invalidCheck2">
        
      </label>
    </div>
  </div>
  <button class="btn btn-primary" type="submit">Submit form</button>
</form>
    <label class="btn btn-default">
      <input type="file" ref="file" @change="selectFile" />
    </label>

    <button class="btn btn-success" :disabled="!selectedFiles" @click="upload">
      Upload
    </button>

    <div class="alert alert-light" role="alert">{{ message }}</div>

    <div class="card">
      <div class="card-header">List of Files</div>
      <ul class="list-group list-group-flush">
        <li
          class="list-group-item"
          v-for="(file, index) in fileInfos"
          :key="index"
        >
          <a :href="file.url">{{ file.name }}</a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
import UploadService from "../services/UploadFilesService";

export default {
  name: "upload-files",
  data() {
    return {
        selectedFiles: undefined,
      currentFile: undefined,
      progress: 0,
      message: "",

      fileInfos: []

    };
  },
  methods: {

      selectFile() {
      this.selectedFiles = this.$refs.file.files;
    },

    upload() {
      this.progress = 0;

      this.currentFile = this.selectedFiles.item(0);
      UploadService.upload(this.currentFile, event => {
        this.progress = Math.round((100 * event.loaded) / event.total);
      })
        .then(response => {
          this.message = response.data.message;
          return UploadService.getFiles();
        })
        .then(files => {
          this.fileInfos = files.data;
        })
        .catch(() => {
          this.progress = 0;
          this.message = "Could not upload the file!";
          this.currentFile = undefined;
        })

      this.selectedFiles = undefined;
    }
  
  },

  mounted() {
    UploadService.getFiles().then(response => {
      this.fileInfos = response.data;
    });
  }
};
</script>