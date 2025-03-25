# How to use hw1-RAG?
Please just execute the mlhw1.ipynb on colab.
# How to evaluate the public.txt result?
After you get the result on colab, you can use answers-from-public-txt.md to evaluate your public answer. 
I gave my answer and answers-from-public-txt.md to claude3.7 to check the correctness of my answer.
You may use the following prompt to evalute: "請你根據answers-from-public-txt.md來評估my_answer.txt的答案是否正確?只要你認為兩者表達的意思相同就可算對。請幫我計算有幾題是正確的，並列出正確和錯誤的題目 "
# Method
I implemented the strong baseline architecture.
I used Meta-Llama-3.1-8B-Instruct-Q8_0 as our only LLM model. It plays three roles in my pipeline: question_extraction_agent, keyword_extraction_agent, and qa_agent. When a user's query comes in, the question_extraction_agent extracts the essential part of the query. The keyword_extraction_agent then extracts keywords for searching on Google based on the result from the question_extraction_agent. Finally, I combine the search results and the question for the qa_agent which answers the question.
# My Result
I got 21 correct answers.