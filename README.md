# chessops

[![Test](https://github.com/lichess-org/chessops/workflows/Test/badge.svg)](https://github.com/lichess-org/chessops/actions)
[![npm](https://img.shields.io/npm/v/chessops)](https://www.npmjs.com/package/chessops)

Chess and chess variant rules and operations in TypeScript.

## Documentation

[View TypeDoc](https://lichess-org.github.io/chessops/)

## Features

- [Read and write FEN](https://lichess-org.github.io/chessops/modules/fen.html)
- Vocabulary (Square, SquareSet, Color, Role, Piece, Board, Castles, Setup,
  Position)
- [Variant rules](https://lichess-org.github.io/chessops/modules/variant.html): Standard chess, Crazyhouse, King of the Hill, Three-check,
  Antichess, Atomic, Horde, Racing Kings
  - Move making
  - Legal move and drop move generation
  - Game end and outcome
  - Insufficient material
  - Setup validation
- Supports Chess960
- [Attacks and rays](https://lichess-org.github.io/chessops/modules/attacks.html) using hyperbola quintessence
- Read and write UCI move notation
- [Read and write SAN](https://lichess-org.github.io/chessops/modules/san.html)
- [Position hashing](https://lichess-org.github.io/chessops/modules/hash.html)
- [Transformations](https://lichess-org.github.io/chessops/modules/transform.html): Mirroring and rotating
- [Compatibility](https://lichess-org.github.io/chessops/modules/compat.html): [chessground](https://github.com/ornicar/chessground) and [scalachess](https://github.com/ornicar/scalachess)

[File an issue](https://github.com/lichess-org/chessops/issues/new) to request more.

## Example

```javascript
import { parseFen } from 'chessops/fen';
import { Chess } from 'chessops/chess';

const setup = parseFen('r1bqkbnr/ppp2Qpp/2np4/4p3/2B1P3/8/PPPP1PPP/RNB1K1NR b KQkq - 0 4').unwrap();
const pos = Chess.fromSetup(setup).unwrap();
console.assert(pos.isCheckmate());
```

## License

chessops is licensed under the GNU General Public License 3 or any later
version at your choice. See LICENSE.txt for details.
