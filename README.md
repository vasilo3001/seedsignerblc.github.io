# seedsignerblc.github.io
SeedSigner Workshop Bitcoin ChiangMai
---
marp: true
theme: gaia
paginate: true
header: "SeedSigner Workshop 101"
footer: ""
style: |
  /* Force light theme colors, ignore browser dark mode */
  section {
    --color-background: #fff8e1 !important;
    --color-background-stripe: rgba(69,90,100,.1) !important;
    --color-foreground: #455a64 !important;
    --color-dimmed: #6a7a7d !important;
    --color-highlight: #0288d1 !important;
    font-size: 28px;
  }
  h1 {
    color: #f7931a;
    font-size: 2.2em;
  }
  h2 {
    color: #f7931a;
    font-size: 1.8em;
  }
  h3 {
    color: #e8820e;
  }
  .danger {
    color: #e74c3c;
    font-weight: bold;
  }
  .success {
    color: #27ae60;
    font-weight: bold;
  }
  .warning {
    color: #e67e22;
    font-weight: bold;
  }
  .highlight {
    background: #fff3cd;
    padding: 4px 8px;
    border-radius: 4px;
  }
  .two-col {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 20px;
  }
  table {
    font-size: 0.7em;
    width: 100%;
    border-collapse: collapse;
  }
  th {
    background: #f7931a;
    color: white;
    padding: 6px 4px;
  }
  td {
    padding: 5px 4px;
    border-bottom: 1px solid #ddd;
  }
  tr:nth-child(even) {
    background: #f8f9fa;
  }
  tr.closerow td {
    color: #e74c3c;
    font-weight: bold;
  }
  tr.openrow td {
    color: #27ae60;
    font-weight: bold;
  }
  .emoji {
    font-size: 1.4em;
  }
  blockquote {
    background: #f8f9fa;
    border-left: 4px solid #f7931a;
    padding: 10px 16px;
    margin: 10px 0;
  }
---

<div style="text-align: center; margin-bottom: 10px;">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAABDgAAAF9CAYAAADhvdj3AAAACXBIWXMAAAsTAAALEwEAmpwYAAAAtGVYSWZJSSoACAAAAAYAEgEDAAEAAAABAAAAGgEFAAEAAABWAAAAGwEFAAEAAABeAAAAKAEDAAEAAAACAAAAEwIDAAEAAAABAAAAaYcEAAEAAABmAAAAAAAAAEgAAAABAAAASAAAAAEAAAAGAACQBwAEAAAAMDIxMAGRBwAEAAAAAQIDAACgBwAEAAAAMDEwMAGgAwABAAAA//8AAAKgBAABAAAAOAQAAAOgBAABAAAAfQEAAAAAAABt30mJAAAgAElEQVR4nOzdTWycV37v+d8JOpguAo2uouYmPSVgXOwSkACi4SJAamYWtMiF5dyNSa6krFQEZnGdjcT2Xdx0d0ATM/YkizapTesCMwBLQIJIwASiBEw6lnFDygRuT0wCpGEK42DEkB1ARKfniqxOY1i5uAOcWRw+fJEpiVX1nOf1+wEKsrrtp069P+f3/M//SAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAClj4h4AEDe7vyftrLu/7G5Le9tH/+fm4ziGBAAAALSvUJTKbx39vTri/ixVZM71xTIkIErfinsAgG+HAUYQXuz94uif37oqSTbO8QEAAAC+2Q9kXABSk3orUukN98+FosyF0biHB4SCgAOZYp8uHoQZv3B/Vi9LrwowFv/M3QAAAIAs2Fg49peZ4//PS8+J7Qcyh8FH+S1X+VGuyfSUPA0S8IOAA6l1GGZsPnZ/fv+UMGP5lvRo5tT/HgAAAMiVVlPaXJI2v/H/nBp+2I8qLvioXnaBB5UeSDgCDqSC3d87+DI+CDNKb0gvfhGv3nE3AAAAAO3ZWXe3jQUdVn70Vk6cb9sPZFQdcYFHdYTAA4lDwIHEsl/dd4EGYQYAAAAQvd1tdzta9nIy8Phx0QUeF8dc4EEjU8SMgAOJYZ9vSU8WXKjxrf9KCr5AV+9ID6diHRsAAAAAHVRVL0makQrFk4HHT2pG/WNS/7jM+YFYhod8I+BArOyzNWnljvSd35WOJ8Lr99wNAAAAQDK1mq66I6jwKNcOz+ftRxWji+PS0HXCDkSGgAOROww1fvtYlcb6Pemv/zjWcQEAAADoQtDH49HMif4d9qOK0fAN6eI4y1jgFQEHImGfb7kdTV4MNf6WLVoBAACAzNndlpbn3O142PHTEaPB6zKXJmMcHLLKxD0AZJfd33Plar/5pVS7ZrV8y/XY2N2Oe2gAAAAA4lAdkQavSw+njPrHpXemqepAaKjgQOjs00UXarD8BAAAAMBxQZPSYw1KqepAWKjgQCgOqzV+9bX0+39gtXrH/b3VjHtoAAAAAJIsqOr4bMb16hisy/SU4h4VUogKDnTFPt9yjYSCao2//1RapK8GAAAAgDMKqjqO9+r4dNposM7yFbSFCg50xD5ddL00qiOut8Zqg2oNAAAAAN0rFBVUcuizGUOfDpzVb8U9AKSLfboo++m0JFn9w2Orj/tcZ2TCDQAAAABhaDXdVrMf90muUtzau3VXPQ68AgEHzuREsLH52Or2qLTSiHlUAAAAADJtpUHQgTMj4MArnRpsbC7FPCoAAAAAufJi0PHptNvoADiGgAOnItgAAAAAkDgrDWl2QAqCjs9n4x0PEoWAAyfY51sEGwAAAACS64UeHfajitsEAblHwAFJkt3fk/1iXiLYAAAAAJAGrab0YEoKqjl+OkJ/jpwj4IDs//Uz6fiuKAQbAAAAANJid1u6PSod68+BfDJxDwDxsU8X3Rav5ZrV8i22egUAAACQflempdU7RlfnZS6Mxj0aRIgKjhyyz7dk/8P/IklWO19aPZoh3AAAAACQDY9mpKCaY+Emu63kyLfiHgCidbgc5R//TvrrP457OPHrrUililQoSuW33P9Wrrm/S1KpInOuj0onAF07aH5mD0poAQCAT8GyleGbVpLsV/eNeXMi5kHBNyZuOWGfrUmfz0nna/mr2CgUXWhRrkm9b7g/CS4ARIyAAwCAmBSK0tV56ckDo/dmZXpKcY8InlDBkQN27S8ltxxFWr0T93D8Ktek8zVXjXEQapiekpGW5G4AAAAAcqXVlBoT0lDdVXM8XTT05sgmrmBnmH22Jv3tn0q/8/v2YB1a9lRHpOpl9+dhmAEAyUMFBwAACdBbcdUcGw+MGZ+LezQIGZPBjLJrf+mCjbuT0s563MMJz7FAw1wY5f0LIDUIOAAASJDhm9LmklH9vsy5vrhHg5CwRCVj7PMt6a//nfSrr63+/A/jHk73eisu1Lg45kKNw+UmGa1IAQAAAODf8pxUrtGANGO4Ap4h9v9elHorVo2JdFdtlGsu1Bi6LnN+gPcogEygggMAgAQKGpBuPmbJSgYwecwAu78nLd+SSm9YPZxK5w4pvRVp8Lo0WGd3EwCZRMABAECCsWQlE34r7gGgO3Z3S5Ks9rat7k2mK9woFN0XyQ/WZH60bcy7M4ZwAwAAAEDkluckyUqyBxclkEJMJlPMfv0z6TvfS18j0f5xafC6zJsTvP8A5AYVHAAApEChKNXvS7vbxlyajHs0aBMVHCll/8OfSv/8S3einIZwo7ciXZmWfrglM7lgCDcAAAAAJE6rqYOLEdbercc8GLSLSWbK2P096a/ed5UbyyloglMdcdUalyZ5rwHINSo4AABImaG6tLvt+nL0lOIeDc6AbWJT5LDfxm9+Ka3fjXs4rzZUd8HGhdGDbV0BAAAAIEVWGlJ1xG0l+3zL0Hw0+ViikhL26aLUalrNDkibS3EP5+WG6m4ZyrWGceEGAAAAAKTU5tLRkpVnazEPBq9DwJECdu0vXbhxe1Ta3Y57OKc7HmywEwoAAACArNhZl2YHJHZYSTwCjoSzn34o/Zd/sWpMJHMLWIINAAAAAFl3vPnoF/NxjwYvQcCRUHZ/T/ZuXdrbtrqXwO2JCDYAAAAA5AkhR+IRcCSQ3d+TJCvJaqUR72BeVB2RfrBGsAEAAAAgn9wFaEKOBCLgSJjDcOP2qBIVbvRWpPcXZf5oyZjzAwQbAAAAAPIrCDk+nY57JDiGgCNBToQbO+txD8cpFKUr0zI/2mZXFAAAAAAIBCHH3XrMA0GAgCMh7O6WlLRwo39cmlqTeXeGYAMAAAAAXvRoRiLkSAwCjgSwz9bcNrAf9yUj3AiWo0wu0GcDAAAAAF7FtRawduFmzAMBAUfM7LM1KajcSMI2sMM3XdUGy1EAAAAA4GyCkIPGo7Ei4IhRosKNoGpjfM6YnhLhBgAAAAC0Y3lOIuSIFQFHTBIVblC1AQAAAADdYwvZWBFwxOBEQ9E4ww2qNgAAAAAgXEHI8dX9uEeSOwQcEbP7e9K3i/GHG8EOKVRtAAAAAEC4gpDDVe4jIgQcEbL7e1ISKjfGZt0OKVRtAAAAAIAfhByRI+CIyIlwI66tYHsr0g/WZN6eItgAAAAAAJ9aTen2qCTZg/kgPCPgiMpf/KFiDTeCJSnnBwg3AAAAACAKraZ011VyxD2UPCDgiID93/+N9J3v2djCjSvTLEkBAAAAgDjsrEu3R2Xv1uMeSeYRcHhm/8OfSt/6ttVKI/o7LxSl+n2Zd2cINgAAAAAgLu5it7Wfz8Y9kkwj4PDIfnVf+s7vWi3PRX/nwRawb04QbgAAAABA3NxFb7aP9YiAwxP7i59LhaI96JwbrXKNfhsAAAAAkDQPpiR2VvGGgMMDu7vllqU0JqK/86G6q9yg3wYAAAAAJE+wfSw7q4SOgCNkdn9P+nbR6u6k65gbpaG6zLUGzUQBAAAAIKnYWcUbAo6w/dX7UmMi+u1gx2ZlrjUINgAAAAAg6XbWpYdToulouAg4QmQ/n3PbwW4uRXvHV+dl3p4i3AAAAACAtAiajtKPIzQEHCGx2z+XSm9Ev2PK1XmZS5OEGwAAAACQNkHTUfpxhIKAIwT2+Zar3Ih6xxTCDQAAAABIN7c5Bf04QkDAEYaHU+5NGWVTUcINAAAAAEi/3W3Xj+Or+3GPJPUIOLpkP5+TShUbaVNRwg0AAAAAyI6gH8fzrZgHkm4EHF2wz9ai77tBuAEAAAAA2XOPrWO7RcDRIbu/5yo3ouy7QbgBAAAAANnUakr3Jtk6tgsEHJ366z+Otu8G4QYAAAAAZNvmksRSlY4RcHTAbtyXfuf37MGbz78r04QbAAAAAJAHj2Yklqp0hICjTa7vRsUevOn8G6rLvDtDuAEAAAAAecBSlY4RcLTrb/9MujsZzdKU/nGZaw3CDQAAAADIE5aqdISAow32q4OlKVFsCVuuSVfn/d8PAAAAACB5WKrSNgKOM7LPt6RyzWr5lv87KxSl9xdlekpUbwAAAABAHrWa0sMpd6EdZ0LAcVbLt9y+xL6XphBuAAAAAAAkaWNBkqzd34t7JKlAwHEGdvvnUvmtaHZNeW9W5vwA4QYAAAAAQHo4JbFU5Uy+FfcAku4gKbP63/61/zsbvsl2sAAAAACAI7vb0vKc7PMtmXN9cY8m0ajgeJ3VOy4x8700pToiMz5HuAEAAAAAOImGo2dCwPEK9umiW5qy0vB7R4WiVKdxDAAAAADgJR5OuTkqXoqA41XW70kPpvzfT/0+TUUBAAAAAC930HA07mEkGQHHS9jtn0v/7X9ntbPu946uTMtcGCXcAAAAAAC82oMp2S/m4x5FYtFk9BSRNRatjsi8O0O4AQAAAAB4PXcB3kpiHnkKKjhOs7kkLc/5bSxaKEpXSd4AAAAAAG34bEb20+m4R5FIVHC8wD7fkiSre5N+7+i9WZlzfaRuAAAAAICz292WJGv394zpKcU8mGShguNF//BY+mzGb/VG/7jMpUnCDQAAAABA+5ZvSTQc/QYCjmPs8y3p+5f9bgvL0hQAAAAAQDdaTWl5LugfiQMEHMcF1Rs+XZ1nS1gAAAAAQHeo4vgGenAcOOy9cbfu7076x2XenCDcAAAAAAB051gVB704HCo4Ar6rNwpF6b1Zf8cHAAAAAOQLVRwnUMGhiKo3rkyzawoAAAAAIDxUcZxABYfkv3qjXJN5e4pwAwAAAAAQLqo4DuU+4Ihk55QxlqYAAAAAADxoNaWNhbhHkQi5Dzi8V28M1WUujFK9AQAAAADw47MZ2S/m4x5F7HIdcHiv3igUpXem/RwbAAAAAABJ2t2WWKaS74BDv/paWm34O/7wDRqLAgAAAAD8W70j+2wt7lHEKrcBh93fk9747+1BQ5bwFYrS8E0/xwYAAAAA4LjNJSnnVRz53SY2aMLSavo5/nuzMj0lqjcAAAAAANFYvpXrLWNzW8GhnXV/zUV7KzKXJgk3AAAAAADRcf0lc1vFkcuAwz5dlPrH7UEjlvDRWBQAAAAAEAeffSYTLpcBh37zS2n1jp9jU70BAAAAAIjL8i13UT+Hchdw2P096ff+wN/WsFRvAAAAAADikuMtY/PXZNRnuQ7VGwAAAACAuK3eyWWz0dxVcOg3v5S3rWGp3gAAAAAAxM3tGpq7Ko5cVXDYZ2uSZPW3fxb+wQtFqjcAAAAAAPFrNYOQI1fyVcGxfMtf9cbwDT/HBQAAAACgXU8eyD7finsUkcpXwGGtnxSrUJSGb4Z/XAAAAAAAOpHDZSq5WaJiv7ovSdbL9rD94zI9JZanAAAAAACS40m+lqnkp4Kj1ZSXcEOiuSgAAAAAIHlW7uRqmUouKjjs/p4kWd2bDP/g1RGZc31UbwAAAAAAkmVnXXLLVHIxZ81FwOG1e+zgdUlL/o4PAAAAAECncrRMJR8Bx5MHfo7L1rAAAAAAgCRbuSO7vyfTU4p7JN7lowfHt78rbS6Ff9zBevjHBAAAAAAgLEfLVDIv8wGH/eq+1D9u1WqGf/DhG+EfEwAAAACAMPls25Ag2V+i4mt5SrlGc9Eu2WdrOgyedtZ1IoQqVaTeyuFfzYXRSMcGAGhTdcR9b5cqUvktqVB8/X+z+fjgzyVpb1va3fY1OoQpeJ2rI+7vZ3m9d9al1q/dn7vbwdVEAEBUfM2LEyb7Acd3fldavxf+cYeuS+LH+azsszV3Arv52J3U/N4fSG2USdkPZFQoSuXawe2tYAcbb2MGALxCb0W6OC71jx1NdNt1+N8dbLfearrfiI0H7jcjyZPgYJJ/Gh/LYuNUrkn941L1svvns4RXLzrtPRKcF2wsJPu1Drz42F+8OJNmL74+UT+24Bwvi6L6Puj0ezgsWfo8ZNXmkuzTxcxfOM50wGGfrUmS1d/+WfgHH6xLmgr/uBlin61Jy7eCk4GTYcbP/727tXG4U//HjypGF8eloesy5wc6HmvY7Ff3j8KcLF6VPB42Dd8IPWiyz7dct+fNx+7HMmuTBck9d70V6eKYzKVwt7A+fP42HsTz/jt+olq9fPj3rP+g5sZQ3S3R9DEZKRTdSXpwor637Sa/K3finwAXiu63/6yBzt62++5auZPO77D+g/Dq4nhngcZZBK/1lWn3Xf9kQfr8VvyvteS+n4P3+ete771t6dm6uzq60vA/tm6189h21o9Cx7DL24fq0sWDz5Ov91hSbC5Jq3fCfX9UR9wF1+rIy8PWOATh9OZj98+EHsnhXgv7u/91yfzTf9qLezTeZDrg8HZC0T8u01NiecpL2KeL0j/+nRSEEisN6fO57g8cTHSPv669lcPgw35UMRq8Lg3WY6vssF/dl/7+UyknTXwC9m7d6L3Zrjsz2/29oHwuX8/fj4tGV+dl3pzo7jj7e4l+/9kPZA5PqKuXu368iNhQ3U1EozyRLlWk4ZvutrPuQvM4JpBDdem92fYmYaWKC0QG6+53qzGR/BP9QtE910PXo58wBQHSYN0FBo9m3IQ6judsbNY9D2dVqrhb/7h7n9ybTO5a93YfW3AxI3hdHkx1/9jKNWnyfrIm5b4FYd7wDen2aHfv60JRujrv3m9JdPhYD95nGwvu3C6uzzNO2ngg/X//Oe5ReJXpSbr96Ygk2dCDjqvzbA97CvtszX1oqpetHs1Ef8Wqt6Ig4NBnM0bvTEcadNj/eFv6zvesHk5lr2LjdYKTf8l0GnLY/T1Jcs9fGq6AhSk4WWk1TafVHIfP36MZaTmEQNGXYwGH7k0a9Y9Lg9dzUd1hny5KktXtlD3W6oh0bT45k5FWU5F+T/SPS/X73R9nZ737iY0vvRUXXiVtd7hW04Vay3PRPW/tBgAvc28yeb9lYT22xkTnIUdvRZpay37FxqtsLqmr34H6/eSGG68SfJ5XG/k7T06Sck36H39mzHf/m7hH4k22d1EpveFnkp3GLxXPrPsRt9pccifvcZTj7m67Kz4f97mxSNYu3Awmfl7ZlXnpN7+0akzk80t7pRH8WHdUOXA4Of+4L3knhFFoNd0Jo2Q7fr8++tAdI8nhhnRwFX7u8PEGN/tRRfbz2Ug+r2jDlQ+l9xeTE25IR4HgD9ZONKP2Zmw2nOOUa+FMLsNUKLrH98Ot5IUbkhvflWk3visf+r+/MF+jq/Mu/E+K41fUu9XNZ+LKdL7DDelgaUm98/82rfOQ45/nsTYr4hCenXXpt7+dyErfsGQ24LBPF6WhevgvXnWE5SnH2P092flx6dm61ScDyVlnvNI4GXS4fixe2KeLUqnirpznWTBx7cTGgrsim8Qrm1F6OCV1EBLZL+alci38ajXfWs0XwzH3ef10mqAjboWiCzauTMc9kpcr19yVYJ8n+2GvbR+6Ht6xujV80000kha6nCaYGP1oy28jxbdvhHu892aT0zgzzPdeqdLZ4wqWIcH1HunEcMjv0bik6fsni9J2vtimzAYc3+jVEJb+Dr+QMsjubkmS1e62TexV4+W5w8mT/WLez32s3nE3SKt31G6YZJ9vSdURm8vKjRe1mp2V/f7ml67sM812t93a7uPBpK/PLF4tCDfi7sh/FoWiK9f2dXU/7N/8UiX+q5a9Fff6pvEKaqnixl6/72fsYb/nC0XXayIJz3PYj62TYDEN3ylR6fS5SGv1xmmCCrL3F6OpxsORYIv2jMpwwPHYz4t3MUNfLF2wz9akVtMtKUhCt/NXCdY9S9berYd//EIxuc3EouaW57RXgfBkwd3gtLlHuX2+JdWu2cR/Ds+q1Tyx1Mz+pNZ2aIYuBOFGUq46n9WVadcnJGw+noc4n9uhuqt6SftEs3/cXf0Ne7LnYylWqeKWq8Qt7MdWfquD/yZl3ys+FYrtT+qzGgJUR9z3EtUc0dlcynSlbHYDDh/9N3orMuf6cr885XD73aQ2SztNq+kafoUccthna9LgdZua5yEKz9qcaPsKI9Oq3e+tvW13y5pjn1kdLFuBZ2kNNwKDdT8hRxYUiu65uTqfjGqCMATVO2H1SPE5eewfj3fy5mtL57bH0UEokmXthk5J6oUUtqCa41qGvqOSzF0Uy2wfjkwGHN76b1C9cbQsJU3hxnEHzVBDmyy1mul8Hnxqd7LNc3hSq+mqMs5qdzvbjW131qVPBqSgmqOd5wbtGUtQv4BODda5CviiILjKau+D4Zvu8XXL9+TxynR8n6+kTBiTMg4k12DdfZ55r/iXlcrfU2Qy4PDWf6N6Ofxjpojd35O+XbS6O5nuCWkQcjwN4YTI13stzVq/bu/f31nP9Jdsh84e0Ga1guNFromvq+YI47OLk4bq2ZkAj80mu5Q7ykluueaWcqQ9uHqd6kh4lRy+BFU0TNwQSPL3VJzKNUKOKGR4/pLNgGPnS3cLmXlzIt/LUz6bcSXjWZiMHk2WELZ23x9UcHxTHgKLTuysS7MH1Rw0IA1Pb8Xt9pAlSd5pIKqT9rxNEoZvJj/IKdeSH8QgOllectKtvH1/xSHDy8OzGXD8q98LP5VKe0OuLtmvfyaV3rCZaqb5aCbTDXaATGo1j5oGL7AUIRRZ6ssQSPpE17e8Tg7SsMPEYN1VTAFZuGDoE4GgXzvrmV32m7mAwz7fkv6HfxN+08ccL0+xz7ekf/X79qDqITtcCEYVB5BGHpoG51J1JPcBfubkNdyQ0nOu9l7Cl1EhGlSvvh59lfxx779MzoMyF3B4W8+f5xPAJw/c8pQsfhGTnoePk7bu5XFi0onlOYmQoztXMro7TV6/2/McbkjpOU8JdoAB8HpXpjm39CWjv5UEHGeV03JX+3RRKr9lDxpzZo65MJrvvio+lN6IewSpZ84P8L48q6BpMCFH+8q17Ib3Gw/iHkH0gt1S8hpuSF76r3lD+T0y3OQxVIWiW0qJ8BFwpISPBqPlmkxPKZ8Tjr1fSKt34h6FHzkNrbzL88l1GHj+2hf29s958XaCG3F2I6+7W+U93JCUuj5hwzfT0TcE4cvoxNKb6gifFR8y2mg0gwGHhwqO8/mcCNvnW9L3L2e2eiPRXfbTLKtXhKPC89eZIORgd5Wzu5jRk8Ws9Ys6i7FZQvu0bjl+dZ7y+zzKY5VZt6h4Cl9Gd+3LXsDx/cvS7nb4x8yjJwvulkW9FZlLk/msyvGpt8Lyim6lpUleEh1s/2yfrcU9kuSrjkR7tb/VjKayYmMhf9Ub/eM04ZOkB1Nxj6AzlN/nT6sprTbiHkX6lCrsQBS23W3XjiBjMhVw2KeL0lA9/G6weU3WNx5kN2HmZMKPwetxjyDdCkXXMRydezglSZYtoF8jikqh1YbUmJD+rZH+pOS29709evT3xoT7d8JqDNlqBrvr5AeTYyfty5KqI9KVD+MeBaLycCr8i7F5QfW1D5nbSeVbcQ8gVJ6+LHLbiLK3okiWpwSN7spvnQyTNpdcD5DNpXBf2/7x/L6mPvVWDq4i5rA8PCzDN/Lb7ycsraZ0d1J6f9FK4rl8mfJb/o69sfD6E/hW0/17GwtSYcpN0rtdX31vMj27aIRlbDb+vht72+61ftla7sJ33e98ueZnrK2mC8vS7sp0+oMavFqr6b4bs7r0OwrBd0kal6MlVQbDtmwFHD7WEZVrkvL3ITooV/Lbf6M6Il2ZPggbXv4c26/uu7GEkXj3VtyJ9GRGl97Epbci1e8zOe/G8E2Zd2d4/sKwsy49mpF9uihzYTTu0SSTr8rE1YYLmNoRTFCvzXdewfRoJn0NJrtVHYmv4mtnXVq545axtvO7HFzQGLoeXs+QLAVb9fvSx33ZeTx51moeTcJ31t0GCBsLvLZhePtG+78zeLkM9uHIVsDhY3uw8/kMOLwno2OzMm9PGWnptf+qeXNCdn/PaGrNdp18MwkPV3VE6h+TBus8r53orRxMUq5TVRS25Tmpf4wqjpfx0ZByb7u7k867k64KoN0lF6sN6dGHnd9vWl2JYdeg1YYLkzq92BA0Al2eO7zI0dVyqQdT2Qq2CkUXctwmmD2zRzP5/PyH6d92+TNZKB6ey0Sy08nFcUkEHKFJ0/baZ5StgMNHKlp6I/xjpoHPhPnK9EG4cXampyRJxt6tuz4rnYQcV+fT0wCzXEt0t+ijyfjSwS2Bzd2SvKtAqSJzrs9I25IaB7eE6fQ9uLvtJro7X7qJTJylj/cmZT+dlnmXZVORCGP3kpWGe89cm3cN5c5yn3mc3FRHot1x6SzLjtq1uSTdXnKP46yv93GrDReUZE11xC33zOJjQzYdX3LYW5Hem/UbdBSKLFMJUwarirIVcPhYt1gdUS57CvhK83orXZXhm2sN2c9njcZmrR7NnP1DeXU+XbumFIpc0e9WucZz2I0Q3oMHu5nYjkrZw+Duz9r9PXMQksKnsH6DN5ekj/pct/zhG6cHlZtLLtzIa7+CqKo3gsatPqskNpekTwbcpP6sj2t5Lr27ppzF2Kx7XpjAIW12t92Sw6G63wbI1RE+H2HJ4O9otgKOwevS6p1wjxl38664+ErzLo5L6u6qhHl7Svb5ltHFcavPZl69ZOWg5wYTXSB65vyAdLBExH4xL0nuMxtl0LF8Sxq+yVKVKIT9uq403C1YylWqHG03m+cT26iqN3bW3UQlis9rq+kqcVYbLuR4WW+RKAKXpJi874KfDF5dRQ6sNKRn69IPPG3bXr1MlVOIstazLDMBx2FTzJADjtQsaUiLwndDOYw51ydJxj7fkt6Ztnqy4La03Y3dtdgAACAASURBVFk/Kl27OOaqNn6UnQ8skFbm0qQkGfvptCRZLd+K5sS91ZSW52T390QVh2eFop/XdHdb2m2Ef9y0GopgO+7VhquQiHpyvbvterE8mjmq3qmOHOwu8thNaPIy4S9V3BXwLOwQg3zaWXffIz6WXPtqlJ1fmboQlJmAw4veitwaeSRVEHSc/F+bcq9bDq7wAClj3p2RfbZm1D9udXcymivxVHFEo3+c7Q99KxT975zSyU44YdvdzvYSlLPqH6cfB9Jtec7tetJuj53XSWqPNSTCb8U9gNAEnbnDFPaHEVLr17L7e3GPAkCMzPkBqVQxen/RrdP1LWiABr+Gb8Q9guzzvUPBxkL84QZOSnLDbOAswmhAfRqqOMKTsWWf2Qk4Ws3wyxbz/MHprfh5/KsNyZVBAcgx01MKthY2kYQcy7eCpqeQ/JzMlGtuNwz4c3HM37F31l1/CyTP5P389oRD+vlqYsmF6PBkbOlfhgKOX7tbmPK6RazkHruPx99qSo9mZD9P7haoAKJjrjWkKEION6EnXA34OpkZrLuQg8lY+ApFvxUcdyczd5KbGaVKoreOB14pzu3icTZhz6Fjlp2Aw8cSlTyfoBWK/h6/W0tq7U9HZJ9v+bkPAKlhrjWkVtN4L79fCXmXrTTbfOzv2IN11zk/isqcPPG5c8qjmcyVKGfOYJ3PFNIrg1uRZkrGvv+zE3D4kOc1j+Wa38fvmodZSdberVM6DuTd1Xl387k0cHOJUDXg+2Qm2AHiR1v0EAhL9bKf4x7sNIQUeI/PEgC8Druo4FTmwqjsBzLyWdK9uSR93CcN1a0k2Y8qRhfH3UlcuRbskAIgB0xPye2uUr9v9cmAnzs5WqbCbipRXU0rVdwuEMM33UR6c0na+dK9Frvbmbtq5JWviW1UWzaje4WiWwJ2e5TXLND7ht/qphftrPPcdyLPVfGIXHYCDh8na3lvXhOcTPk+AV1puFtv5USYYj+QUXXkoJrkLel8ze2+kBP2gwjvrFyTztek4RuZeo4jew4LRfcc9o9Jg3WZnlJEd5wt5vyA7MJNo+Gb1tsVZcpknWBnGd/Lgo4Leki8eJ+bS+53ZvOx+2cmD6fzNYmjeiNdyjVXFcVuN85g3f/WyS/aWXfBINtinx2VR8mWsXOj7AQcHphzffm+ytd/0K09qitsu9vuROvoZOsb1SP2x0UXelQvS9WRTE3GT3BfNLE0RLQ/HTGq30//JP32qBTXc/jFvDGXOPnsyJVp9+dqw89Ed+fL8I+ZVk8eRBtwvEx1xN2Gb7q/76y778DNx2zvG/A1OdhYCPdz1luRLo5L59+K5iJRq+k+05tLmTtBf6XBuvt8MMGOR7nmluAN36Ca5iwINxAxAg68XHDi62v/6rN48aSlUDxZ5fHjomtM+P3LUv94+iflcQma9K40pOqIWzK0v2d4Ps8oKL3fXHKfl/dmLSFHZ0xPyVVxDNb9VHGwJOLISsOt6U9a6XDQAyoIPDYWXBgT9mQ8TXy9Rk8ehHOcQlGq3492qUCgf1zStLS37b5/8zLpf29WeuahwT7Orlxz73t3QQUvM3Tdz3F57+MlstNkdPhG3CPIHHN+QLo7aRKVvAZl1Q+mdLBO3x6/2flx2S/mZff3Yh1mqm0uxVr9kHqtpnRvUpIs78MODd/w952+ucT3w3HLt+Iewev1j7urpf/Tnus/kISqk6j5Cg7CqnqIK9w4Lmhsm5ftVIN+HEkLKPOmOpLP76SzKhT9LSHKa+DtSZaasGci4LDPt6Thm+FOxpI0qY+Tz4lGGFpNd7Xm3qT0JyXpeNjB7iyd21lnXXa3Hh7uFIQ2mXN9UmPCZ7jK6xJYnkvXSeJg3U2mf7QlXfmQyV03Wk23NLRb5Vr84cZxwzeTNR6fgn4ciNegpwqFLLjqKYSjesOHzJwbZSLg0N62u4WJkyZJkrk0KX02Y7xu3RimjQUXdnzcJwVBx09HZJ8uxjywFFq9k6k0N3JBtRE60z921AcobJwYHTmqOEqXUsX1a/lhToKOwnfDP2ZYn4MkXr32VRLfCd/LfAfr0lDd733g1fISqLXLZ8Udv+PhC3suHaNsBBzw6+q8u6VJUNlxbBmL/ekIFR3tcFf2MpPmxiKs9e15FDSehH8bC+kN4wrFo6AjiRPtsPioZgrrZLb8VjjHCdPFBL0XHn3ovwHqe7NUHsepUFRqLgRGobcivb/od3ebZzQMx8sRcOC1zIVRafmWSe3J48meEtZ+kbKwJk4k5N3h+euYuTAq3R71s5NVnnZbOKt7k+m+ehM0ubzG9/uZ7f4inOMksXomaRPOxoTfpWD044hfFLsGJV2h6Crqptb8X6B4ktJQHpFgFxWcTVDBsbMezprdOGwuuYqOq/PW3q0bc60R94iSjwl6d9L6WUmK4GQ9TT0i0qrVlOYn3FW3NE+SgiuGd1O47AbhKlWS8x3carqQ432Py2WDfhy899GubsKI3or7rFUvR1d1ubednM82EomAA2diekqyz9aM6vdt6vf8vjcpDdWtXbhpzDiNNOGXfbroqhHQvqDkmoqLaOysu2q3LIQcrabbbQv+JXVpRNLew5tL7j3psynoYF3afJyfrXIRDp/Bmw9pXVKJyLBEBWdmzg9Ikkn9ya8U/PizXOV1Wr+OewRZQB8TpEcQcqR5uYrkdtJI67JKhCOJwcvynP/JGf04kHVp2N4csSLgQFsyFXK4bVAtO4W8AktUgPzZWXfL+dK+VbSv7QlxEr8T7fHd74Z+HMiyzSWWp+C1CDjQNnN+QPp20WhqLf1XCR5OSVxhf7kkNWkDEJ1gicft0fQuESoU/S4HSLvq5bhHkE9Bvxufgn4cQNb43nYZmUDAgY6Yc30y5/qM+seMrkyn90pBqyndm5T96n7cI0mm0htxjyD1zAVPO4EAUQh2oUpr0DFYz8Z2w5uPwz9mWn+3s2Bn3X+PmMG6NFT3ex84kubedGmxuZTO3yFEjoADXTHvzkjDN41+uKXUBh3uy5IqDiBp9rbT3wsiK44HHWlr8DZ0Pe4RJFNYFZg+wpc8WJ6TVht+74N+HNFhqZZ/NI7GGRFwoGumpyTTUzKpDjoeTsk+TVkX6ShwYtQdlvh05/uX/ay1zcIV/bhsLrntLj/uc6XCaQigBuvp/yz6ujocxmeBiV3nHkz5ff7oxxENqgr8W57juwZnRsCB0Hwj6Lg6n54JsptEUcXxorS8fknFRLpj9umiNFTnM5lUu9vSow+lj/pc4LHaSHaJ9sWU76ji68S+f6z7Y2wsMPHoVKsp3Z30+9mhH4d/Gw/iHkG27azTewNtIeBA6IKgw1yaNLo2b/SDNbcONOlXEFbvxD2CZOmtuD4r6Nz3aeLXsZ11f5OmUsXPcfNqY8FN0v6kdBR2JK2yI4yJfJx8PZ9hbaV7e5SQo1M760HDc3/4zvOn1fS/1CjPoggBkTnfinsAofBxlTlpJ2cpdbitrBQ08rR68sCdECfty2pjQfbposyF0bhHkgzvTEs/mox7FOlVKMpcmiQg6pSV9MTPVTGCO482Fo56dJRrroqpetn9GWfInfZqqt1t95sZ9nNYqrjnptsS+1bTbS3cP+5e73bPy8q15F8E8Wml4Z63wXrcI0G77jH59uqh52VcOJKhqu1MBBympyT7gYzCXGLAHsuhM29OSEHY4fpdWG08cCdWSfjycj9QVgdjzLVyjcl5t67OS/+z560AM8o+35Ik6+WqZnVE0lL4x8U3BVU4y3Pu770VdwJVrrmKiqhPpsKYyMdpZ91PUDN0Pbzn5XjA1Y73F9MfQnXrwdTR5wPJt7ftXrO0NV1Ok3uTLvxDJExPKTPn/ZkIOJA+B1USLuzY35Mkq531g7DjS3ciF0fIlOaT37CUa+5k84NS3CNJr6vzMm9OZOaHInK/+lr6x//Tz7HLNRFwxGR32902Flz/jt6K643x9o1oSujLtXR/x28+9hMCDNbd+nYu7MQrKMV/fzHf1Szt2tuO7r3barpzVLYr9W+1QbiBjhFwvIJ9thYssYBHpqckvVA1cXgF98mCDqs8orDzZTT3kzS9FXfi/P3LrnKDcKN9QSn+YJ0lEF04DDz/4g/93EH5LT/HRft2t111x/Kc69N0Zdpv0JH2SaPPSser866PBuIV9OO4Oh/3SNJj5Y4LTJEtF8clsUwanclOwBGcuIS7Do7lCjEx5/qkoMIjCDs+m/Gf5iblClZEXc/NhdGD9/e2pMbBLSPGZv2X+paON2JdOrjR6bsrf/83roIjydtiInwrDVfZMTbrrw9B2sMtn6Xw1RHXP4Ny+/jRjwNw87qhOlUcUSkUJWWnl0x2Ao5gIhPmlX6aBiVCEHbY51vSO9NW9yb9VXQkoReI5BpUHoYP6Ei5xnOYMvb5lvQvTas/91S9wc5AZ3O8V0arGV2fpKBEX/IzuUt7BYfkAoiwdj550dX5+JaH4iT6cQDS8A0CjqhkbPku28Sibfb5luzCTdmf1GQ/kLt9VJH9dDooL/fCnOtzk5PeitFQ3dv9+HwMAE5n9/ekQtEeTnB9uOhpYpgVQf+dH25J9ftuycjYrPSDtWibQD6Y4gLDy3jaWUiSC4Dq9/0dH2fH1pgAIR86RsDxKjQQ+obDrV5fcbOf+11aYa41pM0lo96Kr7sIbzceAGfzV++7juk+KwWGrvs7dtpd+dAFGS8LMaojLuQYm/VfCdFqSk9YKnEq30tIyjXpGv0fEmFn3X0nAnn29o24R5APWahwPCY7AUf1srvBC7u/J3u3Lu2sW33c55rCHZ+I7G67Luwf90mStfPjfish3pl2Nx+SskwFyAl7ty799ret18lbb0Xm/ADLU05zbd5Va5zF8E0XdPgLmJ3dX/g9flq1mm53AZ8G64QcSbGxcLTNMpBHg/XMTb4TKe09ql6QnYDDh7zuqPGCw10NdretHr2mgWKr6cqLg2qOZ2t+BtVb8X+CDcAru78nOz8uSdb7OttBqjdOdW2+/X4X5Zo0tea3dLj3DX/HTruVO/7vg5AjOR5MceEF+TZ8M+4RIGWyE3CUKuFvL8fax6Nw4/Zoe0t2NhaCLef8hRy+kBQD3tndg92RWk3/4YbEjgSn6WbHkkLRb18On9vFpt3mkrS37f9+BuvuNeY3MX6NCc5JkV/DLFPxLmO/udnZRcXH1XwSc+kv/lD651929lzsrLuQ4/1Fa5+tGXN+ILxxefyhp4wd8Mfu77lGia2mC06j2LFhqM7uKS8aqnd/VSwIOdoNwM9yXB/BSRShQFQezbhdT3yrjrjeLHc97l6G19vddv04aAILH8L6bPdW/EyU2TLWv4xVxWcn4PBxhaHVlH26KHNhNPxjp4D9P/6d9JtfWn39N50fpNX0E3JsPg7nOAAiYff3pF99LUlWz9alu/Xo7vydaUmN6O4v6Xor0nshNoOu33ff82FdFPC1DWqW+nqsNFzflCiuupUqLshannPBCpUE8Qj6cVCuj7DdDmme0z/uL4Rjy1i/Mlapl5klKub8gPSJlyvvudxRw379M+k7vxtO6XgQcoS5XOVfPHXZz9gHHIibfbYm+9WCJFn96uujJsVRoXrjm67Oh/tdF1RyhLF9d6EYbvhyXNaqMl2/q+gM33RbCF/5MNz3T7mWuauH3tCPA0m2seCvUq5ci26r8hzKWvV6dio4pKMf3DCvLkRRPp0w9vnB2vg//8PwDnq8kuPzWWPe7vzEzH79M+mff+ln3X65Jmkp/OMCKWSfLrb/H+1uuxOcnS+DSYvV5pJ0rx7PlV+qN07ydZJYKLrgpHrZTcI6ea2DoMRX0Jy13/ONBVdaHuVJf6HoKkeGb7iLDBsP2t+6NliCVL3srvhmbO23d40J1+SXCzJO9bIL3ZJoZ919F7aa+QmmPr/l+jv5MHyDpXI+9FYkbcc8iHBlK+AIOrqH+ebP0prds/rHv5P+/m/Cn4y0mtInA9LYrLU/HTG6Oi9zrq+tQ9hf/Fz61rfDDV+OS9BVJPtB3CN4jULRnZwOXk/sMq7EP4flmtQ/Jg3flOkpxT2ak9znv7sKtpWG9HmMWxxemaZ640W+ln8EBuvSxXHp4VR75cTVEbdrh6/JblYnGA+mXI+MqBWK7rUOmtRuLh1M5n599FwXiid32qle9rdGP0/ox3FSdSQdV/b3tt0OSMtz2V7mtdrwF3D0j7vvkKyF1XErVUTAkWTB5HQzxGPmbKvYw11T/vyavzt5MCVVR6wk2bt1o3emXxt02KeL7rX4L/9i9b/+a38/DknZB9qFdKlZHmV/OmI0NqtQG8l262BZVNzDOCv76bQx775mG+YoBU2C06q3crBWPUHPaV4E1RxXpt3VvCcLp5+QVkfcBHjout8tZ6XsXvXbWXd9Ma5MxzuOtEwys4J+HOlTqrjP6dB1aX4im4Gr5M7PVxv+di4bvhH98rysS9DF3bBkK+AovRH+MXfWZff3knd11ZeovnA3l6SP+6Shugs6flIz6h875d97LP3O70uS1c669MDzjzknaGfXarortCuNo8Bqf8/k5rMShp11d1u+JQ3fsIkLOdLs6rxMT4nqjTiVKu5K3tjsyQqKOL5nnzyI/j6j8uhDVwnmOyRCsriLRbzuaVOquGq1TxJ0QShsn9/yF3AM1ml2HDYf8+eYZabJqCT3JR/2F7276pSaq8Cps9JwQYd7jk+/rd9120n67p7cW8lck53IbC65dcF8VjrTarofbMkeVFGhG1emZS6M8lk+TVzLLg/7LozEc//t9olIm7uTnPDnUWOC1z2NyrVwmjIn1c66v6q5YHkcwpPBi7vZCjh6K37KbLJaRnaaUiWe9bFBme2Lt82l6H68L3pem551u9vR7o6RRcu3JEKi7pRrMu/OEG68zMZC/iZEq43sP+adddf3BPkS9ONA+lw8pWo5S1bv+Dv22zf8HTuPMtiwOFMBh7etYnMUcJhzfVJjwuSy5HHoetwjSL/lWwptK+A8CtauojPBLhx4uVYzCNLyY8XjiXaSrDQImY/Ly7lb0I8D6eK74XPcVhr+guVSJfvPX4SyWL2eqYBDkp9lKpuPwz1e0g3fcLc8qY5k8gMeuTB23si7jQz3CvDpINyg78YZZL2L/3GbS9ltMHqaB1PZX45zVnkJOCT3uufp8WZF1i8m+gzT8zZP8SWj78HsBRzna+4Wpp112edb4R4zwcylSemzGZPFrrovFXcH+ix5xklWVzhJ7czVeULKs2o181PWnpfHedy9Sb5H9rbzt5Uk/TjSJ4NLA07wWZFaHcnk7h+RC3vOnBDZCzhKb4TfDTaPjUavzrtbHlRHaEgYpriaGGZFq5mrQDUUV+dl3pzgM9yOjYWgsW12Lc/lb5IruUnu7dF8hxxZf2+fhn4cSJrdbb8hB73zupfBHVSkLAYcvrq05+xEwVwYlTaXTC4qG8Zm4x5BtrR+HfcIsiBfgWo3rs7LXJok3OjEow+zu5xhbzufk9xAnkOOnXX/u64lFf040iUPFQg+eyDRO697GdxBRcpiwOGjB4eUvz4cksy7M9LOlybTjXyGb1LWHrY8nlCHjSqYsyHc6F4WlzO0mtI85fq5DDlaTbdlbp7RjyM94ti1MGqbS/7ej+Va9pf5+EYPjnQwPSVpdiD8/hGbS7L7e+EeMw2CpSpZ/ACUazLjc0yOgLQJGooSbnQvmBBmKQx4mPAJXpQBZhBy5GV3psZEsl77uMZCP450yEsDZJ/NRrM4P4lKuZbZxuyZCzgk+Vmm4n6kclc2bnpK0t620bX5bKWkhaJUvx/3KAC0q7fiwg365oRnZ91NgrMwIbo3mfzlCVH3BQlCrCwvXQga5yZtwhjXZ4p+HEgSn1vGonMZbTAqZTXgKL/lbmHL6lrl1zDnByTJ6P3FbIQcwdXfc31MkHwgTe9eO2WrpUo+ylwlt+/91BrLynzYWZc+7kvW1e92pSHciNODqWxe2Q+qVLp97bO2NDCJ/Tiy9hxHzcf3c1Svia8qDt5TnfMxV06IbAYcvhqN/kP++nAEToQcaW6KFIQbYU2Q8jS5PKvCd9v79331zUmxtsK33kq6P5NnUShKY7Mykwsmq+WUidBqSp8MJG9S9DphTXBPk+bA5zQbC9LsQPIqHTq1s+4eTxivUxZ33ElaP47dX8Q9gmRp93PoI5yM6n3v43dlcymbn9uoZLTBqJTRgMOcH5Buj5rQqw02l2SfrYV7zBQx5wekUsVoai2dH4qgtD3Mq795mFy2q93Ap1DMRmVQWNp9LrL+/FVHXNXG21MEG1FJ05X+jQVXeeJrwr7zZbjHazXjDxd2t10g9GAqHa/xyzyacYFcmBOcsMOAjQfhHq8Tvj7LnTy2JIUtcev0uQj7+yOq16TVDL8X0IOpcI+XJ4VipqthMxlwSPJzVdj9iOauD8dxpqfkGtJUL6drC1lfpe1UH3xTu2v6eA5PajM89Bboxq234nZJ+aMlw3KyGATBQVKbU+5tu4mb7yAm7KWpTxK01HV5zlU/pG357eaSCzYefRj+scPe0jIJr7evfhydPLaNhXSHamHq9L0WdmjmswHoi8LcujuLO4BFKY0XqtuQ3YCjetndwpa2EwFPzLszUv+40Q/Wkj05PWgm6qu03fSU3OQyyc9BlHor7YdIvj6raXVxrP3/xteyvDgUitKVaRdIsktKvILmlLdHk7POudV0J8kf9UXze9xqhltaHeYJfhh2t11IdHs0/sqS19nbdpMan1vfrjbCm4CvNpJTPh92P45uHluUE+qk6qaaIc3v0d3t7r9nfC5JzJOMn3dn9uTxYCmJ1ScD4R64XJPq94051xfucVPMfjotSVbLt5KVzF+ZloZvet8CyX4xL0mWjuWSrkzLvDvT9vNtP6pIkk3MyWBcCkXph1ttv2ft00VJsro96mdcUeitSO9MS/3jmd22LPWv01Ddfa/G0Xdob1v6/Fa4J/fteH+x+xAxDU1QqyPS0HVpsB73SI5sLEird6K7wNQ/3v0ua0ndmejafPevbRiPLYxxpFljorv3c7mmrhv/x/Ue7Wbsq430L61Lih9ku2F7Zh+YJNkfFyXJhv5B+OEWO3C8wD7fkiSrz2biP4EbqkvvTEf6Gtm7dUmysT/2OJVrMh+sd/ScHwaSSTwhjNLV+Y6rFlL5HiwU3WRi8Houtn1NfcARCCbBF8f993+JenL7Kp0GPJtLrnIj6RUSx/VW3Os7dD2eKs2ddVfC/2QhniqIck0am20/1Go1XYXC8lxyf8uufCgN32j/sxv2Y4szMI3L3raboIfxfVYoSsM3238t97bdZyvO9+hQXXpv9mzjbjXd98CjmeRURKVdoajvzf7a/NP/m92uC5k+obTz45JkQz8xGpul4d1LHAYdqw13UhrVl1FvRRq8HknFxssktpIlCgeJfDfP/WHI8WAqXROBsHQRbgRS8R4s19ykoX8sF6HGcZkJOI47eC0PX9du7W27z//m4+Su1y/XXDDX+8bLJ2ebj48eS9pPyoOwo3rZvcY+Qq2ddXdL2uveW3GPuVR5eUn33rbbHWRzKT2/XUG4XKq4rSJf9ppG8diC747zb2Uz7IjiOayOuOexUPzm6xnc/9629Gw9OX0ryjVp8v7LX/Mg5Iyrai/L+sf1vRs/M//0z/857pF4k+mTS/v5rBRMmMLEMpUzsV/dlySrzcd+rsIEJx4Xx2TenEjEe9nu70lBwLP52H1Bp/3k9mXKNddQNOTn/zDoWLlzcMK7FNahk6VQPDixuywN1kOrODp8D24suK2td7fd8xjlCUJwoiW5x1equP4sOQs0XpTJgONF1RH33VyqvDoACOysS61fu8/53nZ2vy+zJPjuPz45Dr7PXub4d1Dwmgf/W1a/4wG83os9xIKwk98Cf67O63t/cMP80+4/xz0SbzJ9snlYTfCxhyCCZSptOXwtNpfctnvBF1g7k67gxLn8llQdyfTaMQDZk4uAAwAAJNcPt/S93x8y//T//Ke4R+LNt+IegE/mXJ/sRxWj3kr4zQuTsPVXihxUu3wjkDi8Wv+KoOPoqu+Sj6EBAAAAQLaVa7m4QJ/pgEOSWzcqhbs9liQt35J9tiZzPuRdWnLm4PnL/AcNAAAAAGJTHZGUkD4sHv1W3APwbui6u4XNVYRkt/0sAAAAACAbfMyJEyjzAYc5PyDdHjVeun4v3woa+gEAAAAAkDyFYm76F2Y+4JDktsLqHw//uG77Wao4AAAAAADJ5GMunFD5CDgujrlb2FrNIOQAAAAAACB5fMyFEyoXAYd5c0K6N+lvmYrbCQQAAAAAgOQoFGXenMjF8hQpJwGHJH/LVHbWJZapAAAAAACSJkfLU6Q8BRy+lqlINBsFAAAAACTPYD52TwnkJuAwb05ID6eMeivhH3ylIVHFAQAAAABIit6KzIXR3CxPkXIUcEiSLo67mw/Lc1RxAAAAAACSwdfcN8HyFXAM33A3H5ZvSVRxAAAAAACSwNfcN8FyFXCYc31SY8KoXAv/4GwZCwAAAABIgnJN5lxfrpanSDkLOCT5reL4bEb2i3k/xwYAAAAA4CxyWL0h5THgCLaLLRTDP/butsQyFQAAAABAXArF3G0PG8hdwGF6Sm43FV8vOFUcAAAAAIC49I/L9JRytzxFymHAIcnvMhWqOAAAAAAAccnp8hQppwGHOT8gPZgyqo74uYPPZmQ/nfZzbAAAAAAATlMdkTk/kMvqDSmnAYckafC6u/lwUMVh9/f8HB8AAAAAgBf5muOmRG4DDnNpUvpsxqi34ucOlm9JLFUBAAAAAEShtyJzaTK31RtSjgMOSX6rOFpNaXlO9vmWn+MDAAAAABDIefWGlPeAY/imu/nYMlaSHs1IVHEAAAAAAHwqFN3cNudyHXCYnpL0aMZosO7vTh5OyT5d9Hd8AAAAAEC+DdZzuzXscbkOOCT53TJWkjYWJKo4AAAAAAC+5Hhr2ONyH3CYc32uJAmyPAAADGNJREFU2ehQ3d+dPJhi21gAAAAAQPiG6jLn+nJfvSERcDjvTLubLzvrkmRpOAoAAAAACJXPuWzKEHAooioOto0FAAAAAISJ6o0TCDgCvqs4Wk3p3qTsV/f93QcAAAAAID+o3jiBgONAJFUcm0uSZO3+nr/7AAAAAABkH9Ub30DAcZzvKg5JujcpsVQFAAAAANANqje+gYDjGHOuT1q+ZTR809+dBEtVvpj3dx8AAAAAgOwavkn1xikIOF50ZdrdCkV/97GxILGrCgAAAACgXYWim7PiGwg4XmB6StLynNHwDb939HBKYqkKAAAAAKAdwzdkekpUb5yCgOM0wzfdrbfi7z6CpSqfkrwBAAAAAM6gtyLz7gzhxksQcJzC9JSkjQXjvWlLsKvK00W/9wMAAAAASD8ai74SAcdLmEuT0uodo+qI3zt6NCOxdSwAAAAA4FWqIzKXJqneeAUCjlcZm3U33xoTEv04AAAAAAAvE8XcNOUIOF7BnB+QVu743TZWcv04GhOyC57vBwAAAACQPsM3Zc4PUL3xGgQcrxPFtrHSUT+OL+b93g8AAAAAID3YFvbMCDhe47Dh6HsRlAMtz0mStc/W/N8XAAAAACD5rs6zLewZEXCcQWQNRyXp4ZRE01EAAAAAQHVE5s0Jwo0zIuA4q6vz7uZ7qUqrKd0elQg5AAAAACC/CkU3B8WZEXCckTnXJz1ZMJGsfToWcvi/MwAAAABA4lyZljnXR/VGGwg42mDenpI2HkSzVGVnXbo3KXu37v++AAAAAADJUR2ReXuKcKNNBBztimqpiiRtLEiStZ+z3zEAAAAA5AJLUzpGwNGmSJeqSNJKQ2L7WAAAAADIB5amdIyAowORLlWRpAcHO6sQcgAAAABAdrE0pSsEHJ2q33e3KJaqSNK9SYmQAwAAAACyqVB0c0x0jICjQ6anJG0umUjXRhFyAAAAAEA2XZ2X6SlRvdEFAo4umDcnpM3HRsM3o7tTQg4AAAAAyJbhmzJvThBudImAo0tmfM5VcpRr0d0pIQcAAAAAZEO5JjM+R7gRAgKOMETdj0Mi5AAAAACAtKPvRqgIOEJgzvVJO+vR9uOQCDkAAAAAIM2uzrMlbIgIOEJi3pxwIceV6WjvOAg5Po34fgEAAAAAnbsyTd+NkBFwhMi8O+OajlZHor3jIOS4W4/2fgEAAAAA7esfl3l3hnAjZAQcYQv6cUTZdFSSHs1IkrXz47L7e9HeNwAAAADgbMo1Rd7eICcIOEJmekrS3rbRtflom45K0kpDkqwka59vRXvfAAAAAIBXKxSla/MyPSWqNzwg4PDAnB+QWk0TSzfcjQXp9qgkWftsLfr7BwAAAACcrn5f5vwA4YYnBByemAuj0u529DurSNLOujQ7ILHDCgAAAAAkw9V5mQujhBseEXB4ZC5NSjtfGg3fjP7OW03pk4OQg+ajAAAAABCf4ZsylyYJNzwj4PDMjM9J/9I0GqrHM4Bgh5Wf1ERfDgAAAACI2FBdZnyOcCMCBBwRMNca0rN1E/nOKoHjzUe/iqEvCAAAAADkUXVE5lqDcCMiBBxReX/R3eIKOY735ViIYckMAAAAAORJuaZYNp7IMQKOiJiekiSZWEOOVlNqTEjBkhV2WQEAAACA8JVr0vuLbAcbMQKOCJ0IOXor8Q1keU4Klqx8PhvfOAAAAAAgawg3YkPAETHTU5L2to3q96VCMb6B7KxLt0clydqfjtCAFAAAAAC6VShK1+YJN2JCwBEDc35ACio54gw5Wk3pwZRENQcAAAAAdKdQdJUb5wcIN2JCwBGTxIQckrS5dNSAlN4cAAAAANAewo1EIOCIUaJCjherORZuyu7vxTsmAAAAAEg6wo3EIOCI2YmQI67dVY7bWZc+cdUckqz9Yj7mAQEAAABAQpVr0tQa4UZCEHAkgDk/IJUqyQk5JLfTysd9UtCE9Oli3CMCAAAAgOQIdks510e4kRAEHAlxYgvZpIQcraZ0b1IKqjnmx9ltBQAAAADYCjaRCDgS5ETIUR2JeTTHbC4dbikrydq7dYIOAAAAAPlUHSHcSCgCjoQxPSX3QemtGA3V4x7OSRsLh8tWRNABAAAAIG+G6jJ/tGQIN5KJgCOhzLWGVHrD6Mp03EP5ppUGQQcAAACAfLkyLXOtQbCRYAQcCWbenXHNR68mdCeT04KOZ2vxjgkAAAAAwnZ1XubdGcKNhCPgSDhzaVI6XzP6wZrbXzmJXgw6fjoi+9X9eMcEAAAAAN0qFKUfrMlcmiTcSAECjhQw5wekbxeNptaSs8PKaVYa0icDUhB0fFSR/XxWdn8v3nEBAAAAQLvKNWlqTeb8AOFGShBwpIQ51ycVim6HlaQ1H33R5pLUmJAOgg4Fy1eo6gAAAACQBkN1t1PKuT7CjRQh4EiRwx1Wym8Zjc3GPZzX292WHkxJf1KSjld1LNykVwcAAACAZBqblbnWYKeUFCLgSCHz9pRUrrlqjqT25XjRSuObVR0/qbklLOzAAgAAACBuhaKr2nh7imAjpQg4UspcGHUhxw+3pOpI3MM5u91taXnuRK8OBWEHlR0AAAAA4lAdkX64JXNhlHAjxQg4UuxwyUr1stGV6biH076ddbeE5dgOLJKs/XFR9m5d9ot5qjsAAAAA+HVlWuaPlliSkgG8gBlxUPlg1ZhwVRJpVihK/ePS9y+7JLUxYVQdkaqXpXLNNVwFgJSxTxclyer2aNxDAQAAktRbker32SUlQ3ghM+RgO1arh1Ou50VWlGs6HnDo348alWtS+S33v5drMj2luEcJAK9EwAEAQIIM33SVG1RtZMq34h4AwnMwyTf2q/vSxTGre5NSqxn3sLq3s+5uy3Pu770V++K/Yj+qGJUqLgQpVVwaS/ABAAAA4LhCUbo6L/PmhJHm4h4NQkZalVGH1Rz3JqWNhbiH419vRacFHPqTkqv2KBTd3wvfPfrnAEEIgAhQwQEAQMz6x124QdVGZlHBkVEnqjkGr7tlK2nvzfEqu9vutrn04v/zjWqP09gPCPsAeLZ6Rxq8HvcoAADIn96KCzYujBpN5uDib44xqcuBw2qORzNHyzwAAAAAIOvotZErvMg5crjTyt1J19MCAAAAALKoXJOuzbNDSs7wYueQ/WJeCnZbyUITUgAAAACQXL+992ZlLk0y180hXvScYtkKAAAAgExhOUru8cLnnH2+JQXVHHnYbQUAAABAtvSPu6qNc33Mb3OONwAkHdu+8NHMaTuRAAAAAECyVEdcxcaFUea1kETAgRccBh33JrO9rSwAAACAdCrXpLFZgg18A28InOqwEelnMwQdAAAAAOLXW5HemaaBKF6KNwZe6TDoWL3D0hUAAAAA0auOSMM3ZN6cYP6KV+INgjOhRwcAAACASNFjA23ijYK2HO668tmMtNKIeTQAAAAAMmeo7paisCsK2sQbBh2x+3uSZLU8J63eoU8HAAAAgM71VqTB69LwTZmeEvNUdIQ3Drpmv7ovBX06NhbiHg4AAACAtOgflwav018DoeBNhNAcLl95siAt36KqAwAAAMA39Vak4RvSxXGWoSBUvJnghX22JklWK3ek1YbUasY8IgAAAACxKRSlwbo0dF3m/ADzUHjBGwveHS5hefLALWEh7AAAAACyr1B0S1AujrEEBZHgTYZInajseLLAMhYAAAAgS3or0sVxKjUQC95wiM2Jnh2bj2lQCgAAAKRNoShVR6TqZXpqIHa8+ZAY9umiJFltLrnAY3Mp3gEBAAAA+KYg0KiOyFwYZU6JxODNiMQ6DDx21l3gsbPOkhYAAAAgSr0VqVxzgUa5RqCBROPNidSw+3vSYeCxJO39wgUeVHoAAAAA3auOuECj9Ib753JNpqfEnBGpwZsVqXfYy2Nv21V5tJqu4kMi/AAAAACOq44c/HnZ9c8o16RShd4ZyATexMi8w51bgu1pj4cerV+7UAQAAABIu3JNKnz36O9BmFEosqMJAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA8P+3B4cEAAAAAIL+v/aGAQAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAOAp7dEmlYt+HnwAAAABJRU5ErkJggg==" style="width: 350px;" alt="SeedSigner Logo">
</div>

# SeedSigner Workshop 101

## Self-Sovereign Bitcoin Hardware Wallet

### Build Your Own. Verify Everything. Trust Nothing.

---

## Agenda

1. **The Risk** — Unpopular, hidden, non-marketed risks of proprietary wallets
2. **The Why** — Open-source, verifiable security with SeedSigner
3. **The Build** — It's easier than you think
4. **The Workflow** — How air-gapped signing works
5. **Hands-On Demo** — Step-by-step with Nunchuk
6. **Why This Matters** — True self-custody
7. **Multisig** — The cheapest setup ever

---

## Part 1: The Risk

- **Unpopular**
- **Hidden**
- **Non-Marketed**
- **Unsponsored**
- **Unbiased**

<p style="color: #f7931a; font-size: 0.9em;">Presentation</p>

<span style="color: #f7931a; font-size: 1.4em; font-weight: bold;">Risks of Proprietary Wallets</span>

<p style="font-size: 0.7em; color: #888; margin-top: 20px;">No wallet manufacturer funds this content. These are documented facts.</p>

---

## What You're Really Buying

Most people buy a Ledger, Trezor, or similar device and assume:

> "My keys are safe because it's a branded, 'secure' device."

**This assumption is the vulnerability.**

---

## The Supply Chain Attack Vector

Proprietary manufacturers collect **shipping data**:

- **Full name** · **Home address** · **Email** · **Phone**
- **Device model & serial** · **Purchase date**

**This data is stored in their databases — databases that get breached.**

---

## Ledger: A Timeline of Breaches (2018–2026)

| Year | Incident | Impact |
|------|----------|--------|
| **2018** | Saleem Rashid: pre-setup tampering | Physical supply chain compromised |
| **2018** | Chaos Comm Congress: side-channel attacks | Lab-level key extraction possible |
| **2020** | **Major data breach** | **600K+ records: names, emails, addresses, devices** |
| **2020–21** | Targeted phishing campaigns | Personalized scams using real customer data |
| **2021** | Fake replacement devices via mail | Modified devices sent to real customers |
| **2023** | Ledger Recover controversy | Firmware CAN export key material (encrypted) |
| **2023** | Ledger Connect Kit attack | Malicious code in library used by thousands of dApps |
| **2026** | Global-e third-party breach | Names & contact details exposed again |

<span class="danger">
**8 major incidents in 8 years.** The hardware was never remotely hacked — the attack surface was always the company, its data, its software, its supply chain.
</span>

---

## The Single Point of Failure

```
┌──────────────────────────────┐
│  ┌───────────────┐           │
│  │  LEDGER INC.  │ ← Breach  │
│  │  (HQ: Paris)  │ ← 2020,   │
│  └───────┬───────┘ ← 2026    │
│  ┌───────┼───────┐ ← Phishing│
│  ▼       ▼       ▼ ← Fake    │
│ DB1    DB2    DB3 ← FW upd   │
└──────────────────────────────┘
 Every device = one company's
 entire ecosystem as trust anchor
```

<span class="danger">
One company. One HQ. One legal jurisdiction. One target for hackers, governments, and criminals.
</span>

<p style="font-size: 0.75em; color: #666; margin-top: 16px; font-style: italic;">
<strong>Disclaimer:</strong> I don't mean to rant and to gravedig Ledger only, but I conclude the reason that Ledger has the most breaches is because it's the most juicy target for bad actors. I assume that they have sold the most devices through the years, making them a prime target.
</p>

---

## The "Wrench Attack" — What Nobody Warns You About

> Proprietary wallets tie your **identity** to your **device** to your **address**.
>
> Here's the chain:

```
  Shipping data breach
       ↓
  Attacker knows: NAME + ADDRESS + "owns Ledger Nano X"
       ↓
  Your crypto holdings become PUBLIC knowledge
       ↓
  You're not a wallet address — you're a TARGET
       ↓
  Physical coercion, extortion, or theft
```

<span class="danger">
This isn't theoretical. It's documented, tracked, and accelerating.
</span>

---

## 187 Documented Physical Bitcoin Attacks (2014–2026)

*Source: [jlopp/physical-bitcoin-attacks](https://github.com/jlopp/physical-bitcoin-attacks)*

| Era | Avg/Year | Total | Trend |
|-----|----------|-------|-------|
| 2014–2017 | **3** | 13 | Early incidents |
| 2018–2021 | **12** | 50 | 4× growth |
| 2022–2024 | **18** | 54 | 6× growth |
| 2025–2026 | **35** | 70 | **12× growth** |

<span class="danger">
**35 attacks per year in 2025–2026** — up from just 3/year in the early days.
Kidnapping, torture, murder. Not phishing. Not hacks. **Physical violence.**
</span>

> ⚠️ These are only the **documented** attacks that made it to the press. The actual number is significantly higher — most incidents are never reported.

---

## The Market — Popular Proprietary Wallets

| Device | Price | SE Chip | Air-Gap | Connectivity | Coins | SE Rating |
|--------|-------|---------|---------|-------------|-------|-----------|
| NGRAVE Zero | $398 | <span class="danger">Proprietary</span> | Yes (QR) | QR only | ~1,500 | EAL7 |
| Ledger Flex | $249 | <span class="danger">Proprietary</span> | No | USB + BT + NFC | 5,500+ | CC EAL5+ |
| ELLIPAL Titan 2.0 | $169 | <span class="danger">Proprietary</span> | Yes (QR) | QR only | 10,000+ | EAL5+ |
| Ledger Nano X | $149 | <span class="danger">Proprietary</span> | No | USB + Bluetooth | 5,500+ | CC EAL5+ |
| Keystone 3 Pro | $149 | <span class="danger">Proprietary</span> | Yes (QR) | QR only | BTC + alts | EAL5+ |
| Trezor Safe 5 | $169 | <span class="warning">OPTIGA EAL6+ (certified)</span> | No | USB-C | 9,000+ | EAL6+ |
| COLDCARD Q | $249 | <span class="danger">Proprietary</span> | Yes | USB + NFC + SD | BTC only | Dual SE |
| Foundation Passport | $199 | <span class="success">ATECC608B (open)</span> | Yes | QR + SD | BTC only | ATECC608B |
| BitBox02 Bitcoin | €149 | <span class="success">ATECC608B (open)</span> | No | USB-C | BTC only | ATECC608B |
| Blockstream Jade Core | $99 | <span class="success">None (Virtual)</span> | Yes (QR) | USB + BT + cam | BTC + Liquid | Virtual SE |
| Blockstream Jade Plus | $169 | <span class="success">None (Virtual)</span> | Yes (QR) | USB + BT + cam | BTC + Liquid | Virtual SE |
| Trezor Safe 3 | $79 | <span class="warning">OPTIGA EAL6+ (certified)</span> | No | USB-C | BTC variant | EAL6+ |

<p style="font-size: 0.65em; color: #888;">
Many wallets use a proprietary Secure Element chip whose internal firmware is closed source — even if the app layer is open. The SE is where your keys live. Some (ATECC608B) are fully open; some (Trezor OPTIGA, EAL6+) are third-party certified but still closed firmware; others (EAL7, Ledger ST) are proprietary black boxes with NDAs.
</p>

---

## Transparency ≠ Open Source ≠ Game Theory

<div class="two-col">

<div>

### "Source-Available" 

- **Company owns the code** — they set the rules
- **View-only** — you can read, but not fork or modify
- **No security research** — bug bounties controlled by the vendor
- **Can be revoked** — transparency is a privilege, not a right
- **Can you verify what your device runs?** ⚠️ Hard — some vendors offer hashes

<span class="danger">This is a privilege, not a right.</span>

</div>

<div>

### True Open Source (FOSS)

- **Community owns the code** — fork, modify, redistribute
- **No permission needed** — copy, change, ship your own build
- **Security research is free** — anyone can audit and find bugs
- **No single point of control** — fork lives on even if maintainer quits
- **Peer-reviewed by default** — many eyes = many auditors

</div>

</div>

---

## Part 2: The Why

### Verifiable Security with SeedSigner


---

## No Company. No Sponsors. No Agenda.

SeedSigner because:

- **FOSS** — Free and Open Source Software. Code is open for all and anyone is free to use, study, and modify. This principle allows others to contribute to developing and improving the software like a community.
- **Community-driven** — No VC funding, no investors demanding ROI
- **No automatic updates** — No forced firmware changes from a remote server
- **No lock-in** — Uses standard BIP39/BIP32/BIP84 standards
- **No markup** — You pay component cost, not brand premium
- **No supply chain risk** — Buy parts from any retailer
- **Affordable sovereignty** — Enterprise-grade security for under $50. No brand markup. No planned obsolescence. No subscription fees.

---

## Eventually FOSS Wins — This Is the Way

**Why?**

- **People and companies die.** Open-source outlives its creators — the code persists, evolves, and endures beyond any single **lifetime**.
- **No board of directors. No shareholders.** Proprietary software is steered by profit motives and short-term vision — extract value from customers, move on. FOSS answers only to what works and what users actually need.
- **Open to be picked up by anyone.** The community takes the code forward, driven by pure end-user needs and pure engineering problems — a **vision that transcends lifetimes**.

---

## How SeedSigner Stops Wrench & Supply Chain Attacks

- **No shipping data** — parts from generic suppliers, no name or address tied to your wallet
- **No customer database** — there's no central target to breach
- **No device registration** — nobody knows you own one
- **No serial numbers** — commodity hardware, indistinguishable from any Pi Zero project
- **No supply chain** — you build it yourself, you control every step from parts to firmware
- **No firmware updates** — no OTA, no backdoors pushed remotely
- **Plausible deniability** — looks like a hobby project, not a crypto wallet
- **Stateless** — keys live in RAM only. Power off = nothing to extract

<span class="success">
No database to breach. No factory to compromise. No one knows you exist.
</span>

---

## What "Stateless" Actually Means

<div class="two-col">

<div>

### Every Other Wallet

```
┌──────────────────────┐
│  Hardware Wallet      │
│  ┌──────────────────┐ │
│  │ Flash Memory      │ │
│  │ Seed: ENC(12 words)│ │
│  │ Settings: saved   │ │
│  └──────────────────┘ │
└──────────────────────┘
         ↓
  If stolen → attacker has
  persistent seed to attack
```

</div>

<div>

### SeedSigner

```
┌──────────────────────┐
│  Raspberry Pi Zero    │
│  ┌──────────────────┐ │
│  │ RAM (volatile)    │ │
│  │ Seed: via QR code │ │
│  │ Sign → DONE       │ │
│  │ RAM: CLEARED      │ │
│  └──────────────────┘ │
└──────────────────────┘
         ↓
  If stolen → nothing to extract
  Seed lives on PAPER, not silicon
```

</div>

</div>

<span class="success">Power off = keys gone. Forever. That's stateless security.</span>

---

## Critical Difference: Where Your Keys Live

| Device | Keys Stored On Device? | Seed Persisted? | Stateless? |
|--------|------------------------|-----------------|------------|
| Ledger Nano X/Flex | ✅ Yes (SE chip) | ✅ Yes (encrypted) | ❌ No |
| Trezor Safe 3/5 | ✅ Yes (SE chip) | ✅ Yes (encrypted) | ❌ No |
| NGRAVE Zero | ✅ Yes (EAL7 SE) | ❌ No (LiTE card) | ❌ No |
| ELLIPAL Titan 2.0 | ✅ Yes (SE chip) | ✅ Yes (encrypted) | ❌ No |
| Keystone 3 Pro | ✅ Yes (SE chip) | ✅ Yes (encrypted) | ❌ No |
| COLDCARD MK4/Q | ✅ Yes (RAM + flash) | ✅ Yes (encrypted) | ❌ No |
| Foundation Passport | ✅ Yes (RAM + SE) | ✅ Yes (encrypted) | ❌ No |
| BitBox02 | ✅ Yes (ATECC608B) | ✅ Yes (encrypted) | ❌ No |
| Blockstream Jade Core | ✅ Yes (virtual SE) | ⚠️ Partial (oracle) | ❌ No |
| Blockstream Jade Plus | ✅ Yes (virtual SE) | ⚠️ Partial (oracle) | ❌ No |
| **SeedSigner** | **❌ No — RAM only** | **❌ Never stored** | **✅ YES** |

<span class="danger">Every other wallet stores your seed persistently on the device — even encrypted, it's there.</span>

---

## <span style="display:block; text-align:center;">The Trust Model</span>

<div class="two-col" style="margin-top: 10px;">

<div>
### Proprietary Wallet
<span class="danger">TRUST</span> the manufacturer

<ul style="list-style-type: disc; padding-left: 20px; text-align: left;">
<li>Trust their firmware</li>
<li>Trust their supply chain</li>
<li>Trust their cloud</li>
<li>Trust their employees</li>
</ul>
</div>

<div>
### SeedSigner
<span class="success">VERIFY</span> everything

<ul style="list-style-type: disc; padding-left: 20px; text-align: left;">
<li>Verify the code (GitHub)</li>
<li>Verify the image (SHA256)</li>
<li>Verify the transaction (on-screen)</li>
<li>Trust YOURSELF</li>
</ul>
</div>

</div>

---

## Part 3: The Build

### It's Easier Than You Think

---

## You Don't Need to Be an Engineer

SeedSigner runs on a **Raspberry Pi Zero** — one of the cheapest, most documented single-board computers ever made.

### What You Need:
- Raspberry Pi Zero 2 W (~$30)
- 1.3-inch display with buttons (~$9)
- Zero Camera Module 5MP (~$5)
- MicroSD card (~$5)
- 3D-printed case (~$7)
- Micro USB cable (~$1)

**Total: ~$57**

---

## Simple Assembly

1. **Connect** the Camera Module ribbon cable
2. **Place** the display on the Pi soldered pins
3. **Slide** it into the 3D printed case (or skip if you don't have one)
4. **Download and verify** SeedSignerOS
5. **Flash** the SD card using BalenaEtcher
6. **Ready** to plug into a power source

<span class="highlight">No soldering, not even a screw to screw.</span>

---

## Part 4: The Workflow — Step 1: Seed Setup

> SeedSigner is **stateless** — every time you power it on, it starts fresh.

```
              Do you have a seed?
                 /        \
              YES          NO
               |            |
    ┌──────────┘            └─────────────┐
    ▼                                     ▼
 Scan QR Code                        Generate Seed
    ▼                                     │
 Import Seed                           ├── Write it down
    ▼                                     │
 Export XPUB                           └── Export as SeedQR
    ▼                                     │
    └──────────→ Import XPUB ←───────────┘
                into compatible wallet
```

---

## Part 4: The Workflow — Step 2: Send Bitcoin

```
              Do you have a wallet?
                 /          \
              YES            NO
               |              |
               |        Create wallet using
               |        imported XPUB
               |              |
               |              |
               |              |
               ▼              ▼
           Create Transaction
               ▼
        Scan QR with SeedSigner
           to sign
               ▼
        Scan signed QR back
           into wallet
               │
               ▼
           Broadcast → TX sent!
```

<span class="success">
Private keys never leave SeedSigner. Communication is QR codes only — no USB, no Bluetooth, no WiFi.
</span>

---

## SeedSigner Compatibility

Compatible with any wallet that supports QR code signing:

<div style="display:flex; flex-direction:column; gap:10px; max-width:500px; margin:0 auto; font-size:1.1em;">

<div style="display:flex; align-items:center; gap:12px;">
<img src="assets/sparrow.png" width="40" height="40" style="flex-shrink:0">
<strong>Sparrow Wallet</strong><span style="color:#888; margin-left:auto;">🖥 Desktop</span>
</div>

<div style="display:flex; align-items:center; gap:12px;">
<img src="assets/specter.png" width="40" height="40" style="flex-shrink:0">
<strong>Specter Desktop</strong><span style="color:#888; margin-left:auto;">🖥 Desktop</span>
</div>

<div style="display:flex; align-items:center; gap:12px;">
<img src="assets/bluewallet.png" width="40" height="40" style="flex-shrink:0">
<strong>BlueWallet</strong><span style="color:#888; margin-left:auto;">📱 Mobile</span>
</div>

<div style="display:flex; align-items:center; gap:12px;">
<img src="assets/keeper.png" width="40" height="40" style="flex-shrink:0">
<strong>Keeper Wallet</strong><span style="color:#888; margin-left:auto;">📱 Mobile</span>
</div>

<div style="display:flex; align-items:center; gap:12px;">
<img src="assets/nunchuk.png" width="40" height="40" style="flex-shrink:0">
<strong>Nunchuk</strong><span style="color:#888; margin-left:auto;">🖥📱 Both</span>
</div>

</div>

---


## The Air-Gapped Signing Loop

```
   ┌──────────────┐
   │  SeedSigner   │  (Air-gapped, offline)
   │              │
   │  • Seed      │
   │  • Private    │
   │    Keys       │
   │  • Signing    │
   └──────┬───────┘
          │
    QR CODE (visual only)
    No data leaves the device
          │
   ┌──────▼───────┐
   │  Your Phone   │  (Online, untrusted)
   │  / Computer   │
   │              │
   │  • XPUB       │
   │  • Tx creation│
   │  • Broadcast  │
   └──────────────┘
```

---

## Part 5: Hands-On Demo

### Step-by-Step with Nunchuk

---

## Demo Step 1: Generate or Import Your Seed

**On SeedSigner:**

- Navigate to **Generate Seed**
- Choose your method:
  - 🎲 **Dice rolls** (most secure — physical entropy)
  - 📷 **Camera entropy** (capture random scenes)
  - ✍️ **Manual entry** (import existing BIP39 seed)
- **Write down your seed phrase on paper**
- Verify the seed by re-entering it

<span class="danger">This is the only time your seed exists. Protect it.</span>

---

## Demo Step 2: Import into Nunchuk

### Create a Wallet in Nunchuk using SeedSigner

1. **Open Nunchuk** — Download on iOS / Android / Desktop
2. **Add a Key:**
   - Tap **Add a Key** → **+**
   - Select **Add Air-Gapped Key**
   - Name it (e.g., "My SeedSigner")
3. **Scan XPUB:**
   - On SeedSigner: Navigate to **Export XPUB**
   - Use your phone's camera to scan the QR code
   - Nunchuk imports the public key

<span class="success">Private keys never leave the SeedSigner.</span>

---

## Demo Step 3: Create the Wallet

### Option A: Single-Sig (Simple)

- Create a new wallet in Nunchuk
- Select your imported SeedSigner key as the sole signer
- Done — you have a self-custody wallet

### Option B: Multisig (Advanced)

- Create a **2-of-3** wallet
- Add SeedSigner as **Signer 1**
- Add a second key (another SeedSigner or software key) as **Signer 2**
- Add a third key as **Signer 3** (optional)
- Save the wallet configuration (**BSMS file**) for backup

---

## Demo Step 4: Create a Transaction

### Build a Testnet Transaction

1. **Send Funds:**
   - In Nunchuk, go to your wallet → **Send**
   - Enter recipient address (use a testnet faucet address)
   - Enter amount and fee
2. **Review:**
   - Check transaction details carefully
   - Tap **Continue** to proceed to signing

---

## Demo Step 5: Sign with SeedSigner

### The Air-Gapped Signature

1. **Export PSBT:**
   - In Nunchuk, tap **Sign** next to your SeedSigner key
   - Nunchuk displays a **Dynamic QR Code** (Partially Signed Bitcoin Transaction)
2. **Scan with SeedSigner:**
   - On SeedSigner, go to **Sign Transaction**
   - Scan the Dynamic QR Code from your phone screen
3. **Verify & Sign:**
   - SeedSigner displays: **To, Amount, Fee**
   - Review carefully — this is your moment of truth
   - Press the button to **Sign**
   - SeedSigner displays the **Signed Transaction QR Code**

---

## Demo Step 6: Broadcast

### Finalize the Transaction

1. **Import Signature:**
   - Go back to Nunchuk
   - Tap **Import Signature**
   - Scan the Signed QR Code from the SeedSigner screen
2. **Broadcast:**
   - Nunchuk confirms the signature
   - Tap **Broadcast Transaction**
   - Wait for confirmation on the blockchain explorer

<span class="success">Transaction complete. Your private key never touched the internet.</span>

---

## Part 6: Why This Matters

### The Result

---

## What You Just Accomplished

### ✅ You Controlled the Keys
Your private key never touched the internet-connected phone or computer. It existed only on the SeedSigner, in RAM, during signing.

### ✅ You Verified the Code
You used open-source tools (SeedSigner + Nunchuk) where the logic is transparent, auditable, and community-reviewed.

### ✅ You Avoided Custody
No exchange can freeze your funds. No company can block your transactions. You are your own bank.

---

## The Bigger Picture

```
Proprietary Wallet          SeedSigner
─────────────────           ───────────
Company controls firmware   You verify the code
Company has your data       No data collection
Company can OTA update      Stateless boot from RAM
Company can be subpoenaed   No company to subpoena
Expensive ($79-$259)        Affordable (~$50)
Single point of failure     Modular, repairable
```

---

## Part 7: Multisig with QR Codes

### The Cheapest Multisig Setup Ever

---

## Why Multisig?

Single-sig = one seed phrase = one point of failure.

Multisig = multiple keys = distributed trust.

**A 2-of-3 multisig means:**
- Any 2 of 3 keys can sign a transaction
- Lose 1 key? Still fine.
- 1 key compromised? Still safe.
- No single person has full control.

---

## The Cheapest Multisig Ever

### Three SeedSigners = ~$150 total

```
┌─────────────┐  ┌─────────────┐  ┌─────────────┐
│ SeedSigner 1 │  │ SeedSigner 2 │  │ SeedSigner 3 │
│  (Home)      │  │  (Safe)      │  │  (Travel)    │
│  $50         │  │  $50         │  │  $50         │
└─────────────┘  └─────────────┘  └─────────────┘
       │                 │                 │
       └────────┬────────┘─────────────────┘
                │
         2-of-3 Multisig Wallet
         Any 2 keys sign transactions
```

<span class="success">Compare: Ledger Trezor Model T × 3 = ~$777</span>

---

## QR Code Multisig Workflow

Each SeedSigner generates its own seed and XPUB via QR codes:

1. **SeedSigner 1** → Generate seed → Export XPUB (QR) → Scan into Nunchuk
2. **SeedSigner 2** → Generate seed → Export XPUB (QR) → Scan into Nunchuk
3. **SeedSigner 3** → Generate seed → Export XPUB (QR) → Scan into Nunchuk
4. **Create 2-of-3 wallet** in Nunchuk with all three XPUBs
5. **To sign:** Scan PSBT with SeedSigner 1 → Sign → Scan signature with SeedSigner 2 → Sign → Broadcast

<span class="highlight">All communication via QR codes. Zero internet on any signer.</span>

---

## Physical Security Strategy

| Signer | Location | Purpose |
|--------|----------|---------|
| **SeedSigner 1** | Home desk | Daily transactions |
| **SeedSigner 2** | Safe deposit box | Backup / emergency |
| **SeedSigner 3** | Travel / separate location | Redundancy |

<span class="success">
Lose any one? Your funds are still safe.
Need two attackers to compromise different locations? That's real security.
</span>

---

## Comparison: Multisig Cost Analysis

| Setup | Cost | Verifiable | Air-Gapped |
|-------|------|-----------|------------|
| 3× Trezor Model T | ~$777 | ❌ | ⚠️ USB |
| 3× Ledger Stax | ~$987 | ❌ | ❌ NFC/USB |
| **3× SeedSigner** | **~$150** | ✅ | ✅ QR |
| Professional multisig service | $500+/yr | ❌ | ❌ |

<span class="success">SeedSigner: 80% cheaper, 100% more transparent.</span>

---

## Summary

### What You've Learned Today

1. **Proprietary wallets are black boxes** — you can't verify what's inside
2. **Shipping data is a liability** — it enables targeted attacks
3. **SeedSigner is open source** — every line is auditable
4. **Air-gapped via QR codes** — private keys never touch the internet
5. **Stateless & verifiable** — boots from RAM, you verify the image
6. **Under $50 per device** — sovereignty shouldn't be expensive
7. **Multisig is affordable** — 3 SeedSigners for ~$150

---

## Next Steps

### After This Workshop

- ✅ **Build your SeedSigner** — Parts list available online
- ✅ **Generate your first seed** — Use dice rolls for maximum entropy
- ✅ **Set up Nunchuk** — Connect your XPUB
- ✅ **Practice on testnet** — Sign a test transaction before going live
- ✅ **Build a multisig** — Add a second or third SeedSigner for real security

### Resources
- SeedSigner GitHub: `github.com/SeedSigner/seedsigner_os`
- Nunchuk: `nunchuk.com`
- Bitcoin Whitepaper: `bitcoin.org`

---

## Thank You

### Be Your Own Bank.

<span class="emoji">🛡️</span> Build it yourself. <span class="emoji">🔍</span> Verify everything. <span class="emoji">🔑</span> Trust nothing.
