//[qa_sdk](../../../index.md)/[com.quantactions.sdk.data.entity](../index.md)/[QuestionnaireResponseEntity](index.md)

# QuestionnaireResponseEntity

[androidJvm]\
@JsonClass(generateAdapter = true)

data class [QuestionnaireResponseEntity](index.md)(**id**: [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html), **qFullID**: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), **qName**: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), **qCode**: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), **qDate**: [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html), **qResponse**: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html))

Entity of the table questionnaires_response containing all information about a questionnaire response. The fullID is defined as the concatenation (with ':') between the study_id and the questionnaire code. The response is a JSON encoded hash-map with key-value pairs where the keys are the questions code and the values and the numeric values of the response.

## Constructors

| | |
|---|---|
| [QuestionnaireResponseEntity](-questionnaire-response-entity.md) | [androidJvm]<br>fun [QuestionnaireResponseEntity](-questionnaire-response-entity.md)(id: [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html), qFullID: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), qName: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), qCode: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), qDate: [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html), qResponse: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)) |

## Properties

| Name | Summary |
|---|---|
| [id](id.md) | [androidJvm]<br>val [id](id.md): [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) |
| [qCode](q-code.md) | [androidJvm]<br>val [qCode](q-code.md): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
| [qDate](q-date.md) | [androidJvm]<br>val [qDate](q-date.md): [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) |
| [qFullID](q-full-i-d.md) | [androidJvm]<br>val [qFullID](q-full-i-d.md): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
| [qName](q-name.md) | [androidJvm]<br>val [qName](q-name.md): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
| [qResponse](q-response.md) | [androidJvm]<br>val [qResponse](q-response.md): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
