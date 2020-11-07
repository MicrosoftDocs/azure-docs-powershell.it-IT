---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: b3e2b3ea03ca0bae0db1bea1606e4ae6b94a597e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860877"
---
# <span data-ttu-id="2f815-101">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2f815-101">Get-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="2f815-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2f815-102">SYNOPSIS</span></span>
<span data-ttu-id="2f815-103">Ottiene una configurazione esistente di una sonda sanitaria da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2f815-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="2f815-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2f815-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f815-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2f815-105">DESCRIPTION</span></span>
<span data-ttu-id="2f815-106">Il cmdlet Get-AzApplicationGatewayProbeConfig ottiene una configurazione della sonda di integrità esistente da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2f815-106">The Get-AzApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="2f815-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2f815-107">EXAMPLES</span></span>

### <span data-ttu-id="2f815-108">Esempio 1: ottenere una sonda esistente da un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="2f815-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="2f815-109">Questo comando ottiene la sonda di integrità denominata Probe02 dal gateway dell'applicazione denominata gateway.</span><span class="sxs-lookup"><span data-stu-id="2f815-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="2f815-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2f815-110">PARAMETERS</span></span>

### <span data-ttu-id="2f815-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2f815-111">-ApplicationGateway</span></span>
<span data-ttu-id="2f815-112">Specifica il gateway dell'applicazione a cui questo cmdlet ottiene una configurazione Probe.</span><span class="sxs-lookup"><span data-stu-id="2f815-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

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

### <span data-ttu-id="2f815-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f815-113">-DefaultProfile</span></span>
<span data-ttu-id="2f815-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2f815-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f815-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="2f815-115">-Name</span></span>
<span data-ttu-id="2f815-116">Specifica il nome del probe.</span><span class="sxs-lookup"><span data-stu-id="2f815-116">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="2f815-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f815-117">CommonParameters</span></span>
<span data-ttu-id="2f815-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f815-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f815-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f815-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f815-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2f815-120">INPUTS</span></span>

### <span data-ttu-id="2f815-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2f815-121">PSApplicationGateway</span></span>
<span data-ttu-id="2f815-122">Il parametro ' ApplicationGateway ' accetta il valore di tipo ' PSApplicationGateway ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="2f815-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="2f815-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2f815-123">OUTPUTS</span></span>

### <span data-ttu-id="2f815-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="2f815-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

### <span data-ttu-id="2f815-125">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbe]</span><span class="sxs-lookup"><span data-stu-id="2f815-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe]</span></span>

## <span data-ttu-id="2f815-126">Note</span><span class="sxs-lookup"><span data-stu-id="2f815-126">NOTES</span></span>

## <span data-ttu-id="2f815-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2f815-127">RELATED LINKS</span></span>

[<span data-ttu-id="2f815-128">Aggiungere una sonda a un gateway applicazione esistente</span><span class="sxs-lookup"><span data-stu-id="2f815-128">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="2f815-129">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2f815-129">Add-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="2f815-130">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2f815-130">New-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="2f815-131">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2f815-131">Remove-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="2f815-132">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2f815-132">Set-AzApplicationGatewayProbeConfig</span></span>]()

