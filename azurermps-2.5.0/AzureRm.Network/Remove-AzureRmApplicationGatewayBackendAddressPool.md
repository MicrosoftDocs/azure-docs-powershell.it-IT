---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F34C5D18-C505-4815-9DDB-C563E205515C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
ms.openlocfilehash: 7b82cf189d912d000c143b20cca76c4f2683b7d1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866468"
---
# <span data-ttu-id="1b9a9-101">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="1b9a9-101">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="1b9a9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1b9a9-102">SYNOPSIS</span></span>
<span data-ttu-id="1b9a9-103">Rimuove un pool di indirizzi back-end da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1b9a9-103">Removes a back-end address pool from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b9a9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1b9a9-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayBackendAddressPool -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b9a9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b9a9-105">DESCRIPTION</span></span>
<span data-ttu-id="1b9a9-106">Il cmdlet **Remove-AzureRmApplicationGatewayBackendAddressPool** rimuove un pool di indirizzi back-end da un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="1b9a9-106">The **Remove-AzureRmApplicationGatewayBackendAddressPool** cmdlet removes a back-end address pool from an Azure application gateway.</span></span>

## <span data-ttu-id="1b9a9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1b9a9-107">EXAMPLES</span></span>

### <span data-ttu-id="1b9a9-108">Esempio 1: rimuovere un pool di indirizzi back-end da un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="1b9a9-108">Example 1: Remove a back-end address pool from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "BackEndPool02"
```

<span data-ttu-id="1b9a9-109">Il primo comando consente di ottenere il gateway dell'applicazione denominato ApplicationGateway01 appartenente al gruppo di risorse denominato ResourceGroup01 e di salvarlo nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="1b9a9-109">The first command gets the application gateway named ApplicationGateway01 belonging to the resource group named ResourceGroup01 and saves it in the $AppGw variable.</span></span>

<span data-ttu-id="1b9a9-110">Il secondo comando rimuove il pool di indirizzi back-end denominato BackEndPool02 dal gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1b9a9-110">The second command removes the back-end address pool named BackEndPool02 from the application gateway.</span></span>

## <span data-ttu-id="1b9a9-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1b9a9-111">PARAMETERS</span></span>

### <span data-ttu-id="1b9a9-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1b9a9-112">-ApplicationGateway</span></span>
<span data-ttu-id="1b9a9-113">Specifica il gateway dell'applicazione da cui questo cmdlet rimuove un pool di indirizzi back-end.</span><span class="sxs-lookup"><span data-stu-id="1b9a9-113">Specifies the application gateway from which this cmdlet removes a back-end address pool.</span></span>

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

### <span data-ttu-id="1b9a9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b9a9-114">-DefaultProfile</span></span>
<span data-ttu-id="1b9a9-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1b9a9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b9a9-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="1b9a9-116">-Name</span></span>
<span data-ttu-id="1b9a9-117">Specifica il nome del pool di indirizzi back-end rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b9a9-117">Specifies the name of the back-end address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1b9a9-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1b9a9-118">-Confirm</span></span>
<span data-ttu-id="1b9a9-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b9a9-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b9a9-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b9a9-120">-WhatIf</span></span>
<span data-ttu-id="1b9a9-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1b9a9-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b9a9-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1b9a9-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b9a9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b9a9-123">CommonParameters</span></span>
<span data-ttu-id="1b9a9-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b9a9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b9a9-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b9a9-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b9a9-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1b9a9-126">INPUTS</span></span>

### <span data-ttu-id="1b9a9-127">System. String</span><span class="sxs-lookup"><span data-stu-id="1b9a9-127">System.String</span></span>

## <span data-ttu-id="1b9a9-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1b9a9-128">OUTPUTS</span></span>

### <span data-ttu-id="1b9a9-129">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="1b9a9-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="1b9a9-130">Note</span><span class="sxs-lookup"><span data-stu-id="1b9a9-130">NOTES</span></span>

## <span data-ttu-id="1b9a9-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1b9a9-131">RELATED LINKS</span></span>

[<span data-ttu-id="1b9a9-132">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="1b9a9-132">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="1b9a9-133">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="1b9a9-133">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="1b9a9-134">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="1b9a9-134">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="1b9a9-135">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="1b9a9-135">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Set-AzureRmApplicationGatewayBackendAddressPool.md)


