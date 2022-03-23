# Aceitar pedido

Quando o status da entrega retornar **Ready_to_ship** você poderá realizar o aceite do pedido.

Para aceitar o pedido que foi confirmado no PDV/POS, realize um PUT enviando o `shipment_id` e o `access-token` (gerado pelo processo de autenticação do OAuth) ao endpoint [/proximity-integration/shipments/{shipment_id}/accept](https://www.mercadopago[FAKER][URL][DOMAIN]/developers/pt/reference/mp_delivery/_proximity-integration_shipments_shipment_id_accept/put). Veja [Segurança](https://www.mercadopago[FAKER][URL][DOMAIN]/developers/pt/guides/security/oauth/introduction) para mais informações sobre OAuth.

Ao aceitar o pedido, o status será alterado e no response será indicado o novo status do pedido.

> NOTE
>
> Importante
>
> É importante saber que apenas nos estados **ready_to_ship** e **ready_to_print** é possível aceitar um pedido. Após aceitar o pedido, o substatus passará a ser “printed”. Caso o pedido não seja aceito 5 minutos após a sua criação, o mesmo será cancelado automaticamente.  

> NEXT_STEP_CARD_PT
>
> Imprimir comprovante do pedido
>
> Saiba como imprimir o comprovante dos pedidos com o Mercado Pago Delivery.
>
> [Imprimir comprovante do pedido](https://www.mercadopago[FAKER][URL][DOMAIN]/developers/pt/guides/mp-delivery/print-order-receipt)