---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayprobeconfig
schema: 2.0.0
ms.openlocfilehash: 39ce61f4a1e973dfdac8104a6364bdd3d8b9151a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866863"
---
# <span data-ttu-id="a5cd6-101">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a5cd6-101">Remove-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="a5cd6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a5cd6-102">SYNOPSIS</span></span>
<span data-ttu-id="a5cd6-103">Rimuove una sonda di integrità da un gateway applicazione esistente.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-103">Removes a health probe from an existing application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5cd6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a5cd6-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5cd6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a5cd6-105">DESCRIPTION</span></span>
<span data-ttu-id="a5cd6-106">Il cmdlet Remove-AzureRmApplicationGatewayProbeConfig consente di rimuovere una sonda di integrità da un gateway applicazione esistente.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-106">The Remove-AzureRmApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="a5cd6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a5cd6-107">EXAMPLES</span></span>

### <span data-ttu-id="a5cd6-108">Esempio 1: rimuovere una sonda di integrità da un gateway applicazione esistente</span><span class="sxs-lookup"><span data-stu-id="a5cd6-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="a5cd6-109">Questo comando rimuove la sonda di integrità denominata Probe04 dal gateway dell'applicazione denominata gateway.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="a5cd6-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a5cd6-110">PARAMETERS</span></span>

### <span data-ttu-id="a5cd6-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a5cd6-111">-ApplicationGateway</span></span>
<span data-ttu-id="a5cd6-112">Specifica il gateway dell'applicazione a cui questo cmdlet rimuove un probe.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5cd6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5cd6-113">-DefaultProfile</span></span>
<span data-ttu-id="a5cd6-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5cd6-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="a5cd6-115">-Name</span></span>
<span data-ttu-id="a5cd6-116">Specifica il nome del probe per cui viene rimosso questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-116">Specifies the name of the probe for which this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5cd6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5cd6-117">CommonParameters</span></span>
<span data-ttu-id="a5cd6-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5cd6-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5cd6-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5cd6-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a5cd6-120">INPUTS</span></span>

### <span data-ttu-id="a5cd6-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a5cd6-121">PSApplicationGateway</span></span>
<span data-ttu-id="a5cd6-122">Il parametro ' ApplicationGateway ' accetta il valore di tipo ' PSApplicationGateway ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="a5cd6-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="a5cd6-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a5cd6-123">OUTPUTS</span></span>

### <span data-ttu-id="a5cd6-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a5cd6-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a5cd6-125">Note</span><span class="sxs-lookup"><span data-stu-id="a5cd6-125">NOTES</span></span>

## <span data-ttu-id="a5cd6-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a5cd6-126">RELATED LINKS</span></span>

[<span data-ttu-id="a5cd6-127">Rimuovere una sonda da un gateway applicazione esistente</span><span class="sxs-lookup"><span data-stu-id="a5cd6-127">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="a5cd6-128">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a5cd6-128">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="a5cd6-129">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a5cd6-129">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="a5cd6-130">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a5cd6-130">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="a5cd6-131">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a5cd6-131">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

