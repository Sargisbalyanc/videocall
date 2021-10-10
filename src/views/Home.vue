<template>
  <div class="conferance-content">
    <div class="container">
      <div class="table_conferanse">
        <div class="table_conferanse_-content">
          <div class="table_conferanse_blok">
            <div class="users_info_content">
              <div class="users_info_title_user">
                <span>
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    width="14"
                    height="18"
                    viewBox="0 0 14 18"
                    fill="none"
                  >
                    <path
                      fill-rule="evenodd"
                      clip-rule="evenodd"
                      d="M6.98583 11.7885C3.76282 11.7885 1.01044 12.2758 1.01044 14.2274C1.01044 16.179 3.74536 16.6838 6.98583 16.6838C10.2088 16.6838 12.9604 16.1957 12.9604 14.2449C12.9604 12.2941 10.2263 11.7885 6.98583 11.7885Z"
                      stroke="#BB6BD9"
                      stroke-width="1.5"
                      stroke-linecap="round"
                      stroke-linejoin="round"
                    />
                    <path
                      fill-rule="evenodd"
                      clip-rule="evenodd"
                      d="M6.98582 9.00492C9.1009 9.00492 10.8152 7.28984 10.8152 5.17476C10.8152 3.05968 9.1009 1.3454 6.98582 1.3454C4.87074 1.3454 3.15566 3.05968 3.15566 5.17476C3.14852 7.2827 4.85169 8.99778 6.95884 9.00492H6.98582Z"
                      stroke="#BB6BD9"
                      stroke-width="1.42857"
                      stroke-linecap="round"
                      stroke-linejoin="round"
                    />
                  </svg>
                </span>
                <span class="users"> Users </span>
              </div>
              <div class="users_info_title">
                <span class="auditStart">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    width="20"
                    height="20"
                    viewBox="0 0 20 20"
                    fill="none"
                  >
                    <path
                      fill-rule="evenodd"
                      clip-rule="evenodd"
                      d="M17.7082 10.0004C17.7082 14.2579 14.2573 17.7087 9.99984 17.7087C5.74234 17.7087 2.2915 14.2579 2.2915 10.0004C2.2915 5.74289 5.74234 2.29205 9.99984 2.29205C14.2573 2.29205 17.7082 5.74289 17.7082 10.0004Z"
                      stroke="#BB6BD9"
                      stroke-width="1.5"
                      stroke-linecap="round"
                      stroke-linejoin="round"
                    />
                    <path
                      d="M12.8583 12.4526L9.71661 10.5785V6.53931"
                      stroke="#BB6BD9"
                      stroke-width="1.5"
                      stroke-linecap="round"
                      stroke-linejoin="round"
                    />
                  </svg>
                </span>
                <span class="users"> Audio Start </span>
                <span class="time_title">(( hh:mm:ss ))</span>
              </div>
              <div class="users_info_title">
                <span class="auditStart">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    width="20"
                    height="20"
                    viewBox="0 0 20 20"
                    fill="none"
                  >
                    <path
                      fill-rule="evenodd"
                      clip-rule="evenodd"
                      d="M16.7082 9.00039C16.7082 13.2579 13.2573 16.7087 8.99984 16.7087C4.74234 16.7087 1.2915 13.2579 1.2915 9.00039C1.2915 4.74289 4.74234 1.29205 8.99984 1.29205C13.2573 1.29205 16.7082 4.74289 16.7082 9.00039Z"
                      stroke="#BB6BD9"
                      stroke-width="1.5"
                      stroke-linecap="round"
                      stroke-linejoin="round"
                    />
                    <path
                      d="M11.8583 11.4526L8.71661 9.57847V5.53931"
                      stroke="#BB6BD9"
                      stroke-width="1.5"
                      stroke-linecap="round"
                      stroke-linejoin="round"
                    />
                  </svg>
                </span>
                <span class="users"> Audio End </span>
                <span class="time_title">(( hh:mm:ss ))</span>
              </div>
            </div>
          </div>
          <div class="information_content">
            <div class="d-flex justify-content-between mb-3 align-items-center">
              <div class="addnew_users d-flex">
                <button
                  class="add_new_btn"
                  @click="() => (this.isAddUserOpen = !this.isAddUserOpen)"
                >
                  <span>
                    <svg
                      xmlns="http://www.w3.org/2000/svg"
                      width="20"
                      height="20"
                      viewBox="0 0 20 20"
                      fill="none"
                    >
                      <path
                        fill-rule="evenodd"
                        clip-rule="evenodd"
                        d="M16.7082 9.00039C16.7082 13.2579 13.2573 16.7087 8.99984 16.7087C4.74234 16.7087 1.2915 13.2579 1.2915 9.00039C1.2915 4.74289 4.74234 1.29205 8.99984 1.29205C13.2573 1.29205 16.7082 4.74289 16.7082 9.00039Z"
                        stroke="#BB6BD9"
                        stroke-width="1.5"
                        stroke-linecap="round"
                        stroke-linejoin="round"
                      />
                      <path
                        d="M11.8583 11.4526L8.71661 9.57847V5.53931"
                        stroke="#BB6BD9"
                        stroke-width="1.5"
                        stroke-linecap="round"
                        stroke-linejoin="round"
                      />
                    </svg>
                  </span>
                  <span class="add_new"> Add New </span>
                </button>
              </div>
              <div v-if="isAddUserOpen">
                <div class="d-flex align-items-center">
                  <select
                    v-model="newAudio.participant_id"
                    placeholder="Select"
                  >
                    <option
                      v-for="(member, i) in members"
                      :value="member.participant_id"
                      :key="i"
                    >
                      {{ member.name }}
                    </option>
                  </select>
                  <input
                    type="time"
                    step="1"
                    class="timeInput"
                    v-model="newAudio.audio_start"
                  />
                  <input
                    type="time"
                    step="1"
                    class="timeInput"
                    v-model="newAudio.audio_end"
                  />

                  <button @click="addAudio" class="add_new_btn">
                    <span class="add_new">Add</span>
                  </button>
                </div>
              </div>
            </div>
            <div
              class="user_all_info_content"
              ref="user_all"
              v-for="(audio, i) in getAudios"
              :key="i"
            >
              <div class="user_conferase_content user_name_table">
                <span class="user_name">
                  {{ getMember(audio.participant_id).name }}
                </span>
              </div>
              <div class="user_conferase_content users_data_infos">
                <span class="user_name2">
                  {{ dateFormatter(audio.audio_start) }}
                </span>
              </div>
              <div class="user_conferase_content users_data_infos2">
                <span class="user_name2">
                  {{ dateFormatter(audio.audio_end) }}
                </span>
              </div>
            </div>
          </div>
        </div>
        <div class="time_info_content">
          <div class="w-100 d-flex justify-content-end mb-3">
            <button v-b-modal.addNewUsers class="add_new_btn">
              <span class="add_new">Enter Name</span>
            </button>
          </div>
          <div class="hide_show_content">
            <div class="hide_show_m">
              <button class="hide_btn" @click="hideUserInfo('hide')">
                <span>
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    width="24"
                    height="24"
                    viewBox="0 0 24 24"
                    fill="none"
                  >
                    <g id="Iconly/Light/Hide">
                      <g id="Hide">
                        <path
                          id="Stroke 1"
                          d="M9.76057 14.3668C9.18557 13.7928 8.83557 13.0128 8.83557 12.1378C8.83557 10.3848 10.2476 8.9718 11.9996 8.9718C12.8666 8.9718 13.6646 9.3228 14.2296 9.8968"
                          stroke="white"
                          stroke-width="1.5"
                          stroke-linecap="round"
                          stroke-linejoin="round"
                        />
                        <path
                          id="Stroke 3"
                          d="M15.103 12.6988C14.871 13.9888 13.855 15.0068 12.566 15.2408"
                          stroke="white"
                          stroke-width="1.5"
                          stroke-linecap="round"
                          stroke-linejoin="round"
                        />
                        <path
                          id="Stroke 5"
                          d="M6.65457 17.4723C5.06757 16.2263 3.72357 14.4063 2.74957 12.1373C3.73357 9.85829 5.08657 8.02829 6.68357 6.77229C8.27057 5.51629 10.1016 4.83429 11.9996 4.83429C13.9086 4.83429 15.7386 5.52629 17.3356 6.79129"
                          stroke="white"
                          stroke-width="1.5"
                          stroke-linecap="round"
                          stroke-linejoin="round"
                        />
                        <path
                          id="Stroke 7"
                          d="M19.4476 8.99078C20.1356 9.90478 20.7406 10.9598 21.2496 12.1368C19.2826 16.6938 15.8066 19.4388 11.9996 19.4388C11.1366 19.4388 10.2856 19.2988 9.46759 19.0258"
                          stroke="white"
                          stroke-width="1.5"
                          stroke-linecap="round"
                          stroke-linejoin="round"
                        />
                        <path
                          id="Stroke 9"
                          d="M19.887 4.24957L4.11298 20.0236"
                          stroke="white"
                          stroke-width="1.5"
                          stroke-linecap="round"
                          stroke-linejoin="round"
                        />
                      </g>
                    </g>
                  </svg>
                </span>
                <span class="hide"> Hide </span>
              </button>
              <button class="show_btn" @click="hideUserInfo('show')">
                <span>
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    width="24"
                    height="24"
                    viewBox="0 0 24 24"
                    fill="none"
                  >
                    <g id="Iconly/Light/Show">
                      <g id="Show">
                        <path
                          id="Stroke 1"
                          fill-rule="evenodd"
                          clip-rule="evenodd"
                          d="M15.1628 12.0535C15.1628 13.7995 13.7468 15.2145 12.0008 15.2145C10.2548 15.2145 8.83984 13.7995 8.83984 12.0535C8.83984 10.3065 10.2548 8.89154 12.0008 8.89154C13.7468 8.89154 15.1628 10.3065 15.1628 12.0535Z"
                          stroke="#fff"
                          stroke-width="1.5"
                          stroke-linecap="round"
                          stroke-linejoin="round"
                        />
                        <path
                          id="Stroke 3"
                          fill-rule="evenodd"
                          clip-rule="evenodd"
                          d="M11.998 19.3549C15.806 19.3549 19.289 16.6169 21.25 12.0529C19.289 7.48892 15.806 4.75092 11.998 4.75092H12.002C8.194 4.75092 4.711 7.48892 2.75 12.0529C4.711 16.6169 8.194 19.3549 12.002 19.3549H11.998Z"
                          stroke="#fff"
                          stroke-width="1.5"
                          stroke-linecap="round"
                          stroke-linejoin="round"
                        />
                      </g>
                    </g>
                  </svg>
                </span>
                <span class="show"> Show </span>
              </button>
            </div>
            <div class="select_add_new">
              <div class="">
                <input
                  type="checkbox"
                  id="searchCourseOnline"
                  name="searchCourseOnline"
                  value="online"
                  style="display: none"
                  :checked="selectedMembers.length === members.length"
                  @click="selectOrClearAll"
                />
                <label for="searchCourseOnline" class="checkbox-label"
                  ><span class="select_all pr-2"> Select All </span>
                </label>
              </div>
            </div>
          </div>
          <div class="content-time-blok-1">
            <div class="information_user_tolk_time">
              <div class="users_info_title_user24">
                <span class="auditStart">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    width="20"
                    height="20"
                    viewBox="0 0 20 20"
                    fill="none"
                  >
                    <path
                      fill-rule="evenodd"
                      clip-rule="evenodd"
                      d="M9.98583 12.7885C6.76282 12.7885 4.01044 13.2758 4.01044 15.2274C4.01044 17.179 6.74536 17.6838 9.98583 17.6838C13.2088 17.6838 15.9604 17.1957 15.9604 15.2449C15.9604 13.2941 13.2263 12.7885 9.98583 12.7885Z"
                      stroke="#BB6BD9"
                      stroke-width="1.5"
                      stroke-linecap="round"
                      stroke-linejoin="round"
                    />
                    <path
                      fill-rule="evenodd"
                      clip-rule="evenodd"
                      d="M9.98582 10.0049C12.1009 10.0049 13.8152 8.28984 13.8152 6.17476C13.8152 4.05968 12.1009 2.3454 9.98582 2.3454C7.87074 2.3454 6.15566 4.05968 6.15566 6.17476C6.14852 8.2827 7.85169 9.99778 9.95884 10.0049H9.98582Z"
                      stroke="#BB6BD9"
                      stroke-width="1.42857"
                      stroke-linecap="round"
                      stroke-linejoin="round"
                    />
                  </svg>
                </span>
                <span class="users"> Users </span>
              </div>
              <div
                class="users_info_title_user24 d-flex justify-content-center"
              >
                <span class="auditStart">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    width="21"
                    height="20"
                    viewBox="0 0 21 20"
                    fill="none"
                  >
                    <g clip-path="url(#clip0)">
                      <path
                        d="M9.06181 15.7584C9.06177 16.3106 8.61407 16.7583 8.06181 16.7583H3.25945C2.70717 16.7583 2.25945 16.3106 2.25945 15.7583V12.7283C1.13733 11.6937 0.5 10.2473 0.5 8.7104C0.5 5.69504 2.95326 3.242 5.96839 3.242C8.43012 3.242 10.6 4.90015 11.2449 7.27452L11.265 7.3477L11.3057 8.24435L12.3805 9.75146C12.6992 10.1983 12.5981 10.8186 12.154 11.1412L11.5054 11.6123V12.4182C11.5054 13.3887 10.7158 14.1786 9.74456 14.1786H9.06196L9.06181 15.7584ZM3.63152 15.3862H7.68965V12.8069H9.74433C9.95883 12.8069 10.1331 12.6325 10.1331 12.4184V10.9137L10.6481 10.5396C10.8702 10.3783 10.9207 10.0681 10.7613 9.8447L9.95289 8.71154L9.90098 7.56449C9.39468 5.82379 7.78776 4.61453 5.96816 4.61453C3.7095 4.61453 1.87184 6.45219 1.87184 8.71085C1.87184 9.94572 2.42113 11.1024 3.37906 11.8842L3.6313 12.09L3.63152 15.3862Z"
                        fill="#BB6BD9"
                      />
                      <path
                        d="M14.4841 13.0283L13.5141 12.0582C14.1329 11.4392 14.1329 10.4321 13.5138 9.81283L14.4843 8.84277C15.638 9.99669 15.638 11.8746 14.4841 13.0283Z"
                        fill="#BB6BD9"
                      />
                      <path
                        d="M16.3362 14.4893L15.3661 13.5193C16.7906 12.0949 16.7906 9.77674 15.3661 8.35207L16.3362 7.38202C18.2953 9.34157 18.2953 12.53 16.3362 14.4893Z"
                        fill="#BB6BD9"
                      />
                      <path
                        d="M18.4638 15.8591L17.4933 14.8891C19.6728 12.7091 19.6728 9.16227 17.4937 6.98251L18.4638 6.01245C21.1787 8.72664 21.1787 13.144 18.4638 15.8591Z"
                        fill="#BB6BD9"
                      />
                    </g>
                    <defs>
                      <clipPath id="clip0">
                        <rect
                          width="20"
                          height="20"
                          fill="white"
                          transform="translate(0.5)"
                        />
                      </clipPath>
                    </defs>
                  </svg>
                </span>
                <span class="users"> Average </span>
              </div>
              <div class="users_quantity d-flex justify-content-center">
                <span class="users"> Count </span>
              </div>
            </div>
            <div class="table_users_name-content">
              <div class="" v-for="(member, i) in members" :key="i">
                <div class="user_info_content w-100">
                  <input
                    type="checkbox"
                    name="searchCourseOnline"
                    style="display: none"
                    :id="`notifyDelete${i + 1}`"
                    v-model="selectedMembers"
                    :value="member.participant_id"
                  />
                  <label
                    :for="`notifyDelete${i + 1}`"
                    class="checkbox-label d-flex"
                  >
                    <div class="table_users_information_content_name">
                      <span class="name_tabel_for_users">
                        {{ member.name }}
                      </span>
                    </div>
                    <div
                      class="
                        table_users_information_content_avarage
                        d-flex
                        justify-content-center
                      "
                    >
                      <span class="name_tabel_for_users text-center">
                        {{ member.average ? member.average : 0 }} second
                      </span>
                    </div>
                    <div
                      class="
                        table_users_information_content_audios
                        d-flex
                        justify-content-center
                      "
                    >
                      <span
                        class="
                          times_tabel_for_users
                          name_tabel_for_users
                          text-center
                        "
                      >
                        {{
                          audios.filter(
                            (m) => m.participant_id === member.participant_id
                          ).length
                        }}
                      </span>
                    </div>
                  </label>
                </div>
              </div>
            </div>
          </div>
          <div class="content-time-blok-1">
            <div class="information_user_tolk_time">
              <div class="users_info_title_user141">
                <span class="users"> The Most </span>
              </div>
              <div class="users_info_title_user142">
                <span class="users"> The Least </span>
              </div>
            </div>
            <div class="table_users_name-content">
              <div class="table_users_name_time">
                <div class="last_most">
                  <div
                    class="table_users_name_time_most"
                    v-for="(member, i) in getSortedMembers.slice(0, 1)"
                    :key="i"
                  >
                    <span class="name_tabel_for_users">
                      {{ member.name }}
                    </span>
                    <span class="name_tabel_for_users_most">
                      {{ getDuration(member) }}
                    </span>
                  </div>
                </div>
                <div class="last_most">
                  <div
                    class="times_tabel_for_users_content_loast"
                    v-for="(member, i) in getSortedMembers.slice(-1)"
                    :key="i"
                  >
                    <span class="name_tabel_for_users">
                      {{ member.name }}
                    </span>
                    <span class="name_tabel_for_users_least">
                      {{ getDuration(member) }}
                    </span>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <b-modal
      id="addNewUsers"
      title="BootstrapVue"
      @ok="addUser"
      body-class="add-users-name p-0"
      ok-variant="danger"
      hide-header
      hide-footer
      centered
    >
      <div class="modal_body">
        <input
          type="text"
          class="add_name_input"
          placeholder="Enter Name"
          v-model="newUserName"
        />
        <div class="d-flex w-100 justify-content-end btn_groups">
          <button class="cancelbtn" @click="$bvModal.hide('addNewUsers')">
            Cancel
          </button>
          <button class="ok_btn" @click="addUser">Ok</button>
        </div>
      </div>
    </b-modal>
  </div>
</template>

<script>
import members from "@/assets/data/members.json";
import audios from "@/assets/data/audio_segments.json";

export default {
  name: "Home",
  data() {
    return {
      newAudio: {
        participant_id: 1,
        audio_start: "12:05:09",
        audio_end: "12:05:26",
      },
      members: members,
      audios: audios,
      selectedMembers: [],
      newUser: false,
      isAddUserOpen: false,
      newUserName: "",
    };
  },
  computed: {
    getSortedMembers: function () {
      let members = this.members;
      return members.sort((a, b) => b.average - a.average);
    },
    getAudios: function () {
      return this.audios.filter((audio) => {
        return !this.members.find(
          (member) => member.participant_id === audio.participant_id
        ).isHidden;
      });
    },
  },
  mounted() {
    let members = [...this.members];
    members.map((member) => {
      member.average = this.getAverageOfMemberAudios(member.participant_id);
      member.isHidden = false;
    });
    this.members = members;
  },
  methods: {
    getMember(participant_id) {
      return this.members.find(
        (member) => member.participant_id === participant_id
      );
    },
    getAverageOfMemberAudios(participant_id) {
      let audios = this.audios.filter(
        (audio) => audio.participant_id === participant_id
      );
      let sum = 0;
      for (let audio of audios) {
        sum +=
          new Date(audio.audio_end).getTime() -
          new Date(audio.audio_start).getTime();
      }
      return (sum / audios.length / 1000).toFixed(2); // dividing by 1000 to get as seconds
    },
    addUser() {
      if (this.newUserName) {
        let user = {
          name: this.newUserName,
          participant_id: new Date().getTime(),
        };
        this.members.push(user);
        this.newUserName = "";
      }
      this.$bvModal.hide("addNewUsers");
    },
    addAudio() {
      let startTime = "2021-10-06 " + this.newAudio.audio_start + " UTC";
      let endTime = "2021-10-06 " + this.newAudio.audio_end + " UTC";
      if (new Date(startTime).getTime() > new Date(endTime).getTime()) {
        let reverseTime = startTime;
        startTime = endTime;
        endTime = reverseTime;
      }
      this.audios.unshift({
        audio_end: endTime,
        audio_start: startTime,
        participant_id: this.newAudio.participant_id,
      });
      let members = [...this.members]
      let memberIndex = members.findIndex(member => member.participant_id === this.newAudio.participant_id)
      members[memberIndex].average = this.getAverageOfMemberAudios(members[memberIndex].participant_id)
      this.members = members
      this.newAudio = {};
    },
    getDuration(member) {
      let audios = this.audios.filter(
        (audio) => audio.participant_id === member.participant_id
      );
      let duration = 0;
      for (let audio of audios) {
        duration +=
          (new Date(audio.audio_end).getTime() -
            new Date(audio.audio_start).getTime()) /
          1000;
      }
      if (!duration) return "00 : 00";
      let sec = duration % 60;
      let min = Math.trunc(duration / 60);
      if (min < 10) min = "0" + min;
      if (sec < 10) sec = "0" + sec;
      let string = min + " : " + sec;
      return string;
    },
    dateFormatter(d) {
      let dateObj = new Date(d);
      let hr = dateObj.getHours();
      let min = dateObj.getMinutes();
      let sec = dateObj.getSeconds();
      if (hr < 10) hr = "0" + hr;
      if (min < 10) min = "0" + min;
      if (sec < 10) sec = "0" + sec;
      let output = hr + " : " + min + " : " + sec;
      return output;
    },
    selectOrClearAll() {
      let selectedMembers = [];
      if (this.selectedMembers.length !== this.members.length) {
        this.members.map((member) => {
          selectedMembers.push(member.participant_id);
        });
      }
      this.selectedMembers = selectedMembers;
    },
    hideUserInfo(action) {
      let members = [...this.members];
      if (action === "hide") {
        for (let id of this.selectedMembers) {
          members.find(
            (member) => member.participant_id === id
          ).isHidden = true;
        }
      } else if (action === "show") {
        for (let id of this.selectedMembers) {
          members.find(
            (member) => member.participant_id === id
          ).isHidden = false;
        }
      }
      this.members = members;
      this.selectedMembers = [];
    },
  },
};
</script>
<style scoped src='@/assets/css/Home.css'></style>
