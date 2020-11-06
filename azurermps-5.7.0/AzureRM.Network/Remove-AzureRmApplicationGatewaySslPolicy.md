---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A308E4DD-49FA-4905-94A7-CEA3AAEC3959
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewaySslPolicy.md
ms.openlocfilehash: 8019cb905859e6e46fbf5ae90b90d72b170c631e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521426"
---
# <span data-ttu-id="68430-101">Remove-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="68430-101">Remove-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="68430-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="68430-102">SYNOPSIS</span></span>
<span data-ttu-id="68430-103">Rimuove un criterio SSL da un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="68430-103">Removes an SSL policy from an Azure application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68430-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="68430-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68430-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="68430-105">DESCRIPTION</span></span>
<span data-ttu-id="68430-106">Il cmdlet Remove-AzureRmApplicationGatewaySslPolicy rimuove i criteri SSL da un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="68430-106">The Remove-AzureRmApplicationGatewaySslPolicy cmdlet removes SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="68430-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="68430-107">EXAMPLES</span></span>

### <span data-ttu-id="68430-108">Esempio 1: rimuovere un criterio SSL da un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="68430-108">Example 1: Remove an SSL policy from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGW = Remove-AzureRmApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="68430-109">Questo comando rimuove i criteri SSL dal gateway dell'applicazione denominato ApplicationGateway01.</span><span class="sxs-lookup"><span data-stu-id="68430-109">This command removes the SSL policy from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="68430-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="68430-110">PARAMETERS</span></span>

### <span data-ttu-id="68430-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="68430-111">-ApplicationGateway</span></span>
<span data-ttu-id="68430-112">Specifica il gateway dell'applicazione da cui questo cmdlet rimuove i criteri SSL.</span><span class="sxs-lookup"><span data-stu-id="68430-112">Specifies the application gateway from which this cmdlet removes SSL policy.</span></span>

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

### <span data-ttu-id="68430-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68430-113">-DefaultProfile</span></span>
<span data-ttu-id="68430-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="68430-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68430-115">-Force</span><span class="sxs-lookup"><span data-stu-id="68430-115">-Force</span></span>
<span data-ttu-id="68430-116">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="68430-116">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68430-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="68430-117">-Confirm</span></span>
<span data-ttu-id="68430-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68430-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68430-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68430-119">-WhatIf</span></span>
<span data-ttu-id="68430-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="68430-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68430-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="68430-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68430-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68430-122">CommonParameters</span></span>
<span data-ttu-id="68430-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68430-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68430-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68430-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68430-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="68430-125">INPUTS</span></span>

### <span data-ttu-id="68430-126">System. String</span><span class="sxs-lookup"><span data-stu-id="68430-126">System.String</span></span>

## <span data-ttu-id="68430-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="68430-127">OUTPUTS</span></span>

### <span data-ttu-id="68430-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="68430-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="68430-129">Note</span><span class="sxs-lookup"><span data-stu-id="68430-129">NOTES</span></span>
<span data-ttu-id="68430-130">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="68430-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="68430-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="68430-131">RELATED LINKS</span></span>

[<span data-ttu-id="68430-132">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="68430-132">Set-AzureRmApplicationGatewaySslPolicy</span></span>](./Set-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="68430-133">New-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="68430-133">New-AzureRmApplicationGatewaySslPolicy</span></span>](./New-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="68430-134">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="68430-134">Get-AzureRmApplicationGatewaySslPolicy</span></span>](./Get-AzureRmApplicationGatewaySslPolicy.md)

