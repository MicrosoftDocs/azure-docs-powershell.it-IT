---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayprobeconfig
schema: 2.0.0
ms.openlocfilehash: cbe38933cb4c2c75b5219bf0deccc0b28052a61f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866293"
---
# <span data-ttu-id="7b6ca-101">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7b6ca-101">Get-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="7b6ca-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7b6ca-102">SYNOPSIS</span></span>
<span data-ttu-id="7b6ca-103">Ottiene una configurazione esistente di una sonda sanitaria da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7b6ca-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b6ca-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7b6ca-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b6ca-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7b6ca-105">DESCRIPTION</span></span>
<span data-ttu-id="7b6ca-106">Il cmdlet Get-AzureRmApplicationGatewayProbeConfig ottiene una configurazione della sonda di integrità esistente da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7b6ca-106">The Get-AzureRmApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="7b6ca-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7b6ca-107">EXAMPLES</span></span>

### <span data-ttu-id="7b6ca-108">Esempio 1: ottenere una sonda esistente da un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="7b6ca-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="7b6ca-109">Questo comando ottiene la sonda di integrità denominata Probe02 dal gateway dell'applicazione denominata gateway.</span><span class="sxs-lookup"><span data-stu-id="7b6ca-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="7b6ca-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7b6ca-110">PARAMETERS</span></span>

### <span data-ttu-id="7b6ca-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7b6ca-111">-ApplicationGateway</span></span>
<span data-ttu-id="7b6ca-112">Specifica il gateway dell'applicazione a cui questo cmdlet ottiene una configurazione Probe.</span><span class="sxs-lookup"><span data-stu-id="7b6ca-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

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

### <span data-ttu-id="7b6ca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b6ca-113">-DefaultProfile</span></span>
<span data-ttu-id="7b6ca-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7b6ca-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b6ca-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="7b6ca-115">-Name</span></span>
<span data-ttu-id="7b6ca-116">Specifica il nome del probe.</span><span class="sxs-lookup"><span data-stu-id="7b6ca-116">Specifies the name of the probe.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b6ca-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b6ca-117">CommonParameters</span></span>
<span data-ttu-id="7b6ca-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b6ca-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b6ca-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b6ca-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b6ca-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7b6ca-120">INPUTS</span></span>

### <span data-ttu-id="7b6ca-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7b6ca-121">PSApplicationGateway</span></span>
<span data-ttu-id="7b6ca-122">Il parametro ' ApplicationGateway ' accetta il valore di tipo ' PSApplicationGateway ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="7b6ca-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="7b6ca-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7b6ca-123">OUTPUTS</span></span>

### <span data-ttu-id="7b6ca-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="7b6ca-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

### <span data-ttu-id="7b6ca-125">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbe]</span><span class="sxs-lookup"><span data-stu-id="7b6ca-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe]</span></span>

## <span data-ttu-id="7b6ca-126">Note</span><span class="sxs-lookup"><span data-stu-id="7b6ca-126">NOTES</span></span>

## <span data-ttu-id="7b6ca-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7b6ca-127">RELATED LINKS</span></span>

[<span data-ttu-id="7b6ca-128">Aggiungere una sonda a un gateway applicazione esistente</span><span class="sxs-lookup"><span data-stu-id="7b6ca-128">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="7b6ca-129">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7b6ca-129">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="7b6ca-130">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7b6ca-130">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="7b6ca-131">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7b6ca-131">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="7b6ca-132">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7b6ca-132">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

