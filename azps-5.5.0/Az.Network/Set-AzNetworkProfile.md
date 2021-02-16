---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkProfile.md
ms.openlocfilehash: edbfdcdfc7e02c8bfdb266e1ec7a6b1308c07fa2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186846"
---
# <span data-ttu-id="4ab31-101">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4ab31-101">Set-AzNetworkProfile</span></span>

## <span data-ttu-id="4ab31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ab31-102">SYNOPSIS</span></span>
<span data-ttu-id="4ab31-103">Aggiorna un profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="4ab31-103">Updates a network profile.</span></span>

## <span data-ttu-id="4ab31-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4ab31-104">SYNTAX</span></span>

```
Set-AzNetworkProfile -NetworkProfile <PSNetworkProfile> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ab31-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4ab31-105">DESCRIPTION</span></span>
<span data-ttu-id="4ab31-106">Il **cmdlet Set-AzPublicIpPrefix aggiorna** un profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="4ab31-106">The **Set-AzPublicIpPrefix** cmdlet updates a network profile.</span></span>

## <span data-ttu-id="4ab31-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4ab31-107">EXAMPLES</span></span>

### <span data-ttu-id="4ab31-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4ab31-108">Example 1</span></span>
```powershell
$networkProfile = Get-AzNetworkProfile -Name np1 -ResourceGroupName rg1

$networkProfile.Tags = "TestTag"

$networkProfile.ContainerNetworkInterfaceConfigurations = New-AzNetworkProfileContainerNicConfig -Name cnicconfig1

$networkProfile | Set-AzNetworkProfile
```

<span data-ttu-id="4ab31-109">Il primo comando ottiene un profilo di rete esistente.</span><span class="sxs-lookup"><span data-stu-id="4ab31-109">The first command gets an existing network profile.</span></span> <span data-ttu-id="4ab31-110">Il secondo comando aggiorna un tag e il terzo aggiunge una configurazione dell'interfaccia di rete nel profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="4ab31-110">The second command updates a tag and the third adds a network interface configuration on the network profile.</span></span> <span data-ttu-id="4ab31-111">Il quarto comando aggiorna il profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="4ab31-111">The fourth command updates the network profile.</span></span>

## <span data-ttu-id="4ab31-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ab31-112">PARAMETERS</span></span>

### <span data-ttu-id="4ab31-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4ab31-113">-AsJob</span></span>
<span data-ttu-id="4ab31-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="4ab31-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4ab31-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ab31-115">-DefaultProfile</span></span>
<span data-ttu-id="4ab31-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4ab31-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ab31-117">-NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4ab31-117">-NetworkProfile</span></span>
<span data-ttu-id="4ab31-118">Il profilo di rete</span><span class="sxs-lookup"><span data-stu-id="4ab31-118">The network profile</span></span>

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

### <span data-ttu-id="4ab31-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4ab31-119">-Confirm</span></span>
<span data-ttu-id="4ab31-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ab31-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ab31-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ab31-121">-WhatIf</span></span>
<span data-ttu-id="4ab31-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4ab31-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ab31-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4ab31-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ab31-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ab31-124">CommonParameters</span></span>
<span data-ttu-id="4ab31-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ab31-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ab31-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ab31-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ab31-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="4ab31-127">INPUTS</span></span>

### <span data-ttu-id="4ab31-128">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4ab31-128">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="4ab31-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4ab31-129">OUTPUTS</span></span>

### <span data-ttu-id="4ab31-130">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4ab31-130">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="4ab31-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="4ab31-131">NOTES</span></span>

## <span data-ttu-id="4ab31-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4ab31-132">RELATED LINKS</span></span>

[<span data-ttu-id="4ab31-133">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4ab31-133">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="4ab31-134">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4ab31-134">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="4ab31-135">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4ab31-135">Remove-AzNetworkProfile</span></span>](./Remove-AzNetworkProfile.md)
