---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/restore-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Restore-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Restore-AzNetAppFilesVolume.md
ms.openlocfilehash: 8c07b375214ef78f281bdfab2b31a94e0504b30e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968238"
---
# <span data-ttu-id="f49f9-101">Restore-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="f49f9-101">Restore-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="f49f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f49f9-102">SYNOPSIS</span></span>
<span data-ttu-id="f49f9-103">Ripristinare/ripristinare uno snapshot di un volume</span><span class="sxs-lookup"><span data-stu-id="f49f9-103">Restore/Revert a volume to one of its snapshots</span></span>

## <span data-ttu-id="f49f9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f49f9-104">SYNTAX</span></span>

### <span data-ttu-id="f49f9-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f49f9-105">ByFieldsParameterSet (Default)</span></span>
```
Restore-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-SnapshotId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f49f9-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f49f9-106">ByParentObjectParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -Name <String> -PoolObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f49f9-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f49f9-107">ByResourceIdParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f49f9-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f49f9-108">ByObjectParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f49f9-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f49f9-109">DESCRIPTION</span></span>
<span data-ttu-id="f49f9-110">Ripristinare/ripristinare un volume nello snapshot specificato nel parametro SnapshotId</span><span class="sxs-lookup"><span data-stu-id="f49f9-110">Restore/Revert a volume to the snapshot specified in the SnapshotId paramter</span></span>

## <span data-ttu-id="f49f9-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f49f9-111">EXAMPLES</span></span>

### <span data-ttu-id="f49f9-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f49f9-112">Example 1</span></span>
```powershell
PS C:\> Restore-AzNetAppFilesVolume -ResourceGroupName "MyRG" -Location "westus2" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -SnapshotId 7d6e4069-6c78-6c61-7bf6-c60968e45fbf
```

<span data-ttu-id="f49f9-113">Questo comando ripristina/ripristina il volume MyVolume a uno dei suoi snapshot con snapshotId di 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span><span class="sxs-lookup"><span data-stu-id="f49f9-113">This command Restores/Reverts the volume MyVolume to one of its snapshots with the snapshotId of 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span></span>

## <span data-ttu-id="f49f9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f49f9-114">PARAMETERS</span></span>

### <span data-ttu-id="f49f9-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f49f9-115">-AccountName</span></span>
<span data-ttu-id="f49f9-116">Nome dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="f49f9-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="f49f9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f49f9-117">-DefaultProfile</span></span>
<span data-ttu-id="f49f9-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f49f9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f49f9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f49f9-119">-InputObject</span></span>
<span data-ttu-id="f49f9-120">L'oggetto volume da rimuovere</span><span class="sxs-lookup"><span data-stu-id="f49f9-120">The volume object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f49f9-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f49f9-121">-Name</span></span>
<span data-ttu-id="f49f9-122">Nome del volume ANF</span><span class="sxs-lookup"><span data-stu-id="f49f9-122">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f49f9-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f49f9-123">-PassThru</span></span>
<span data-ttu-id="f49f9-124">Verificare se il volume specificato è stato ripristinato/ripristinato correttamente</span><span class="sxs-lookup"><span data-stu-id="f49f9-124">Return whether the specified volume was successfully restored/reverted</span></span>

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

### <span data-ttu-id="f49f9-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="f49f9-125">-PoolName</span></span>
<span data-ttu-id="f49f9-126">Nome del pool ANF</span><span class="sxs-lookup"><span data-stu-id="f49f9-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="f49f9-127">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="f49f9-127">-PoolObject</span></span>
<span data-ttu-id="f49f9-128">Oggetto pool contenente il volume da rimuovere</span><span class="sxs-lookup"><span data-stu-id="f49f9-128">The pool object containing the volume to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f49f9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f49f9-129">-ResourceGroupName</span></span>
<span data-ttu-id="f49f9-130">Gruppo di risorse del volume ANF</span><span class="sxs-lookup"><span data-stu-id="f49f9-130">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="f49f9-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f49f9-131">-ResourceId</span></span>
<span data-ttu-id="f49f9-132">ID risorsa del volume ANF</span><span class="sxs-lookup"><span data-stu-id="f49f9-132">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="f49f9-133">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="f49f9-133">-SnapshotId</span></span>
<span data-ttu-id="f49f9-134">SnapshotId dello snapshot.</span><span class="sxs-lookup"><span data-stu-id="f49f9-134">SnapshotId of the snapshot.</span></span>
<span data-ttu-id="f49f9-135">UUID v4 usato per identificare lo snapshot</span><span class="sxs-lookup"><span data-stu-id="f49f9-135">UUID v4 used to identify the Snapshot</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f49f9-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f49f9-136">-Confirm</span></span>
<span data-ttu-id="f49f9-137">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f49f9-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f49f9-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f49f9-138">-WhatIf</span></span>
<span data-ttu-id="f49f9-139">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f49f9-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f49f9-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f49f9-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f49f9-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f49f9-141">CommonParameters</span></span>
<span data-ttu-id="f49f9-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f49f9-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f49f9-143">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f49f9-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f49f9-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="f49f9-144">INPUTS</span></span>

### <span data-ttu-id="f49f9-145">System.String</span><span class="sxs-lookup"><span data-stu-id="f49f9-145">System.String</span></span>

### <span data-ttu-id="f49f9-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="f49f9-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="f49f9-147">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="f49f9-147">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="f49f9-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f49f9-148">OUTPUTS</span></span>

### <span data-ttu-id="f49f9-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f49f9-149">System.Boolean</span></span>

## <span data-ttu-id="f49f9-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="f49f9-150">NOTES</span></span>

## <span data-ttu-id="f49f9-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f49f9-151">RELATED LINKS</span></span>
