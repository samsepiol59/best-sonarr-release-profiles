# best-sonarr-release-profiles
Optimised Sonarr Release Profiles

## The profiles
Let's start with the negatives, the "must not contain list"
> /(x|h).?265/i,/hevc|hecv/i,/2160p/i,/4k/i,/DVD9|DVD5/i,/1080i/i,/upscale/i,/megusta/i,/VOSTFR/i,/-nl/i,/bluray(?!.*(-EPSiLON|-FraMeSToR|-kralimarko|-NTb|-BTN|-DON|-VIETHD|-EBP|-HAB|-DECIBEL|-D-Z0N3|-FORM|-CTRLHD|-HIFI|-HDMANIACS|-HIDT|-CRISC|-TAYTO|-THORA|-LORD|-SA89|-SBR|-MAG|-HDB|-iNK|-BMF|-TDD|-ZQ|-LolHD|-Ncmt))/i

With that out of the way, let's move to the real profiles - the streaming sources
- /amzn|amazon/i +300
- /\.nf|netflix/i +200
- /DNSP|ATVP/i +180
- /DNSY|DISNEY/i +160
- /-DEFLATE|-INFLATE/i +140
- /hulu|\.hbo\./i +120
- /(\.iT|iTunes)\.web.?(dl|rip)/i +100

Qualities
- /1080p/i +250
- /720p/i +50
- /720p\.ip\./i +50
- /576p/i +20
- /480p/i +10

Sources
- /blu.?ray/i +950
- /remux/i +500
- /web.?dl/i +250
- /web.?rip/i +200
- /HDTV/i +60
- /DVDRip/i +30

Release Groups for most files
- /NTb|BTN/i +200
- /AJP69/i +180
- /CasStudio|NTG|KiNGS/i +160
- /RTN|ViSUM|TEPES|TrollHD|monkee|MZABI|SiGMA|QOQ|CtrlHD/i +140
- /iTOONZ|caffeine|-DEEP|BTW|SA89|iJP|-LAZY|TVSmash/i +120
- /AMCON|MEMENTO|METCON/i +100
- /CHX|XLF/i +90
- /-STARZ|AMRAP|-TRUMP|STRiFE/i +80
- /-TBS|DCU/i +70
- /NOGRP/i +60
- /-GHOSTS|-ROBOTS/i +50
- /REPACK3/i +3
- /REPACK2/i +2
- /REPACK|PROPER/i +1

Release Groups for BLURAY/REMUX
- /EPSiLON|FraMeSToR/i +300
- /-decibel/i +260
- /kralimarko/i +240
- /-LORD/i +220
- /-DON/i +220
- /-EBP/i +220
- /-D-Z0N3/i +220
- /-BMF/i +220
- /-Ncmt/i +220
- /-VietHD/i +220
- /-HDB/i +220
- /-HIDT/i +200
- /-HDMANIACS/i +200
- /-HAB/i +200
- /-THORA/i +200
- /-SBR/i +200
- /-MAG/i +200
- /-iNK/i +200
- /-TDD/i +200
- /-CRISC/i +200
- /-TAYTO/i +200
- /-LolHD/i +200

Release Groups HDTV/DVD
- /-CBFM/i +100
- /-fqm/i +100
- /-qpel/i +100
- /-MTB/i +100
- /-W4F/i +100
- /-CRiMSON/i +100
- /-cct/i +100
- /-orenji/i +100
- /-LiNKLE/i +100
- /Cherzo/i +80
- /ACES/i +60
- /KETTLE/i +60
- /DEADPOOL/i +60
- /LucidTV/i +60
- /mSD/i +40
- /AVS/i +40
- /SVA/i +40
- /SPRiNTER/i +20
- /HANDJOB/i +20
- /HAGGiS/i +20
- /PFa/i +20
- /ION10/ +20

Now some minuses - although you might want to add these to the "must not contain list" too, depends on your preference
- /internal/i -10
- /\.MULTI\./i -50
- /RARTV|EZTV|TGx/i -1500
- /AsRequested|BUYMORE/i -1500
- /obfuscated|postbot|rakuv/i -1500
- /scrambled|whiterev/i -1500

Now the interesting part - I will add three bluray scores to level the ratings, plus four webrips - these particular webrips are all ripped from a 4K source, so they're preferable even to the 1080p amzn webdl ntb!
- /(\.nf|netflix).+webrip.+(NTb|BTN)/i +200
- /(\.nf|netflix).+webrip.+AJP69/i +195
- /(amzn|amazon).+webrip.+(NTb|BTN)/i +150
- /(amzn|amazon).+webrip.+AJP69/i +145
- /blu.?ray.+SA89/i +100
- /blu.?ray.+(NTb|BTN)/i +80
- /blu.?ray.+CtrlHD/i +80
