---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeRole.md
ms.openlocfilehash: fb53f13bf6455770b272ae253a9bbe412d048064
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019015"
---
# <span data-ttu-id="435b4-101">Set-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="435b4-101">Set-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="435b4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="435b4-102">SYNOPSIS</span></span>
<span data-ttu-id="435b4-103">Aggiorna un ruolo per un dispositivo</span><span class="sxs-lookup"><span data-stu-id="435b4-103">Updates a Role for a device</span></span>

## <span data-ttu-id="435b4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="435b4-104">SYNTAX</span></span>

### <span data-ttu-id="435b4-105">SetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="435b4-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="435b4-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="435b4-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeRole -ResourceId <String> -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="435b4-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="435b4-107">SetByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeRole -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSDataBoxEdgeRole> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="435b4-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="435b4-108">DESCRIPTION</span></span>
<span data-ttu-id="435b4-109">Il cmdlet **set-AzDataBoxEdgeRole** aggiorna un ruolo molto importante per un dispositivo Edge della casella dati.</span><span class="sxs-lookup"><span data-stu-id="435b4-109">The **Set-AzDataBoxEdgeRole** cmdlet updates an IoT role for a Data Box Edge device.</span></span> <span data-ttu-id="435b4-110">Le vecchie condivisioni montate verranno sostituite con quelle appena fornite nel parametro ShareName.</span><span class="sxs-lookup"><span data-stu-id="435b4-110">The old mounted shares will be replaced with the newly provided ones in the ShareName parameter.</span></span>

## <span data-ttu-id="435b4-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="435b4-111">EXAMPLES</span></span>

### <span data-ttu-id="435b4-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="435b4-112">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleiot -ShareName sharename1,sharename2,sharename3

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
roleiot ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="435b4-113">I nomi delle condivisioni sostituiranno le vecchie condivisioni montate con quelle appena fornite</span><span class="sxs-lookup"><span data-stu-id="435b4-113">Share Names will replace the old mounted shares with the newly provided ones</span></span>

### <span data-ttu-id="435b4-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="435b4-114">Example 2</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleiot -ShareName @()

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
roleiot ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="435b4-115">Per smontare tutte le condivisioni</span><span class="sxs-lookup"><span data-stu-id="435b4-115">To unmount all shares</span></span>

## <span data-ttu-id="435b4-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="435b4-116">PARAMETERS</span></span>

### <span data-ttu-id="435b4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="435b4-117">-DefaultProfile</span></span>
<span data-ttu-id="435b4-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="435b4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="435b4-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="435b4-119">-DeviceName</span></span>
<span data-ttu-id="435b4-120">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="435b4-120">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="435b4-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="435b4-121">-InputObject</span></span>
<span data-ttu-id="435b4-122">Immettere l'oggetto dispositivo corrispondente</span><span class="sxs-lookup"><span data-stu-id="435b4-122">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole
Parameter Sets: SetByInputObjectParameterSet
Aliases: Role

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="435b4-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="435b4-123">-Name</span></span>
<span data-ttu-id="435b4-124">Nome del ruolo</span><span class="sxs-lookup"><span data-stu-id="435b4-124">Name of the Role</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="435b4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="435b4-125">-ResourceGroupName</span></span>
<span data-ttu-id="435b4-126">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="435b4-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="435b4-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="435b4-127">-ResourceId</span></span>
<span data-ttu-id="435b4-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="435b4-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="435b4-129">-ShareName</span><span class="sxs-lookup"><span data-stu-id="435b4-129">-ShareName</span></span>
<span data-ttu-id="435b4-130">Condivisione (s) in un ruolo</span><span class="sxs-lookup"><span data-stu-id="435b4-130">Share(s) in a role</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="435b4-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="435b4-131">-Confirm</span></span>
<span data-ttu-id="435b4-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="435b4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="435b4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="435b4-133">-WhatIf</span></span>
<span data-ttu-id="435b4-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="435b4-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="435b4-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="435b4-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="435b4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="435b4-136">CommonParameters</span></span>
<span data-ttu-id="435b4-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="435b4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="435b4-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="435b4-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="435b4-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="435b4-139">INPUTS</span></span>

### <span data-ttu-id="435b4-140">System. String</span><span class="sxs-lookup"><span data-stu-id="435b4-140">System.String</span></span>

### <span data-ttu-id="435b4-141">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="435b4-141">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="435b4-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="435b4-142">OUTPUTS</span></span>

### <span data-ttu-id="435b4-143">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="435b4-143">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="435b4-144">Note</span><span class="sxs-lookup"><span data-stu-id="435b4-144">NOTES</span></span>

## <span data-ttu-id="435b4-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="435b4-145">RELATED LINKS</span></span>
