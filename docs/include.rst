.. raw:: html

    <style>
        /*Header Separation for longer docs*/
        
        /*Table of Contents targets*/
        a.toc-backref {
            text-decoration: none;
            color: black;
        }
        a.toc-backref:hover {
            background-color: inherit;
        }

        h1, h2, h3, h4, h5, h6 {
            border: thin solid black;
            border-radius: 6px;
            padding: 4px;
            background-color: #cccccc;
        }
        h1.title {
            text-align: center;
            font-variant: small-caps;
            background-color: #161616;
            color: #dddddd;
            border: thick solid black;
            border-radius: 12px;
        }
        h1 {
            background-color: #666666;
            border: medium solid black;
        }
        h2 {
            background-color: #808080;
            border: medium solid black;
            margin-left: 2.5vw;
        }
        h3 {
            background-color: #888888;
            margin-left: 5vw;
        }
        h4 {
            background-color: #aaaaaa;
            margin-left: 7.5vw;
        }
        h5 {
            background-color: #cccccc;
            margin-left: 10vw;
        }
        h6 {
            background-color: #eeeeee;
            margin-left: 12.5vw;
        }
        
        /*Traffic light styling to all admonitions*/
        .attention, .caution, .danger, .error, .hint, .important, .note, .tip, .warning {
            border-radius:8px;
            color: black;
            padding: 3px;
            width: 80%;
        }
        .hint, .important, .note, .tip {
            background-color: #90ee90;
            border: medium solid green;
        }
        .attention, .caution, .warning {
            background-color: #ffe2ae;
            border: medium solid orange;
        }
        .danger, .error {
            background-color:  #ffa4a4;
            border: medium solid red;
        }

        p.admonition-title {
            text-align: center;
            font-weight: bold;
            font-variant: small-caps;
            display: block;
            margin: 0;
            /*Trick CSS to make title block background darker*/
            background-color: rgba(0,0,0,.2);
            border-radius: 4px;
        }
        :is(.hint, .important, .note, .tip) p.admonition-title::before {
            content:"📑 ";
        }
        :is(.attention, .caution, .warning) p.admonition-title::before {
        content:"⚠️ ";
        }
        :is(.danger, .error) p.admonition-title::before {
        content:"⛔ ";
        }
    </style>