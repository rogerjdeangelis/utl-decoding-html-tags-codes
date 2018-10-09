# utl-decoding-html-tags-codes
Decoding html tags codes.

    Decoding html tags codes

    github
    https://github.com/rogerjdeangelis/utl-decoding-html-tags-codes

    https://tinyurl.com/y9ac43lw
    https://communities.sas.com/t5/SAS-Programming/htmldecode-function-in-open-code/m-p/502546#M134163

    Chris Prooks
    https://communities.sas.com/t5/user/viewprofilepage/user-id/32246


    Converting '&lt' to '<' and &gt to '>'
    ======================================

    Datastep
    --------

    data have;
      tagged = '&lt;tag&gt;';
      decode = htmldecode(tagged);
    run;quit;

    WORK.HAVE total obs=1

         TAGGED       DECODE

       &lt;tag&gt;    <tag>

    Macro
    -----

       %let tagged = %nrstr(&lt;tag&gt;);
       %let decode = %qsysfunc(htmldecode(&tagged));
       %Put &=decode;

       DECODE=<tag>


