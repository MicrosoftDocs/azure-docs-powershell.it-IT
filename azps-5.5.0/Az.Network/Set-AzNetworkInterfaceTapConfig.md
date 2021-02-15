---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 31a02e6f27d766d9f74b34c331a69c66e82d8fc5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189454"
---
# <span data-ttu-id="314c5-101">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="314c5-101">Set-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="314c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="314c5-102">SYNOPSIS</span></span>
<span data-ttu-id="314c5-103">Aggiorna una configurazione di tocco per un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="314c5-103">Updates a tap configuration for a network interface.</span></span>

## <span data-ttu-id="314c5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="314c5-104">SYNTAX</span></span>

```
Set-AzNetworkInterfaceTapConfig -NetworkInterfaceTapConfig <PSNetworkInterfaceTapConfiguration> [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="314c5-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="314c5-105">DESCRIPTION</span></span>
<span data-ttu-id="314c5-106">**Set-AzNetworkInterfaceTapConfig** aggiorna una configurazione di tocco per un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="314c5-106">The **Set-AzNetworkInterfaceTapConfig** updates a tap configuration for a network interface.</span></span>

## <span data-ttu-id="314c5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="314c5-107">EXAMPLES</span></span>

### <span data-ttu-id="314c5-108">Esempio 1: Impostare la configurazione TapConfiguration con il nome TapConfig aggiornato</span><span class="sxs-lookup"><span data-stu-id="314c5-108">Example 1: Set the TapConfiguration with updated TapConfig name</span></span>
```
PS C:\>$tapConfig = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
PS C:\>$tapConfig.Name = "NewTapName"
PS C:\>Set-AzNetworkInterfaceTapConfig -NetworkInterfaceTapConfig $tapConfig
```

## <span data-ttu-id="314c5-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="314c5-109">PARAMETERS</span></span>

### <span data-ttu-id="314c5-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="314c5-110">-AsJob</span></span>
<span data-ttu-id="314c5-111">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="314c5-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="314c5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="314c5-112">-DefaultProfile</span></span>
<span data-ttu-id="314c5-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="314c5-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="314c5-114">-Force</span><span class="sxs-lookup"><span data-stu-id="314c5-114">-Force</span></span>
<span data-ttu-id="314c5-115">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="314c5-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="314c5-116">-NetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="314c5-116">-NetworkInterfaceTapConfig</span></span>
<span data-ttu-id="314c5-117">Configurazione di Tocco Di NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="314c5-117">The NetworkInterface Tap configuration</span></span>

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

### <span data-ttu-id="314c5-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="314c5-118">-Confirm</span></span>
<span data-ttu-id="314c5-119">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="314c5-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="314c5-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="314c5-120">-WhatIf</span></span>
<span data-ttu-id="314c5-121">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="314c5-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="314c5-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="314c5-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="314c5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="314c5-123">CommonParameters</span></span>
<span data-ttu-id="314c5-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="314c5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="314c5-125">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="314c5-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="314c5-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="314c5-126">INPUTS</span></span>

### <span data-ttu-id="314c5-127">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="314c5-127">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="314c5-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="314c5-128">OUTPUTS</span></span>

### <span data-ttu-id="314c5-129">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="314c5-129">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="314c5-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="314c5-130">NOTES</span></span>

## <span data-ttu-id="314c5-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="314c5-131">RELATED LINKS</span></span>

[<span data-ttu-id="314c5-132">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="314c5-132">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="314c5-133">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="314c5-133">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="314c5-134">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="314c5-134">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)
