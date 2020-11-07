---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: df81af46023c1e28ecfe39cf880f45cd9b2319ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688008"
---
# <span data-ttu-id="d937a-101">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="d937a-101">Remove-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="d937a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d937a-102">SYNOPSIS</span></span>
<span data-ttu-id="d937a-103">Rimuove una sonda di integrità da un gateway applicazione esistente.</span><span class="sxs-lookup"><span data-stu-id="d937a-103">Removes a health probe from an existing application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d937a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d937a-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d937a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d937a-105">DESCRIPTION</span></span>
<span data-ttu-id="d937a-106">Il cmdlet Remove-AzureRmApplicationGatewayProbeConfig consente di rimuovere una sonda di integrità da un gateway applicazione esistente.</span><span class="sxs-lookup"><span data-stu-id="d937a-106">The Remove-AzureRmApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="d937a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d937a-107">EXAMPLES</span></span>

### <span data-ttu-id="d937a-108">Esempio 1: rimuovere una sonda di integrità da un gateway applicazione esistente</span><span class="sxs-lookup"><span data-stu-id="d937a-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="d937a-109">Questo comando rimuove la sonda di integrità denominata Probe04 dal gateway dell'applicazione denominata gateway.</span><span class="sxs-lookup"><span data-stu-id="d937a-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="d937a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d937a-110">PARAMETERS</span></span>

### <span data-ttu-id="d937a-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d937a-111">-ApplicationGateway</span></span>
<span data-ttu-id="d937a-112">Specifica il gateway dell'applicazione a cui questo cmdlet rimuove un probe.</span><span class="sxs-lookup"><span data-stu-id="d937a-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

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

### <span data-ttu-id="d937a-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="d937a-113">-Name</span></span>
<span data-ttu-id="d937a-114">Specifica il nome del probe per cui viene rimosso questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d937a-114">Specifies the name of the probe for which this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d937a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d937a-115">-DefaultProfile</span></span>
<span data-ttu-id="d937a-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d937a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d937a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d937a-117">CommonParameters</span></span>
<span data-ttu-id="d937a-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d937a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d937a-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d937a-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d937a-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d937a-120">INPUTS</span></span>

### <span data-ttu-id="d937a-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d937a-121">PSApplicationGateway</span></span>
<span data-ttu-id="d937a-122">Il parametro ' ApplicationGateway ' accetta il valore di tipo ' PSApplicationGateway ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="d937a-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="d937a-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d937a-123">OUTPUTS</span></span>

### <span data-ttu-id="d937a-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d937a-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d937a-125">Note</span><span class="sxs-lookup"><span data-stu-id="d937a-125">NOTES</span></span>

## <span data-ttu-id="d937a-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d937a-126">RELATED LINKS</span></span>

[<span data-ttu-id="d937a-127">Rimuovere una sonda da un gateway applicazione esistente</span><span class="sxs-lookup"><span data-stu-id="d937a-127">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="d937a-128">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="d937a-128">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="d937a-129">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="d937a-129">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="d937a-130">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="d937a-130">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="d937a-131">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="d937a-131">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

