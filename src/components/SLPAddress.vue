<!--
 Copyright 2020 Coinbase, Inc.

 Licensed under the Apache License, Version 2.0 (the "License");
 you may not use this file except in compliance with the License.
 You may obtain a copy of the License at

      http://www.apache.org/licenses/LICENSE-2.0

 Unless required by applicable law or agreed to in writing, software
 distributed under the License is distributed on an "AS IS" BASIS,
 WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 See the License for the specific language governing permissions and
 limitations under the License.
-->

<template>
  <div id="slpaddress">
    <div v-for="(token, index) in tokens" :key="index">
      <br>
      <table class="table is-bordered is-striped" align="center">
        <thead></thead>
        <tbody>
          <tr>
            <td>Name</td>
            <td>{{token.name}}</td>
          </tr>
          <tr>
            <td>Token ID</td>
            <td>{{token.token_id}}</td>
          </tr>
          <tr>
            <td>Balance</td>
            <td>{{token.balance.div(10**token.decimals).toFixed()}} {{token.ticker}}</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<script>
export default {
  name: "slpaddress",
  props: ["tokens"]
};
</script>
