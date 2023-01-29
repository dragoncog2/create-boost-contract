<template>
  <div class="container mx-auto">
    <div class="mx-auto max-w-7xl py-6 sm:px-6 lg:px-8">
      <div class="mt-10 sm:mt-0">
        <div class="md:grid md:grid-cols-1 md:gap-6">
          <div class="">
            <div class="px-4 sm:px-0">
              <h3
                class="text-center text-lg font-medium leading-6 text-gray-900"
              >
                Tạo hợp đồng Boostcommerce
              </h3>
            </div>
          </div>
          <div class="">
            <form id="myForm">
              <div class="overflow-hidden shadow sm:rounded-md">
                <div class="bg-white px-4 py-5 sm:p-6">
                  <div class="grid grid-cols-12 gap-6">
                    <div class="col-span-12">
                      <label
                        for="contract_file"
                        class="block text-sm font-medium text-gray-700"
                        >Loại file hợp đồng</label
                      >
                      <select
                        v-model="contractFile"
                        name="contract_file"
                        class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500 sm:text-sm"
                      >
                        <option value="probation">Hợp đồng thử việc</option>
                        <option value="fulltime">Hợp đồng chính thức</option>
                        <option value="appendix">Phụ lục hợp đồng</option>
                        <option value="training">Thoả thuận tham gia đào tạo</option>
                      </select>
                    </div>
                    <div class="col-span-6 sm:col-span-3 lg:col-span-3">
                      <label
                        class="block text-sm font-medium text-gray-700"
                        >Mã số hợp đồng</label
                      >
                      <input
                        type="text"
                        name="contract_id"
                        placeholder="Mã số hợp đồng"
                        class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500 sm:text-sm"
                      />
                    </div>
                    <div class="col-span-6 sm:col-span-3 lg:col-span-3">
                      <label
                        class="block text-sm font-medium text-gray-700"
                        >Ngày viết hợp đồng</label
                      >
                      <input
                        type="date"
                        name="contract_date"
                        class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500 sm:text-sm"
                      />
                    </div>
                    <div class="col-span-6 sm:col-span-3 lg:col-span-3">
                      <label
                        class="block text-sm font-medium text-gray-700"
                        >Ngày bắt đầu</label
                      >
                      <input
                        type="date"
                        name="start_date"
                        class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500 sm:text-sm"
                      />
                    </div>
                    <div v-if="contractFile === 'probation' || contractFile === 'fulltime'" class="col-span-6 sm:col-span-3 lg:col-span-3">
                      <label
                        class="block text-sm font-medium text-gray-700"
                        >Ngày kết thúc</label
                      >
                      <input
                        type="date"
                        name="end_date"
                        class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500 sm:text-sm"
                      />
                    </div>
                    <div v-if="contractFile === 'appendix'" class="col-span-6 sm:col-span-6 lg:col-span-6">
                      <label
                        class="block text-sm font-medium text-gray-700"
                        >Mã số hợp đồng lao động</label
                      >
                      <input
                        type="text"
                        name="labor_contract_id"
                        placeholder="Mã số hợp đồng lao động"
                        class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500 sm:text-sm"
                      />
                    </div>
                    <div v-if="contractFile === 'appendix'" class="col-span-6 sm:col-span-6 lg:col-span-6">
                      <label
                        class="block text-sm font-medium text-gray-700"
                        >Ngày ký hợp đồng lao động</label
                      >
                      <input
                        type="date"
                        name="contract_date_sign"
                        class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500 sm:text-sm"
                      />
                    </div>
                    <div v-if="contractFile === 'appendix'" class="col-span-6 sm:col-span-3 lg:col-span-3">
                      <label
                        class="block text-sm font-medium text-gray-700"
                        >Chức danh cũ</label
                      >
                      <input
                        type="text"
                        name="old_title"
                        placeholder="Chức danh cũ"
                        class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500 sm:text-sm"
                      />
                    </div>
                    <div v-if="contractFile === 'appendix'" class="col-span-6 sm:col-span-3 lg:col-span-3">
                      <label
                        class="block text-sm font-medium text-gray-700"
                        >Chức danh cũ (tiếng anh)</label
                      >
                      <input
                        type="text"
                        name="old_title_eng"
                        placeholder="Chức danh cũ (tiếng anh)"
                        class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500 sm:text-sm"
                      />
                    </div>
                    <div v-if="contractFile === 'appendix'" class="col-span-6 sm:col-span-3 lg:col-span-3">
                      <label
                        class="block text-sm font-medium text-gray-700"
                        >Chức danh mới</label
                      >
                      <input
                        type="text"
                        name="new_title"
                        placeholder="Chức danh mới"
                        class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500 sm:text-sm"
                      />
                    </div>
                    <div v-if="contractFile === 'appendix'" class="col-span-6 sm:col-span-3 lg:col-span-3">
                      <label
                        class="block text-sm font-medium text-gray-700"
                        >Chức danh mới (tiếng anh)</label
                      >
                      <input
                        type="text"
                        name="new_title_eng"
                        placeholder="Chức danh mới (tiếng anh)"
                        class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500 sm:text-sm"
                      />
                    </div>
                    <div v-if="contractFile === 'appendix'" class="col-span-6 sm:col-span-6 lg:col-span-6">
                      <label
                        class="block text-sm font-medium text-gray-700"
                        >Lương cũ</label
                      >
                      <input
                        type="text"
                        name="old_salary"
                        placeholder="Lương cũ"
                        class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500 sm:text-sm"
                      />
                    </div>
                    <div v-if="contractFile === 'appendix'" class="col-span-6 sm:col-span-6 lg:col-span-6">
                      <label
                        class="block text-sm font-medium text-gray-700"
                        >Lương mới</label
                      >
                      <input
                        type="text"
                        name="new_salary"
                        placeholder="Lương mới"
                        class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500 sm:text-sm"
                      />
                    </div>
                    <div v-if="contractFile === 'training'" class="col-span-6 sm:col-span-6 lg:col-span-6">
                      <label
                        class="block text-sm font-medium text-gray-700"
                        >Tên khoá học</label
                      >
                      <input
                        type="text"
                        name="training_course_title"
                        placeholder="Tên khoá học"
                        class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500 sm:text-sm"
                      />
                    </div>
                    <div v-if="contractFile === 'training'" class="col-span-6 sm:col-span-6 lg:col-span-6">
                      <label
                        class="block text-sm font-medium text-gray-700"
                        >Tên khoá học (tiếng anh)</label
                      >
                      <input
                        type="text"
                        name="training_course_title_eng"
                        placeholder="Tên khoá học (tiếng anh)"
                        class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500 sm:text-sm"
                      />
                    </div>
                    <div v-if="contractFile === 'training'" class="col-span-6 sm:col-span-4 lg:col-span-4">
                      <label
                        class="block text-sm font-medium text-gray-700"
                        >Chứng chỉ</label
                      >
                      <input
                        type="text"
                        name="certificate"
                        placeholder="Chứng chỉ"
                        class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500 sm:text-sm"
                      />
                    </div>
                    <div v-if="contractFile === 'training'" class="col-span-6 sm:col-span-4 lg:col-span-4">
                      <label
                        class="block text-sm font-medium text-gray-700"
                        >Chứng chỉ (tiếng anh)</label
                      >
                      <input
                        type="text"
                        name="certificate_eng"
                        placeholder="Chứng chỉ (tiếng anh)"
                        class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500 sm:text-sm"
                      />
                    </div>
                    <div v-if="contractFile === 'training'" class="col-span-6 sm:col-span-4 lg:col-span-4">
                      <label
                        class="block text-sm font-medium text-gray-700"
                        >Học phí</label
                      >
                      <input
                        type="text"
                        name="fees"
                        placeholder="Học phí"
                        class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500 sm:text-sm"
                      />
                    </div>
                    <div class="col-span-12 sm:col-span-1">
                      <label
                        for="vocative"
                        class="block text-sm font-medium text-gray-700"
                        >Xưng hô</label
                      >
                      <select
                        type="text"
                        name="vocative"
                        class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500 sm:text-sm"
                      >
                        <option value="Ông">Ông</option>
                        <option value="Bà">Bà</option>
                      </select>
                    </div>
                    <div class="col-span-12 sm:col-span-5">
                      <label
                        for="full_name"
                        class="block text-sm font-medium text-gray-700"
                        >Họ và tên</label
                      >
                      <input
                        type="text"
                        name="full_name"
                        placeholder="Họ và tên"
                        class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500 sm:text-sm"
                      />
                    </div>

                    <div class="col-span-6 sm:col-span-3">
                      <label class="block text-sm font-medium text-gray-700"
                        >Ngày sinh</label
                      >
                      <input
                        type="date"
                        name="dob"
                        class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500 sm:text-sm"
                      />
                    </div>

                    <div class="col-span-6 sm:col-span-3">
                      <label
                        class="block text-sm font-medium text-gray-700"
                        >Tại</label
                      >
                      <input
                        type="text"
                        name="location_dob"
                        placeholder="Nơi sinh"
                        class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500 sm:text-sm"
                      />
                    </div>

                    <div class="col-span-9">
                      <label
                        class="block text-sm font-medium text-gray-700"
                        >Địa chỉ thường trú</label
                      >
                      <input
                        type="text"
                        name="residential_address"
                        placeholder="Địa chỉ thường trú"
                        class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500 sm:text-sm"
                      />
                    </div>

                    <div class="col-span-3">
                      <label
                        class="block text-sm font-medium text-gray-700"
                        >SDT</label
                      >
                      <input
                        type="text"
                        name="tel"
                        placeholder="Số điện thoại"
                        class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500 sm:text-sm"
                      />
                    </div>

                    <div v-if="contractFile === 'probation' || contractFile === 'fulltime'" class="col-span-12 sm:col-span-5">
                      <label
                        class="block text-sm font-medium text-gray-700"
                        >Chức vụ (tiếng việt)</label
                      >
                      <input
                        type="text"
                        name="job_position"
                        placeholder="Chức vụ"
                        class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500 sm:text-sm"
                      />
                    </div>

                    <div v-if="contractFile === 'probation' || contractFile === 'fulltime'" class="col-span-12 sm:col-span-5">
                      <label
                        class="block text-sm font-medium text-gray-700"
                        >Chức vụ (Tiếng Anh)</label
                      >
                      <input
                        type="text"
                        name="job_position_eng"
                        placeholder="Job position"
                        class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500 sm:text-sm"
                      />
                    </div>

                    <div v-if="contractFile === 'probation' || contractFile === 'fulltime'" class="col-span-12 sm:col-span-2">
                      <label
                        class="block text-sm font-medium text-gray-700"
                        >Số giờ làm việc</label
                      >
                      <input
                        type="text"
                        name="working_hours"
                        placeholder="Số giờ làm việc"
                        class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500 sm:text-sm"
                      />
                    </div>

                    <div v-if="contractFile === 'probation' || contractFile === 'fulltime'" class="col-span-12 sm:col-span-6">
                      <label
                        class="block text-sm font-medium text-gray-700"
                        >Loại hợp đồng lao động</label
                      >
                      <input
                        type="text"
                        name="labor_contract_type"
                        placeholder="Loại Hợp đồng lao động"
                        class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500 sm:text-sm"
                      />
                    </div>

                    <div v-if="contractFile === 'probation' || contractFile === 'fulltime'" class="col-span-12 sm:col-span-6">
                      <label
                        class="block text-sm font-medium text-gray-700"
                        >Loại hợp đồng lao động (Tiếng Anh)</label
                      >
                      <input
                        type="text"
                        name="labor_contract_type_eng"
                        placeholder="Labor contract type"
                        class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500 sm:text-sm"
                      />
                    </div>

                    <div class="col-span-6 sm:col-span-6 lg:col-span-3">
                      <label class="block text-sm font-medium text-gray-700"
                        >CMND/Hộ chiếu số</label
                      >
                      <input
                        type="text"
                        name="id_number"
                        placeholder="CMND/Hộ chiếu số"
                        title="Xin hãy nhập số ở đây"
                        class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500 sm:text-sm"
                      />
                    </div>

                    <div class="col-span-6 sm:col-span-6 lg:col-span-3">
                      <label class="block text-sm font-medium text-gray-700"
                        >Ngày cấp</label
                      >
                      <input
                        type="date"
                        name="issued_on"
                        placeholder="Ngày cấp"
                        class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500 sm:text-sm"
                      />
                    </div>

                    <div class="col-span-6 sm:col-span-3 lg:col-span-3">
                      <label
                        class="block text-sm font-medium text-gray-700"
                        >Tại</label
                      >
                      <input
                        type="text"
                        name="id_number_at"
                        placeholder="Nơi cấp"
                        class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500 sm:text-sm"
                      />
                    </div>

                    <div v-if="contractFile === 'probation' || contractFile === 'fulltime'" class="col-span-6 sm:col-span-3 lg:col-span-3">
                      <label
                        class="block text-sm font-medium text-gray-700"
                        >Lương</label
                      >
                      <input
                        type="text"
                        name="salary"
                        placeholder="Lương"
                        title="Xin hãy nhập số ở đây"
                        class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500 sm:text-sm"
                      />
                    </div>
                    <div class="col-span-6 sm:col-span-3 lg:col-span-3">
                      <label
                        class="block text-sm font-medium text-gray-700"
                        >Template HD {{ contractFile }}</label
                      >
                      <input
                        type="file"
                        id="doc1"
                        class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500 sm:text-sm"
                      />
                    </div>
                    <div v-if="contractFile === 'probation'" class="col-span-6 sm:col-span-3 lg:col-span-3">
                      <label
                        class="block text-sm font-medium text-gray-700"
                        >Template NDA</label
                      >
                      <input
                        type="file"
                        id="doc2"
                        class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500 sm:text-sm"
                      />
                    </div>
                  </div>
                </div>
                <div class="bg-gray-50 px-4 py-3 text-right sm:px-6">
                  <button
                    @click.stop.prevent="renderDoc(contractFile)"
                    class="inline-flex justify-center rounded-md border border-transparent bg-indigo-600 py-2 px-4 ml-2 text-sm font-medium text-white shadow-sm hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-indigo-500 focus:ring-offset-2"
                  >
                    HĐ {{ contractFile }}
                  </button>
                  <button v-if="contractFile === 'probation'"
                    @click.stop.prevent="renderDoc('nda')"
                    class="inline-flex justify-center rounded-md border border-transparent bg-indigo-600 py-2 px-4 ml-2 text-sm font-medium text-white shadow-sm hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-indigo-500 focus:ring-offset-2"
                  >
                    NDA
                  </button>
                </div>
              </div>
            </form>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Docxtemplater from "docxtemplater";
import PizZip from "pizzip";
import { saveAs } from "file-saver";

function getDataForm() {
  const form = document.getElementById("myForm");
  let formData = new FormData(form);
  formData = Object.fromEntries(formData);
  // add additional english fields & standard value
  // add filed contract_date_eng
  let contract_date_eng = new Date(formData.contract_date);
  const date = ordinal(contract_date_eng.getDate());
  const month_list = ["January","February","March","April","May","June","July","August","September","October","November","December"];
  const month = month_list[contract_date_eng.getMonth()];
  formData.contract_date_eng = `${month} ${date}, ${contract_date_eng.getFullYear()}`;

  formData.contract_date = new Date(formData.contract_date).toLocaleDateString("vi-VN", {
    year: "numeric",
    month: "long",
    day: "numeric",
  });

  formData.dob = new Date(formData.dob).toLocaleDateString('en-gb');
  formData.start_date = new Date(formData.start_date).toLocaleDateString('en-gb');
  formData.end_date = new Date(formData.end_date).toLocaleDateString('en-gb');
  formData.issued_on = new Date(formData.issued_on).toLocaleDateString('en-gb');

  formData.contract_date = "Ngày " + formData.contract_date.replace(',', ' Năm').replace('t', 'T');
  formData.vocative_eng = formData.vocative === 'Ông' ? 'Mr' : 'Ms';
  formData.sex = formData.vocative === 'Ông' ? 'Nam' : 'Nữ';
  formData.sex_eng = formData.vocative === 'Ông' ? 'Male' : 'Female';
  formData.full_name_eng = removeAccents(formData.full_name);
  formData.location_dob_eng = removeAccents(formData.location_dob);
  formData.residential_address_eng = removeAccents(formData.residential_address);
  formData.id_number_at_eng = removeAccents(formData.id_number_at);
  if (formData.salary) {
    formData.salary = new Intl.NumberFormat().format(parseInt(formData.salary.replace(/,/, '').replace(/\./, '')));
  }

  if (formData.old_salary) {
    formData.old_salary = new Intl.NumberFormat().format(parseInt(formData.old_salary.replace(/,/, '').replace(/\./, '')));
    formData.new_salary = new Intl.NumberFormat().format(parseInt(formData.new_salary.replace(/,/, '').replace(/\./, '')));
  }

  if (formData.fees) {
    formData.fees = new Intl.NumberFormat().format(parseInt(formData.fees.replace(/,/, '').replace(/\./, '')));
  }

  return formData;
}

function removeAccents(str) {
  return str.normalize('NFD')
            .replace(/[\u0300-\u036f]/g, '')
            .replace(/đ/g, 'd').replace(/Đ/g, 'D');
}

function ordinal(n) {
  const s = ["th", "st", "nd", "rd"];
  const v = n%100;
  return n + (s[(v-20)%10] || s[v] || s[0]);
}

export default {
  name: "MainApp",
  data() {
    return {
      contractFile: "probation",
    }
  },
  methods: {
    renderDoc(contract_type) {
      //console.log(JSON.parse(JSON.stringify(this.$data)));
      let dataForm = getDataForm();
      //console.log(dataForm);
      let docs = null;
      docs = document.getElementById("doc1");
      if (contract_type === 'nda') {
        docs = document.getElementById("doc2");
      }

      const reader = new FileReader();
      if (docs.files.length === 0) {
        alert("no selected files");
      }
      reader.readAsBinaryString(docs.files.item(0));

      reader.onerror = function (evt) {
        console.log("error reading file", evt);
        alert("error reading file" + evt);
      };

      reader.onload = function (evt) {
        const content = evt.target.result;
        const zip = new PizZip(content);
        const doc = new Docxtemplater(zip, {
          paragraphLoop: true,
          linebreaks: true,
        });
        doc.setData(dataForm);
        try {
          // render the document (replace all occurrences of {first_name} by John, {last_name} by Doe, ...)
          doc.render();
        } catch (error) {
          // The error thrown here contains additional information when logged with JSON.stringify (it contains a properties object containing all sub errors).
          // eslint-disable-next-line no-inner-declarations
          function replaceErrors(key, value) {
            if (value instanceof Error) {
              return Object.getOwnPropertyNames(value).reduce(function (
                error,
                key
              ) {
                error[key] = value[key];
                return error;
              },
              {});
            }
            return value;
          }
          console.log(JSON.stringify({ error: error }, replaceErrors));

          if (error.properties && error.properties.errors instanceof Array) {
            const errorMessages = error.properties.errors
              .map(function (error) {
                return error.properties.explanation;
              })
              .join("\n");
            console.log("errorMessages", errorMessages);
            // errorMessages is a humanly readable message looking like this :
            // 'The tag beginning with "foobar" is unopened'
          }
          throw error;
        }
        const out = doc.getZip().generate({
          type: "blob",
          mimeType:
            "application/vnd.openxmlformats-officedocument.wordprocessingml.document",
        });
        // Output the document using Data-URI
        if (contract_type === 'probation') {
          saveAs(out, dataForm.full_name_eng + " - Probation Contract.docx");
        } else if (contract_type === 'nda') {
          saveAs(out, dataForm.full_name_eng + " - NDA.docx");
        } else if (contract_type === 'fulltime') {
          saveAs(out, dataForm.full_name_eng + " - Labor Contract.docx");
        } else if (contract_type === 'appendix') {
          saveAs(out, "Appendix of Labor Contract - " + dataForm.full_name_eng + ".docx");
        } else if (contract_type === 'training') {
          saveAs(out, "Training Bond Agreement - " + dataForm.full_name_eng + ".docx");
        }
      };
    },
  },
};
</script>