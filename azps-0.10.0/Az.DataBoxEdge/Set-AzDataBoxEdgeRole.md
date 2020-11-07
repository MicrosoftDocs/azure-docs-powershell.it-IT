---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeRole.md
ms.openlocfilehash: 22dee84aadc590d140d64cbd71eeaed3c16f03e2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861554"
---
# <span data-ttu-id="c8924-101">Set-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="c8924-101">Set-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="c8924-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c8924-102">SYNOPSIS</span></span>
<span data-ttu-id="c8924-103">Aggiorna un ruolo per un dispositivo</span><span class="sxs-lookup"><span data-stu-id="c8924-103">Updates a Role for a device</span></span>

## <span data-ttu-id="c8924-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c8924-104">SYNTAX</span></span>

### <span data-ttu-id="c8924-105">SetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c8924-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8924-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8924-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeRole -ResourceId <String> -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8924-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8924-107">SetByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeRole -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSDataBoxEdgeRole> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8924-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c8924-108">DESCRIPTION</span></span>
<span data-ttu-id="c8924-109">Il cmdlet **set-AzDataBoxEdgeRole** aggiorna un ruolo molto importante per un dispositivo Edge della casella dati.</span><span class="sxs-lookup"><span data-stu-id="c8924-109">The **Set-AzDataBoxEdgeRole** cmdlet updates an IoT role for a Data Box Edge device.</span></span> <span data-ttu-id="c8924-110">Le vecchie condivisioni montate verranno sostituite con quelle appena fornite nel parametro ShareName.</span><span class="sxs-lookup"><span data-stu-id="c8924-110">The old mounted shares will be replaced with the newly provided ones in the ShareName parameter.</span></span>

## <span data-ttu-id="c8924-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c8924-111">EXAMPLES</span></span>

### <span data-ttu-id="c8924-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c8924-112">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleiot -ShareName sharename1,sharename2,sharename3

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
roleiot ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="c8924-113">I nomi delle condivisioni sostituiranno le vecchie condivisioni montate con quelle appena fornite</span><span class="sxs-lookup"><span data-stu-id="c8924-113">Share Names will replace the old mounted shares with the newly provided ones</span></span>

### <span data-ttu-id="c8924-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c8924-114">Example 2</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleiot -ShareName @()

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
roleiot ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="c8924-115">Per smontare tutte le condivisioni</span><span class="sxs-lookup"><span data-stu-id="c8924-115">To unmount all shares</span></span>

## <span data-ttu-id="c8924-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c8924-116">PARAMETERS</span></span>

### <span data-ttu-id="c8924-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8924-117">-DefaultProfile</span></span>
<span data-ttu-id="c8924-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c8924-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8924-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="c8924-119">-DeviceName</span></span>
<span data-ttu-id="c8924-120">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="c8924-120">Device Name</span></span>

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

### <span data-ttu-id="c8924-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c8924-121">-InputObject</span></span>
<span data-ttu-id="c8924-122">Immettere l'oggetto dispositivo corrispondente</span><span class="sxs-lookup"><span data-stu-id="c8924-122">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="c8924-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="c8924-123">-Name</span></span>
<span data-ttu-id="c8924-124">Nome del ruolo</span><span class="sxs-lookup"><span data-stu-id="c8924-124">Name of the Role</span></span>

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

### <span data-ttu-id="c8924-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8924-125">-ResourceGroupName</span></span>
<span data-ttu-id="c8924-126">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="c8924-126">Resource Group Name</span></span>

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

### <span data-ttu-id="c8924-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c8924-127">-ResourceId</span></span>
<span data-ttu-id="c8924-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="c8924-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="c8924-129">-ShareName</span><span class="sxs-lookup"><span data-stu-id="c8924-129">-ShareName</span></span>
<span data-ttu-id="c8924-130">Condivisione (s) in un ruolo</span><span class="sxs-lookup"><span data-stu-id="c8924-130">Share(s) in a role</span></span>

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

### <span data-ttu-id="c8924-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c8924-131">-Confirm</span></span>
<span data-ttu-id="c8924-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8924-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8924-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8924-133">-WhatIf</span></span>
<span data-ttu-id="c8924-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c8924-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c8924-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c8924-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8924-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8924-136">CommonParameters</span></span>
<span data-ttu-id="c8924-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8924-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8924-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c8924-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8924-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c8924-139">INPUTS</span></span>

### <span data-ttu-id="c8924-140">System. String</span><span class="sxs-lookup"><span data-stu-id="c8924-140">System.String</span></span>

### <span data-ttu-id="c8924-141">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="c8924-141">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="c8924-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c8924-142">OUTPUTS</span></span>

### <span data-ttu-id="c8924-143">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="c8924-143">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="c8924-144">Note</span><span class="sxs-lookup"><span data-stu-id="c8924-144">NOTES</span></span>

## <span data-ttu-id="c8924-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c8924-145">RELATED LINKS</span></span>
