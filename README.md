Inovarti_PromoFilter
====================

Módulo permite que você ative ou desative os métodos de pagamento e transporte do checkout criando regras de promoção

Por exemplo: Você pode habilitar o modulo Cielo somente para os produtos de determinada categoria, ou desabilitar o frete gratis para envios fora de sua cidade.
Como usar: Após a instalação limpe o cache e visite o item de menu na administração do Magento, em

"Promoções" => "Regras no Checkout"

Testado Magento 1.7.2

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

