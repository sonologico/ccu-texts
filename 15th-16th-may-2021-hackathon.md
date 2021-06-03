# May 2021 On-The-Fly Hackathon

On the 15th and 16th of May 2021, we had a small hackathon as part of the On-The-Fly project at Creative Coding Utrecht. There were seven people involved: Fabian Van Sluijs, Felipe Ignacio Noriega, Ibo Ibelings, Sietse van der Meer, Timo Hoogland, Vera van de Seyp, and I, Raphael Sousa Santos. Our source material was the preliminary result of an online survey targeted at creative coders, related institutions, and their audience. We had three main goals:
 * To make sense of the response of the survey and see how we could improve it going forward
 * To experiment with the data in the responses and present it in creative ways
 * To experiment with this format of hackathon and think about out how to host a larger one in a similar format
On Saturday morning, we started slowly with a round of introductions and, after an initial bolt of collaboration extracting the survey response into a JSON file, we decided to each take some time to play with the data independently. That went well and we gravitated to what we would be doing for the rest of the day.

Felipe and I collaborated on an API to expose the data and aggregated results more flexibly. Having that in place, we could easily extract responses to specific questions and group them by other criteria. Getting a distribution of creative coding tools used per country, for example, was insightful. Doing that involved splitting and normalizing the responses, which highlighted changes that could be done to the survey to make automated processing easier. With the API available through a web server, the other participants could use it in their projects.

The Saturday ended with Timo sharing the output of his sonification of the responses using speech synthesis done with Max. The repeating words and multiple layers of voices at different speeds caused a powerful impression. On Sunday, Timo expanded into the browser using the Web Speech API. That proved to be less flexible than Max, which led to a simpler sonic output. This made the higher representation of certain tools, countries and gender in the survey evidently clear. Timo also included a visualization of the spoken words, which added to the overall message.

In parallel, Fabian and Vera had been working on a hand curated database of creative coders and related institutions. Felipe worked on merging the two sources of information, which led to us having more data to play with on Sunday. The day ended with Vera and Ibo showing us their D3.js-based visualizations. Both really illustrated the complexity of the data set.

In the end, we felt that the format worked. We ended up with multiple presentations of the data, the 2 D3.js visualizations and the 2 sonifications based on speech synthesis, and having an API in place. More importantly, we now also have an idea of the next steps towards exposing this data to a wider audience with the goal of growing it into a community knowledge base of creative coding practitioners and resources:
 * Update the survey questions based on our insights going through the responses [link to survey](https://onthefly.creativecodingutrecht.nl)
 * Improve the survey interface and response storage format to capture the data in a more structured format. For example, on questions that allow multiple answers, such as when we ask what tools people are using, we would provide multiple input fields instead of a single text field as we currently do. This should make it easier to process the responses later
 * Improve the API. The two immediate points to address are to make it more robust regarding error handling and to make it read the data from a production database instead of from a JSON file
 * Productionize the API in order to have it publicly available
 * Design an accessible UI to navigate and collaboratively update this data so that it remains relevant. This is a larger effort and a project in and of itself.
