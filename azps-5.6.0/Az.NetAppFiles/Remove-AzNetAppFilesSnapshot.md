---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/remove-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 340adf5b3114750212ad1e2458159f48a9dae91f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968285"
---
# <span data-ttu-id="4d469-101">Remove-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="4d469-101">Remove-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="4d469-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d469-102">SYNOPSIS</span></span>
<span data-ttu-id="4d469-103">Elimina uno snapshot dei file (ANF) di Azure NetApp.</span><span class="sxs-lookup"><span data-stu-id="4d469-103">Deletes an Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="4d469-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4d469-104">SYNTAX</span></span>

### <span data-ttu-id="4d469-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4d469-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesSnapshot -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d469-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d469-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d469-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d469-107">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -VolumeObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d469-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d469-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -InputObject <PSNetAppFilesSnapshot> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d469-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4d469-109">DESCRIPTION</span></span>
<span data-ttu-id="4d469-110">Il cmdlet **Remove-AzNetAppFilesSnapshot** elimina uno snapshot ANF.</span><span class="sxs-lookup"><span data-stu-id="4d469-110">The **Remove-AzNetAppFilesSnapshot** cmdlet deletes an ANF snapshot.</span></span>

## <span data-ttu-id="4d469-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4d469-111">EXAMPLES</span></span>

### <span data-ttu-id="4d469-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4d469-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesSnapshot -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -Name "MyAnfSnapshot"
```

<span data-ttu-id="4d469-113">Questo comando elimina lo snapshot ANF "MyAnfSnapshot".</span><span class="sxs-lookup"><span data-stu-id="4d469-113">This command deletes the ANF snapshot "MyAnfSnapshot".</span></span>

## <span data-ttu-id="4d469-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d469-114">PARAMETERS</span></span>

### <span data-ttu-id="4d469-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4d469-115">-AccountName</span></span>
<span data-ttu-id="4d469-116">Nome dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="4d469-116">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d469-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d469-117">-DefaultProfile</span></span>
<span data-ttu-id="4d469-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4d469-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d469-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d469-119">-InputObject</span></span>
<span data-ttu-id="4d469-120">Oggetto snapshot da rimuovere</span><span class="sxs-lookup"><span data-stu-id="4d469-120">The snapshot object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d469-121">-Name</span><span class="sxs-lookup"><span data-stu-id="4d469-121">-Name</span></span>
<span data-ttu-id="4d469-122">Nome dello snapshot ANF</span><span class="sxs-lookup"><span data-stu-id="4d469-122">The name of the ANF snapshot</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: SnapshotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d469-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4d469-123">-PassThru</span></span>
<span data-ttu-id="4d469-124">Verificare se il volume specificato è stato rimosso correttamente</span><span class="sxs-lookup"><span data-stu-id="4d469-124">Return whether the specified volume was successfully removed</span></span>

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

### <span data-ttu-id="4d469-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="4d469-125">-PoolName</span></span>
<span data-ttu-id="4d469-126">Nome del pool ANF</span><span class="sxs-lookup"><span data-stu-id="4d469-126">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d469-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d469-127">-ResourceGroupName</span></span>
<span data-ttu-id="4d469-128">Gruppo di risorse dello snapshot ANF</span><span class="sxs-lookup"><span data-stu-id="4d469-128">The resource group of the ANF snapshot</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d469-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4d469-129">-ResourceId</span></span>
<span data-ttu-id="4d469-130">ID risorsa dello snapshot ANF</span><span class="sxs-lookup"><span data-stu-id="4d469-130">The resource id of the ANF snapshot</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d469-131">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="4d469-131">-VolumeName</span></span>
<span data-ttu-id="4d469-132">Nome del volume ANF</span><span class="sxs-lookup"><span data-stu-id="4d469-132">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d469-133">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="4d469-133">-VolumeObject</span></span>
<span data-ttu-id="4d469-134">Oggetto volume contenente lo snapshot da rimuovere</span><span class="sxs-lookup"><span data-stu-id="4d469-134">The volume object containing the snapshot to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d469-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4d469-135">-Confirm</span></span>
<span data-ttu-id="4d469-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d469-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d469-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d469-137">-WhatIf</span></span>
<span data-ttu-id="4d469-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4d469-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d469-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4d469-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d469-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d469-140">CommonParameters</span></span>
<span data-ttu-id="4d469-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d469-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d469-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4d469-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d469-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="4d469-143">INPUTS</span></span>

### <span data-ttu-id="4d469-144">System.String</span><span class="sxs-lookup"><span data-stu-id="4d469-144">System.String</span></span>

### <span data-ttu-id="4d469-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="4d469-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

### <span data-ttu-id="4d469-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="4d469-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="4d469-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4d469-147">OUTPUTS</span></span>

### <span data-ttu-id="4d469-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4d469-148">System.Boolean</span></span>

## <span data-ttu-id="4d469-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="4d469-149">NOTES</span></span>

## <span data-ttu-id="4d469-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4d469-150">RELATED LINKS</span></span>
