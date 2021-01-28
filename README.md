# Knowledge-Tracing (In-Progress)

I have used Microsoft's LightGBM model for knowledge tracing as it overperformed the XGBOOST model in terms of accuracy.

**Riiid AIEd Challenge 2020**

[Challenge Website](https://www.ednetchallenge.ai/)

Riiid Labs, an AI solutions provider delivering creative disruption to the education market, empowers global education players to rethink traditional ways of learning leveraging AI. With a strong belief in equal opportunity in education, Riiid launched an AI tutor based on deep-learning algorithms in 2017 that attracted more than one million South Korean students. This year, the company released EdNet, the world’s largest open database for AI education containing more than 100 million student interactions.

In this competition, your challenge is to create algorithms for "Knowledge Tracing," the modeling of student knowledge over time. The goal is to accurately predict how students will perform on future interactions. You will pair your machine learning skills using Riiid’s EdNet data.

Your innovative algorithms will help tackle global challenges in education. If successful, it’s possible that any student with an Internet connection can enjoy the benefits of a personalized learning experience, regardless of where they live. With your participation, we can build a better and more equitable model for education in a post-COVID-19 world.

## Data

● Files

》train.csv

• row_id: (int64) ID code for the row.

• timestamp: (int64) the time in milliseconds between this user interaction and the first event completion from that user.

• user_id: (int32) ID code for the user.

• content_id: (int16) ID code for the user interaction

• content_type_id: (int8) 0 if the event was a question being posed to the user, 1 if the event was the user watching a lecture.

• task_container_id: (int16) Id code for the batch of questions or lectures. For example, a user might see three questions in a row before seeing the explanations for any of them. Those three would all share a task_container_id.

• user_answer: (int8) the user's answer to the question, if any. Read -1 as null, for lectures.

• answered_correctly: (int8) if the user responded correctly. Read -1 as null, for lectures.

• prior_question_elapsed_time: (float32) The average time in milliseconds it took a user to answer each question in the previous question bundle, ignoring any lectures in between. Is null for a user's first question bundle or lecture. Note that the time is the average time a user took to solve each question in the previous bundle.

• prior_question_had_explanation: (bool) Whether or not the user saw an explanation and the correct response(s) after answering the previous question bundle, ignoring any lectures in between. The value is shared across a single question bundle, and is null for a user's first question bundle or lecture. Typically the first several questions a user sees were part of an onboarding diagnostic test where they did not get any feedback.
