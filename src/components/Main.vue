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
                Tạo hợp đồng
              </h3>
            </div>
          </div>
          <div class="">
            <form id="myForm">
              <div class="overflow-hidden shadow sm:rounded-md">
                <div class="bg-white px-4 py-5 sm:p-6">
                  <div class="grid grid-cols-12 gap-6">
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
                        >Ngày bắt đầu thử việc</label
                      >
                      <input
                        type="date"
                        name="start_date"
                        class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500 sm:text-sm"
                      />
                    </div>
                    <div class="col-span-6 sm:col-span-3 lg:col-span-3">
                      <label
                        class="block text-sm font-medium text-gray-700"
                        >Ngày kết thúc thử việc</label
                      >
                      <input
                        type="date"
                        name="end_date"
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

                    <div class="col-span-12">
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

                    <div class="col-span-12 sm:col-span-5">
                      <label
                        class="block text-sm font-medium text-gray-700"
                        >Chúc vụ (tiếng việt)</label
                      >
                      <input
                        type="text"
                        name="job_position"
                        placeholder="Chức vụ"
                        class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500 sm:text-sm"
                      />
                    </div>

                    <div class="col-span-12 sm:col-span-5">
                      <label
                        class="block text-sm font-medium text-gray-700"
                        >Chức vụ (tiếng anh)</label
                      >
                      <input
                        type="text"
                        name="job_position_eng"
                        placeholder="Job position"
                        class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500 sm:text-sm"
                      />
                    </div>

                    <div class="col-span-12 sm:col-span-2">
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

                    <div class="col-span-6 sm:col-span-3 lg:col-span-3">
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
                        >Template HD Thử Việc</label
                      >
                      <input
                        type="file"
                        id="doc1"
                        class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500 sm:text-sm"
                      />
                    </div>
                    <div class="col-span-6 sm:col-span-3 lg:col-span-3">
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
                    <div class="col-span-6 sm:col-span-3 lg:col-span-3">
                      <label
                        class="block text-sm font-medium text-gray-700"
                        >Template HD chính thức</label
                      >
                      <input
                        type="file"
                        id="doc3"
                        class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500 sm:text-sm"
                      />
                    </div>
                  </div>
                </div>
                <div class="bg-gray-50 px-4 py-3 text-right sm:px-6">
                  <button
                    @click="renderDoc"
                    class="inline-flex justify-center rounded-md border border-transparent bg-indigo-600 py-2 px-4 ml-2 text-sm font-medium text-white shadow-sm hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-indigo-500 focus:ring-offset-2"
                  >
                    HĐ thử việc
                  </button>
                  <button
                    @click="renderDoc"
                    class="inline-flex justify-center rounded-md border border-transparent bg-indigo-600 py-2 px-4 ml-2 text-sm font-medium text-white shadow-sm hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-indigo-500 focus:ring-offset-2"
                  >
                    NDA
                  </button>
                  <button
                    @click="renderDoc"
                    class="inline-flex justify-center rounded-md border border-transparent bg-indigo-600 py-2 px-4 ml-2 text-sm font-medium text-white shadow-sm hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-indigo-500 focus:ring-offset-2"
                  >
                    HD chính thức
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
  formData.contract_date_eng = new Date(formData.contract_date).toLocaleDateString("en-US", {
    year: "numeric",
    month: "long",
    day: "numeric",
  });

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
  formData.full_name_eng = removeAccents(formData.full_name);
  formData.location_dob_eng = removeAccents(formData.location_dob);
  formData.residential_address_eng = removeAccents(formData.residential_address);
  formData.id_number_at_eng = removeAccents(formData.id_number_at);
  formData.salary = new Intl.NumberFormat().format(parseInt(formData.salary));

  return formData;
}

function removeAccents(str) {
  return str.normalize('NFD')
            .replace(/[\u0300-\u036f]/g, '')
            .replace(/đ/g, 'd').replace(/Đ/g, 'D');
}

export default {
  name: "MainApp",
  methods: {
    renderDoc(event) {
      event.preventDefault();
      let dataForm = getDataForm();
      console.log(dataForm);
      const docs = document.getElementById("doc1");
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
        saveAs(out, "output.docx");
      };
    },
  },
};
</script>
