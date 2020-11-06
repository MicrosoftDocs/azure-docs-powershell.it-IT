---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkInterfaceTapConfig.md
ms.openlocfilehash: b2034f27cb6c5332b190e3412963dde99f4c9ba0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507391"
---
# <span data-ttu-id="718d0-101">Set-AzureRmNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="718d0-101">Set-AzureRmNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="718d0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="718d0-102">SYNOPSIS</span></span>
<span data-ttu-id="718d0-103">Imposta lo stato obiettivo di una configurazione di tocco</span><span class="sxs-lookup"><span data-stu-id="718d0-103">Sets the goal state of a Tap Configuration</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="718d0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="718d0-104">SYNTAX</span></span>

```
Set-AzureRmNetworkInterfaceTapConfig -NetworkInterfaceTapConfig <PSNetworkInterfaceTapConfiguration> [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="718d0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="718d0-105">DESCRIPTION</span></span>
<span data-ttu-id="718d0-106">**Set-AzureRmNetworkInterfaceTapConfig** imposta lo stato dell'obiettivo per un'interfaccia di rete Azure.</span><span class="sxs-lookup"><span data-stu-id="718d0-106">The **Set-AzureRmNetworkInterfaceTapConfig** sets the goal state for an Azure network interface.</span></span>

## <span data-ttu-id="718d0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="718d0-107">EXAMPLES</span></span>

### <span data-ttu-id="718d0-108">Esempio 1: impostare TapConfiguration con il nome TapConfig aggiornato</span><span class="sxs-lookup"><span data-stu-id="718d0-108">Example 1: Set the TapConfiguration with updated TapConfig name</span></span>
```
PS C:\>$tapConfig = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
PS C:\>$tapConfig.Name = "NewTapName"
PS C:\>Set-AzureRmNetworkInterfaceTapConfig -NetworkInterfaceTapConfig $tapConfig
```

## <span data-ttu-id="718d0-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="718d0-109">PARAMETERS</span></span>

### <span data-ttu-id="718d0-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="718d0-110">-AsJob</span></span>
<span data-ttu-id="718d0-111">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="718d0-111">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="718d0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="718d0-112">-DefaultProfile</span></span>
<span data-ttu-id="718d0-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="718d0-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="718d0-114">-Force</span><span class="sxs-lookup"><span data-stu-id="718d0-114">-Force</span></span>
<span data-ttu-id="718d0-115">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="718d0-115">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="718d0-116">-NetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="718d0-116">-NetworkInterfaceTapConfig</span></span>
<span data-ttu-id="718d0-117">Il NetworkInterface toccare configurtion</span><span class="sxs-lookup"><span data-stu-id="718d0-117">The NetworkInterface Tap configurtion</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="718d0-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="718d0-118">-Confirm</span></span>
<span data-ttu-id="718d0-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="718d0-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="718d0-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="718d0-120">-WhatIf</span></span>
<span data-ttu-id="718d0-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="718d0-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="718d0-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="718d0-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="718d0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="718d0-123">CommonParameters</span></span>
<span data-ttu-id="718d0-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="718d0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="718d0-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="718d0-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="718d0-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="718d0-126">INPUTS</span></span>

### <span data-ttu-id="718d0-127">Microsoft. Azure. Commands. Network. Models. PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="718d0-127">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="718d0-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="718d0-128">OUTPUTS</span></span>

### <span data-ttu-id="718d0-129">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="718d0-129">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="718d0-130">Note</span><span class="sxs-lookup"><span data-stu-id="718d0-130">NOTES</span></span>

## <span data-ttu-id="718d0-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="718d0-131">RELATED LINKS</span></span>
