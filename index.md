---

layout: ribbon

style: |

    #Cover h2 {
        margin:30px 0 0;
        color:#FFF;
        text-align:center;
        font-size:70px;
        }
    #Cover p {
        margin:10px 0 0;
        text-align:center;
        color:#FFF;
        font-style:italic;
        font-size:20px;
        }
        #Cover p a {
            color:#FFF;
            }
    #Picture h2 {
        color:#FFF;
        }
    #SeeMore h2 {
        font-size:100px
        }
    #SeeMore img {
        width:0.72em;
        height:0.72em;
        }
---

# Cloud development paradigm {#Cover}

*David Kubec@[vsechnovcloudu.cz](http://vsechnovcloudu.cz/) powered by [Jekyller](https://github.com/shower/jekyller)*

![](img/corpident/cover.jpg)

## Pic
{:.cover #Picture}

![](pictures/slide_9.jpg)

## Cloud = neomezené škálování {#cloud}
Pronájem zdrojů misto jejich vlastnění.  
Poskytovatel cloudu přidává hardware rychleji, než jejich zákazníci konzumují.  
Služby managované cloud providerem zásadně zjednodušují a zrychlují procesy.  

## Automatizace {#automation}

![](pictures/giphy.gif)

## Atomické zpracování dat {#atomic}

Místo jednolitého monolitu pro pevně daný počet uživatelů...  
... budujeme proces přesně pro *jednoho uživatele* - a cloud škáluje za nás.

## Úroveň abstrakce {#abstraction}

1. …Hardware ... díky cloudu "jakobychom neměli hardware"
2. …Operační systém ... díky kontajnerům "jakobychom neměli operační systém".
3. …Server ... "server less" = "jakobychom neměli server".
4. …**Aplikace + konfigurace** ( = to jediné, co nás vlastně zajímá)

## Infrastruktura už není tím, čím bývala {#server}

![](pictures/server.jpg)

## Všechno je software! {#software}

    resource "aws_instance" "web" {
      ami           = "${data.aws_ami.ubuntu.id}"
      instance_type = "t2.micro"
      subnet_id     = "${var.SUBNET}"

      tags {
        Name = "My server"
      }
    }

## Trade off

Používání cloudu dělá naše životy pohodlnější

## Cena

Cloud není levný!  
Pokud k němu přistupujete, jako k "jinému" datacentru, proděláte kalhoty.  
Začít v malém je základ.  

## Bezpečnost a soukromí

Šifrování, jako výchozí stav.  
Globální kontrola nad veškerými zdroji v cloudu.  
