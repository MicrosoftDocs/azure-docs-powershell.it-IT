---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F34C5D18-C505-4815-9DDB-C563E205515C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 5655272afa9ddc9c0ff4c1873a0fac7a0e1f50dd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510443"
---
# <span data-ttu-id="640a2-101">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="640a2-101">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="640a2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="640a2-102">SYNOPSIS</span></span>
<span data-ttu-id="640a2-103">Rimuove un pool di indirizzi back-end da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="640a2-103">Removes a back-end address pool from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="640a2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="640a2-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayBackendAddressPool -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="640a2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="640a2-105">DESCRIPTION</span></span>
<span data-ttu-id="640a2-106">Il cmdlet **Remove-AzureRmApplicationGatewayBackendAddressPool** rimuove un pool di indirizzi back-end da un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="640a2-106">The **Remove-AzureRmApplicationGatewayBackendAddressPool** cmdlet removes a back-end address pool from an Azure application gateway.</span></span>

## <span data-ttu-id="640a2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="640a2-107">EXAMPLES</span></span>

### <span data-ttu-id="640a2-108">Esempio 1: rimuovere un pool di indirizzi back-end da un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="640a2-108">Example 1: Remove a back-end address pool from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "BackEndPool02"
```

<span data-ttu-id="640a2-109">Il primo comando consente di ottenere il gateway dell'applicazione denominato ApplicationGateway01 appartenente al gruppo di risorse denominato ResourceGroup01 e di salvarlo nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="640a2-109">The first command gets the application gateway named ApplicationGateway01 belonging to the resource group named ResourceGroup01 and saves it in the $AppGw variable.</span></span>

<span data-ttu-id="640a2-110">Il secondo comando rimuove il pool di indirizzi back-end denominato BackEndPool02 dal gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="640a2-110">The second command removes the back-end address pool named BackEndPool02 from the application gateway.</span></span>

## <span data-ttu-id="640a2-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="640a2-111">PARAMETERS</span></span>

### <span data-ttu-id="640a2-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="640a2-112">-ApplicationGateway</span></span>
<span data-ttu-id="640a2-113">Specifica il gateway dell'applicazione da cui questo cmdlet rimuove un pool di indirizzi back-end.</span><span class="sxs-lookup"><span data-stu-id="640a2-113">Specifies the application gateway from which this cmdlet removes a back-end address pool.</span></span>

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

### <span data-ttu-id="640a2-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="640a2-114">-Name</span></span>
<span data-ttu-id="640a2-115">Specifica il nome del pool di indirizzi back-end rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="640a2-115">Specifies the name of the back-end address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="640a2-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="640a2-116">-Confirm</span></span>
<span data-ttu-id="640a2-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="640a2-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="640a2-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="640a2-118">-WhatIf</span></span>
<span data-ttu-id="640a2-119">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="640a2-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="640a2-120">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="640a2-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="640a2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="640a2-121">-DefaultProfile</span></span>
<span data-ttu-id="640a2-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="640a2-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="640a2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="640a2-123">CommonParameters</span></span>
<span data-ttu-id="640a2-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="640a2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="640a2-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="640a2-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="640a2-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="640a2-126">INPUTS</span></span>

### <span data-ttu-id="640a2-127">System. String</span><span class="sxs-lookup"><span data-stu-id="640a2-127">System.String</span></span>

## <span data-ttu-id="640a2-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="640a2-128">OUTPUTS</span></span>

### <span data-ttu-id="640a2-129">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="640a2-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="640a2-130">Note</span><span class="sxs-lookup"><span data-stu-id="640a2-130">NOTES</span></span>

## <span data-ttu-id="640a2-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="640a2-131">RELATED LINKS</span></span>

[<span data-ttu-id="640a2-132">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="640a2-132">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="640a2-133">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="640a2-133">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="640a2-134">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="640a2-134">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="640a2-135">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="640a2-135">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Set-AzureRmApplicationGatewayBackendAddressPool.md)


