# novaposhta 0.3.0

## Instalation

You can add this package using following commands:

```
npm i novaposhta_3
```

```
yarn add novaposhta_3
```

## Usage

Basic example:

```javascript
import NovaPoshta from 'novaposhta_3';

const api = new NovaPoshta({ apiKey: '...' });

api.address.getCities({ Ref: "ebc0eda9-93ec-11e3-b441-0050568002cf" }).then((json) => {
    // do something
});
```

Winston Logger:

```javascript
import NovaPoshta from 'novaposhta_3';
import Winston from 'winston';
import WinstonFormatter from 'winston-console-formatter';

const winstonLogger = new Winston.Logger({ level: "debug" });
winstonLogger.add(Winston.transports.Console, WinstonFormatter.config());

const api = new NovaPoshta({
    apiKey: '...',
    logger: winstonLogger,
});

api.address.getCities({ Ref: "ebc0eda9-93ec-11e3-b441-0050568002cf" }).then((json) => {
	// do something
});
```

## Supported Methods

### Address

```javascript
const api = new NovaPoshta({ apiKey: '...' });

api.address.getCities({ Ref: "ebc0eda9-93ec-11e3-b441-0050568002cf" }).then((json) => {
    // do something
});
```

- [searchSettlements](https://devcenter.novaposhta.ua/docs/services/556d7ccaa0fe4f08e8f7ce43/operations/58e5ebeceea27017bc851d67)
- [searchSettlementStreets](https://devcenter.novaposhta.ua/docs/services/556d7ccaa0fe4f08e8f7ce43/operations/58e5f369eea27017540b58ac)
- [update](https://devcenter.novaposhta.ua/docs/services/556d7ccaa0fe4f08e8f7ce43/operations/556d9db5a0fe4f08e8f7ce4b)
- [save](https://devcenter.novaposhta.ua/docs/services/556d7ccaa0fe4f08e8f7ce43/operations/556d9925a0fe4f08e8f7ce4a)
- [getAreas](https://devcenter.novaposhta.ua/docs/services/556d7ccaa0fe4f08e8f7ce43/operations/556d9130a0fe4f08e8f7ce48)
- [getCities](https://devcenter.novaposhta.ua/docs/services/556d7ccaa0fe4f08e8f7ce43/operations/556d885da0fe4f08e8f7ce46)
- [getSettlements](https://devcenter.novaposhta.ua/docs/services/556d7ccaa0fe4f08e8f7ce43/operations/56248fffa0fe4f0da0550ea8)
- [getWarehouses](https://devcenter.novaposhta.ua/docs/services/556d7ccaa0fe4f08e8f7ce43/operations/556d8211a0fe4f08e8f7ce45)
- [getWarehouseTypes](https://devcenter.novaposhta.ua/docs/services/556d7ccaa0fe4f08e8f7ce43/operations/556d8211a0fe4f08e8f7ce45)
- [getStreet](https://devcenter.novaposhta.ua/docs/services/556d7ccaa0fe4f08e8f7ce43/operations/556d8db0a0fe4f08e8f7ce47)
- [delete](https://devcenter.novaposhta.ua/docs/services/556d7ccaa0fe4f08e8f7ce43/operations/556da062a0fe4f08e8f7ce4c)

### Common

```javascript
const api = new NovaPoshta({ apiKey: '...' });

api.common.getTimeIntervals({ "RecipientCityRef": "8d5a980d-391c-11dd-90d9-001a92567626" }).then((json) => {
    // do something
});
```

- [getTimeIntervals](https://devcenter.novaposhta.ua/docs/services/55702570a0fe4f0cf4fc53ed/operations/55702571a0fe4f0b6483890f)
- [getCargoTypes](https://devcenter.novaposhta.ua/docs/services/55702570a0fe4f0cf4fc53ed/operations/55702571a0fe4f0b64838909)
- [getBackwardDeliveryCargoTypes](https://devcenter.novaposhta.ua/docs/services/55702570a0fe4f0cf4fc53ed/operations/55702571a0fe4f0b64838907)
- [getPalletsList](https://devcenter.novaposhta.ua/docs/services/55702570a0fe4f0cf4fc53ed/operations/5824774ba0fe4f0e60694eb0)
- [getTypesOfPayers](https://devcenter.novaposhta.ua/docs/services/55702570a0fe4f0cf4fc53ed/operations/55702571a0fe4f0b64838913)
- [getTypesOfPayersForRedelivery](https://devcenter.novaposhta.ua/docs/services/55702570a0fe4f0cf4fc53ed/operations/55702571a0fe4f0b64838914)
- [getPackList](https://devcenter.novaposhta.ua/docs/services/55702570a0fe4f0cf4fc53ed/operations/582b1069a0fe4f0298618f06)
- [getTiresWheelsList](https://devcenter.novaposhta.ua/docs/services/55702570a0fe4f0cf4fc53ed/operations/55702571a0fe4f0b64838910)
- [getCargoDescriptionList](https://devcenter.novaposhta.ua/docs/services/55702570a0fe4f0cf4fc53ed/operations/55702571a0fe4f0b64838908)
- [getMessageCodeText](https://devcenter.novaposhta.ua/docs/services/55702570a0fe4f0cf4fc53ed/operations/58f0730deea270153c8be3cd)
- [getServiceTypes](https://devcenter.novaposhta.ua/docs/services/55702570a0fe4f0cf4fc53ed/operations/55702571a0fe4f0b6483890e)
- [getTypesOfCounterparties](https://devcenter.novaposhta.ua/docs/services/55702570a0fe4f0cf4fc53ed/operations/55702571a0fe4f0b64838912)
- [getPaymentForms](https://devcenter.novaposhta.ua/docs/services/55702570a0fe4f0cf4fc53ed/operations/55702571a0fe4f0b6483890d)
- [getOwnershipFormsList](https://devcenter.novaposhta.ua/docs/services/55702570a0fe4f0cf4fc53ed/operations/55702571a0fe4f0b6483890b)

### Counterparty

```javascript
const api = new NovaPoshta({ apiKey: '...' });

api.counterparty.getCounterpartyContactPerson({ ... }).then((json) => {
    // do something
});
```

- [getCounterpartyAddresses](https://devcenter.novaposhta.ua/docs/services/557eb8c8a0fe4f02fc455b2d/operations/557fdcb4a0fe4f105c087611)
- [getCounterpartyOptions](https://devcenter.novaposhta.ua/docs/services/557eb8c8a0fe4f02fc455b2d/operations/55801976a0fe4f105c087614)
- [getCounterpartyContactPerson](https://devcenter.novaposhta.ua/docs/services/557eb8c8a0fe4f02fc455b2d/operations/557fe424a0fe4f105c087612)
- [getCounterparties](https://devcenter.novaposhta.ua/docs/services/557eb8c8a0fe4f02fc455b2d/operations/557fd789a0fe4f105c08760f)
- [saveCounterparty](https://devcenter.novaposhta.ua/docs/services/557eb8c8a0fe4f02fc455b2d/operations/557ebbd3a0fe4f02fc455b2e)
- [updateCounterparty](https://devcenter.novaposhta.ua/docs/services/557eb8c8a0fe4f02fc455b2d/operations/557fbe62a0fe4f105c08760d)
- [deleteCounterparty](https://devcenter.novaposhta.ua/docs/services/557eb8c8a0fe4f02fc455b2d/operations/557fd35da0fe4f105c08760e)
- [saveContactPerson](https://devcenter.novaposhta.ua/docs/services/557eb8c8a0fe4f02fc455b2d/operations/55828c4ca0fe4f0adc08ef27)
- [updateContactPerson](https://devcenter.novaposhta.ua/docs/services/557eb8c8a0fe4f02fc455b2d/operations/558297aca0fe4f0adc08ef28)
- [deleteContactPerson](https://devcenter.novaposhta.ua/docs/services/557eb8c8a0fe4f02fc455b2d/operations/55829aa2a0fe4f0adc08ef29)

### Internet Document

```javascript
const api = new NovaPoshta({ apiKey: '...' });

api.document.getDocumentList({ ... }).then((json) => {
    // do something
});
```

- [getDocumentList](https://devcenter.novaposhta.ua/docs/services/556eef34a0fe4f02049c664e/operations/557eb417a0fe4f02fc455b2c)
- [getDocumentDeliveryDate](https://devcenter.novaposhta.ua/docs/services/556eef34a0fe4f02049c664e/operations/558153cca0fe4f12149812a1)
- [getDocumentPrice](https://devcenter.novaposhta.ua/docs/services/556eef34a0fe4f02049c664e/operations/55702ee2a0fe4f0cf4fc53ef)
- [getStatusDocuments](https://devcenter.novaposhta.ua/docs/services/557eb8c8a0fe4f02fc455b2d/operations/557fd789a0fe4f105c08760f)
- [saveInternetDocument](https://devcenter.novaposhta.ua/docs/services/556eef34a0fe4f02049c664e/operations/556ef753a0fe4f02049c664f)
- [updateInternetDocument](https://devcenter.novaposhta.ua/docs/services/556eef34a0fe4f02049c664e/operations/55701ec2a0fe4f0cf4fc53eb)
- [deleteInternetDocument](https://devcenter.novaposhta.ua/docs/services/556eef34a0fe4f02049c664e/operations/55701fa5a0fe4f0cf4fc53ec)
- [generateReport](https://devcenter.novaposhta.ua/docs/services/556eef34a0fe4f02049c664e/operations/55815af6a0fe4f12149812a2)


## Contribute

What to help or have a suggestion? Open a [new ticket](https://github.com/eugene-manuilov/novaposhta/issues/new) and we can discuss it or submit pull request. Please, make sure you run `npm test` before submitting a pull request.

## License

MIT
