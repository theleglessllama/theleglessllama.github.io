---
layout: post
title: "Intern Offer Letter"
date: 2013-10-03 10:35
comments: true
categories: ["Internship", "Contract Templates", "Recruitment"]
---

## Uses

This letter

- Extends an offer of internship to a possible intern
- Recognizes the intern as a member of openlectures
- States the terms of internship, including
	- Duties
	- Compensation
	- Confidentiality Statement
	- Conflict of Interest Declaration

## Compilation

Compile the follow code using XeLaTeX, replacing the relevant variables.

## Code

```
\documentclass{scrartcl}
\usepackage{dominatrix}
\usepackage[top=2cm,bottom=3cm]{geometry}

\def\DefaultWidthofText{\textwidth}

% Variables
\newcommand{\mycompany}{openlectures\xspace}
\newcommand{\me}{Linan Qiu\xspace}
\newcommand{\myposition}{Founder\xspace}
\newcommand{\you}{John Doe\xspace}
\newcommand{\yourposition}{Student Intern\xspace}
\newcommand{\supervisor}{\textbf{Royce Zhou}, Academic Director\xspace}
\newcommand{\signdate}{7 June 2013\xspace}
\newcommand{\startdate}{13 June 2013\xspace}
\newcommand{\finishdate}{14 June 2013\xspace}
\newcommand{\duties}{writing and the production of video content. \xspace}

% Title Information
\title{Internship Offer Letter}
\author{\mycompany}
\date{Revised Date: \today}
\begin{document}
\maketitle
Dear \textbf{\you}:\\

It gives me great pleasure to offer you a position at openlectures (the ``company''). In addition to confirming the offer, this letter will describe the terms and conditions of your internship.\\

TITLE: Your title will be \textbf{\yourposition}. You will report to \supervisor, or as otherwise directed by \mycompany.

DUTIES: You will assist with \duties

EFFECTIVE DATE: Your internship will begin on \textbf{\startdate} and end on \textbf{\finishdate}.

COMPENSATION: The spirit of \mycompany is non-profit. As an intern, you will not be an employee of \mycompany. Therefore, you will not receive a salary, wages, or other compensation. In addition, you will not be eligible for any of the employee benefits that company employees are entitled to, including, but not limited to, health insurance, vacation or sick pay, or paid holidays.

However, \mycompany will aim to break even on cost expenditures which includes but is not limited to filming equipment and other associated costs.

When and if \mycompany has the means to issue dividends, \mycompany will offer to compensate you at the rates attached behind this contract. You may or may not choose decide to accept your dividends. If you do, we wish you all the best and encourage you not to spend it on booze. If you donât, a donation to \mycompany of that exact amount will be made in your name, and \mycompany will honor it as we would all other donations.

INTELLECTUAL PROPERTY: Content that you produce as an intern with \mycompany while with \mycompany belongs to \mycompany. Content that you produce for third parties that are not \mycompany while you're with \mycompany is yours to use.

CONFIDENTIALITY: During your internship and (if your internship is discontinued for any reason whatsoever) thereafter, you agree to keep strictly confidential all trade secrets and information that \mycompany holds proprietary or confidential. You also agree that as condition of your internship, you will sign, and comply with, a company-standard Intern Proprietary Information and Inventions and Non-Competition Agreement, including the related arbitration agreement. You further agree to follow \mycompany's strict policy that interns must not disclose, either directly or indirectly, any information, including any of the terms of this letter, regarding compensation to any person, including other interns of \mycompany; provided, however, that you may discuss the terms of this letter with members of your immediate family and any legal, tax or accounting specialists who provide you with individual, legal or tax accounting advice. In addition, upon conclusion of your internship, you must return all company-owned property, equipment, and documents, including electronic mail or other information.

INTERN REPRESENTATION: You represent that:
\begin{inparaenum}[(1)]
\item you are not a party to any agreement that would prohibit you from entering into internship with \mycompany;
\item no trade secret or proprietary information belonging to your previous employers will be disclosed by you at \mycompany, and that no such information, whether in the form of documents, memoranda, software, drawings, etc., will be retained by you or brought with you to \mycompany; and
\item you have brought to \mycompany's attention and provided it with a copy of any agreement, order of any court or administrative body or any other similar item that may impact your future internship at \mycompany, including but not limited to any non-disclosure, non-competition, non-solicitation or invention assignment agreements containing future work restrictions.
\end{inparaenum}

AT-WILL INTERNSHIP: Your internship with \mycompany is ``At-Will''. As an intern, either \mycompany or you may discontinue the internship relationship at any time for any reason not prohibited by law. Accordingly, there is no guarantee of continuous employment and the terms and/or conditions of employment may be modified at any time. 

TERMINATION: As an intern, either \mycompany or you may discontinue the internship relationship at any time for any reason not prohibited by law. Furthermore, there is no guarantee of continuous employment and the terms and/or conditions of employment may be modified at any time. 

This letter and its enclosures reflect the entire agreement regarding the terms and conditions of your internship. Accordingly, it supersedes and completely replaces any prior oral or written communication on this subject. This letter may not be modified or amended except by a written agreement, signed by \mycompany and you. The offer described above is contingent upon the results of your reference/background check.\\

We look forward to having you join us, and we expect that our relationship will be mutually rewarding. To confirm your acceptance of this offer and position, please sign and return this document by \textbf{\signdate}. If this letter is not received by said date, the offer will be considered retracted.\\

\begin{figure}[ht!]
\vspace{20ex}
\hspace*{-1.5ex}\begin{tabular}{ll}
\makebox[0.49\textwidth]{\hrulefill} & \makebox[0.49\textwidth]{\hrulefill}\\
\textbf{\you} & \textbf{\me}\\
& \myposition \\
& \mycompany \\
\today & \today
\end{tabular}
\end{figure}

\newpage

\textbf{Compensation Rates}

When, if ever, \mycompany chooses to convert to a profit model, \mycompany will use the first \$10,000 to cover the expenses of setting up \mycompany. Following which, \textbf{writers, editors and filmers} will be given the following choices

\begin{enumerate}
\item Be compensated at the following rates

WRITERS: \$5 per checkpoint used in \mycompany's final products. A final product is defined to be a video checkpoint uploaded to YouTube and made available on \mycompany's webpage.

EDITORS: \$3 per checkpoint used in \mycompany's final products. A final product is defined to be a video checkpoint uploaded to YouTube and made available on \mycompany's webpage. If editing involved rewriting more than 50\% of the script, the editor shall be paid at the rate of \textbf{writers}.

FILMERS: \$2 per checkpoint used in \mycompany's final products. This only applies to final takes that are used eventually. B-takes are not included. A final product is defined to be a video checkpoint uploaded to YouTube and made available on \mycompany's webpage. 

\item Forgo the compensation and take up a \textbf{salaried position} at \mycompany. The rates, and \textbf{equity stake}, if any, will open to discussion.
\end{enumerate}

Interns are free to discuss the terms of internship. Those terms override these terms stated here.

\newpage

\end{document}
```