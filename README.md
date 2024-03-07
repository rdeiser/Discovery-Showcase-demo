Ex Libris Documentation: https://developers.exlibrisgroup.com/blog/primo-showcase-how-to-embed/

Ex Libris source Git Repository:  https://github.com/ExLibrisGroup/Discovery-Showcase


| The following modifications were made to the source `Discovery-Showcase/src/pnx-card.ts` file starting on line `41`      |
| ------------- |
```typescript
            <a  href="${this.getDeeplink()}" target="_blank" aria-label="">
                ${until(imgPromise, imagePlaceHolder)}
                <div class="record-details">
                    <h2>${this?.doc?.pnx?.display?.title?.[0] ?? ''}</h2>
                    <span>${this?.doc?.pnx?.sort?.author?.[0] ?? ''}</span><br> <!-- This line was added to display author/creator if available in the PNX record  -->
                    <span>${this?.doc?.pnx?.display?.publisher?.[0] ?? ''}--${this?.doc?.pnx?.display?.creationdate?.[0] ?? ''}</span> <!-- Appended the publisher data with a 2-em dash and the publication date if available in the PNX record  -->
                </div>
            </a>

```
