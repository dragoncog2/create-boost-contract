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
                Thông tin nhân viên Booster
              </h3>
            </div>
          </div>
          <div class="">
            <form id="myForm">
              <div class="overflow-hidden shadow sm:rounded-md">
                <div class="bg-white px-4 py-5 sm:p-6">
                  <div class="grid grid-cols-12 gap-6">
                    <div class="col-span-12 sm:col-span-6">
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
                        for="full_name"
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
                        for="street-address"
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

                    <div class="col-span-6 sm:col-span-6 lg:col-span-3">
                      <label class="block text-sm font-medium text-gray-700"
                        >CMND/Hộ chiếu số</label
                      >
                      <input
                        type="text"
                        name="id_number"
                        placeholder="CMND/Hộ chiếu số"
                        pattern="[0-9]"
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
                        for="region"
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
                        for="postal-code"
                        class="block text-sm font-medium text-gray-700"
                        >Lương</label
                      >
                      <input
                        type="text"
                        name="salary"
                        placeholder="Lương"
                        pattern="[0-9]"
                        title="Xin hãy nhập số ở đây"
                        class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500 sm:text-sm"
                      />
                    </div>
                    <div class="col-span-6 sm:col-span-3 lg:col-span-3">
                      <label
                        for="postal-code"
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
                        for="postal-code"
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
                        for="postal-code"
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
  var formData = new FormData(form);
  return Object.fromEntries(formData);
}

export default {
  name: "MainApp",
  methods: {
    renderDoc() {
      let dataForm = getDataForm();
      dataForm.dob = new Date(
        dataForm.dob.toLocaleDateString("en-gb", {
          year: "numeric",
          month: "long",
          day: "2-digit",
        })
      );
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
