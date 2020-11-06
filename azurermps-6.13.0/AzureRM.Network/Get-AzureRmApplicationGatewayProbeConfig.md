---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 2730e3ba1e85a876940492b4abfd4fbe5dbca956
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519737"
---
# <span data-ttu-id="5da61-101">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5da61-101">Get-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="5da61-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5da61-102">SYNOPSIS</span></span>
<span data-ttu-id="5da61-103">Ottiene una configurazione esistente di una sonda sanitaria da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5da61-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5da61-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5da61-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5da61-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5da61-105">DESCRIPTION</span></span>
<span data-ttu-id="5da61-106">Il cmdlet Get-AzureRmApplicationGatewayProbeConfig ottiene una configurazione della sonda di integrità esistente da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5da61-106">The Get-AzureRmApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="5da61-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5da61-107">EXAMPLES</span></span>

### <span data-ttu-id="5da61-108">Esempio 1: ottenere una sonda esistente da un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="5da61-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="5da61-109">Questo comando ottiene la sonda di integrità denominata Probe02 dal gateway dell'applicazione denominata gateway.</span><span class="sxs-lookup"><span data-stu-id="5da61-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="5da61-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5da61-110">PARAMETERS</span></span>

### <span data-ttu-id="5da61-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5da61-111">-ApplicationGateway</span></span>
<span data-ttu-id="5da61-112">Specifica il gateway dell'applicazione a cui questo cmdlet ottiene una configurazione Probe.</span><span class="sxs-lookup"><span data-stu-id="5da61-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

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

### <span data-ttu-id="5da61-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5da61-113">-DefaultProfile</span></span>
<span data-ttu-id="5da61-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5da61-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5da61-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="5da61-115">-Name</span></span>
<span data-ttu-id="5da61-116">Specifica il nome del probe.</span><span class="sxs-lookup"><span data-stu-id="5da61-116">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="5da61-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5da61-117">CommonParameters</span></span>
<span data-ttu-id="5da61-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5da61-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5da61-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5da61-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5da61-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5da61-120">INPUTS</span></span>

### <span data-ttu-id="5da61-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5da61-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="5da61-122">Parametri: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5da61-122">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="5da61-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5da61-123">OUTPUTS</span></span>

### <span data-ttu-id="5da61-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="5da61-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="5da61-125">Note</span><span class="sxs-lookup"><span data-stu-id="5da61-125">NOTES</span></span>

## <span data-ttu-id="5da61-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5da61-126">RELATED LINKS</span></span>

[<span data-ttu-id="5da61-127">Aggiungere una sonda a un gateway applicazione esistente</span><span class="sxs-lookup"><span data-stu-id="5da61-127">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="5da61-128">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5da61-128">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="5da61-129">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5da61-129">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="5da61-130">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5da61-130">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="5da61-131">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5da61-131">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

