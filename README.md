# Temperature_rise
The objective of this project is to perform exploratory data analysis in order to understand the relationship between Temperature rise and CO2 emmission derriving from the agri-food sector activities.

<!DOCTYPE html>

<html lang="en">

<head>

    <script nonce="4QoCa3wo6f+wopLQU0G2tA==">

    document.addEventListener('keydown', (e) => {

        // Stop propagation on ESC because otherwise it will halt outbound XHRs

        // See b/131755324 for more info.

        if (e.key === 'Escape') {

            e.stopPropagation();

            e.preventDefault();

        }

    });

    </script>

    <meta name="referrer" content="origin"/>

    <meta name="viewport" content="width=device-width, initial-scale=1">

    <title>Google Colab</title>

    <link rel="search" type="application/opensearchdescription+xml" href="/opensearch.xml" title="Google Colaboratory"/>

    <style>

    .gb_bb:not(.gb_dd) {

        font: 13px/27px Roboto, Arial, sans-serif;

        z-index:986

    }



    @-webkit-keyframes gb__a {

        0% {

            opacity:0

        }



        50% {

            opacity:1

        }

    }



    @keyframes gb__a {

        0% {

            opacity:0

        }



        50% {

            opacity:1

        }

    }



    a.gb_sa {

        border: none;

        color: #4285f4;

        cursor: default;

        font-weight: bold;

        outline: none;

        position: relative;

        text-align: center;

        text-decoration: none;

        text-transform: uppercase;

        white-space: nowrap;

        -webkit-user-select:none

    }



    a.gb_sa:hover:after, a.gb_sa:focus:after {

        background-color: rgba(0, 0, 0, .12);

        content: "";

        height: 100%;

        left: 0;

        position: absolute;

        top: 0;

        width:100%

    }



    a.gb_sa:hover, a.gb_sa:focus {

        text-decoration:none

    }



    a.gb_sa:active {

        background-color: rgba(153, 153, 153, .4);

        text-decoration:none

    }



    a.gb_ta {

        background-color: #4285f4;

        color:#fff

    }



    a.gb_ta:active {

        background-color:#0043b2

    }



    .gb_ua {

        box-shadow:0 1px 1px rgba(0, 0, 0, .16)

    }



    .gb_sa, .gb_ta, .gb_va, .gb_wa {

        display: inline-block;

        line-height: 28px;

        padding: 0 12px;

        border-radius:2px

    }



    .gb_va {

        background: #f8f8f8;

        border:1px solid #c6c6c6

    }



    .gb_wa {

        background:#f8f8f8

    }



    .gb_va, #gb a.gb_va.gb_va, .gb_wa {

        color: #666;

        cursor: default;

        text-decoration:none

    }



    #gb a.gb_wa {

        cursor: default;

        text-decoration:none

    }



    .gb_wa {

        border: 1px solid #4285f4;

        font-weight: bold;

        outline: none;

        background: #4285f4;

        background: -webkit-gradient(linear, left top, left bottom, from(top), color-stop(#4387fd), to(#4683ea));

        background: -webkit-linear-gradient(top, #4387fd, #4683ea);

        background: linear-gradient(top, #4387fd, #4683ea);

        filter:progid:DXImageTransform.Microsoft.gradient(startColorstr=#4387fd, endColorstr=#4683ea, GradientType=0)

    }



    #gb a.gb_wa {

        color:#fff

    }



    .gb_wa:hover {

        box-shadow:0 1px 0 rgba(0, 0, 0, .15)

    }



    .gb_wa:active {

        box-shadow: inset 0 2px 0 rgba(0, 0, 0, .15);

        background: #3c78dc;

        background: -webkit-gradient(linear, left top, left bottom, from(top), color-stop(#3c7ae4), to(#3f76d3));

        background: -webkit-linear-gradient(top, #3c7ae4, #3f76d3);

        background: linear-gradient(top, #3c7ae4, #3f76d3);

        filter:progid:DXImageTransform.Microsoft.gradient(startColorstr=#3c7ae4, endColorstr=#3f76d3, GradientType=0)

    }



    #gb .gb_xa {

        background: #fff;

        border: 1px solid #dadce0;

        color: #1a73e8;

        display: inline-block;

        text-decoration:none

    }



    #gb .gb_xa:hover {

        background: #f8fbff;

        border-color: #dadce0;

        color:#174ea6

    }



    #gb .gb_xa:focus {

        background: #f4f8ff;

        color: #174ea6;

        outline:1px solid #174ea6

    }



    #gb .gb_xa:active, #gb .gb_xa:focus:active {

        background: #ecf3fe;

        color:#174ea6

    }



    #gb .gb_xa.gb_j {

        background: transparent;

        border: 1px solid #5f6368;

        color: #8ab4f8;

        text-decoration:none

    }



    #gb .gb_xa.gb_j:hover {

        background: rgba(255, 255, 255, .04);

        color:#e8eaed

    }



    #gb .gb_xa.gb_j:focus {

        background: rgba(232, 234, 237, .12);

        color: #e8eaed;

        outline:1px solid #e8eaed

    }



    #gb .gb_xa.gb_j:active, #gb .gb_xa.gb_j:focus:active {

        background: rgba(232, 234, 237, .1);

        color:#e8eaed

    }



    .gb_p {

        display:none !important

    }



    .gb_Va {

        visibility:hidden

    }



    .gb_Kd {

        display: inline-block;

        vertical-align:middle

    }



    .gb_Md .gb_o {

        bottom: -3px;

        right:-5px

    }



    .gb_g {

        position:relative

    }



    .gb_d {

        display: inline-block;

        outline: none;

        vertical-align: middle;

        border-radius: 2px;

        box-sizing: border-box;

        height: 40px;

        width: 40px;

        cursor: pointer;

        text-decoration:none

    }



    #gb#gb a.gb_d {

        cursor: pointer;

        text-decoration:none

    }



    .gb_d, a.gb_d {

        color:#000

    }



    .gb_bf {

        border-color: transparent;

        border-bottom-color: #fff;

        border-style: dashed dashed solid;

        border-width: 0 8.5px 8.5px;

        display: none;

        position: absolute;

        left: 11.5px;

        top: 33px;

        z-index: 1;

        height: 0;

        width: 0;

        -webkit-animation: gb__a .2s;

        animation:gb__a .2s

    }



    .gb_cf {

        border-color: transparent;

        border-style: dashed dashed solid;

        border-width: 0 8.5px 8.5px;

        display: none;

        position: absolute;

        left: 11.5px;

        z-index: 1;

        height: 0;

        width: 0;

        -webkit-animation: gb__a .2s;

        animation: gb__a .2s;

        border-bottom-color: rgba(0, 0, 0, .2);

        top:32px

    }



    x:-o-prefocus, div.gb_cf {

        border-bottom-color:#ccc

    }



    .gb_0 {

        background: #fff;

        border: 1px solid #ccc;

        border-color: rgba(0, 0, 0, .2);

        color: #000;

        -webkit-box-shadow: 0 2px 10px rgba(0, 0, 0, .2);

        box-shadow: 0 2px 10px rgba(0, 0, 0, .2);

        display: none;

        outline: none;

        overflow: hidden;

        position: absolute;

        right: 8px;

        top: 62px;

        -webkit-animation: gb__a .2s;

        animation: gb__a .2s;

        border-radius: 2px;

        -webkit-user-select:text

    }



    .gb_Kd.gb_Fa .gb_bf, .gb_Kd.gb_Fa .gb_cf, .gb_Kd.gb_Fa .gb_0, .gb_Fa.gb_0 {

        display:block

    }



    .gb_Kd.gb_Fa.gb_df .gb_bf, .gb_Kd.gb_Fa.gb_df .gb_cf {

        display:none

    }



    .gb_Nd {

        position: absolute;

        right: 8px;

        top: 62px;

        z-index:-1

    }



    .gb_2a .gb_bf, .gb_2a .gb_cf, .gb_2a .gb_0 {

        margin-top:-10px

    }



    .gb_Kd:first-child, #gbsfw:first-child + .gb_Kd {

        padding-left:4px

    }



    .gb_Ka.gb_Od .gb_Kd:first-child {

        padding-left:0

    }



    .gb_Pd {

        position:relative

    }



    .gb_Ka .gb_Qd .gb_Id.gb_gd, .gb_Ka.gb_La .gb_Qd .gb_Id.gb_gd {

        padding:3px 8px 3px 16px

    }



    .gb_Qd .gb_Rd {

        display:inline-block

    }



    .gb_Qd .gb_gd {

        -webkit-border-radius: 100px;

        border-radius: 100px;

        background: #0b57d0;

        color: #fff;

        font-size: 14px;

        font-weight: 500;

        white-space: nowrap;

        width:auto

    }



    .gb_Qd .gb_Sd {

        -webkit-box-align: center;

        -webkit-align-items: center;

        -webkit-align-items: center;

        align-items: center;

        display: -webkit-inline-box;

        display: -webkit-inline-flex;

        display: -webkit-inline-box;

        display: -webkit-inline-flex;

        display:inline-flex

    }



    .gb_Qd .gb_x {

        fill: #0b57d0;

        margin-left:8px

    }



    .gb_Qd .gb_x circle {

        fill:#fff

    }



    .gb_Qd .gb_gd .gb_Dd {

        -webkit-box-flex: 1;

        -webkit-flex-grow: 1;

        -webkit-box-flex: 1;

        box-flex: 1;

        -webkit-flex-grow: 1;

        flex-grow: 1;

        text-align:center

    }



    .gb_Qd .gb_gd:hover {

        background:#3763cd

    }



    .gb_Qd .gb_gd:hover .gb_x {

        fill:#3763cd

    }



    .gb_Qd .gb_gd:focus, .gb_Qd .gb_gd:active, .gb_Qd .gb_gd:focus:hover, .gb_Qd .gb_gd[aria-expanded=true], .gb_Qd .gb_gd:hover[aria-expanded=true] {

        background:#416acf

    }



    .gb_Qd .gb_gd:focus .gb_x, .gb_Qd .gb_gd:active .gb_x, .gb_Qd .gb_gd:focus:hover .gb_x, .gb_Qd .gb_gd[aria-expanded=true] .gb_x, .gb_Qd .gb_gd:hover[aria-expanded=true] .gb_x {

        fill:#416acf

    }



    .gb_Qd .gb_gd:hover, .gb_Qd .gb_gd:focus, .gb_Qd .gb_gd:active, .gb_Qd .gb_gd[aria-expanded=true] {

        -webkit-box-shadow: 0 1px 3px 1px rgba(66, 64, 67, .15), 0 1px 2px 0 rgba(60, 64, 67, .3);

        box-shadow:0 1px 3px 1px rgba(66, 64, 67, .15), 0 1px 2px 0 rgba(60, 64, 67, .3)

    }



    .gb_Qd .gb_gd:focus-visible {

        outline: 1px solid #416acf;

        outline-offset:2px

    }



    .gb_Qd .gb_j.gb_gd {

        background: #a8c7fa;

        color:#062e6f

    }



    .gb_Qd .gb_j.gb_gd .gb_x {

        fill:#a8c7fa

    }



    .gb_Qd .gb_j.gb_gd .gb_x circle {

        fill:#062e6f

    }



    .gb_Qd .gb_j.gb_gd:hover {

        background:#b4cbf6

    }



    .gb_Qd .gb_j.gb_gd:hover .gb_x {

        fill:#b4cbf6

    }



    .gb_Qd .gb_j.gb_gd:focus, .gb_Qd .gb_j.gb_gd:focus:hover, .gb_Qd .gb_j.gb_gd:active, .gb_Qd .gb_j.gb_gd[aria-expanded=true], .gb_Qd .gb_j.gb_gd:hover[aria-expanded=true] {

        background:#b8cdf7

    }



    .gb_Qd .gb_j.gb_gd:focus .gb_x, .gb_Qd .gb_j.gb_gd:focus:hover .gb_x, .gb_Qd .gb_j.gb_gd:active .gb_x, .gb_Qd .gb_j.gb_gd[aria-expanded=true] .gb_x, .gb_Qd .gb_j.gb_gd:hover[aria-expanded=true] .gb_x {

        fill:#b8cdf7

    }



    .gb_Qd .gb_j.gb_gd:focus-visible {

        outline-color:#b8cdf7

    }



    .gb_Qd .gb_j.gb_gd:hover, .gb_Qd .gb_j.gb_gd:focus, .gb_Qd .gb_j.gb_gd:active, .gb_Qd .gb_j.gb_gd[aria-expanded=true] {

        -webkit-box-shadow: 0 1px 3px 1px rgba(66, 64, 67, .15), 0 1px 2px 0 rgba(60, 64, 67, .3);

        box-shadow:0 1px 3px 1px rgba(66, 64, 67, .15), 0 1px 2px 0 rgba(60, 64, 67, .3)

    }



    .gb_0c .gb_Pd, .gb_f .gb_Pd {

        float:right

    }



    .gb_d {

        padding: 8px;

        cursor:pointer

    }



    .gb_d:after {

        content: "";

        position: absolute;

        top: -4px;

        bottom: -4px;

        left: -4px;

        right:-4px

    }



    .gb_Ka .gb_ge:not(.gb_sa):focus img {

        background-color: rgba(0, 0, 0, .2);

        outline: none;

        -webkit-border-radius: 50%;

        border-radius:50%

    }



    .gb_Td button svg, .gb_d {

        -webkit-border-radius: 50%;

        border-radius:50%

    }



    .gb_Td button:focus:not(:focus-visible) svg, .gb_Td button:hover svg, .gb_Td button:active svg, .gb_d:focus:not(:focus-visible), .gb_d:hover, .gb_d:active, .gb_d[aria-expanded=true] {

        outline:none

    }



    .gb_Jc .gb_Td.gb_pe button:focus-visible svg, .gb_Td button:focus-visible svg, .gb_d:focus-visible {

        outline:1px solid #202124

    }



    .gb_Jc .gb_Td button:focus-visible svg, .gb_Jc .gb_d:focus-visible {

        outline:1px solid #f1f3f4

    }



    @media (forced-colors: active) {

        .gb_Jc .gb_Td.gb_pe button:focus-visible svg, .gb_Td button:focus-visible svg, .gb_Jc .gb_Td button:focus-visible svg {

            outline:1px solid currentcolor

        }

    }



    .gb_Jc .gb_Td.gb_pe button:focus svg, .gb_Jc .gb_Td.gb_pe button:focus:hover svg, .gb_Td button:focus svg, .gb_Td button:focus:hover svg, .gb_d:focus, .gb_d:focus:hover {

        background-color:rgba(60, 64, 67, .1)

    }



    .gb_Jc .gb_Td.gb_pe button:active svg, .gb_Td button:active svg, .gb_d:active {

        background-color:rgba(60, 64, 67, .12)

    }



    .gb_Jc .gb_Td.gb_pe button:hover svg, .gb_Td button:hover svg, .gb_d:hover {

        background-color:rgba(60, 64, 67, .08)

    }



    .gb_ya .gb_d.gb_Aa:hover {

        background-color:transparent

    }



    .gb_d[aria-expanded=true], .gb_d:hover[aria-expanded=true] {

        background-color:rgba(95, 99, 104, .24)

    }



    .gb_d[aria-expanded=true] .gb_i {

        fill: #5f6368;

        opacity:1

    }



    .gb_Jc .gb_Td button:hover svg, .gb_Jc .gb_d:hover {

        background-color:rgba(232, 234, 237, .08)

    }



    .gb_Jc .gb_Td button:focus svg, .gb_Jc .gb_Td button:focus:hover svg, .gb_Jc .gb_d:focus, .gb_Jc .gb_d:focus:hover {

        background-color:rgba(232, 234, 237, .1)

    }



    .gb_Jc .gb_Td button:active svg, .gb_Jc .gb_d:active {

        background-color:rgba(232, 234, 237, .12)

    }



    .gb_Jc .gb_d[aria-expanded=true], .gb_Jc .gb_d:hover[aria-expanded=true] {

        background-color:rgba(255, 255, 255, .12)

    }



    .gb_Jc .gb_d[aria-expanded=true] .gb_i {

        fill: #fff;

        opacity:1

    }



    .gb_Kd {

        padding:4px

    }



    .gb_Ka.gb_Od .gb_Kd {

        padding:4px 2px

    }



    .gb_Ka.gb_Od .gb_b.gb_Kd {

        padding-left:6px

    }



    .gb_0 {

        z-index: 991;

        line-height:normal

    }



    .gb_0.gb_Ud {

        left: 0;

        right:auto

    }



    @media (max-width: 350px) {

        .gb_0.gb_Ud {

            left:0

        }

    }



    .gb_Vd .gb_0 {

        top:56px

    }



    .gb_l .gb_d, .gb_Z .gb_l .gb_d {

        background-position:-64px -29px

    }



    .gb_E .gb_l .gb_d {

        background-position: -29px -29px;

        opacity:1

    }



    .gb_l .gb_d, .gb_l .gb_d:hover, .gb_l .gb_d:focus {

        opacity:1

    }



    .gb_ed {

        display:none

    }



    @media screen and (max-width: 319px) {

        .gb_ld:not(.gb_qd) .gb_l {

            display: none;

            visibility:hidden

        }

    }



    .gb_o {

        display:none

    }



    .gb_8c {

        font-family: Google Sans, Roboto, Helvetica, Arial, sans-serif;

        font-size: 20px;

        font-weight: 400;

        letter-spacing: 0.25px;

        line-height: 48px;

        margin-bottom: 2px;

        opacity: 1;

        overflow: hidden;

        padding-left: 16px;

        position: relative;

        text-overflow: ellipsis;

        vertical-align: middle;

        top: 2px;

        white-space: nowrap;

        -webkit-flex: 1 1 auto;

        -webkit-box-flex: 1;

        flex:1 1 auto

    }



    .gb_8c.gb_9c {

        color:#3c4043

    }



    .gb_Ka.gb_La .gb_8c {

        margin-bottom:0

    }



    .gb_ad.gb_bd .gb_8c {

        padding-left:4px

    }



    .gb_Ka.gb_La .gb_cd {

        position: relative;

        top:-2px

    }



    .gb_Ka {

        color: black;

        min-width: 160px;

        position: relative;

        -webkit-transition: box-shadow 250ms;

        transition:box-shadow 250ms

    }



    .gb_Ka.gb_Rc {

        min-width:120px

    }



    .gb_Ka.gb_jd .gb_kd {

        display:none

    }



    .gb_Ka.gb_jd .gb_ld {

        height:56px

    }



    header.gb_Ka {

        display:block

    }



    .gb_Ka svg {

        fill:currentColor

    }



    .gb_md {

        position: fixed;

        top: 0;

        width:100%

    }



    .gb_nd {

        -webkit-box-shadow: 0 4px 5px 0 rgba(0, 0, 0, .14), 0 1px 10px 0 rgba(0, 0, 0, .12), 0 2px 4px -1px rgba(0, 0, 0, .2);

        box-shadow:0 4px 5px 0 rgba(0, 0, 0, .14), 0 1px 10px 0 rgba(0, 0, 0, .12), 0 2px 4px -1px rgba(0, 0, 0, .2)

    }



    .gb_od {

        height:64px

    }



    .gb_ld {

        -webkit-box-sizing: border-box;

        box-sizing: border-box;

        position: relative;

        width: 100%;

        display: -webkit-box;

        display: -webkit-flex;

        display: flex;

        -webkit-box-pack: space-between;

        -webkit-justify-content: space-between;

        justify-content: space-between;

        min-width: -webkit-min-content;

        min-width:min-content

    }



    .gb_Ka:not(.gb_La) .gb_ld {

        padding:8px

    }



    .gb_Ka.gb_pd .gb_ld {

        -webkit-flex: 1 0 auto;

        -webkit-box-flex: 1;

        flex:1 0 auto

    }



    .gb_Ka .gb_ld.gb_qd.gb_rd {

        min-width:0

    }



    .gb_Ka.gb_La .gb_ld {

        padding: 4px;

        padding-left: 8px;

        min-width:0

    }



    .gb_kd {

        height: 48px;

        vertical-align: middle;

        white-space: nowrap;

        -webkit-box-align: center;

        -webkit-align-items: center;

        align-items: center;

        display: -webkit-box;

        display: -webkit-flex;

        display: flex;

        -webkit-user-select:none

    }



    .gb_td > .gb_kd {

        display: table-cell;

        width:100%

    }



    .gb_ad {

        padding-right: 30px;

        box-sizing: border-box;

        -webkit-flex: 1 0 auto;

        -webkit-box-flex: 1;

        flex:1 0 auto

    }



    .gb_Ka.gb_La .gb_ad {

        padding-right:14px

    }



    .gb_ud {

        -webkit-flex: 1 1 100%;

        -webkit-box-flex: 1;

        flex:1 1 100%

    }



    .gb_ud > :only-child {

        display:inline-block

    }



    .gb_vd.gb_1c {

        padding-left:4px

    }



    .gb_vd.gb_wd, .gb_Ka.gb_pd .gb_vd, .gb_Ka.gb_La:not(.gb_f) .gb_vd {

        padding-left:0

    }



    .gb_Ka.gb_La .gb_vd.gb_wd {

        padding-right:0

    }



    .gb_Ka.gb_La .gb_vd.gb_wd .gb_ya {

        margin-left:10px

    }



    .gb_1c {

        display:inline

    }



    .gb_Ka.gb_Uc .gb_vd.gb_xd, .gb_Ka.gb_f .gb_vd.gb_xd {

        padding-left:2px

    }



    .gb_8c {

        display:inline-block

    }



    .gb_vd {

        -webkit-box-sizing: border-box;

        box-sizing: border-box;

        height: 48px;

        line-height: normal;

        padding: 0 4px;

        padding-left: 30px;

        -webkit-flex: 0 0 auto;

        -webkit-box-flex: 0;

        flex: 0 0 auto;

        -webkit-box-pack: flex-end;

        -webkit-justify-content: flex-end;

        justify-content:flex-end

    }



    .gb_f {

        height:48px

    }



    .gb_Ka.gb_f {

        min-width:auto

    }



    .gb_f .gb_vd {

        float: right;

        padding-left:32px

    }



    .gb_f .gb_vd.gb_yd {

        padding-left:0

    }



    .gb_zd {

        font-size: 14px;

        max-width: 200px;

        overflow: hidden;

        padding: 0 12px;

        text-overflow: ellipsis;

        white-space: nowrap;

        -webkit-user-select:text

    }



    .gb_fd {

        -webkit-transition: background-color .4s;

        -webkit-transition: background-color .4s;

        transition:background-color .4s

    }



    .gb_Fd {

        color:black

    }



    .gb_Jc {

        color:white

    }



    .gb_Ka a, .gb_Oc a {

        color:inherit

    }



    .gb_P {

        color:rgba(0, 0, 0, .87)

    }



    .gb_Ka svg, .gb_Oc svg, .gb_ad .gb_id, .gb_0c .gb_id {

        color: #5f6368;

        opacity:1

    }



    .gb_Jc svg, .gb_Oc.gb_Sc svg, .gb_Jc .gb_ad .gb_id, .gb_Jc .gb_ad .gb_Ic, .gb_Jc .gb_ad .gb_cd, .gb_Oc.gb_Sc .gb_id {

        color:rgba(255, 255, 255, .87)

    }



    .gb_Jc .gb_ad .gb_Hc:not(.gb_Hd) {

        opacity:.87

    }



    .gb_9c {

        color: inherit;

        opacity: 1;

        text-rendering: optimizeLegibility;

        -webkit-font-smoothing:antialiased

    }



    .gb_Jc .gb_9c, .gb_Fd .gb_9c {

        opacity:1

    }



    .gb_Ad {

        position:relative

    }



    .gb_Bd {

        font-family: arial, sans-serif;

        line-height: normal;

        padding-right:15px

    }



    a.gb_B, span.gb_B {

        color: rgba(0, 0, 0, .87);

        text-decoration:none

    }



    .gb_Jc a.gb_B, .gb_Jc span.gb_B {

        color:white

    }



    a.gb_B:focus {

        outline-offset:2px

    }



    a.gb_B:hover {

        text-decoration:underline

    }



    .gb_C {

        display: inline-block;

        padding-left:15px

    }



    .gb_C .gb_B {

        display: inline-block;

        line-height: 24px;

        vertical-align:middle

    }



    .gb_Id {

        font-family: Google Sans, Roboto, Helvetica, Arial, sans-serif;

        font-weight: 500;

        font-size: 14px;

        letter-spacing: .25px;

        line-height: 16px;

        margin-left: 10px;

        margin-right: 8px;

        min-width: 96px;

        padding: 9px 23px;

        text-align: center;

        vertical-align: middle;

        border-radius: 4px;

        box-sizing:border-box

    }



    .gb_Ka.gb_f .gb_Id {

        margin-left:8px

    }



    #gb a.gb_wa.gb_Id {

        cursor:pointer

    }



    .gb_wa.gb_Id:hover {

        background: #1b66c9;

        -webkit-box-shadow: 0 1px 3px 1px rgba(66, 64, 67, .15), 0 1px 2px 0 rgba(60, 64, 67, .3);

        box-shadow:0 1px 3px 1px rgba(66, 64, 67, .15), 0 1px 2px 0 rgba(60, 64, 67, .3)

    }



    .gb_wa.gb_Id:focus, .gb_wa.gb_Id:hover:focus {

        background: #1c5fba;

        -webkit-box-shadow: 0 1px 3px 1px rgba(66, 64, 67, .15), 0 1px 2px 0 rgba(60, 64, 67, .3);

        box-shadow:0 1px 3px 1px rgba(66, 64, 67, .15), 0 1px 2px 0 rgba(60, 64, 67, .3)

    }



    .gb_wa.gb_Id:active {

        background: #1b63c1;

        -webkit-box-shadow: 0 1px 3px 1px rgba(66, 64, 67, .15), 0 1px 2px 0 rgba(60, 64, 67, .3);

        box-shadow:0 1px 3px 1px rgba(66, 64, 67, .15), 0 1px 2px 0 rgba(60, 64, 67, .3)

    }



    .gb_Id {

        background: #1a73e8;

        border:1px solid transparent

    }



    .gb_Ka.gb_La .gb_Id {

        padding: 9px 15px;

        min-width:80px

    }



    .gb_Cd {

        text-align:left

    }



    #gb .gb_Jc a.gb_Id:not(.gb_j), #gb.gb_Jc a.gb_Id:not(.gb_t) {

        background: #fff;

        border-color: #dadce0;

        -webkit-box-shadow: none;

        box-shadow: none;

        color:#1a73e8

    }



    #gb a.gb_wa.gb_j.gb_Id {

        background: #8ab4f8;

        border: 1px solid transparent;

        -webkit-box-shadow: none;

        box-shadow: none;

        color:#202124

    }



    #gb .gb_Jc a.gb_Id:hover:not(.gb_j), #gb.gb_Jc a.gb_Id:not(.gb_t):hover {

        background: #f8fbff;

        border-color:#cce0fc

    }



    #gb a.gb_wa.gb_j.gb_Id:hover {

        background: #93baf9;

        border-color: transparent;

        -webkit-box-shadow: 0 1px 3px 1px rgba(0, 0, 0, .15), 0 1px 2px rgba(0, 0, 0, .3);

        box-shadow:0 1px 3px 1px rgba(0, 0, 0, .15), 0 1px 2px rgba(0, 0, 0, .3)

    }



    #gb .gb_Jc a.gb_Id:focus:not(.gb_j), #gb .gb_Jc a.gb_Id:focus:hover:not(.gb_j), #gb.gb_Jc a.gb_Id:focus:not(.gb_j), #gb.gb_Jc a.gb_Id:focus:hover:not(.gb_j) {

        background: #f4f8ff;

        outline:1px solid #c9ddfc

    }



    #gb a.gb_wa.gb_j.gb_Id:focus, #gb a.gb_wa.gb_j.gb_Id:focus:hover {

        background: #a6c6fa;

        border-color: transparent;

        -webkit-box-shadow: none;

        box-shadow:none

    }



    #gb .gb_Jc a.gb_Id:active:not(.gb_j), #gb.gb_Jc a.gb_Id:not(.gb_t):active {

        background:#ecf3fe

    }



    #gb a.gb_wa.gb_j.gb_Id:active {

        background: #a1c3f9;

        -webkit-box-shadow: 0 1px 2px rgba(60, 64, 67, .3), 0 2px 6px 2px rgba(60, 64, 67, .15);

        box-shadow:0 1px 2px rgba(60, 64, 67, .3), 0 2px 6px 2px rgba(60, 64, 67, .15)

    }



    .gb_Jd {

        display:none

    }



    @media screen and (max-width: 319px) {

        .gb_ld:not(.gb_qd) .gb_l {

            display: none;

            visibility:hidden

        }

    }



    .gb_ya {

        background-color: rgba(255, 255, 255, .88);

        border: 1px solid #dadce0;

        -webkit-box-sizing: border-box;

        box-sizing: border-box;

        cursor: pointer;

        display: inline-block;

        max-height: 48px;

        overflow: hidden;

        outline: none;

        padding: 0;

        vertical-align: middle;

        width: 134px;

        -webkit-border-radius: 8px;

        border-radius:8px

    }



    .gb_ya.gb_j {

        background-color: transparent;

        border:1px solid #5f6368

    }



    .gb_Ea {

        display:inherit

    }



    .gb_ya.gb_j .gb_Ea {

        background: #fff;

        -webkit-border-radius: 4px;

        border-radius: 4px;

        display: inline-block;

        left: 8px;

        margin-right: 5px;

        position: relative;

        padding: 3px;

        top:-1px

    }



    .gb_ya:hover {

        border: 1px solid #d2e3fc;

        background-color:rgba(248, 250, 255, .88)

    }



    .gb_ya.gb_j:hover {

        background-color: rgba(241, 243, 244, .04);

        border:1px solid #5f6368

    }



    .gb_ya:focus-visible, .gb_ya:focus {

        background-color: #fff;

        outline: 1px solid #202124;

        -webkit-box-shadow: 0 1px 2px 0 rgba(60, 64, 67, .3), 0 1px 3px 1px rgba(60, 64, 67, .15);

        box-shadow:0 1px 2px 0 rgba(60, 64, 67, .3), 0 1px 3px 1px rgba(60, 64, 67, .15)

    }



    .gb_ya.gb_j:focus-visible, .gb_ya.gb_j:focus {

        background-color: rgba(241, 243, 244, .12);

        outline: 1px solid #f1f3f4;

        -webkit-box-shadow: 0 1px 3px 1px rgba(0, 0, 0, .15), 0 1px 2px 0 rgba(0, 0, 0, .3);

        box-shadow:0 1px 3px 1px rgba(0, 0, 0, .15), 0 1px 2px 0 rgba(0, 0, 0, .3)

    }



    .gb_ya.gb_j:active, .gb_ya.gb_Fa.gb_j:focus {

        background-color: rgba(241, 243, 244, .1);

        border:1px solid #5f6368

    }



    .gb_Ha {

        display: inline-block;

        padding-bottom: 2px;

        padding-left: 7px;

        padding-top: 2px;

        text-align: center;

        vertical-align: middle;

        line-height: 32px;

        width:78px

    }



    .gb_ya.gb_j .gb_Ha {

        line-height: 26px;

        margin-left: 0;

        padding-bottom: 0;

        padding-left: 0;

        padding-top: 0;

        width:72px

    }



    .gb_Ha.gb_Ia {

        background-color: #f1f3f4;

        -webkit-border-radius: 4px;

        border-radius: 4px;

        margin-left: 8px;

        padding-left: 0;

        line-height:30px

    }



    .gb_Ha.gb_Ia .gb_Ja {

        vertical-align:middle

    }



    .gb_Ka:not(.gb_La) .gb_ya {

        margin-left: 10px;

        margin-right:4px

    }



    .gb_Ma {

        max-height: 32px;

        width:78px

    }



    .gb_ya.gb_j .gb_Ma {

        max-height: 26px;

        width:72px

    }



    .gb_n {

        -webkit-background-size: 32px 32px;

        background-size: 32px 32px;

        border: 0;

        -webkit-border-radius: 50%;

        border-radius: 50%;

        display: block;

        margin: 0px;

        position: relative;

        height: 32px;

        width: 32px;

        z-index:0

    }



    .gb_Wa {

        background-color: #e8f0fe;

        border: 1px solid rgba(32, 33, 36, .08);

        position:relative

    }



    .gb_Wa.gb_n {

        height: 30px;

        width:30px

    }



    .gb_Wa.gb_n:hover, .gb_Wa.gb_n:active {

        -webkit-box-shadow: none;

        box-shadow:none

    }



    .gb_Xa {

        background: #fff;

        border: none;

        -webkit-border-radius: 50%;

        border-radius: 50%;

        bottom: 2px;

        -webkit-box-shadow: 0px 1px 2px 0px rgba(60, 64, 67, .30), 0px 1px 3px 1px rgba(60, 64, 67, .15);

        box-shadow: 0px 1px 2px 0px rgba(60, 64, 67, .30), 0px 1px 3px 1px rgba(60, 64, 67, .15);

        height: 14px;

        margin: 2px;

        position: absolute;

        right: 0;

        width:14px

    }



    .gb_Za {

        color: #1f71e7;

        font: 400 22px/32px Google Sans, Roboto, Helvetica, Arial, sans-serif;

        text-align: center;

        text-transform:uppercase

    }



    @media (-webkit-min-device-pixel-ratio: 1.25),(min-resolution: 1.25dppx),(min-device-pixel-ratio: 1.25) {

        .gb_n::before, .gb_0a::before {

            display: inline-block;

            -webkit-transform: scale(0.5);

            -webkit-transform: scale(0.5);

            transform: scale(0.5);

            -webkit-transform-origin: left 0;

            -webkit-transform-origin: left 0;

            transform-origin:left 0

        }



        .gb_H .gb_0a::before {

            -webkit-transform: scale(scale(0.416666667));

            -webkit-transform: scale(scale(0.416666667));

            transform:scale(scale(0.416666667))

        }

    }



    .gb_n:hover, .gb_n:focus {

        -webkit-box-shadow: 0 1px 0 rgba(0, 0, 0, .15);

        box-shadow:0 1px 0 rgba(0, 0, 0, .15)

    }



    .gb_n:active {

        -webkit-box-shadow: inset 0 2px 0 rgba(0, 0, 0, .15);

        box-shadow:inset 0 2px 0 rgba(0, 0, 0, .15)

    }



    .gb_n:active::after {

        background: rgba(0, 0, 0, .1);

        -webkit-border-radius: 50%;

        border-radius: 50%;

        content: "";

        display: block;

        height:100%

    }



    .gb_1a {

        cursor: pointer;

        line-height: 40px;

        min-width: 30px;

        opacity: .75;

        overflow: hidden;

        vertical-align: middle;

        text-overflow:ellipsis

    }



    .gb_d.gb_1a {

        width:auto

    }



    .gb_1a:hover, .gb_1a:focus {

        opacity:.85

    }



    .gb_2a .gb_1a, .gb_2a .gb_3a {

        line-height:26px

    }



    #gb#gb.gb_2a a.gb_1a, .gb_2a .gb_3a {

        font-size: 11px;

        height:auto

    }



    .gb_4a {

        border-top: 4px solid #000;

        border-left: 4px dashed transparent;

        border-right: 4px dashed transparent;

        display: inline-block;

        margin-left: 6px;

        opacity: .75;

        vertical-align:middle

    }



    .gb_Aa:hover .gb_4a {

        opacity:.85

    }



    .gb_ya > .gb_b {

        padding:3px 3px 3px 4px

    }



    .gb_5a.gb_Va {

        color:#fff

    }



    .gb_E .gb_1a, .gb_E .gb_4a {

        opacity:1

    }



    #gb#gb.gb_E.gb_E a.gb_1a, #gb#gb .gb_E.gb_E a.gb_1a {

        color:#fff

    }



    .gb_E.gb_E .gb_4a {

        border-top-color: #fff;

        opacity:1

    }



    .gb_Z .gb_n:hover, .gb_E .gb_n:hover, .gb_Z .gb_n:focus, .gb_E .gb_n:focus {

        -webkit-box-shadow: 0 1px 0 rgba(0, 0, 0, .15), 0 1px 2px rgba(0, 0, 0, .2);

        box-shadow:0 1px 0 rgba(0, 0, 0, .15), 0 1px 2px rgba(0, 0, 0, .2)

    }



    .gb_6a .gb_b, .gb_7a .gb_b {

        position: absolute;

        right:1px

    }



    .gb_b.gb_D, .gb_8a.gb_D, .gb_Aa.gb_D {

        -webkit-flex: 0 1 auto;

        -webkit-box-flex: 0;

        flex:0 1 auto

    }



    .gb_9a.gb_ab .gb_1a {

        width:30px !important

    }



    .gb_m {

        height: 40px;

        position: absolute;

        right: -5px;

        top: -5px;

        width:40px

    }



    .gb_bb .gb_m, .gb_cb .gb_m {

        right: 0;

        top:0

    }



    .gb_b .gb_d {

        padding:4px

    }



    .gb_q {

        display:none

    }



    sentinel {

    }

    </style>

    <script nonce="4QoCa3wo6f+wopLQU0G2tA==">

    ;

    this.gbar_ = {

        CONFIG: [[[0, "www.gstatic.com", "og.qtm.en_US.nx2Jnk1Ygb4.2019.O", "gr", "en-GB", "425", 0, [4, 2, "", "", "", "562419365", "0"], null, "cVwAZdzlNf3KwN4P4rCUkAc", null, 0, "og.qtm.EUdp1kxzvEQ.L.W.O", "AA2YrTszxV_5VMFUaEh4OLex-3Cy10nllw", "AA2YrTtfOtKifcJmQnNkq6t0R2Yv9F4pXg", "", 2, 1, 200, "GRC", null, null, "425", "425", 1], null, [1, 0.1000000014901161, 2, 1], null, [1, 0, 0, null, "0", "dkastrinakis@gmail.com", "", "AMN_icOoSUrklgExCEDmc98bIVD6ANrRt-DTwoQRiSrZsmMuUMntndg2bSV3xvcrmxu3amwIAyCterIhvtNY4nUIYSMnVYR_2g", 0, 0, 0], [0, 0, "", 1, 0, 0, 0, 0, 0, 0, null, 0, 0, null, 0, 0, null, null, 0, 0, 0, "", "", "", "", "", "", null, 0, 0, 0, 0, 0, null, null, null, "rgba(32,33,36,1)", "rgba(255,255,255,1)", 0, 0, 0, null, null, 1, 0, 0], ["%1$s (default)", "Brand account", 1, "%1$s (delegated)", 1, null, 83, "https://colab.research.google.com/drive/1PThCmmKaBpYL00ELUku1mk4dIpFOcQ1e?authuser=$authuser", null, null, null, 1, "https://accounts.google.com/ListAccounts?listPages=0\u0026authuser=0\u0026pid=425\u0026gpsia=1\u0026source=ogb\u0026atic=1\u0026mo=1\u0026mn=1\u0026hl=en-GB\u0026ts=250", 0, "dashboard", null, null, null, null, "Profile", "", 1, null, "Signed out", "https://accounts.google.com/AccountChooser?source=ogb\u0026continue=$continue\u0026Email=$email\u0026ec=GAhAqQM", "https://accounts.google.com/RemoveLocalAccount?source=ogb", "Remove", "Sign in", 0, 1, 1, 0, 1, 1, 0, null, null, null, "Session expired", null, null, null, "Visitor", null, "Default", "Delegated", "Sign out of all accounts", 1, null, null, 0, null, null, "myaccount.google.com", "https", 0, 1, 0], null, ["1", "gci_91f30755d6a6b787dcc2a4062e6e9824.js", "googleapis.client:gapi.iframes", "0", "en-GB"], null, null, null, null, ["m;/_/scs/abc-static/_/js/k=gapi.gapi.en.vIVemAYlBvo.O/d=1/rs=AHpOoo_eZqauDOH0vAaumGJQwp71CTPx9g/m=__features__", "https://apis.google.com", "", "", "1", "", null, 1, "es_plusone_gc_20230802.0_p0", "en-GB", null, 0], [0.009999999776482582, "gr", "425", [null, "", "0", null, 1, 5184000, null, null, "", null, null, null, null, null, 0, null, 0, null, 1, 0, 0, 0, null, null, 0, 0, null, 0, 0, 0, 0, 0], null, null, null, 0, null, null, ["5061451", "google\\.(com|ru|ca|by|kz|com\\.mx|com\\.tr)$", 1], "114591953"], [1, 1, null, 40400, 425, "GRC", "en-GB", "562419365.0", 8, 0.009999999776482582, 1, 0, null, null, null, null, "3700942,3701183,3701185", null, null, null, "cVwAZdzlNf3KwN4P4rCUkAc", 0, 0, 0, null, 2, 5, "nn", 12, 0, 0, 1, 1, 1], [[null, null, null, "https://www.gstatic.com/og/_/js/k=og.qtm.en_US.nx2Jnk1Ygb4.2019.O/rt=j/m=qabr,qgl,q_dnp,qcwid,qbd,qapid,qrcd,q_dg/exm=qaaw,qadd,qaid,qein,qhaw,qhba,qhbr,qhch,qhga,qhid,qhin/d=1/ed=1/rs=AA2YrTszxV_5VMFUaEh4OLex-3Cy10nllw"], [null, null, null, "https://www.gstatic.com/og/_/ss/k=og.qtm.EUdp1kxzvEQ.L.W.O/m=qcwid/excm=qaaw,qadd,qaid,qein,qhaw,qhba,qhbr,qhch,qhga,qhid,qhin/d=1/ed=1/ct=zgms/rs=AA2YrTtfOtKifcJmQnNkq6t0R2Yv9F4pXg"]], null, null, null, [[[null, null, [null, null, null, "https://ogs.google.com/u/0/widget/account?amf=1\u0026amb=1\u0026sea=1"], 0, 414, 436, 57, 4, 1, 0, 0, 65, 66, 8000, "https://accounts.google.com/SignOutOptions?hl=en-GB\u0026continue=https://colab.research.google.com/drive/1PThCmmKaBpYL00ELUku1mk4dIpFOcQ1e\u0026ec=GBRAqQM", 68, 2, null, null, 1, 113, "Something went wrong.%1$s Refresh to try again or %2$schoose another account%3$s.", 3, null, null, 75, 0, null, null, null, null, null, null, null, "/widget/account", ["https", "myaccount.google.com", 0, 32, 83, 0], 0, 0, 1, ["Critical security alert", "Important account alert"], 0, 1, null, 1, 1]], null, null, "425", "425", 1, 0, null, "en-GB", 0, ["https://colab.research.google.com/drive/1PThCmmKaBpYL00ELUku1mk4dIpFOcQ1e?authuser=$authuser", "https://accounts.google.com/AddSession?hl=en-GB\u0026continue=https://colab.research.google.com/drive/1PThCmmKaBpYL00ELUku1mk4dIpFOcQ1e\u0026ec=GAlAqQM", "https://accounts.google.com/Logout?hl=en-GB\u0026continue=https://colab.research.google.com/drive/1PThCmmKaBpYL00ELUku1mk4dIpFOcQ1e\u0026timeStmp=1694522481\u0026secTok=.AG5fkS8iXjP0ni7-UB-6fo774W05vUAd3Q\u0026ec=GAdAqQM", "https://accounts.google.com/ListAccounts?listPages=0\u0026authuser=0\u0026pid=425\u0026gpsia=1\u0026source=ogb\u0026atic=1\u0026mo=1\u0026mn=1\u0026hl=en-GB\u0026ts=250", 0, 0, "", 0, 0, null, 0, 0, "https://accounts.google.com/ServiceLogin?passive=true\u0026continue=https%3A%2F%2Fcolab.research.google.com%2Fdrive%2F1PThCmmKaBpYL00ELUku1mk4dIpFOcQ1e\u0026ec=GAZAqQM"], 0, 0, 0, null, 0, "114591953"], null, [["mousedown", "touchstart", "touchmove", "wheel", "keydown"], 300000], [[null, null, null, "https://accounts.google.com/RotateCookiesPage"], 3, 4000, 1, 0, 3701183]]],

    };

    this.gbar_ = this.gbar_ || {};

    (function(_) {

        var window = this;

        try {

            /*



             Copyright The Closure Library Authors.

             SPDX-License-Identifier: Apache-2.0

            */

            var ia,

                na,

                qa,

                ra,

                za,

                Ba,

                Ca,

                Da,

                Ea,

                Ha,

                Qa,

                Sa,

                Ra,

                Ua,

                Wa,

                Va,

                Xa,

                Ya,

                db;

            _.aa = function(a, b) {

                if (Error.captureStackTrace)

                    Error.captureStackTrace(this, _.aa);

                else {

                    const c = Error().stack;

                    c && (this.stack = c)

                }

                a && (this.message = String(a));

                void 0 !== b && (this.cause = b)

            };

            _.ca = function(a) {

                _.p.setTimeout(() => {

                    throw a;

                }, 0)

            };

            _.ea = function() {

                var a = _.p.navigator;

                return a && (a = a.userAgent) ? a : ""

            };

            ia = function(a) {

                return fa ? ha ? ha.brands.some(({brand: b}) => b && -1 != b.indexOf(a)) : !1 : !1

            };

            _.t = function(a) {

                return -1 != _.ea().indexOf(a)

            };

            _.ja = function() {

                return fa ? !!ha && 0 < ha.brands.length : !1

            };

            _.ka = function() {

                return _.ja() ? !1 : _.t("Opera")

            };

            _.la = function() {

                return _.ja() ? !1 : _.t("Trident") || _.t("MSIE")

            };

            _.ma = function() {

                return _.t("Firefox") || _.t("FxiOS")

            };

            _.oa = function() {

                return _.t("Safari") && !(na() || (_.ja() ? 0 : _.t("Coast")) || _.ka() || (_.ja() ? 0 : _.t("Edge")) || (_.ja() ? ia("Microsoft Edge") : _.t("Edg/")) || (_.ja() ? ia("Opera") : _.t("OPR")) || _.ma() || _.t("Silk") || _.t("Android"))

            };

            na = function() {

                return _.ja() ? ia("Chromium") : (_.t("Chrome") || _.t("CriOS")) && !(_.ja() ? 0 : _.t("Edge")) || _.t("Silk")

            };

            _.pa = function() {

                return _.t("Android") && !(na() || _.ma() || _.ka() || _.t("Silk"))

            };

            qa = function() {

                return fa ? !!ha && !!ha.platform : !1

            };

            ra = function() {

                return _.t("iPhone") && !_.t("iPod") && !_.t("iPad")

            };

            _.sa = function() {

                return ra() || _.t("iPad") || _.t("iPod")

            };

            _.ta = function() {

                return qa() ? "macOS" === ha.platform : _.t("Macintosh")

            };

            _.va = function(a, b) {

                return 0 <= _.ua(a, b)

            };

            _.wa = function(a) {

                let b = "",

                    c = 0;

                const d = a.length - 10240;

                for (; c < d;)

                    b += String.fromCharCode.apply(null, a.subarray(c, c += 10240));

                b += String.fromCharCode.apply(null, c ? a.subarray(c) : a);

                return btoa(b)

            };

            _.xa = function(a) {

                return null != a && a instanceof Uint8Array

            };

            _.ya = function(a) {

                return Array.prototype.slice.call(a)

            };

            za = function(a) {

                const b = a[_.u] | 0;

                1 !== (b & 1) && (Object.isFrozen(a) && (a = _.ya(a)), a[_.u] = b | 1)

            };

            _.Aa = function(a) {

                a[_.u] |= 1;

                return a

            };

            Ba = function(a, b) {

                b[_.u] = (a | 0) & -255

            };

            Ca = function(a, b) {

                b[_.u] = (a | 34) & -221

            };

            Da = function(a) {

                a = a >> 11 & 1023;

                return 0 === a ? 536870912 : a

            };

            Ea = function(a) {

                return null !== a && "object" === typeof a && !Array.isArray(a) && a.constructor === Object

            };

            _.Fa = function(a) {

                if (a & 2)

                    throw Error();

            };

            Ha = function(a, b) {

                (b = _.Ga ? b[_.Ga] : void 0) && (a[_.Ga] = _.ya(b))

            };

            _.Ia = function(a) {

                Number.isFinite(a) || _.ca(Error());

                return a

            };

            _.Ja = function(a) {

                if ("number" !== typeof a)

                    throw Error();

                Number.isFinite(a);

                return a

            };

            _.Ka = function(a) {

                if (null != a && "string" !== typeof a)

                    throw Error();

                return a

            };

            _.La = function(a) {

                return null == a || "string" === typeof a ? a : void 0

            };

            _.Na = function(a, b, c) {

                var d = !1;

                if (null != a && "object" === typeof a && !(d = Array.isArray(a)) && a.qe === Ma)

                    return a;

                if (d) {

                    var e = d = a[_.u] | 0;

                    0 === e && (e |= c & 32);

                    e |= c & 2;

                    e !== d && (a[_.u] = e);

                    return new b(a)

                }

            };

            _.Pa = function(a, b) {

                Oa = b;

                a = new a(b);

                Oa = void 0;

                return a

            };

            Qa = function(a, b, c) {

                const d = 1023 + b,

                    e = a.length;

                for (let f = d; f < e; f++) {

                    const g = a[f];

                    null != g && g !== c && (c[f - b] = g)

                }

                a.length = d + 1;

                a[d] = c

            };

            Sa = function(a, b) {

                return Ra(b)

            };

            Ra = function(a) {

                switch (typeof a) {

                case "number":

                    return isFinite(a) ? a : String(a);

                case "boolean":

                    return a ? 1 : 0;

                case "object":

                    if (a && !Array.isArray(a)) {

                        if (_.xa(a))

                            return _.wa(a);

                        if ("function" == typeof _.Ta && a instanceof _.Ta)

                            return a.hg()

                    }

                }

                return a

            };

            Ua = function(a, b, c) {

                const d = _.ya(a);

                var e = d.length;

                const f = b & 256 ? d[e - 1] : void 0;

                e += f ? -1 : 0;

                for (b = b & 512 ? 1 : 0; b < e; b++)

                    d[b] = c(d[b]);

                if (f) {

                    b = d[b] = {};

                    for (const g in f)

                        b[g] = c(f[g])

                }

                Ha(d, a);

                return d

            };

            Wa = function(a, b, c, d, e, f) {

                if (null != a) {

                    if (Array.isArray(a))

                        a = e && 0 == a.length && (a[_.u] | 0) & 1 ? void 0 : f && (a[_.u] | 0) & 2 ? a : Va(a, b, c, void 0 !== d, e, f);

                    else if (Ea(a)) {

                        const g = {};

                        for (let h in a)

                            g[h] = Wa(a[h], b, c, d, e, f);

                        a = g

                    } else

                        a = b(a, d);

                    return a

                }

            };

            Va = function(a, b, c, d, e, f) {

                const g = d || c ? a[_.u] | 0 : 0;

                d = d ? !!(g & 32) : void 0;

                const h = _.ya(a);

                for (let k = 0; k < h.length; k++)

                    h[k] = Wa(h[k], b, c, d, e, f);

                c && (Ha(h, a), c(g, h));

                return h

            };

            Xa = function(a) {

                return a.qe === Ma ? a.toJSON() : Ra(a)

            };

            Ya = function(a, b, c=Ca) {

                if (null != a) {

                    if (a instanceof Uint8Array)

                        return b ? a : new Uint8Array(a);

                    if (Array.isArray(a)) {

                        const d = a[_.u] | 0;

                        return d & 2 ? a : !b || d & 68 || !(d & 32 || 0 === d) ? Va(a, Ya, d & 4 ? Ca : c, !0, !1, !0) : (a[_.u] = d | 34, a)

                    }

                    a.qe === Ma && (b = a.na, c = b[_.u], a = c & 2 ? a : _.Pa(a.constructor, _.Za(b, c, !0)));

                    return a

                }

            };

            _.Za = function(a, b, c) {

                const d = c || b & 2 ? Ca : Ba,

                    e = !!(b & 32);

                a = Ua(a, b, f => Ya(f, e, d));

                a[_.u] = a[_.u] | 32 | (c ? 2 : 0);

                return a

            };

            _.$a = function(a) {

                const b = a.na,

                    c = b[_.u];

                return c & 2 ? _.Pa(a.constructor, _.Za(b, c, !1)) : a

            };

            _.ab = function(a, b, c, d, e) {

                var f = Da(b);

                if (c >= f || e) {

                    e = b;

                    if (b & 256)

                        f = a[a.length - 1];

                    else {

                        if (null == d)

                            return;

                        f = a[f + (+!!(b & 512) - 1)] = {};

                        e |= 256

                    }

                    f[c] = d;

                    e !== b && (a[_.u] = e)

                } else

                    a[c + (+!!(b & 512) - 1)] = d,

                    b & 256 && (a = a[a.length - 1], c in a && delete a[c])

            };

            _.bb = function(a, b) {

                return null != a ? a : b

            };

            db = function(a, b, c) {

                var d = a.constructor.ya,

                    e = Da((c ? a.na : b)[_.u]),

                    f = !1;

                if (d) {

                    if (!c) {

                        b = _.ya(b);

                        var g;

                        if (b.length && Ea(g = b[b.length - 1]))

                            for (f = 0; f < d.length; f++)

                                if (d[f] >= e) {

                                    Object.assign(b[b.length - 1] = {}, g);

                                    break

                                }

                        f = !0

                    }

                    e = b;

                    c = !c;

                    g = a.na[_.u];

                    a = Da(g);

                    g = +!!(g & 512) - 1;

                    var h;

                    for (let F = 0; F < d.length; F++) {

                        var k = d[F];

                        if (k < a) {

                            k += g;

                            var m = e[k];

                            null == m ? e[k] = c ? _.cb : _.Aa([]) : c && m !== _.cb && za(m)

                        } else {

                            if (!h) {

                                var n = void 0;

                                e.length && Ea(n = e[e.length - 1]) ? h = n : e.push(h = {})

                            }

                            m = h[k];

                            null == h[k] ? h[k] = c ? _.cb : _.Aa([]) : c && m !== _.cb && za(m)

                        }

                    }

                }

                d =

                b.length;

                if (!d)

                    return b;

                let q,

                    v;

                if (Ea(h = b[d - 1])) {

                    a:

                    {

                        var r = h;

                        n = {};

                        e = !1;

                        for (let F in r)

                            c = r[F],

                            Array.isArray(c) && c != c && (e = !0),

                            null != c ? n[F] = c : e = !0;

                        if (e) {

                            for (let F in n) {

                                r = n;

                                break a

                            }

                            r = null

                        }

                    }r != h && (q = !0);

                    d--

                }

                for (; 0 < d; d--) {

                    h = b[d - 1];

                    if (null != h)

                        break;

                    v = !0

                }

                if (!q && !v)

                    return b;

                var D;

                f ? D = b : D = Array.prototype.slice.call(b, 0, d);

                b = D;

                f && (b.length = d);

                r && b.push(r);

                return b

            };

            _.w = function(a, b) {

                return null != a ? !!a : !!b

            };

            _.x = function(a, b) {

                void 0 == b && (b = "");

                return null != a ? a : b

            };

            _.eb = function(a, b) {

                void 0 == b && (b = 0);

                return null != a ? a : b

            };

            _.gb = function(a, b) {

                let c,

                    d;

                for (let e = 1; e < arguments.length; e++) {

                    d = arguments[e];

                    for (c in d)

                        a[c] = d[c];

                    for (let f = 0; f < fb.length; f++)

                        c = fb[f],

                        Object.prototype.hasOwnProperty.call(d, c) && (a[c] = d[c])

                }

            };

            var mb,

                nb;

            _.hb = _.hb || {};

            _.p = this || self;

            _.ib = function(a, b) {

                a = a.split(".");

                b = b || _.p;

                for (var c = 0; c < a.length; c++)

                    if (b = b[a[c]], null == b)

                        return null;

                return b

            };

            _.jb = function(a) {

                var b = typeof a;

                return "object" != b ? b : a ? Array.isArray(a) ? "array" : b : "null"

            };

            _.kb = function(a) {

                var b = typeof a;

                return "object" == b && null != a || "function" == b

            };

            _.lb = "closure_uid_" + (1E9 * Math.random() >>> 0);

            mb = function(a, b, c) {

                return a.call.apply(a.bind, arguments)

            };

            nb = function(a, b, c) {

                if (!a)

                    throw Error();

                if (2 < arguments.length) {

                    var d = Array.prototype.slice.call(arguments, 2);

                    return function() {

                        var e = Array.prototype.slice.call(arguments);

                        Array.prototype.unshift.apply(e, d);

                        return a.apply(b, e)

                    }

                }

                return function() {

                    return a.apply(b, arguments)

                }

            };

            _.y = function(a, b, c) {

                _.y = Function.prototype.bind && -1 != Function.prototype.bind.toString().indexOf("native code") ? mb : nb;

                return _.y.apply(null, arguments)

            };

            _.z = function(a, b) {

                a = a.split(".");

                var c = _.p;

                a[0] in c || "undefined" == typeof c.execScript || c.execScript("var " + a[0]);

                for (var d; a.length && (d = a.shift());)

                    a.length || void 0 === b ? c[d] && c[d] !== Object.prototype[d] ? c = c[d] : c = c[d] = {} : c[d] = b

            };

            _.A = function(a, b) {

                function c() {}

                c.prototype = b.prototype;

                a.V = b.prototype;

                a.prototype = new c;

                a.prototype.constructor = a;

                a.xi = function(d, e, f) {

                    for (var g = Array(arguments.length - 2), h = 2; h < arguments.length; h++)

                        g[h - 2] = arguments[h];

                    return b.prototype[e].apply(d, g)

                }

            };

            _.A(_.aa, Error);

            _.aa.prototype.name = "CustomError";

            _.ob = String.prototype.trim ? function(a) {

                return a.trim()

            } : function(a) {

                return /^[\s\xa0]*([\s\S]*?)[\s\xa0]*$/.exec(a)[1]

            };

            var fa,

                pb = _.ib("WIZ_global_data.oxN3nb"),

                qb = pb && pb[610401301];

            fa = null != qb ? qb : !1;

            var ha,

                rb = _.p.navigator;

            ha = rb ? rb.userAgentData || null : null;

            _.ua = function(a, b) {

                return Array.prototype.indexOf.call(a, b, void 0)

            };

            _.sb = function(a, b, c) {

                Array.prototype.forEach.call(a, b, c)

            };

            _.tb = function(a) {

                _.tb[" "](a);

                return a

            };

            _.tb[" "] = function() {};

            var Gb,

                Hb,

                Mb;

            _.ub = _.ka();

            _.B = _.la();

            _.vb = _.t("Edge");

            _.wb = _.vb || _.B;

            _.xb = _.t("Gecko") && !(-1 != _.ea().toLowerCase().indexOf("webkit") && !_.t("Edge")) && !(_.t("Trident") || _.t("MSIE")) && !_.t("Edge");

            _.yb = -1 != _.ea().toLowerCase().indexOf("webkit") && !_.t("Edge");

            _.zb = _.ta();

            _.Ab = qa() ? "Windows" === ha.platform : _.t("Windows");

            _.Bb = qa() ? "Android" === ha.platform : _.t("Android");

            _.Cb = ra();

            _.Db = _.t("iPad");

            _.Eb = _.t("iPod");

            _.Fb = _.sa();

            Gb = function() {

                var a = _.p.document;

                return a ? a.documentMode : void 0

            };

            a:

            {

                var Ib = "",

                    Jb = function() {

                        var a = _.ea();

                        if (_.xb)

                            return /rv:([^\);]+)(\)|;)/.exec(a);

                        if (_.vb)

                            return /Edge\/([\d\.]+)/.exec(a);

                        if (_.B)

                            return /\b(?:MSIE|rv)[: ]([^\);]+)(\)|;)/.exec(a);

                        if (_.yb)

                            return /WebKit\/(\S+)/.exec(a);

                        if (_.ub)

                            return /(?:Version)[ \/]?(\S+)/.exec(a)

                    }();

                Jb && (Ib = Jb ? Jb[1] : "");

                if (_.B) {

                    var Kb = Gb();

                    if (null != Kb && Kb > parseFloat(Ib)) {

                        Hb = String(Kb);

                        break a

                    }

                }

                Hb = Ib

            }_.Lb = Hb;

            if (_.p.document && _.B) {

                var Nb = Gb();

                Mb = Nb ? Nb : parseInt(_.Lb, 10) || void 0

            } else

                Mb = void 0;

            _.Ob = Mb;

            _.Pb = _.ma();

            _.Qb = ra() || _.t("iPod");

            _.Rb = _.t("iPad");

            _.Sb = _.pa();

            _.Tb = na();

            _.Ub = _.oa() && !_.sa();

            _.Vb = "undefined" !== typeof TextDecoder;

            _.Wb = "undefined" !== typeof TextEncoder;

            _.u = Symbol();

            var Ma,

                Xb,

                Yb;

            Ma = {};

            Yb = [];

            Yb[_.u] = 39;

            _.cb = Object.freeze(Yb);

            var Oa;

            _.C = function(a, b) {

                a = a.na;

                return _.$b(a, a[_.u], b)

            };

            _.$b = function(a, b, c, d) {

                if (-1 === c)

                    return null;

                if (c >= Da(b)) {

                    if (b & 256)

                        return a[a.length - 1][c]

                } else {

                    var e = a.length;

                    if (d && b & 256 && (d = a[e - 1][c], null != d))

                        return d;

                    b = c + (+!!(b & 512) - 1);

                    if (b < e)

                        return a[b]

                }

            };

            _.ac = function(a, b, c, d) {

                const e = a.na,

                    f = e[_.u];

                _.Fa(f);

                _.ab(e, f, b, c, d);

                return a

            };

            _.E = function(a, b) {

                a = _.C(a, b);

                return null == a ? a : "boolean" !== typeof a && "number" !== typeof a ? void 0 : !!a

            };

            _.bc = function(a, b, c, d) {

                a = a.na;

                const e = a[_.u],

                    f = _.$b(a, e, c, d);

                b = _.Na(f, b, e);

                b !== f && null != b && _.ab(a, e, c, b, d);

                return b

            };

            _.G = function(a, b, c, d=!1) {

                b = _.bc(a, b, c, d);

                if (null == b)

                    return b;

                a = a.na;

                const e = a[_.u];

                if (!(e & 2)) {

                    const f = _.$a(b);

                    f !== b && (b = f, _.ab(a, e, c, b, d))

                }

                return b

            };

            _.H = function(a, b, c) {

                null == c && (c = void 0);

                return _.ac(a, b, c)

            };

            _.I = function(a, b) {

                return _.La(_.C(a, b))

            };

            _.J = function(a, b) {

                return _.bb(_.E(a, b), !1)

            };

            _.cc = function(a, b, c=0) {

                a = a.na;

                const d = a[_.u],

                    e = _.$b(a, d, b);

                var f = null == e ? e : "number" === typeof e || "NaN" === e || "Infinity" === e || "-Infinity" === e ? Number(e) : void 0;

                null != f && f !== e && _.ab(a, d, b, f);

                return _.bb(f, c)

            };

            _.K = function(a, b) {

                return _.bb(_.I(a, b), "")

            };

            _.L = function(a, b, c) {

                if (null != c) {

                    if ("boolean" !== typeof c)

                        throw Error("q`" + _.jb(c) + "`" + c);

                    c = !!c

                }

                return _.ac(a, b, c)

            };

            _.M = function(a, b, c) {

                return _.ac(a, b, null == c ? c : _.Ja(c))

            };

            _.N = function(a, b, c) {

                return _.ac(a, b, _.Ka(c))

            };

            _.O = function(a, b, c) {

                return _.ac(a, b, null == c ? c : _.Ia(c))

            };

            _.P = class {

                constructor(a, b, c)

                {

                    a:

                    {

                        null == a && (a = Oa);

                        Oa = void 0;

                        if (null == a) {

                            var d = 96;

                            c ? (a = [c], d |= 512) : a = [];

                            b && (d = d & -2095105 | (b & 1023) << 11)

                        } else {

                            if (!Array.isArray(a))

                                throw Error();

                            d = a[_.u] | 0;

                            if (d & 64) {

                                _.Zb && delete a[_.Zb];

                                break a

                            }

                            d |= 64;

                            if (c && (d |= 512, c !== a[0]))

                                throw Error();

                            b:

                            {

                                c = a;

                                var e = c.length;

                                if (e) {

                                    const g = e - 1;

                                    var f = c[g];

                                    if (Ea(f)) {

                                        d |= 256;

                                        b = +!!(d & 512) - 1;

                                        e = g - b;

                                        1024 <= e && (Qa(c, b, f), e = 1023);

                                        d = d & -2095105 | (e & 1023) << 11;

                                        break b

                                    }

                                }

                                b && (f = +!!(d & 512) - 1, b = Math.max(b, e - f), 1024 < b && (Qa(c, f, {}), d |= 256, b = 1023), d = d & -2095105 |

                                (b & 1023) << 11)

                            }

                        }

                        a[_.u] = d

                    }this.na = a

                }

                toJSON()

                {

                    if (Xb)

                        var a = db(this, this.na, !1);

                    else

                        a = Va(this.na, Xa, void 0, void 0, !1, !1),

                        a = db(this, a, !0);

                    return a

                }

                Ia()

                {

                    Xb = !0;

                    try {

                        return JSON.stringify(this.toJSON(), Sa)

                    } finally {

                        Xb = !1

                    }

                }

                Yb()

                {

                    return !!((this.na[_.u] | 0) & 2)

                }

            }

            ;

            _.P.prototype.qe = Ma;

            _.P.prototype.toString = function() {

                return db(this, this.na, !1).toString()

            };

            _.dc = Symbol();

            _.ec = Symbol();

            _.fc = Symbol();

            _.gc = Symbol();

            var hc = class  extends _.P{

                constructor()

                {

                    super()

                }

            }

            ;

            _.ic = class  extends _.P{

                constructor()

                {

                    super()

                }

                xd(a)

                {

                    return _.M(this, 3, a)

                }

            }

            ;

            var jc = class  extends _.P{

                constructor(a)

                {

                    super(a)

                }

            }

            ;

            var kc = class  extends _.P{

                constructor(a)

                {

                    super(a)

                }

                Rc(a)

                {

                    return _.N(this, 24, a)

                }

            }

            ;

            _.lc = class  extends _.P{

                constructor(a)

                {

                    super(a)

                }

            }

            ;

            _.mc = function() {

                this.Fa = this.Fa;

                this.ma = this.ma

            };

            _.mc.prototype.Fa = !1;

            _.mc.prototype.isDisposed = function() {

                return this.Fa

            };

            _.mc.prototype.oa = function() {

                this.Fa || (this.Fa = !0, this.N())

            };

            _.mc.prototype.N = function() {

                if (this.ma)

                    for (; this.ma.length;)

                        this.ma.shift()()

            };

            var nc = class  extends _.mc{

                constructor()

                {

                    var a = window;

                    super();

                    this.o = a;

                    this.i = [];

                    this.j = {}

                }

                resolve(a)

                {

                    var b = this.o;

                    a = a.split(".");

                    for (var c = a.length, d = 0; d < c; ++d)

                        if (b[a[d]])

                            b = b[a[d]];

                        else

                            return null;

                    return b instanceof Function ? b : null

                }

                Jc()

                {

                    for (var a = this.i.length, b = this.i, c = [], d = 0; d < a; ++d) {

                        var e = b[d].i(),

                            f = this.resolve(e);

                        if (f && f != this.j[e])

                            try {

                                b[d].Jc(f)

                            } catch (g) {}

                        else

                            c.push(b[d])

                    }

                    this.i = c.concat(b.slice(a))

                }

            }

            ;

            var pc = class  extends _.mc{

                constructor()

                {

                    var a = _.oc;

                    super();

                    this.o = a;

                    this.v = this.i = null;

                    this.s = 0;

                    this.B = {};

                    this.j = !1;

                    a = window.navigator.userAgent;

                    0 <= a.indexOf("MSIE") && 0 <= a.indexOf("Trident") && (a = /\b(?:MSIE|rv)[: ]([^\);]+)(\)|;)/.exec(a)) && a[1] && 9 > parseFloat(a[1]) && (this.j = !0)

                }

                A(a, b)

                {

                    this.i = b;

                    this.v = a;

                    b.preventDefault ? b.preventDefault() : b.returnValue = !1

                }

            }

            ;

            _.qc = class  extends _.P{

                constructor(a)

                {

                    super(a)

                }

            }

            ;

            var rc = class  extends _.P{

                constructor(a)

                {

                    super(a)

                }

            }

            ;

            var tc;

            _.sc = function(a, b) {

                if (a.i) {

                    const c = new hc;

                    _.N(c, 1, b.message);

                    _.N(c, 2, b.stack);

                    _.M(c, 3, b.lineNumber);

                    _.O(c, 5, 1);

                    b = new _.ic;

                    _.H(b, 40, c);

                    a.i.log(98, b)

                }

            };

            tc = class {

                constructor()

                {

                    this.i = null

                }

                log(a)

                {

                    _.sc(this, a)

                }

            }

            ;

            var wc,

                xc,

                Ac,

                Dc;

            _.uc = class {

                constructor(a)

                {

                    this.i = a

                }

                toString()

                {

                    return this.i.toString()

                }

            }

            ;

            _.uc.prototype.Bb = !0;

            _.uc.prototype.nb = function() {

                return this.i.toString()

            };

            _.vc = function(a) {

                return a instanceof _.uc && a.constructor === _.uc ? a.i : "type_error:SafeUrl"

            };

            wc = /^data:(.*);base64,[a-z0-9+\/]+=*$/i;

            xc = /^(?:(?:https?|mailto|ftp):|[^:/?#]*(?:[/?#]|$))/i;

            _.zc = function(a) {

                if (a instanceof _.uc)

                    return a;

                a = "object" == typeof a && a.Bb ? a.nb() : String(a);

                xc.test(a) ? a = _.yc(a) : (a = String(a).replace(/(%0A|%0D)/g, ""), a = a.match(wc) ? _.yc(a) : null);

                return a

            };

            try {

                new URL("s://g"),

                Ac = !0

            } catch (a) {

                Ac = !1

            }

            _.Cc = Ac;

            Dc = {};

            _.yc = function(a) {

                return new _.uc(a, Dc)

            };

            _.Ec = _.yc("about:invalid#zClosurez");

            var Fc,

                Ic,

                Hc;

            _.Gc = function(a) {

                let b;

                b = window.google && window.google.logUrl ? "" : "https://www.google.com";

                b += "/gen_204?use_corp=on&";

                b += a.Ia(2040 - b.length);

                Fc(_.zc(b) || _.Ec)

            };

            Fc = function(a) {

                var b = new Image,

                    c = Hc;

                b.onerror = b.onload = b.onabort = function() {

                    c in Ic && delete Ic[c]

                };

                Ic[Hc++] = b;

                b.src = _.vc(a)

            };

            Ic = [];

            Hc = 0;

            _.Jc = class {

                constructor()

                {

                    this.data = {}

                }

                Ia(a)

                {

                    var b = [],

                        c;

                    for (c in this.data)

                        b.push(encodeURIComponent(c) + "=" + encodeURIComponent(String(this.data[c])));

                    return ("atyp=i&zx=" + (new Date).getTime() + "&" + b.join("&")).substr(0, a)

                }

            }

            ;

            var Kc = class  extends _.Jc{

                constructor(a)

                {

                    super();

                    var b = _.G(a, jc, 8) || new jc;

                    window.google && window.google.kEI && (this.data.ei = window.google.kEI);

                    this.data.sei = _.x(_.I(a, 10));

                    this.data.ogf = _.x(_.I(b, 3));

                    this.data.ogrp = (window.google && window.google.sn ? !/.*hp$/.test(window.google.sn) : _.w(_.E(a, 7))) ? "1" : "";

                    this.data.ogv = _.x(_.I(b, 6)) + "." + _.x(_.I(b, 7));

                    this.data.ogd = _.x(_.I(a, 21));

                    this.data.ogc = _.x(_.I(a, 20));

                    this.data.ogl = _.x(_.I(a, 5));

                    this.data.oggv = "quantum:gapiBuildLabel"

                }

            }

            ;

            var fb = "constructor hasOwnProperty isPrototypeOf propertyIsEnumerable toLocaleString toString valueOf".split(" ");

            var Lc = [1, 2, 3, 4, 5, 6, 9, 10, 11, 13, 14, 28, 29, 30, 34, 35, 37, 38, 39, 40, 42, 43, 48, 49, 50, 51, 52, 53, 62, 500],

                Nc = function(a) {

                    if (!Mc) {

                        Mc = {};

                        for (var b = 0; b < Lc.length; b++)

                            Mc[Lc[b]] = !0

                    }

                    return !!Mc[a]

                },

                Oc = function(a) {

                    a = String(a);

                    return a.replace(".", "%2E").replace(",", "%2C")

                },

                Pc = class  extends Kc{

                    constructor(a, b, c, d, e)

                    {

                        super(a);

                        _.gb(this.data, {

                            oge: c,

                            ogex: _.x(_.I(a, 9)),

                            ogp: _.x(_.I(a, 6)),

                            ogsr: Math.round(1 / (Nc(c) ? _.eb(_.cc(b, 3, 1)) : _.eb(_.cc(b, 2, 1E-4)))),

                            ogus: d

                        });

                        if (e) {

                            "ogw" in e && (this.data.ogw = e.ogw, delete e.ogw);

                            "ved" in e &&

                            (this.data.ved = e.ved, delete e.ved);

                            a = [];

                            for (var f in e)

                                0 != a.length && a.push(","),

                                a.push(Oc(f)),

                                a.push("."),

                                a.push(Oc(e[f]));

                            e = a.join("");

                            "" != e && (this.data.ogad = e)

                        }

                    }

                }

                ,

                Mc = null;

            var Qc = class  extends _.P{

                constructor(a)

                {

                    super(a)

                }

            }

            ;

            var Uc = class {

                constructor()

                {

                    var a = Rc,

                        b = Sc,

                        c = Tc;

                    this.i = a;

                    this.s = b;

                    this.o = _.eb(_.cc(a, 2, 1E-4), 1E-4);

                    this.B = _.eb(_.cc(a, 3, 1), 1);

                    b = Math.random();

                    this.j = _.w(_.E(a, 1)) && b < this.o;

                    this.v = _.w(_.E(a, 1)) && b < this.B;

                    a = 0;

                    _.w(_.E(c, 1)) && (a |= 1);

                    _.w(_.E(c, 2)) && (a |= 2);

                    _.w(_.E(c, 3)) && (a |= 4);

                    this.A = a

                }

                log(a, b)

                {

                    try {

                        if (Nc(a) ? this.v : this.j) {

                            const c = new Pc(this.s, this.i, a, this.A, b);

                            _.Gc(c)

                        }

                    } catch (c) {}

                }

            }

            ;

            var Wc;

            _.Vc = function(a) {

                if (0 < a.j.length) {

                    var b = void 0 !== a.ua,

                        c = void 0 !== a.i;

                    if (b || c) {

                        b = b ? a.o : a.s;

                        c = a.j;

                        a.j = [];

                        try {

                            _.sb(c, b, a)

                        } catch (d) {

                            console.error(d)

                        }

                    }

                }

            };

            _.Xc = class {

                constructor(a)

                {

                    this.ua = a;

                    this.i = void 0;

                    this.j = []

                }

                then(a, b, c)

                {

                    this.j.push(new Wc(a, b, c));

                    _.Vc(this)

                }

                resolve(a)

                {

                    if (void 0 !== this.ua || void 0 !== this.i)

                        throw Error("x");

                    this.ua = a;

                    _.Vc(this)

                }

                o(a)

                {

                    a.j && a.j.call(a.i, this.ua)

                }

                s(a)

                {

                    a.o && a.o.call(a.i, this.i)

                }

            }

            ;

            Wc = class {

                constructor(a, b, c)

                {

                    this.j = a;

                    this.o = b;

                    this.i = c

                }

            }

            ;

            _.Yc = a => {

                var b = "zc";

                if (a.zc && a.hasOwnProperty(b))

                    return a.zc;

                b = new a;

                return a.zc = b

            };

            _.Q = class {

                constructor()

                {

                    this.s = new _.Xc;

                    this.i = new _.Xc;

                    this.C = new _.Xc;

                    this.B = new _.Xc;

                    this.A = new _.Xc;

                    this.v = new _.Xc;

                    this.o = new _.Xc;

                    this.j = new _.Xc;

                    this.G = new _.Xc

                }

                J()

                {

                    return this.s

                }

                L()

                {

                    return this.i

                }

                M()

                {

                    return this.C

                }

                K()

                {

                    return this.B

                }

                Fa()

                {

                    return this.A

                }

                ma()

                {

                    return this.v

                }

                H()

                {

                    return this.o

                }

                F()

                {

                    return this.j

                }

                static i()

                {

                    return _.Yc(_.Q)

                }

            }

            ;

            var cd;

            _.$c = function() {

                return _.G(_.Zc, kc, 1)

            };

            _.ad = function() {

                return _.G(_.Zc, _.lc, 5)

            };

            cd = class  extends _.P{

                constructor()

                {

                    super(bd)

                }

            }

            ;

            var bd;

            window.gbar_ && window.gbar_.CONFIG ? bd = window.gbar_.CONFIG[0] || {} : bd = [];

            _.Zc = new cd;

            var Sc,

                Tc,

                Rc;

            _.G(_.Zc, rc, 3) || new rc;

            _.$c() || new kc;

            _.oc = new tc;

            Sc = _.$c() || new kc;

            Tc = _.ad() || new _.lc;

            Rc = _.G(_.Zc, Qc, 4) || new Qc;

            new Uc;

            _.z("gbar_._DumpException", function(a) {

                _.oc ? _.oc.log(a) : console.error(a)

            });

            _.dd = new pc;

            var gd;

            _.hd = function(a, b) {

                var c = _.ed.i();

                if (a in c.i) {

                    if (c.i[a] != b)

                        throw new gd;

                } else {

                    c.i[a] = b;

                    if (b = c.j[a])

                        for (let d = 0, e = b.length; d < e; d++)

                            b[d].i(c.i, a);

                    delete c.j[a]

                }

            };

            _.ed = class {

                constructor()

                {

                    this.i = {};

                    this.j = {}

                }

                static i()

                {

                    return _.Yc(_.ed)

                }

            }

            ;

            _.id = class  extends _.aa{

                constructor()

                {

                    super()

                }

            }

            ;

            gd = class  extends _.id{}

            ;

            _.z("gbar.A", _.Xc);

            _.Xc.prototype.aa = _.Xc.prototype.then;

            _.z("gbar.B", _.Q);

            _.Q.prototype.ba = _.Q.prototype.L;

            _.Q.prototype.bb = _.Q.prototype.M;

            _.Q.prototype.bd = _.Q.prototype.Fa;

            _.Q.prototype.bf = _.Q.prototype.J;

            _.Q.prototype.bg = _.Q.prototype.K;

            _.Q.prototype.bh = _.Q.prototype.ma;

            _.Q.prototype.bj = _.Q.prototype.H;

            _.Q.prototype.bk = _.Q.prototype.F;

            _.z("gbar.a", _.Q.i());

            var jd = new nc;

            _.hd("api", jd);

            var kd = _.ad() || new _.lc;

            window.__PVT = _.x(_.I(kd, 8));

            _.hd("eq", _.dd);

        } catch (e) {

            _._DumpException(e)

        }

        try {

            _.ld = class  extends _.P{

                constructor(a)

                {

                    super(a)

                }

            }

            ;

        } catch (e) {

            _._DumpException(e)

        }

        try {

            var md = class  extends _.P{

                constructor()

                {

                    super()

                }

            }

            ;

            var nd = class  extends _.mc{

                constructor()

                {

                    super();

                    this.j = [];

                    this.i = []

                }

                o(a, b)

                {

                    this.j.push({

                        features: a,

                        options: b

                    })

                }

                init(a, b, c)

                {

                    window.gapi = {};

                    var d = window.___jsl = {};

                    d.h = _.x(_.I(a, 1));

                    null != _.E(a, 12) && (d.dpo = _.w(_.J(a, 12)));

                    d.ms = _.x(_.I(a, 2));

                    d.m = _.x(_.I(a, 3));

                    d.l = [];

                    _.K(b, 1) && (a = _.I(b, 3)) && this.i.push(a);

                    _.K(c, 1) && (c = _.I(c, 2)) && this.i.push(c);

                    _.z("gapi.load", (0, _.y)(this.o, this));

                    return this

                }

            }

            ;

            var od = _.G(_.Zc, _.qc, 14);

            if (od) {

                var pd = _.G(_.Zc, _.ld, 9) || new _.ld,

                    qd = new md,

                    rd = new nd;

                rd.init(od, pd, qd);

                _.hd("gs", rd)

            }

            ;

        } catch (e) {

            _._DumpException(e)

        }

    })(this.gbar_);

    // Google Inc.

    </script>

    <script nonce="4QoCa3wo6f+wopLQU0G2tA==">

    try {

        const preferences = JSON.parse(window.localStorage.getItem("datalab_prefs_dkastrinakis@gmail.com"));

        document.querySelector('html').setAttribute('theme', preferences['siteTheme'] || 'default');

    } catch (e) {}

    </script>

    <script nonce="4QoCa3wo6f+wopLQU0G2tA==">

    window.performance.mark('head_start');

    </script>

    <script src="https://ssl.gstatic.com/colaboratory-static/common/2c956b8f301c75a168674112b134257f/common%2Fwebcomponentsjs%2Fwebcomponents-lite.js" nonce="4QoCa3wo6f+wopLQU0G2tA=="></script>

    <script src="https://ssl.gstatic.com/colaboratory-static/common/2c956b8f301c75a168674112b134257f/common%2Fwebanimationsjs%2Fweb-animations-next-lite.min.js" nonce="4QoCa3wo6f+wopLQU0G2tA=="></script>

    <script nonce="4QoCa3wo6f+wopLQU0G2tA==">

    var colabVersionTag = 'colab_20230908-060130_RC00_563710671';

    var colabScsVersion = '2c956b8f301c75a168674112b134257f';

    var hl = 'en-GB';

    var colabExperiments = JSON.parse('\x7b\x22accessible_connect\x22: false, \x22aida_cell_button\x22: false, \x22aida_complete_code_model_id\x22: \x22\x22, \x22aida_do_conversation_model_id\x22: \x22\x22, \x22aida_generate_code_model_id\x22: \x22\x22, \x22aida_in_editor\x22: false, \x22aida_model_id\x22: \x22\x22, \x22allowed_public_url_domains\x22: \x5b\x22huggingface.co\x22, \x22dagshub.com\x22\x5d, \x22backend_version\x22: \x22next\x22, \x22bq_tid\x22: true, \x22cde\x22: true, \x22cell_tags\x22: false, \x22chat\x22: true, \x22classified_generate\x22: false, \x22classroom_iframe_parent_origin\x22: \x22\x22, \x22client_text_compose\x22: true, \x22client_trim_completion_text\x22: 100, \x22cloud_origin\x22: \x22\x22, \x22code_ai_in_signup\x22: true, \x22commands_in_toolbar\x22: false, \x22comment_poll_long\x22: 900000, \x22comment_poll_short\x22: 60000, \x22converse_temp\x22: \x220.7\x22, \x22crawler\x22: false, \x22data_integrations\x22: false, \x22data_source_tab\x22: false, \x22dbu\x22: \x22\x22, \x22debug_external\x22: \x22external\x22, \x22debug_prod\x22: \x22prod\x22, \x22development\x22: false, \x22document_change_poll_interval\x22: 30000, \x22drive_anon_api_key\x22: \x22AIzaSyB10s2vWUTwP0pj20wZoxmpZIt3rRodYeg\x22, \x22drive_api_key\x22: \x22AIzaSyCN_sSPJMpYrAzC5AtTrltNC8oRmLtoqBk\x22, \x22drive_background_save_project_number\x22: \x22948411933973\x22, \x22drive_realtime_project_number\x22: \x22\x22, \x22editor_focuses_cell\x22: true, \x22embedding_app\x22: \x22\x22, \x22enable_adhoc_backends\x22: false, \x22enterprise_url\x22: \x22https:\/\/cloud.google.com\/vertex-ai-notebooks\x22, \x22explain_cell\x22: false, \x22explain_error\x22: true, \x22external_trusted_github_org_repos_quick_add\x22: \x22GoogleChrome\/CrUX,google\/generative-ai-docs\x22, \x22first_party_auth\x22: true, \x22generate_code\x22: true, \x22generate_code_prompt\x22: true, \x22generate_df\x22: true, \x22generate_fix\x22: false, \x22generate_temp\x22: \x220.7\x22, \x22gis_auth\x22: true, \x22github_client_id\x22: \x225036cf6d81e65aaa6340\x22, \x22gpu_utilization_check_interval_ms\x22: 600000, \x22hats_surveys\x22: true, \x22hide_editing\x22: true, \x22hrc\x22: false, \x22internal_runtime_cleanup\x22: true, \x22internal_schedule\x22: false, \x22jsraw\x22: \x22compiled\x22, \x22key_promoter\x22: false, \x22local_cloud_apis\x22: false, \x22local_container\x22: true, \x22local_service_worker\x22: false, \x22log_hover_type\x22: false, \x22lsp\x22: true, \x22lsp_autofix\x22: false, \x22lsp_diagnostics_reporting\x22: false, \x22lsp_text_compose\x22: false, \x22lsrp\x22: 0, \x22ml_banner\x22: false, \x22ml_enabled\x22: false, \x22mlpp\x22: false, \x22mlpp_multiline\x22: false, \x22mlpp_on_by_default\x22: true, \x22mlpp_trim_completion_text\x22: 100, \x22mobile\x22: false, \x22no_fun\x22: false, \x22no_http_over_ws\x22: true, \x22open_dialog_redo\x22: false, \x22outage_notification\x22: \x22\x22, \x22outage_notification_link\x22: \x22\x22, \x22outputframe_version\x22: \x22\x22, \x22override_suf_params_for_test\x22: false, \x22promote_enterprise_on_signup\x22: true, \x22quickchart_button\x22: true, \x22recaptcha_polling_frequency_ms\x22: 300000, \x22recaptcha_v2_site_key\x22: \x226LfQttQUAAAAADuPanA_VZMaZgBAOnHZNuuqUewp\x22, \x22recaptcha_v3_site_key\x22: \x226LfQPtEUAAAAAHBpAdFng54jyuB1V5w5dofknpip\x22, \x22reconnect_max_delay_seconds\x22: 300, \x22require_ai_consent\x22: true, \x22resource_poll_interval_ms\x22: 10000, \x22rp_term\x22: false, \x22rt\x22: false, \x22runtime_env_overrides\x22: \x22\\n          \x5b\\n            \x5b\\\x22ENABLE_DIRECTORYPREFETCHER\\\x22, \\\x221\\\x22\x5d\\n          \x5d\\n        \x22, \x22runtime_type_for_test\x22: \x22\x22, \x22server_execution_queue\x22: true, \x22session_resume_coalesce\x22: true, \x22show_payments_interstitial\x22: false, \x22show_signup_survey\x22: true, \x22show_subscription_renewal_time\x22: false, \x22show_switch_to_prod_link\x22: false, \x22skip_header_button\x22: true, \x22sql_cell\x22: false, \x22sql_cell_buttons\x22: false, \x22suspicious_code_matches\x22: \x22\x22, \x22suspicious_code_regexs\x22: \x22\x22, \x22term4all\x22: false, \x22text_compose_report_changes_millis\x22: 10000, \x22uds\x22: false, \x22unified_compose\x22: false, \x22unmanaged_vm_min_label_block\x22: \x22\x22, \x22unmanaged_vm_min_label_warn\x22: \x22\x22, \x22unmanaged_vm_min_release_tag_block\x22: \x22\x22, \x22unmanaged_vm_min_release_tag_warn\x22: \x22\x22, \x22upload_redo\x22: false, \x22use_corplogin\x22: true, \x22use_dm_sql_lsp\x22: false, \x22uxr_survey\x22: false, \x22verbose_warnings\x22: false, \x22vertex_autopush\x22: false, \x22vertex_staging\x22: false, \x22workstations\x22: false, \x22ids\x22: \x5b20730150, 20730129, 20730159\x5d, \x22flag_ids\x22: \x7b\x22accessible_connect\x22: 45425577, \x22aida_cell_button\x22: 45425510, \x22aida_complete_code_model_id\x22: 45427660, \x22aida_do_conversation_model_id\x22: 45427664, \x22aida_generate_code_model_id\x22: 45427663, \x22aida_in_editor\x22: 45425507, \x22aida_model_id\x22: 45427463, \x22allowed_public_url_domains\x22: 45425558, \x22backend_version\x22: 45425541, \x22bq_tid\x22: 45425617, \x22cell_tags\x22: 45425779, \x22chat\x22: 45425490, \x22classified_generate\x22: 45425499, \x22classroom_iframe_parent_origin\x22: 45425537, \x22client_text_compose\x22: 45425512, \x22client_trim_completion_text\x22: 45425628, \x22cloud_origin\x22: 45425538, \x22code_ai_in_signup\x22: 45425576, \x22commands_in_toolbar\x22: 45425502, \x22comment_poll_long\x22: 45425588, \x22comment_poll_short\x22: 45425587, \x22converse_temp\x22: 45425509, \x22crawler\x22: 45425491, \x22data_integrations\x22: 45425611, \x22data_source_tab\x22: 45425619, \x22dbu\x22: 45425545, \x22debug_external\x22: 45425470, \x22debug_prod\x22: 45425471, \x22development\x22: 45425544, \x22document_change_poll_interval\x22: 45425589, \x22drive_anon_api_key\x22: 45425478, \x22drive_api_key\x22: 45425473, \x22drive_background_save_project_number\x22: 45425479, \x22drive_realtime_project_number\x22: 45425629, \x22editor_focuses_cell\x22: 45425573, \x22enable_adhoc_backends\x22: 45425506, \x22enterprise_url\x22: 45425574, \x22explain_cell\x22: 45425505, \x22explain_error\x22: 45425487, \x22external_trusted_github_org_repos_quick_add\x22: 45425555, \x22first_party_auth\x22: 45425560, \x22generate_code\x22: 45425492, \x22generate_code_prompt\x22: 45425488, \x22generate_df\x22: 45425503, \x22generate_fix\x22: 45425504, \x22generate_temp\x22: 45425508, \x22gis_auth\x22: 45425625, \x22github_client_id\x22: 45425556, \x22gpu_utilization_check_interval_ms\x22: 45425561, \x22hats_surveys\x22: 45425559, \x22internal_runtime_cleanup\x22: 45425579, \x22internal_schedule\x22: 45425578, \x22jsraw\x22: 45425557, \x22key_promoter\x22: 45425570, \x22local_cloud_apis\x22: 45425630, \x22local_service_worker\x22: 45425550, \x22log_hover_type\x22: 45425602, \x22lsp\x22: 45425605, \x22lsp_autofix\x22: 45425495, \x22lsp_diagnostics_reporting\x22: 45425604, \x22lsp_text_compose\x22: 45425494, \x22lsrp\x22: 45425612, \x22ml_banner\x22: 45425631, \x22ml_enabled\x22: 45425493, \x22mlpp\x22: 45425608, \x22mlpp_multiline\x22: 45425623, \x22mlpp_on_by_default\x22: 45425609, \x22mlpp_trim_completion_text\x22: 45425622, \x22mobile\x22: 45425562, \x22no_fun\x22: 45425540, \x22no_http_over_ws\x22: 45425827, \x22open_dialog_redo\x22: 45425572, \x22outage_notification\x22: 45425584, \x22outage_notification_link\x22: 45425585, \x22outputframe_version\x22: 45425591, \x22override_suf_params_for_test\x22: 45425592, \x22promote_enterprise_on_signup\x22: 45425575, \x22quickchart_button\x22: 45425501, \x22recaptcha_polling_frequency_ms\x22: 45425582, \x22recaptcha_v2_site_key\x22: 45425581, \x22recaptcha_v3_site_key\x22: 45425580, \x22reconnect_max_delay_seconds\x22: 45425539, \x22require_ai_consent\x22: 45425489, \x22resource_poll_interval_ms\x22: 45425590, \x22rp_term\x22: 45426219, \x22rt\x22: 45425624, \x22runtime_env_overrides\x22: 45425583, \x22runtime_type_for_test\x22: 45425586, \x22server_execution_queue\x22: 45425600, \x22session_resume_coalesce\x22: 45425603, \x22show_payments_interstitial\x22: 45425543, \x22show_signup_survey\x22: 45425620, \x22show_subscription_renewal_time\x22: 45425569, \x22show_switch_to_prod_link\x22: 45425483, \x22skip_header_button\x22: 45425607, \x22sql_cell\x22: 45425497, \x22sql_cell_buttons\x22: 45425498, \x22suspicious_code_matches\x22: 45425615, \x22suspicious_code_regexs\x22: 45425616, \x22term4all\x22: 45425542, \x22text_compose_report_changes_millis\x22: 45425568, \x22uds\x22: 45425601, \x22unified_compose\x22: 45425627, \x22unmanaged_vm_min_label_block\x22: 45425546, \x22unmanaged_vm_min_label_warn\x22: 45425547, \x22unmanaged_vm_min_release_tag_block\x22: 45425548, \x22unmanaged_vm_min_release_tag_warn\x22: 45425549, \x22upload_redo\x22: 45426279, \x22use_corplogin\x22: 45425606, \x22use_dm_sql_lsp\x22: 45425610, \x22uxr_survey\x22: 45425618, \x22verbose_warnings\x22: 45425551, \x22vertex_autopush\x22: 45425613, \x22vertex_staging\x22: 45425614, \x22workstations\x22: 45425626\x7d\x7d');

    var colabUserEmail = 'dkastrinakis@gmail.com';

    var colabRenderDataToken = 'AFWLbD0vPyo0o8eo0AYj868E11ljogIgDclbrRDeUE35b9FfWaoN994XiB3mQsVY666re7X2BFUYQJPQBtEYHl7VGHNhksLCMA3Z79qO';

    var colabConfig = '\x5b\x5b\x22dkastrinakis@gmail.com\x22,\x5b1,\x22AHXL0D0HgUZRHAjufTPCgh+oN8XTvUumqqkj0jFvdmOB0yl1yfZeNMcjk3K1gzBM339cgn65XtqLuNgq7WvVd\/DW6n5Tk8navNUnuTYhR+TnegCBSfAGIgybOSAVImrRpF9F1g9FdpNr4\/+pB9E207I6QZGmnoUXqjCxmrxxQGjEwB+JNu+Yo4h\/01fTpyWBP7t5u97tQ7HKUVDsnElTSC63iRuBle3t6UNdF1IFKOGDFetuqJMh7QIwcNJ54kexXuxU+x+yKMI\/8qAXTNWLXU0qe8G6q77H53LhnQGMQL7wKYwwDFDH9pqWHtogluIIw3ihrFKYWxQmEH+ifZCPUGXMwo\/srHzQryCCLEY+JznIDQ7ir+rZn0Ia7MZyJnNsm9osd\/SS23egnRQcwRsPIbdyj1n3FxsZxr0B+viOevpZt+HHMsHSAJT\/oiQBssTOspZ6sCq5\/4zdgCf0Ah0k92pOiukiv7\/r0jBy5zuaJMfg7NoBHptzBODSQG\/PFHAdAYOnwwQjoAL40pFVn3vQ7t\/YRvr8wB5zPvYz9R8GKNU6fxiewBizylNzFyhhD9KFwU\/i3UrsRuEoSHoh\/BpQJNDHjXZl5\/aThDZym3YdrBqXZkBNFQ3qhyHQp6VKHBKN8ooquwZCUIUqXrvpwYGxcy\/apxr6vtaPUUJYKJ1rfTtXELiAdSxqhKQujSFeTIKyHOcnpyhfE8T2fmvNrzZ3cIG\/sEY0xx2txF0DyLemTrQyaatWE\/okDStIJoY2ykEICxgzDvndhkjdZ0wkvo\/M3hRbLSP54faNGsRyAhHYhyaAtZNe2eP\/qJ4XWTpfkto+DWLhisAs6dgiYXueWYqSLEnO6ne3lOBqnXlgQy100KvAzQsMhzu+VdrECutMgAJlMTVgJndrRtb3jn0Ke01FEjYA\/zJGMe1RqPqhDbbQPsFfqMmnxAm\/9ssVt0N47u6h+VlbEZn3I71ERClMe2Jiv62D2mn\/WyaP7VhMjNRGpZW50n9DGMJT6EXT3W0q4r5SCkot\/6nLIqL15iDCMUnetUmx7ay3PDyfxzrJk2ZT0XxYouznT4e9w5i9LBFXh4L9QJWROFlpDp1YmJ22QL43Q6AqIeY6wkgA7p\/pkvGaanoQWgcSvkAlQ+o+JEB\/2Ml23Xp+RlK7CL73d\/9eA3DiDOGkdmslrwsWILoubWrGhWmSLJS4dfratJKcMRhmMJxORrcswe9GlkIII34YA3oEgTUY09qAZXsCPD39vnvTjtGMiycCTVoEzPvpJeG29tei6nXKsXBzRkzQz7gXA5jaolUAW+MykJv66Ek3z+op2hglxVOoR3jRZyJztbtxJUbWfFqASilwRctDspI\/2NzJaqw0hG36zuxYy+KuPJJHcnNDGzuGsL6XEs1wh3dgRP5LOmjZDOjyiO5f7Dwml8GOcasc9CnwlLFY\/TVDMj0bDmGmsgPprTLtTypLq+K2ssNE8mzcPiO\/0NXMgrhA6bybbJuS6K8x3s8Su6SKIsB2wL8n86qIOqfVg+r5XwHAe5nn3C4\/bhaIeCD3fuurVTkoQHPeBVQh8e2ww3gVxcaIYV16DA2fM6izEVHgOshM70yZj03L3roqBE9vbhCUL4p3c63AP1LVzmIa\/RpPZGZq0Yonxk8ynIRnh5tvZvaYgn3FXCxj5N1zd6FlhgLW+HkVMpA3pmGfXIbk9+XESS0qjedy1989vX2SvOVdx9ApOxEFwYbFowO6RSCBGrlrJR4vcfgHdURkUsSohojcpYmNf2DXMgfF3+u6vhruFLhrHvcJQUe3f6A9cgvQD95u53P2jWK2k5ny1TjWqSWS1z0PC26jcKuy9YDYrhx1n2YzlcsUbXZIJhJ2wGZVLL4zRukUXM74uDNBIBWj\/Q\x3d\x3d\x22,\x22AJ9oCCwshte0UK6wWVevTs8vA7tec\/ChhDXVTihaUwKeYSn1X0z30+oGJ5+go3VysTFSyBt59UbYuQ2IoLWrYdlUeUpYR8ThfIploZ8UA6AQDKVnMz0QH81hRkm5d3WQgfajTm5ifZBI\x22,\x22https:\/\/payments.google.com\/payments\x22,0,0,null,null,null,\x2211,47 €\x22,\x2252,39 €\x22,\x2211,47 €\x22,\x2252,39 €\x22\x5d,\x5b1\x5d,\x22GR\x22\x5d\x5d';

    </script>

    <link id='favicon-link' rel="shortcut icon" href="https://ssl.gstatic.com/colaboratory-static/common/2c956b8f301c75a168674112b134257f/img/favicon.ico"/>

    <link href="https://fonts.googleapis.com/css?family=Google+Sans:300,400,500,600,700|Roboto" rel="stylesheet">

    <link href="https://fonts.googleapis.com/css?family=Material+Icons&display=block" rel="stylesheet">

    <link rel="stylesheet" href="https://ssl.gstatic.com/colaboratory-static/common/2c956b8f301c75a168674112b134257f/v2/external/bundle.css"/>

    <meta name="google-site-verification" content="-wL8iYJTC7X0zF9qBNDQUAd-P1ZkQUK-OhSgv4Wkf1M"/>

    <meta name="google-site-verification" content="o-EECwEDQeUpZv0jTmoGfCDX7dUI8Kul4ESepXmDnO0"/>

    <meta name="google-site-verification" content="KD0T7LOCCaCHCECvO9oHcfvqtPmvpMnFU6vogWZ6FnQ"/>

    <meta name="google-site-verification" content="X_e11vbgvEHdHuaRpMld_RK9XHaPSwlBXKAWbIbJxxs"/>

    <meta name="google-site-verification" content="wdGthzzfu0IjM3qpFqTuQL9poAQZAvAaFKyuzetLpIM"/>

    <meta name="google-site-verification" content="qZJ77guHGO0TObHUBRYVdXQlIhXBBuz8dahJVmIlzCo"/>

    <meta name="google-site-verification" content="7ahoeOOKT2ZR781GZ5xK4L9t7yO1ZOHc-gaoUALEYgw"/>

    <meta name="google-site-verification" content="PHgaSKwdxZELS21aixtLhfpvaHtKen9pnVJ25EI35Zs"/>

    <meta name="google-site-verification" content="Ozey1ptWUQW13_lCEhpPMOcmRBLqdyB3WEL-TJUjskU"/>

    <meta name="google-site-verification" content="8P-D5fVWgUIhw8X2BxnKJbf5itK0zxX0QhoBjbJFTe8"/>

    <meta name="google-site-verification" content="88fgsZDoVRBuRnDPMIEjcHCxsEXzODOqEsJoqtvQsDc"/>

    <meta name="google-site-verification" content="DGionF7db9g0dOgeBXwOAN2tmCzWBdo5yOdc_-5UcuE"/>

    <meta name="google-site-verification" content="Q9LlidR0toR7UtSyVO23xNeaqJmRp8I6r4ghBQTtntU"/>

    <meta name="google-site-verification" content="rQawcZaTEK_UrDG30cz_7nVKOVvBass61QEes0Tm04g"/>

    <meta name="google-site-verification" content="U4VwCDRqo7_kUrEYldjQQWPZbA1j2lL709QZ8IAOhyQ"/>

    <meta name="google-site-verification" content="Osw7QcOK045GmOYJI2MM2_7AaL-s4q6pdn8gIv6JNxA"/>

    <meta name="google-site-verification" content="KiunYPvrY5x8umvAWcjhwPrB677xCar2LeT_8yaVrDg"/>

    <meta property="og:type" content="article"/>

    <meta property="og:image" content="https://colab.research.google.com/img/colab_favicon_256px.png"/>

    <meta property="og:title" content="Google Colaboratory"/>

    <script nonce="4QoCa3wo6f+wopLQU0G2tA==">

    window.performance.mark('head_end');

    window.performance.measure('head', 'head_start', 'head_end');

    </script>

</head>

<body class="">

    <div class="onegoogle">

        <div class="gb_Ka gb_f gb_bb" id="gb">

            <div class="gb_vd gb_9a gb_kd" ng-non-bindable="" data-ogsr-up="" style="padding:0;height:auto;display:block">

                <div class="gb_Pd" style="display:block">

                    <div class="gb_1c"></div>

                    <div class="gb_b gb_Kd gb_Wf gb_D">

                        <div class="gb_g gb_8a gb_Wf gb_D">

                            <a class="gb_d gb_Aa gb_D" aria-label="Google Account: Dimitris Kastrinakis  &#10;(dkastrinakis@gmail.com)" href="https://accounts.google.com/SignOutOptions?hl=en-GB&amp;continue=https://colab.research.google.com/drive/1PThCmmKaBpYL00ELUku1mk4dIpFOcQ1e&amp;ec=GBRAqQM" role="button" tabindex="0">

                                <img class="gb_n gbii" src="https://lh3.googleusercontent.com/ogw/AGvuzYa8RcnYAbxn8PwOIVaoeRnXL2FstCzxa6mrSpsA=s32-c-mo" srcset="https://lh3.googleusercontent.com/ogw/AGvuzYa8RcnYAbxn8PwOIVaoeRnXL2FstCzxa6mrSpsA=s32-c-mo 1x, https://lh3.googleusercontent.com/ogw/AGvuzYa8RcnYAbxn8PwOIVaoeRnXL2FstCzxa6mrSpsA=s64-c-mo 2x " alt="" aria-hidden="true" data-noaft="">

                            </a>

                        </div>

                    </div>

                </div>

            </div>

        </div>

        <script nonce="4QoCa3wo6f+wopLQU0G2tA==">

        this.gbar_ = this.gbar_ || {};

        (function(_) {

            var window = this;

            try {

                _.sd = function(a, b, c) {

                    if (!a.j)

                        if (c instanceof Array)

                            for (var d of c)

                                _.sd(a, b, d);

                        else {

                            d = (0, _.y)(a.A, a, b);

                            const e = a.s + c;

                            a.s++;

                            b.dataset.eqid = e;

                            a.B[e] = d;

                            b && b.addEventListener ? b.addEventListener(c, d, !1) : b && b.attachEvent ? b.attachEvent("on" + c, d) : a.o.log(Error("u`" + b))

                        }

                };

            } catch (e) {

                _._DumpException(e)

            }

            try {

                _.td = function() {

                    if (!_.p.addEventListener || !Object.defineProperty)

                        return !1;

                    var a = !1,

                        b = Object.defineProperty({}, "passive", {

                            get: function() {

                                a = !0

                            }

                        });

                    try {

                        const c = () => {};

                        _.p.addEventListener("test", c, b);

                        _.p.removeEventListener("test", c, b)

                    } catch (c) {}

                    return a

                }();

            } catch (e) {

                _._DumpException(e)

            }

            try {

                var ud = document.querySelector(".gb_l .gb_d"),

                    vd = document.querySelector("#gb.gb_Rc");

                ud && !vd && _.sd(_.dd, ud, "click");

            } catch (e) {

                _._DumpException(e)

            }

            try {

                _.kh = function(a) {

                    const b = [];

                    let c = 0;

                    for (const d in a)

                        b[c++] = a[d];

                    return b

                };

                _.lh = function(a) {

                    if (a.o)

                        return a.o;

                    for (const b in a.i)

                        if (a.i[b].qa() && a.i[b].B())

                            return a.i[b];

                    return null

                };

                _.mh = function(a, b) {

                    a.i[b.J()] = b

                };

                var nh = new class  extends _.mc{

                    constructor()

                    {

                        var a = _.oc;

                        super();

                        this.B = a;

                        this.o = null;

                        this.j = {};

                        this.A = {};

                        this.i = {};

                        this.s = null

                    }

                    v(a)

                    {

                        this.i[a] && (_.lh(this) && _.lh(this).J() == a || this.i[a].O(!0))

                    }

                    Wa(a)

                    {

                        this.s = a;

                        for (const b in this.i)

                            this.i[b].qa() && this.i[b].Wa(a)

                    }

                    wc(a)

                    {

                        return a in this.i ? this.i[a] : null

                    }

                }

                ;

                _.hd("dd", nh);

            } catch (e) {

                _._DumpException(e)

            }

            try {

                _.Vi = function(a, b) {

                    return _.L(a, 36, b)

                };

            } catch (e) {

                _._DumpException(e)

            }

            try {

                var Wi = document.querySelector(".gb_b .gb_d"),

                    Xi = document.querySelector("#gb.gb_Rc");

                Wi && !Xi && _.sd(_.dd, Wi, "click");

            } catch (e) {

                _._DumpException(e)

            }

        })(this.gbar_);

        // Google Inc.

        </script>

    </div>

    <div class="scripts">

        <script nonce="4QoCa3wo6f+wopLQU0G2tA==">

        window.performance.mark('external_scripts_start');

        </script>

        <script src="https://ssl.gstatic.com/colaboratory-static/common/2c956b8f301c75a168674112b134257f/gapi_loader.js" nonce="4QoCa3wo6f+wopLQU0G2tA=="></script>

        <script src="https://ssl.gstatic.com/colaboratory-static/common/2c956b8f301c75a168674112b134257f/socketio_binary.js" nonce="4QoCa3wo6f+wopLQU0G2tA=="></script>

        <script src="https://ssl.gstatic.com/colaboratory-static/common/2c956b8f301c75a168674112b134257f/analytics_binary.js" nonce="4QoCa3wo6f+wopLQU0G2tA=="></script>

        <script src="/static/mathjax/MathJax.js?config=TeX-AMS_HTML-full,Safe&delayStartupUntil=configured" nonce="4QoCa3wo6f+wopLQU0G2tA=="></script>

        <script src="https://ssl.gstatic.com/colaboratory-static/common/2c956b8f301c75a168674112b134257f/js%2Fmonaco_editor%2Fvs%2Floader.js" nonce="4QoCa3wo6f+wopLQU0G2tA=="></script>

        <script nonce="4QoCa3wo6f+wopLQU0G2tA==">

        window.performance.mark('external_scripts_end');

        window.performance.measure('external_scripts', 'external_scripts_start', 'external_scripts_end');

        window.performance.mark('colab_load_start');

        window.Polymer = {

            'legacyOptimizations': true,

        };

        </script>

        <script src="https://ssl.gstatic.com/colaboratory-static/common/2c956b8f301c75a168674112b134257f/external_polymer_binary_l10n__en_gb.js" nonce="4QoCa3wo6f+wopLQU0G2tA=="></script>

        <script nonce="4QoCa3wo6f+wopLQU0G2tA==">

        window.performance.mark('colab_load_end');

        window.performance.measure('colab_load', 'colab_load_start', 'colab_load_end');

        </script>

    </div>

    <div ng-non-bindable="">

        <div class="gb_q">

            <div class="gb_zc">

                <div>Google Account</div>

                <div class="gb_zb">Dimitris Kastrinakis</div>

                <div>dkastrinakis@gmail.com</div>

            </div>

        </div>

    </div>

    <script nonce="4QoCa3wo6f+wopLQU0G2tA==">

    this.gbar_ = this.gbar_ || {};

    (function(_) {

        var window = this;

        try {

            var xd,

                Ad;

            _.wd = function(a) {

                const b = a.length;

                if (0 < b) {

                    const c = Array(b);

                    for (let d = 0; d < b; d++)

                        c[d] = a[d];

                    return c

                }

                return []

            };

            xd = function(a) {

                return a

            };

            _.yd = function(a) {

                var b = null,

                    c = _.p.trustedTypes;

                if (!c || !c.createPolicy)

                    return b;

                try {

                    b = c.createPolicy(a, {

                        createHTML: xd,

                        createScript: xd,

                        createScriptURL: xd

                    })

                } catch (d) {

                    _.p.console && _.p.console.error(d.message)

                }

                return b

            };

            _.zd = function(a, b) {

                return 0 == a.lastIndexOf(b, 0)

            };

            _.Bd = function() {

                void 0 === Ad && (Ad = _.yd("ogb-qtm#html"));

                return Ad

            };

            try {

                (new self.OffscreenCanvas(0, 0)).getContext("2d")

            } catch (a) {}

            ;

            _.Cd = {};

            _.Dd = class {

                constructor(a)

                {

                    this.i = a;

                    this.Bb = !0

                }

                nb()

                {

                    return this.i

                }

                toString()

                {

                    return this.i.toString()

                }

            }

            ;

            _.Ed = new _.Dd("", _.Cd);

            _.Fd = RegExp("^[-+,.\"'%_!#/ a-zA-Z0-9\\[\\]]+$");

            _.Gd = RegExp("\\b(url\\([ \t\n]*)('[ -&(-\\[\\]-~]*'|\"[ !#-\\[\\]-~]*\"|[!#-&*-\\[\\]-~]*)([ \t\n]*\\))", "g");

            _.Hd = RegExp("\\b(calc|cubic-bezier|fit-content|hsl|hsla|linear-gradient|matrix|minmax|radial-gradient|repeat|rgb|rgba|(rotate|scale|translate)(X|Y|Z|3d)?|steps|var)\\([-+*/0-9a-zA-Z.%#\\[\\], ]+\\)", "g");

            var Id;

            Id = {};

            _.Kd = function(a) {

                return a instanceof _.Jd && a.constructor === _.Jd ? a.i : "type_error:SafeHtml"

            };

            _.Ld = function(a) {

                const b = _.Bd();

                a = b ? b.createHTML(a) : a;

                return new _.Jd(a, Id)

            };

            _.Jd = class {

                constructor(a)

                {

                    this.i = a;

                    this.Bb = !0

                }

                nb()

                {

                    return this.i.toString()

                }

                toString()

                {

                    return this.i.toString()

                }

            }

            ;

            _.Md = new _.Jd(_.p.trustedTypes && _.p.trustedTypes.emptyHTML || "", Id);

            _.Nd = _.Ld("<br>");

            var Pd;

            _.Od = function(a) {

                let b = !1,

                    c;

                return function() {

                    b || (c = a(), b = !0);

                    return c

                }

            }(function() {

                var a = document.createElement("div"),

                    b = document.createElement("div");

                b.appendChild(document.createElement("div"));

                a.appendChild(b);

                b = a.firstChild.firstChild;

                a.innerHTML = _.Kd(_.Md);

                return !b.parentElement

            });

            Pd = /^[\w+/_-]+[=]{0,2}$/;

            _.Qd = function(a) {

                a = (a || _.p).document;

                return a.querySelector ? (a = a.querySelector('style[nonce],link[rel="stylesheet"][nonce]')) && (a = a.nonce || a.getAttribute("nonce")) && Pd.test(a) ? a : "" : ""

            };

            _.Rd = function(a, b) {

                this.width = a;

                this.height = b

            };

            _.l = _.Rd.prototype;

            _.l.aspectRatio = function() {

                return this.width / this.height

            };

            _.l.Hb = function() {

                return !(this.width * this.height)

            };

            _.l.ceil = function() {

                this.width = Math.ceil(this.width);

                this.height = Math.ceil(this.height);

                return this

            };

            _.l.floor = function() {

                this.width = Math.floor(this.width);

                this.height = Math.floor(this.height);

                return this

            };

            _.l.round = function() {

                this.width = Math.round(this.width);

                this.height = Math.round(this.height);

                return this

            };

            _.R = function(a, b) {

                var c = b || document;

                if (c.getElementsByClassName)

                    a = c.getElementsByClassName(a)[0];

                else {

                    c = document;

                    var d = b || c;

                    a = d.querySelectorAll && d.querySelector && a ? d.querySelector(a ? "." + a : "") : _.Sd(c, a, b)[0] || null

                }

                return a || null

            };

            _.Sd = function(a, b, c) {

                var d;

                a = c || a;

                if (a.querySelectorAll && a.querySelector && b)

                    return a.querySelectorAll(b ? "." + b : "");

                if (b && a.getElementsByClassName) {

                    var e = a.getElementsByClassName(b);

                    return e

                }

                e = a.getElementsByTagName("*");

                if (b) {

                    var f = {};

                    for (c = d = 0; a = e[c]; c++) {

                        var g = a.className;

                        "function" == typeof g.split && _.va(g.split(/\s+/), b) && (f[d++] = a)

                    }

                    f.length = d;

                    return f

                }

                return e

            };

            _.Ud = function(a) {

                return _.Td(document, a)

            };

            _.Td = function(a, b) {

                b = String(b);

                "application/xhtml+xml" === a.contentType && (b = b.toLowerCase());

                return a.createElement(b)

            };

            _.Vd = function(a) {

                for (var b; b = a.firstChild;)

                    a.removeChild(b)

            };

            _.Wd = function(a) {

                return 9 == a.nodeType ? a : a.ownerDocument || a.document

            };

        } catch (e) {

            _._DumpException(e)

        }

        try {

            var qe,

                se;

            _.le = function(a) {

                if (null == a)

                    return a;

                if ("string" === typeof a) {

                    if (!a)

                        return;

                    a = +a

                }

                if ("number" === typeof a)

                    return a

            };

            _.me = function(a, b) {

                var c = Array.prototype.slice.call(arguments, 1);

                return function() {

                    var d = c.slice();

                    d.push.apply(d, arguments);

                    return a.apply(this, d)

                }

            };

            _.ne = function(a, b) {

                return _.le(_.C(a, b))

            };

            _.oe = function(a, b) {

                if (void 0 !== a.ua || void 0 !== a.i)

                    throw Error("x");

                a.i = b;

                _.Vc(a)

            };

            _.pe = class  extends _.P{

                constructor(a)

                {

                    super(a)

                }

            }

            ;

            qe = class  extends _.id{}

            ;

            _.re = function(a, b) {

                if (b in a.i)

                    return a.i[b];

                throw new qe;

            };

            se = 0;

            _.te = function(a) {

                return Object.prototype.hasOwnProperty.call(a, _.lb) && a[_.lb] || (a[_.lb] = ++se)

            };

            _.ue = function(a) {

                if (a instanceof _.uc)

                    return a;

                a = "object" == typeof a && a.Bb ? a.nb() : String(a);

                a:

                {

                    var b = a;

                    if (_.Cc) {

                        try {

                            var c = new URL(b)

                        } catch (d) {

                            b = "https:";

                            break a

                        }

                        b = c.protocol

                    } else

                        b:

                        {

                            c = document.createElement("a");

                            try {

                                c.href = b

                            } catch (d) {

                                b = void 0;

                                break b

                            }

                            b = c.protocol;

                            b = ":" === b || "" === b ? "https:" : b

                        }

                }"javascript:" === b && (a = "about:invalid#zClosurez");

                return _.yc(a)

            };

            _.ve = function(a) {

                return _.re(_.ed.i(), a)

            };

        } catch (e) {

            _._DumpException(e)

        }

        try {

            var aj;

            aj = {};

            _.bj = class {

                constructor(a)

                {

                    this.i = a

                }

                toString()

                {

                    return this.i + ""

                }

            }

            ;

            _.bj.prototype.Bb = !0;

            _.bj.prototype.nb = function() {

                return this.i.toString()

            };

            _.dj = function(a) {

                return _.cj(a).toString()

            };

            _.cj = function(a) {

                return a instanceof _.bj && a.constructor === _.bj ? a.i : "type_error:TrustedResourceUrl"

            };

            _.ej = function(a) {

                const b = _.Bd();

                a = b ? b.createScriptURL(a) : a;

                return new _.bj(a, aj)

            }; /*



             SPDX-License-Identifier: Apache-2.0

            */







            var fj;

            try {

                new URL("s://g"),

                fj = !0

            } catch (a) {

                fj = !1

            }

            _.gj = fj;

        } catch (e) {

            _._DumpException(e)

        }

        try {

            _.hj = class  extends _.P{

                constructor(a)

                {

                    super(a)

                }

            }

            ;

        } catch (e) {

            _._DumpException(e)

        }

        try {

            _.ij = function(a, b, c) {

                a.rel = c;

                -1 != c.toLowerCase().indexOf("stylesheet") ? (a.href = _.dj(b), (b = _.Qd(a.ownerDocument && a.ownerDocument.defaultView)) && a.setAttribute("nonce", b)) : a.href = b instanceof _.bj ? _.dj(b) : b instanceof _.uc ? _.vc(b) : _.vc(_.ue(b))

            };

        } catch (e) {

            _._DumpException(e)

        }

        try {

            _.jj = function(a) {

                var b;

                let c;

                const d = null == (c = (b = (a.ownerDocument && a.ownerDocument.defaultView || window).document).querySelector) ? void 0 : c.call(b, "script[nonce]");

                (b = d ? d.nonce || d.getAttribute("nonce") || "" : "") && a.setAttribute("nonce", b)

            };

            _.kj = function(a, b) {

                return (b || document).getElementsByTagName(String(a))

            };

        } catch (e) {

            _._DumpException(e)

        }

        try {

            var mj = function(a, b, c) {

                    a < b ? lj(a + 1, b) : _.oc.log(Error("X`" + a + "`" + b), {

                        url: c

                    })

                },

                lj = function(a, b) {

                    if (nj) {

                        const c = _.Ud("SCRIPT");

                        c.async = !0;

                        c.type = "text/javascript";

                        c.charset = "UTF-8";

                        c.src = _.cj(nj);

                        _.jj(c);

                        c.onerror = _.me(mj, a, b, c.src);

                        _.kj("HEAD")[0].appendChild(c)

                    }

                },

                oj = class  extends _.P{

                    constructor(a)

                    {

                        super(a)

                    }

                }

                ;

            var pj = _.G(_.Zc, oj, 17) || new oj,

                qj,

                nj = (qj = _.G(pj, _.hj, 1)) ? _.ej(_.I(qj, 4) || "") : null,

                rj,

                sj = (rj = _.G(pj, _.hj, 2)) ? _.ej(_.I(rj, 4) || "") : null,

                tj = function() {

                    lj(1, 2);

                    if (sj) {

                        const a = _.Ud("LINK");

                        a.setAttribute("type", "text/css");

                        _.ij(a, sj, "stylesheet");

                        let b = _.Qd();

                        b && a.setAttribute("nonce", b);

                        _.kj("HEAD")[0].appendChild(a)

                    }

                };

            (function() {

                const a = _.$c();

                if (_.E(a, 18))

                    tj();

                else {

                    const b = _.ne(a, 19) || 0;

                    window.addEventListener("load", () => {

                        window.setTimeout(tj, b)

                    })

                }

            })();

        } catch (e) {

            _._DumpException(e)

        }

    })(this.gbar_);

    // Google Inc.

    </script>

</body>

</html>
