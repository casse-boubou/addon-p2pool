# Home Assistant Add-on: P2pool

[![GitHub Release][releases-shield]][releases]
[![License][license-shield]](LICENSE)

![Supports aarch64 Architecture][aarch64-shield]

[P2pool][p2pool] est un pool decentralisé pour le minage de cryptomonnaie monero.

Les pages d'états et de surveillance du pool sont disponible sur <https://p2pool.io>,
<https://p2pool.observer> ou <https://p2pool.io/mini>, <https://mini.p2pool.observer>

[![Open your Home Assistant instance and show the add add-on repository dialog
with a specific repository URL pre-filled.][add-repo-shield]][add-repo]
[![Open your Home Assistant instance and show the dashboard of a Supervisor add-on.][add-addon-shield]][add-addon]

## About

- Pour miner sur P2Pool, un nœud Monero synchronisé utilisant monerod v0.18.0.0 ou
  plus récent est requis. Si vous n'en avez pas actuellement, vous pouvez utiliser
  mon autre [addon Monerod][monerod] pour HomeAssistant. Ou télécharger les fichiers
  binaires officiels de Monero, [démarrer monerod sur votre PC][moneronode] et attendre
  qu'il soit entièrement synchronisé.
- Vous devez utiliser une primary wallet address pour le minage. Les subaddresses
  et les integrated addresses ne sont pas prises en charge, tout comme avec l'extraction
  en solo de monerod.
  Il est fortement recommandé de créer un nouveau portefeuille principal pour le
  minage P2Pool car les adresses de portefeuille sont publiques sur P2Pool.
- Vérifiez que les ports 18080 (Monero p2p port) et 37889/37888 (P2Pool/P2Pool mini
  p2p port) sont ouverts dans votre pare-feu pour assurer une meilleure connectivité.
  Si vous exploitez un ordinateur derrière NAT (comme un routeur), vous pouvez envisager
  de transférer les ports vers votre ordinateur local.
- Vous pouvez connecter plusieurs mineurs au même nœud P2Pool. Plus il y en a,
  mieux c'est !

## Support

Je ne suis pas dévellopeur, n'ai aucune formation de code, je suis simplement
autodidact.
Si vous avez une question concernant HA et ses add-ons vous pouvez consulter:

- [Le Forum communautaire francophone][hacf] de HomeAssistant
- [Le Forum communautaire anglophone][forum] de HomeAssistant.
- [Le serveur Discord][discord-ha] de HomeAssistant.

## License

MIT License

Copyright (c) 2023 [Frosch][frosch]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

> **_Parts of the project are originally Copyright (c) 2023, [SChernykh][p2poolauthor],
> distributed under [GNU General Public License v3.0][p2poollicense]:_**
>
> > _1. This program is free software: you can redistribute it and/or modify it under
> > the terms of the GNU General Public License as published by the Free Software
> > Foundation, either version 3 of the License, or (at your option) any later version._
> >
> > _2. This program is distributed in the hope that it will be useful,
> > but WITHOUT ANY WARRANTY; without even the implied warranty of
> > MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
> > GNU General Public License for more details._
> >
> > _3. You should have received a copy of the GNU General Public License
> > along with this program. If not, see <https://www.gnu.org/licenses>._

[add-addon]: https://my.home-assistant.io/redirect/supervisor_addon/?addon=c751e21a_p2pool
[add-addon-shield]: https://my.home-assistant.io/badges/supervisor_addon.svg
[add-repo]: https://my.home-assistant.io/redirect/supervisor_add_addon_repository/?repository_url=https%3A//github.com/erdnaxela02/hassio-addons
[add-repo-shield]: https://my.home-assistant.io/badges/supervisor_add_addon_repository.svg
[releases]: https://github.com/erdnaxela02/addon-p2pool/releases
[releases-shield]: https://img.shields.io/github/v/release/erdnaxela02/addon-p2pool
[license-shield]: https://img.shields.io/github/license/erdnaxela02/addon-p2pool
[aarch64-shield]: https://img.shields.io/badge/aarch64-yes-green.svg
[p2pool]: https://github.com/SChernykh/p2pool
[monerod]: https://github.com/erdnaxela02/addon-monerod
[moneronode]: https://sethforprivacy.com/guides/run-a-monero-node-advanced/
[discord-ha]: https://discord.gg/c5DvZ4e
[forum]: https://community.home-assistant.io
[hacf]: https://forum.hacf.fr/
[frosch]: https://github.com/erdnaxela02
[p2poolauthor]: https://github.com/SChernykh
[p2poollicense]: https://github.com/SChernykh/p2pool/blob/master/LICENSE
