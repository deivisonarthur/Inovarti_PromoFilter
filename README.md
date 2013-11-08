Inovarti_PromoFilter
====================

Módulo permite que você ative ou desative os métodos de pagamento e transporte do checkout criando regras de promoção

Por exemplo: Você pode habilitar o modulo Cielo somente para os produtos de determinada categoria, ou desabilitar o frete gratis para envios fora de sua cidade.
Como usar: Após a instalação limpe o cache e visite o item de menu na administração do Magento, em

"Promoções" => "Regras no Checkout"

Testado Magento 1.7.2

Gostou do módulo? Faça uma doação ao projeto
====================

Pesquisando na web encontrei 2 módulo que somando seus valores somam 200 usd rs

http://amasty.com/payment-restrictions.html
http://amasty.com/shipping-rules.html

Se você gostou, se foi útil para você, se fez você economizar aquela grana pois estava prestes a pagar caro por aquele módulo pago, pois não achava um solução gratuita que te atendesse e queira prestigiar o trabalho feito efetuando uma doação de qualquer valor, não vou negar e vou ficar grato, você pode fazer isso utilizando o Pagseguro para o email 2ds@deivison.com.br

Atualizações futuras
====================

Adicionar promoção para parcelas nos cartões, por exem 15% desconto para pagamento em 1x no cartão

Exeplo de uso da regra www.leoeletro.com.br possui descontos de 15% em 1x

Ou seja vou implementar o script abaixo para dar o desconto no quote collect total after ao verificar qual meio de pagamento foi selecionado e qual numero de parcelas, assim se pode criar regras para parcelas.


$discountAmount = $total * $discountAmount / 100;

$info->getQuote()->setSubtotalWithDiscount($discountAmount);

$info->getQuote()->setBaseSubtotalWithDiscount($discountAmount);

$discountAmountDescription ="Desconto ".$discountAmount."%";

$address->setDiscountDescription($address->getDiscountDescription() . ','.$discountAmountDescription);

