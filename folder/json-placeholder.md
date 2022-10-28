# example

```json
fetch('https://jsonplaceholder.typicode.com/posts', {
        method: 'POST',
        body: JSON.stringify({
          totalCount: 1,
          lists: [
            {
              requestDate: '2022-10-27',
              processingDate: '2022-10-27',
              cpassID: 'khr157929@quagga.ai',
              storeID: 'khr157929',
              orderName: 'QUAGGA',
              currency: '$',
              price: '20',
              state: 'Request',
              coin: 'BTC',
              amount: '20',
              settlementAmount: '20',
              addr: 'bc1qgmds8lw9s8uw56lah352fmsgvlyalv7pj21svy',
              confirmationNumber: 1,
            },
          ],
        }),
        headers: {
          'Content-type': 'application/json; charset=UTF-8',
        },
      })
        .then((response) => response.json())
        .then((json) => {
          delete json.id, commit('SET_ENTERPRISE_PAYMENT_HISTORY_PUSH', json);
        });

```
