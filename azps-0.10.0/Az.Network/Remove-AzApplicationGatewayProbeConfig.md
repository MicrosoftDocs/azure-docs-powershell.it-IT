---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 320588b81791c033b94a07261f769fa0886d2f2c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860350"
---
# <span data-ttu-id="a240b-101">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a240b-101">Remove-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="a240b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a240b-102">SYNOPSIS</span></span>
<span data-ttu-id="a240b-103">Rimuove una sonda di integrità da un gateway applicazione esistente.</span><span class="sxs-lookup"><span data-stu-id="a240b-103">Removes a health probe from an existing application gateway.</span></span>

## <span data-ttu-id="a240b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a240b-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a240b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a240b-105">DESCRIPTION</span></span>
<span data-ttu-id="a240b-106">Il cmdlet Remove-AzApplicationGatewayProbeConfig consente di rimuovere una sonda di integrità da un gateway applicazione esistente.</span><span class="sxs-lookup"><span data-stu-id="a240b-106">The Remove-AzApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="a240b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a240b-107">EXAMPLES</span></span>

### <span data-ttu-id="a240b-108">Esempio 1: rimuovere una sonda di integrità da un gateway applicazione esistente</span><span class="sxs-lookup"><span data-stu-id="a240b-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="a240b-109">Questo comando rimuove la sonda di integrità denominata Probe04 dal gateway dell'applicazione denominata gateway.</span><span class="sxs-lookup"><span data-stu-id="a240b-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="a240b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a240b-110">PARAMETERS</span></span>

### <span data-ttu-id="a240b-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a240b-111">-ApplicationGateway</span></span>
<span data-ttu-id="a240b-112">Specifica il gateway dell'applicazione a cui questo cmdlet rimuove un probe.</span><span class="sxs-lookup"><span data-stu-id="a240b-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

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

### <span data-ttu-id="a240b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a240b-113">-DefaultProfile</span></span>
<span data-ttu-id="a240b-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a240b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a240b-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="a240b-115">-Name</span></span>
<span data-ttu-id="a240b-116">Specifica il nome del probe per cui viene rimosso questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a240b-116">Specifies the name of the probe for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="a240b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a240b-117">CommonParameters</span></span>
<span data-ttu-id="a240b-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a240b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a240b-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a240b-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a240b-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a240b-120">INPUTS</span></span>

### <span data-ttu-id="a240b-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a240b-121">PSApplicationGateway</span></span>
<span data-ttu-id="a240b-122">Il parametro ' ApplicationGateway ' accetta il valore di tipo ' PSApplicationGateway ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="a240b-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="a240b-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a240b-123">OUTPUTS</span></span>

### <span data-ttu-id="a240b-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a240b-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a240b-125">Note</span><span class="sxs-lookup"><span data-stu-id="a240b-125">NOTES</span></span>

## <span data-ttu-id="a240b-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a240b-126">RELATED LINKS</span></span>

[<span data-ttu-id="a240b-127">Rimuovere una sonda da un gateway applicazione esistente</span><span class="sxs-lookup"><span data-stu-id="a240b-127">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="a240b-128">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a240b-128">Add-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="a240b-129">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a240b-129">Get-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="a240b-130">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a240b-130">New-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="a240b-131">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a240b-131">Set-AzApplicationGatewayProbeConfig</span></span>]()

