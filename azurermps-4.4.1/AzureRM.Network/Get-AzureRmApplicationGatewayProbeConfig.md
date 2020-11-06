---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 6583856eb6d44fa170b53a855e43db71602534a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510484"
---
# <span data-ttu-id="f75c4-101">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f75c4-101">Get-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="f75c4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f75c4-102">SYNOPSIS</span></span>
<span data-ttu-id="f75c4-103">Ottiene una configurazione esistente di una sonda sanitaria da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f75c4-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f75c4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f75c4-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f75c4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f75c4-105">DESCRIPTION</span></span>
<span data-ttu-id="f75c4-106">Il cmdlet Get-AzureRmApplicationGatewayProbeConfig ottiene una configurazione della sonda di integrità esistente da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f75c4-106">The Get-AzureRmApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="f75c4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f75c4-107">EXAMPLES</span></span>

### <span data-ttu-id="f75c4-108">Esempio 1: ottenere una sonda esistente da un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="f75c4-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="f75c4-109">Questo comando ottiene la sonda di integrità denominata Probe02 dal gateway dell'applicazione denominata gateway.</span><span class="sxs-lookup"><span data-stu-id="f75c4-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="f75c4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f75c4-110">PARAMETERS</span></span>

### <span data-ttu-id="f75c4-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f75c4-111">-ApplicationGateway</span></span>
<span data-ttu-id="f75c4-112">Specifica il gateway dell'applicazione a cui questo cmdlet ottiene una configurazione Probe.</span><span class="sxs-lookup"><span data-stu-id="f75c4-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f75c4-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="f75c4-113">-Name</span></span>
<span data-ttu-id="f75c4-114">Specifica il nome del probe.</span><span class="sxs-lookup"><span data-stu-id="f75c4-114">Specifies the name of the probe.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f75c4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f75c4-115">-DefaultProfile</span></span>
<span data-ttu-id="f75c4-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f75c4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f75c4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f75c4-117">CommonParameters</span></span>
<span data-ttu-id="f75c4-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f75c4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f75c4-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f75c4-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f75c4-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f75c4-120">INPUTS</span></span>

### <span data-ttu-id="f75c4-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f75c4-121">PSApplicationGateway</span></span>
<span data-ttu-id="f75c4-122">Il parametro ' ApplicationGateway ' accetta il valore di tipo ' PSApplicationGateway ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="f75c4-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="f75c4-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f75c4-123">OUTPUTS</span></span>

### <span data-ttu-id="f75c4-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="f75c4-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

### <span data-ttu-id="f75c4-125">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbe]</span><span class="sxs-lookup"><span data-stu-id="f75c4-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe]</span></span>

## <span data-ttu-id="f75c4-126">Note</span><span class="sxs-lookup"><span data-stu-id="f75c4-126">NOTES</span></span>

## <span data-ttu-id="f75c4-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f75c4-127">RELATED LINKS</span></span>

[<span data-ttu-id="f75c4-128">Aggiungere una sonda a un gateway applicazione esistente</span><span class="sxs-lookup"><span data-stu-id="f75c4-128">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="f75c4-129">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f75c4-129">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="f75c4-130">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f75c4-130">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="f75c4-131">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f75c4-131">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="f75c4-132">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f75c4-132">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

