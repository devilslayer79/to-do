<!-- <template>
     <ol>
          <template v-for="(item,index) in list">
            <li :key="index" v-if="item.title !='menyapu'">
            <span>{{item.title}}</span>
            </li>
                
          </template>
    </ol>
</template>

<script>
import { message } from 'laravel-mix/src/Log';

    export default {
        mounted() {
            console.log('Component mounted.')
        },
        data: function(){
            return{
                list: [
                    {title: "menyapu"},
                    {title: "cuci piring"}
                ]
            }
        }
    }
</script> -->
