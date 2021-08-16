# EnrichedE2E
Enriched version of the E2E dataset introduced in the INLG 2021 paper "Enriching the E2E Dataset"

*Authors: Thiago Castro Ferreira, Helena Vaz, Brian Davis and Adriana Pagano*

## Description

The original E2E dataset is a dataset for training end-to-end, data-driven natural language generation systems in the restaurant domain, bigger than existing, frequently used datasets in the area.

In order to make it easy for researchers to rapidly develop and evaluate data-to-text pipeline systems, this study introduces an enriched version of the dataset with pipeline intermediate representations. We believe that the enriched version of the E2E will provide another data-resource so researchers can better investigate data-driven pipeline systems, their subtasks as well as its comparison with state-of-the-art end-to-end systems.

## Example

```xml
<entry eid="Id1" size="3">
  <source>
    <input attribute="name" tag="__NAME__" value="The Punter"/>
    <input attribute="food" tag="__FOOD__" value="Indian"/>
    <input attribute="priceRange" tag="__PRICERANGE__" value="cheap"/>
  </source>
  <target annotator="16" comment="good" lid="Id1" ref="17">
    <structuring>
      <sentence>
        <input attribute="name" tag="__NAME__" value="The Punter"/>
        <input attribute="priceRange" tag="__PRICERANGE__" value="cheap"/>
      </sentence>
    </structuring>
    <text>The Punter provides Indian food in the cheap price range.</text>
    <template>__NAME__ provides __FOOD__ food in the __PRICERANGE__ price range .</template>
    <lexicalization>__NAME__ VP[Mood=Ind|Number=Sing|Person=3|Tense=Pres|VerbForm=Fin] provide FOOD food in DT[Definite=Def|PronType=Art] the __PRICERANGE__ price range .</lexicalization>
  </target>
  <target annotator="16" comment="good" lid="Id2" ref="1470">
    <structuring>
      <sentence>
        <input attribute="name" tag="__NAME__" value="The Punter"/>
        <input attribute="priceRange" tag="__PRICERANGE__" value="cheap"/>
        <input attribute="food" tag="__FOOD__" value="Indian"/>
      </sentence>
    </structuring>
    <text>The Punter offers cheap @ Indian food.</text>
    <template>__NAME__ offers __PRICERANGE__ @ __FOOD__ food .</template>
    <lexicalization>__NAME__ VP[Mood=Ind|Number=Sing|Person=3|Tense=Pres|VerbForm=Fin] offer __PRICERANGE__ @ __FOOD__ food .</lexicalization>
  </target>
  <target annotator="16" comment="good" lid="Id3" ref="4315">
    <structuring>
      <sentence>
        <input attribute="name" tag="__NAME__" value="The Punter"/>
        <input attribute="priceRange" tag="__PRICERANGE__" value="cheap"/>
        <input attribute="food" tag="__FOOD__" value="Indian"/>
      </sentence>
    </structuring>
    <text>The Punter is known for serving cheap, tasty Indian food.</text>
    <template>__NAME__ is known for serving __PRICERANGE__ , tasty __FOOD__ food .</template>
    <lexicalization>__NAME__ VP[Mood=Ind|Number=Sing|Person=3|Tense=Pres|VerbForm=Fin] be VP[Tense=Past|VerbForm=Part|Voice=Pass] know for VP[VerbForm=Ger] serve __PRICERANGE__ , tasty __FOOD__ food .</lexicalization>
  </target>
  <target annotator="16" comment="good" lid="Id4" ref="12852">
    <structuring>
      <sentence>
        <input attribute="name" tag="__NAME__" value="The Punter"/>
        <input attribute="food" tag="__FOOD__" value="Indian"/>
        <input attribute="priceRange" tag="__PRICERANGE__" value="cheap"/>
      </sentence>
    </structuring>
    <text>The Punter is an Indian restaurant with cheap prices.</text>
    <template>__NAME__ is an __FOOD__ restaurant with __PRICERANGE__ prices .</template>
    <lexicalization>__NAME__ VP[Mood=Ind|Number=Sing|Person=3|Tense=Pres|VerbForm=Fin] be DT[Definite=Ind|PronType=Art] a __FOOD__ restaurant with __PRICERANGE__ prices .</lexicalization>
  </target>
  <target annotator="16" comment="good" lid="Id5" ref="20203">
    <structuring>
      <sentence>
        <input attribute="name" tag="__NAME__" value="The Punter"/>
      </sentence>
      <sentence>
        <input attribute="priceRange" tag="__PRICERANGE__" value="cheap"/>
      </sentence>
    </structuring>
    <text>There is a restaurant called The Punter that provides Indian food. It has a cheap price range.</text>
    <template>There is a restaurant called __NAME__ that provides __FOOD__ food . __NAME__ has a __PRICERANGE__ price range .</template>
    <lexicalization>There VP[Mood=Ind|Number=Sing|Person=3|Tense=Pres|VerbForm=Fin] be DT[Definite=Ind|PronType=Art] a restaurant VP[Tense=Past|VerbForm=Part] call __NAME__ that VP[Mood=Ind|Number=Sing|Person=3|Tense=Pres|VerbForm=Fin] provide FOOD food . __NAME__ VP[Mood=Ind|Number=Sing|Person=3|Tense=Pres|VerbForm=Fin] have DT[Definite=Ind|PronType=Art] a __PRICERANGE__ price range .</lexicalization>
  </target>
  <target annotator="16" comment="good" lid="Id6" ref="21091">
    <structuring>
      <sentence>
        <input attribute="name" tag="__NAME__" value="The Punter"/>
        <input attribute="food" tag="__FOOD__" value="Indian"/>
        <input attribute="priceRange" tag="__PRICERANGE__" value="cheap"/>
      </sentence>
    </structuring>
    <text>The Punter is an Indian restaurant that has a cheap price range</text>
    <template>__NAME__ is an __FOOD__ restaurant that has a __PRICERANGE__ price range</template>
    <lexicalization>__NAME__ VP[Mood=Ind|Number=Sing|Person=3|Tense=Pres|VerbForm=Fin] be DT[Definite=Ind|PronType=Art] a __FOOD__ restaurant that VP[Mood=Ind|Number=Sing|Person=3|Tense=Pres|VerbForm=Fin] have DT[Definite=Ind|PronType=Art] a __PRICERANGE__ price range</lexicalization>
  </target>
</entry>
```

## Citation

```bibtex
@inproceedings{novikova2017e2e,
  title={The {E2E} Dataset: New Challenges for End-to-End Generation},
  author={Novikova, Jekaterina and Du{\v{s}}ek, Ondrej and Rieser, Verena},
  booktitle={Proceedings of the 18th Annual Meeting of the Special Interest 
             Group on Discourse and Dialogue},
  address={Saarbr\"ucken, Germany},
  year={2017},
  note={arXiv:1706.09254},
  url={https://arxiv.org/abs/1706.09254},
}
```

## License

Distributed under the Creative Commons 4.0 Attribution-ShareAlike license (CC4.0-BY-SA).

## Acknowledgements

This research was partially funded by the Brazilian agencies CNPq, CAPES, and FAPEMIG. In particular, the researchers were supported by CNPQ grant No. 310630/2017-7, CAPES Post doctoral grant No. 88887.508597/2020-00, and FAPEMIG grant APQ-01.461-14. It was also funded by the [ADAPT Centre for Digital Content Technology](https://www.adaptcentre.ie) which is funded under the Science Foundation Ireland Research Centres Programme (Grant 13/RC/2106\_P2).
