# KPE-Pro
KPE-Pro(Knowledge Probing \& Evaluation for Proficiency)知识探针评测数据集共包含6620条问答对，涵盖三大类、六小类知识：常识性(物理常识、社会常识)、事实性(地理知识、历史知识)和专业领域性(医学知识、金融 知识)。每一道探针均以标准化的四选一形式呈现，包含三个具有迷惑性的干扰选项和一个正确选项，所有题目均由GPT-4o基于维基百科知识自动生成，严格遵循“主题相关性”与“一跳知识”原则；随后，采用DeepSeek-V3对候选问题进行自动校验。

## 数据集数量分布
<table>
  <thead>
    <tr>
      <th><strong>知识类别</strong></th>
      <th><strong>子类别</strong></th>
      <th><strong>数量</strong></th>
      <th><strong>类别小计</strong></th>
      <th><strong>占比(%)</strong></th>
      <th><strong>合计</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="2"><strong>常识性</strong></td>
      <td>物理常识</td>
      <td>1007</td>
      <td rowspan="2">2033</td>
      <td rowspan="2">30.7</td>
      <td rowspan="5">6620</td>
    </tr>
    <tr>
      <td>社会常识</td>
      <td>1026</td>
    </tr>
    <tr>
      <td rowspan="2"><strong>事实性</strong></td>
      <td>地理知识</td>
      <td>1058</td>
      <td rowspan="2">2176</td>
      <td rowspan="2">32.9</td>
    </tr>
    <tr>
      <td>历史知识</td>
      <td>1118</td>
    </tr>
    <tr>
      <td rowspan="2"><strong>专业领域性</strong></td>
      <td>医学知识</td>
      <td>1049</td>
      <td rowspan="2">2411</td>
      <td rowspan="2">36.4</td>
    </tr>
    <tr>
      <td>金融知识</td>
      <td>1362</td>
    </tr>
  </tbody>
</table>


## 文件说明
数据集以JSON格式存储。每条数据包含问题ID（id）、问题（question）、选项（options）、答案（answer）和知识类别（type）。
示例如下：
```json
{
    "id": 1,
    "question": "中国的国庆节是在哪一天庆祝的？",
    "options": {
      "A": "10月1日",
      "B": "9月1日",
      "C": "8月1日",
      "D": "7月1日"
    },
    "answer": "A",
    "type": "社会常识"
}
