---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkProfile.md
ms.openlocfilehash: e463e6a1d25db24553b62c8d2fea1051eb231840
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020020"
---
# <span data-ttu-id="e0661-101">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e0661-101">New-AzNetworkProfile</span></span>

## <span data-ttu-id="e0661-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e0661-102">SYNOPSIS</span></span>
<span data-ttu-id="e0661-103">Crea un nuovo profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="e0661-103">Creates a new network profile.</span></span>

## <span data-ttu-id="e0661-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e0661-104">SYNTAX</span></span>

```
New-AzNetworkProfile -ResourceGroupName <String> -Name <String> [-Location <String>] [-Tag <Hashtable>]
 [-ContainerNicConfig <PSContainerNetworkInterfaceConfiguration[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0661-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e0661-105">DESCRIPTION</span></span>
<span data-ttu-id="e0661-106">Il cmdlet **New-AzNetworkProfile** crea una nuova risorsa di primo livello del profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="e0661-106">The **New-AzNetworkProfile** cmdlet creates a new network profile top level resource.</span></span>

## <span data-ttu-id="e0661-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e0661-107">EXAMPLES</span></span>

### <span data-ttu-id="e0661-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e0661-108">Example 1</span></span>
```powershell
$networkProfile = New-AzNetworkProfile -Name np1 -ResourceGroupName rg1 -Location westus
```

<span data-ttu-id="e0661-109">Verrà creata una nuova risorsa di primo livello del profilo di rete</span><span class="sxs-lookup"><span data-stu-id="e0661-109">This creates a new network profile top level resource</span></span>

## <span data-ttu-id="e0661-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e0661-110">PARAMETERS</span></span>

### <span data-ttu-id="e0661-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e0661-111">-AsJob</span></span>
<span data-ttu-id="e0661-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="e0661-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e0661-113">-ContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="e0661-113">-ContainerNicConfig</span></span>
<span data-ttu-id="e0661-114">Le configurazioni di interfaccia di rete del contenitore da aggiungere al profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="e0661-114">The container network interface configurations to add to this network profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration[]
Parameter Sets: (All)
Aliases: ContainerNetworkInterfaceConfiguration

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0661-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0661-115">-DefaultProfile</span></span>
<span data-ttu-id="e0661-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e0661-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0661-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e0661-117">-Force</span></span>
<span data-ttu-id="e0661-118">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="e0661-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="e0661-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="e0661-119">-Location</span></span>
<span data-ttu-id="e0661-120">La posizione.</span><span class="sxs-lookup"><span data-stu-id="e0661-120">The location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0661-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="e0661-121">-Name</span></span>
<span data-ttu-id="e0661-122">Nome del profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="e0661-122">The name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0661-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0661-123">-ResourceGroupName</span></span>
<span data-ttu-id="e0661-124">Nome del gruppo di risorse del profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="e0661-124">The resource group name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0661-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="e0661-125">-Tag</span></span>
<span data-ttu-id="e0661-126">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="e0661-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0661-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e0661-127">-Confirm</span></span>
<span data-ttu-id="e0661-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0661-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0661-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0661-129">-WhatIf</span></span>
<span data-ttu-id="e0661-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e0661-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0661-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e0661-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0661-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0661-132">CommonParameters</span></span>
<span data-ttu-id="e0661-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0661-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0661-134">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0661-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0661-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e0661-135">INPUTS</span></span>

### <span data-ttu-id="e0661-136">System. String</span><span class="sxs-lookup"><span data-stu-id="e0661-136">System.String</span></span>

### <span data-ttu-id="e0661-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e0661-137">System.Collections.Hashtable</span></span>

### <span data-ttu-id="e0661-138">Microsoft. Azure. Commands. Network. Models. PSContainerNetworkInterfaceConfiguration []</span><span class="sxs-lookup"><span data-stu-id="e0661-138">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration[]</span></span>

## <span data-ttu-id="e0661-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e0661-139">OUTPUTS</span></span>

### <span data-ttu-id="e0661-140">Microsoft. Azure. Commands. Network. Models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e0661-140">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="e0661-141">Note</span><span class="sxs-lookup"><span data-stu-id="e0661-141">NOTES</span></span>

## <span data-ttu-id="e0661-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e0661-142">RELATED LINKS</span></span>

[<span data-ttu-id="e0661-143">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e0661-143">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="e0661-144">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e0661-144">Remove-AzNetworkProfile</span></span>](./Remove-AzNetworkProfile.md)

[<span data-ttu-id="e0661-145">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e0661-145">Set-AzNetworkProfile</span></span>](./Set-AzNetworkProfile.md)
