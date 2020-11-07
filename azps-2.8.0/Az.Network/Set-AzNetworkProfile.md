---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkProfile.md
ms.openlocfilehash: c63940ab03f6d288de3c1b5b0d767182168ed1fd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93852573"
---
# <span data-ttu-id="52021-101">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="52021-101">Set-AzNetworkProfile</span></span>

## <span data-ttu-id="52021-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="52021-102">SYNOPSIS</span></span>
<span data-ttu-id="52021-103">Aggiorna un profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="52021-103">Updates a network profile.</span></span>

## <span data-ttu-id="52021-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="52021-104">SYNTAX</span></span>

```
Set-AzNetworkProfile -NetworkProfile <PSNetworkProfile> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52021-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="52021-105">DESCRIPTION</span></span>
<span data-ttu-id="52021-106">Il cmdlet **set-AzPublicIpPrefix** aggiorna un profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="52021-106">The **Set-AzPublicIpPrefix** cmdlet updates a network profile.</span></span>

## <span data-ttu-id="52021-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="52021-107">EXAMPLES</span></span>

### <span data-ttu-id="52021-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="52021-108">Example 1</span></span>
```powershell
$networkProfile = Get-AzNetworkProfile -Name np1 -ResourceGroupName rg1

$networkProfile.Tags = "TestTag"

$networkProfile.ContainerNetworkInterfaceConfigurations = New-AzNetworkProfileContainerNicConfig -Name cnicconfig1

$networkProfile | Set-AzNetworkProfile
```

<span data-ttu-id="52021-109">Il primo comando ottiene un profilo di rete esistente.</span><span class="sxs-lookup"><span data-stu-id="52021-109">The first command gets an existing network profile.</span></span> <span data-ttu-id="52021-110">Il secondo comando aggiorna un tag e il terzo aggiunge una configurazione di interfaccia di rete nel profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="52021-110">The second command updates a tag and the third adds a network interface configuration on the network profile.</span></span> <span data-ttu-id="52021-111">Il quarto comando Aggiorna il profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="52021-111">The fourth command updates the network profile.</span></span>

## <span data-ttu-id="52021-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="52021-112">PARAMETERS</span></span>

### <span data-ttu-id="52021-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="52021-113">-AsJob</span></span>
<span data-ttu-id="52021-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="52021-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="52021-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52021-115">-DefaultProfile</span></span>
<span data-ttu-id="52021-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="52021-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52021-117">-NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="52021-117">-NetworkProfile</span></span>
<span data-ttu-id="52021-118">Profilo di rete</span><span class="sxs-lookup"><span data-stu-id="52021-118">The network profile</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52021-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="52021-119">-Confirm</span></span>
<span data-ttu-id="52021-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52021-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52021-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52021-121">-WhatIf</span></span>
<span data-ttu-id="52021-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="52021-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52021-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="52021-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52021-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52021-124">CommonParameters</span></span>
<span data-ttu-id="52021-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52021-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52021-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52021-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52021-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="52021-127">INPUTS</span></span>

### <span data-ttu-id="52021-128">Microsoft. Azure. Commands. Network. Models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="52021-128">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="52021-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="52021-129">OUTPUTS</span></span>

### <span data-ttu-id="52021-130">Microsoft. Azure. Commands. Network. Models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="52021-130">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="52021-131">Note</span><span class="sxs-lookup"><span data-stu-id="52021-131">NOTES</span></span>

## <span data-ttu-id="52021-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="52021-132">RELATED LINKS</span></span>

[<span data-ttu-id="52021-133">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="52021-133">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="52021-134">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="52021-134">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="52021-135">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="52021-135">Remove-AzNetworkProfile</span></span>](./Remove-AzNetworkProfile.md)
