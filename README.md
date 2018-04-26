# Spam-Classifier-using-SVM

## Dataset
Many email services today provide spam filters that are able to classify emails into spam and non-spam email with high accuracy. I used SVM to build the spam classifier. We can begin with training a classifier to classify whether a given email, x, is spam (y = 1) or non-spam (y = 0). In particular, we need to convert each email into a feature vector x 2 Rn. The dataset included is based on a a subset of
the SpamAssassin Public Corpus. We will only be using the body of the email (excluding the email headers).

## Preprocessing the email
In processEmail.m, we have implemented the following email preprocessing and normalization steps:
• Lower-casing: The entire email is converted into lower case, so that captialization is ignored (e.g., IndIcaTE is treated the same as
Indicatt.
• Stripping HTML: All HTML tags are removed from the emails. Many emails often come with HTML formatting; we remove all the
HTML tags, so that only the content remains.
• Normalizing URLs: All URLs are replaced with the text \httpaddr".
• Normalizing Email Addresses: All email addresses are replaced with the text \emailaddr".
• Normalizing Numbers: All numbers are replaced with the text\number".
• Normalizing Dollars: All dollar signs ($) are replaced with the text\dollar".
• Word Stemming: Words are reduced to their stemmed form. For expiample, \discount", \discounts", \discounted" and \discounting" are all
replaced with \discount". Sometimes, the Stemmer actually strips additional characters from the end, so \include", \includes", \included",
and \including" are all replaced with \includ".
• Removal of non-words: Non-words and punctuation have been removed. All white spaces (tabs, newlines, spaces) have all been trimmed
to a single space character.

