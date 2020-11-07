---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F34C5D18-C505-4815-9DDB-C563E205515C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: d3ca233ba82d1ee485e93a898726087f5cc69415
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678186"
---
# <span data-ttu-id="dfcd8-101">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="dfcd8-101">Remove-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="dfcd8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dfcd8-102">SYNOPSIS</span></span>
<span data-ttu-id="dfcd8-103">Rimuove un pool di indirizzi back-end da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="dfcd8-103">Removes a back-end address pool from an application gateway.</span></span>

## <span data-ttu-id="dfcd8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dfcd8-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayBackendAddressPool -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfcd8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dfcd8-105">DESCRIPTION</span></span>
<span data-ttu-id="dfcd8-106">Il cmdlet **Remove-AzApplicationGatewayBackendAddressPool** rimuove un pool di indirizzi back-end da un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="dfcd8-106">The **Remove-AzApplicationGatewayBackendAddressPool** cmdlet removes a back-end address pool from an Azure application gateway.</span></span>

## <span data-ttu-id="dfcd8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dfcd8-107">EXAMPLES</span></span>

### <span data-ttu-id="dfcd8-108">Esempio 1: rimuovere un pool di indirizzi back-end da un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="dfcd8-108">Example 1: Remove a back-end address pool from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "BackEndPool02"
```

<span data-ttu-id="dfcd8-109">Il primo comando consente di ottenere il gateway dell'applicazione denominato ApplicationGateway01 appartenente al gruppo di risorse denominato ResourceGroup01 e di salvarlo nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="dfcd8-109">The first command gets the application gateway named ApplicationGateway01 belonging to the resource group named ResourceGroup01 and saves it in the $AppGw variable.</span></span>
<span data-ttu-id="dfcd8-110">Il secondo comando rimuove il pool di indirizzi back-end denominato BackEndPool02 dal gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="dfcd8-110">The second command removes the back-end address pool named BackEndPool02 from the application gateway.</span></span>

## <span data-ttu-id="dfcd8-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dfcd8-111">PARAMETERS</span></span>

### <span data-ttu-id="dfcd8-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dfcd8-112">-ApplicationGateway</span></span>
<span data-ttu-id="dfcd8-113">Specifica il gateway dell'applicazione da cui questo cmdlet rimuove un pool di indirizzi back-end.</span><span class="sxs-lookup"><span data-stu-id="dfcd8-113">Specifies the application gateway from which this cmdlet removes a back-end address pool.</span></span>

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

### <span data-ttu-id="dfcd8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfcd8-114">-DefaultProfile</span></span>
<span data-ttu-id="dfcd8-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dfcd8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfcd8-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="dfcd8-116">-Name</span></span>
<span data-ttu-id="dfcd8-117">Specifica il nome del pool di indirizzi back-end rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfcd8-117">Specifies the name of the back-end address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="dfcd8-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dfcd8-118">-Confirm</span></span>
<span data-ttu-id="dfcd8-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfcd8-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfcd8-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfcd8-120">-WhatIf</span></span>
<span data-ttu-id="dfcd8-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dfcd8-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfcd8-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dfcd8-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfcd8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfcd8-123">CommonParameters</span></span>
<span data-ttu-id="dfcd8-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfcd8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfcd8-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfcd8-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfcd8-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dfcd8-126">INPUTS</span></span>

### <span data-ttu-id="dfcd8-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dfcd8-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="dfcd8-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dfcd8-128">OUTPUTS</span></span>

### <span data-ttu-id="dfcd8-129">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="dfcd8-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="dfcd8-130">Note</span><span class="sxs-lookup"><span data-stu-id="dfcd8-130">NOTES</span></span>

## <span data-ttu-id="dfcd8-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dfcd8-131">RELATED LINKS</span></span>

[<span data-ttu-id="dfcd8-132">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="dfcd8-132">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="dfcd8-133">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="dfcd8-133">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="dfcd8-134">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="dfcd8-134">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="dfcd8-135">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="dfcd8-135">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)

