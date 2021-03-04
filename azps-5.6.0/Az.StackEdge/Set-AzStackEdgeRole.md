---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/set-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeRole.md
ms.openlocfilehash: 5a6828231b276fc698179d78d3ae4bda7a4c6c7c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950926"
---
# <span data-ttu-id="48c1b-101">Set-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="48c1b-101">Set-AzStackEdgeRole</span></span>

## <span data-ttu-id="48c1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48c1b-102">SYNOPSIS</span></span>
<span data-ttu-id="48c1b-103">Aggiorna un ruolo per un dispositivo</span><span class="sxs-lookup"><span data-stu-id="48c1b-103">Updates a Role for a device</span></span>

## <span data-ttu-id="48c1b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="48c1b-104">SYNTAX</span></span>

### <span data-ttu-id="48c1b-105">SetByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="48c1b-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> -ShareName <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48c1b-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="48c1b-106">SetByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeRole -ResourceId <String> -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48c1b-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="48c1b-107">SetByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeRole -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSStackEdgeRole> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48c1b-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="48c1b-108">DESCRIPTION</span></span>
<span data-ttu-id="48c1b-109">Il cmdlet **Set-AzStackEdgeRole** aggiorna un ruolo IoT per un dispositivo Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="48c1b-109">The **Set-AzStackEdgeRole** cmdlet updates an IoT role for a Stack Edge device.</span></span> <span data-ttu-id="48c1b-110">Le vecchie condivisioni montate verranno sostituite con quelle appena fornite nel parametro ShareName.</span><span class="sxs-lookup"><span data-stu-id="48c1b-110">The old mounted shares will be replaced with the newly provided ones in the ShareName parameter.</span></span>

## <span data-ttu-id="48c1b-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="48c1b-111">EXAMPLES</span></span>

### <span data-ttu-id="48c1b-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="48c1b-112">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleiot -ShareName sharename1,sharename2,sharename3

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
roleiot ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="48c1b-113">I nomi condivisi sostituiranno le vecchie condivisioni montate con quelle appena fornite</span><span class="sxs-lookup"><span data-stu-id="48c1b-113">Share Names will replace the old mounted shares with the newly provided ones</span></span>

### <span data-ttu-id="48c1b-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="48c1b-114">Example 2</span></span>
```powershell
PS C:\> Set-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleiot -ShareName @()

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
roleiot ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="48c1b-115">Per rimuovere l'importo da tutte le condivisioni</span><span class="sxs-lookup"><span data-stu-id="48c1b-115">To unmount all shares</span></span>

## <span data-ttu-id="48c1b-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48c1b-116">PARAMETERS</span></span>

### <span data-ttu-id="48c1b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48c1b-117">-DefaultProfile</span></span>
<span data-ttu-id="48c1b-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="48c1b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48c1b-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="48c1b-119">-DeviceName</span></span>
<span data-ttu-id="48c1b-120">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="48c1b-120">Device Name</span></span>

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

### <span data-ttu-id="48c1b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48c1b-121">-InputObject</span></span>
<span data-ttu-id="48c1b-122">Specifica l'oggetto dispositivo corrispondente</span><span class="sxs-lookup"><span data-stu-id="48c1b-122">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole
Parameter Sets: SetByInputObjectParameterSet
Aliases: Role

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48c1b-123">-Name</span><span class="sxs-lookup"><span data-stu-id="48c1b-123">-Name</span></span>
<span data-ttu-id="48c1b-124">Nome del ruolo</span><span class="sxs-lookup"><span data-stu-id="48c1b-124">Name of the Role</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: RoleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48c1b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48c1b-125">-ResourceGroupName</span></span>
<span data-ttu-id="48c1b-126">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="48c1b-126">Resource Group Name</span></span>

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

### <span data-ttu-id="48c1b-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="48c1b-127">-ResourceId</span></span>
<span data-ttu-id="48c1b-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="48c1b-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="48c1b-129">-ShareName</span><span class="sxs-lookup"><span data-stu-id="48c1b-129">-ShareName</span></span>
<span data-ttu-id="48c1b-130">Condividere uno o più ruoli</span><span class="sxs-lookup"><span data-stu-id="48c1b-130">Share(s) in a role</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48c1b-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="48c1b-131">-Confirm</span></span>
<span data-ttu-id="48c1b-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48c1b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48c1b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48c1b-133">-WhatIf</span></span>
<span data-ttu-id="48c1b-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="48c1b-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="48c1b-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="48c1b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48c1b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48c1b-136">CommonParameters</span></span>
<span data-ttu-id="48c1b-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48c1b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48c1b-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="48c1b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48c1b-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="48c1b-139">INPUTS</span></span>

### <span data-ttu-id="48c1b-140">System.String</span><span class="sxs-lookup"><span data-stu-id="48c1b-140">System.String</span></span>

### <span data-ttu-id="48c1b-141">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="48c1b-141">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="48c1b-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="48c1b-142">OUTPUTS</span></span>

### <span data-ttu-id="48c1b-143">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="48c1b-143">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="48c1b-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="48c1b-144">NOTES</span></span>

## <span data-ttu-id="48c1b-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="48c1b-145">RELATED LINKS</span></span>
