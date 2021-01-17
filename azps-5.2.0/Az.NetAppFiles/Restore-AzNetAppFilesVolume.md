---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/restore-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Restore-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Restore-AzNetAppFilesVolume.md
ms.openlocfilehash: 6606de1a5d4de6df6ecafa700ac1b93d31399b43
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322120"
---
# <span data-ttu-id="6bbc0-101">Restore-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="6bbc0-101">Restore-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="6bbc0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6bbc0-102">SYNOPSIS</span></span>
<span data-ttu-id="6bbc0-103">Ripristina/ripristina un volume in uno degli snapshot</span><span class="sxs-lookup"><span data-stu-id="6bbc0-103">Restore/Revert a volume to one of its snapshots</span></span>

## <span data-ttu-id="6bbc0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6bbc0-104">SYNTAX</span></span>

### <span data-ttu-id="6bbc0-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6bbc0-105">ByFieldsParameterSet (Default)</span></span>
```
Restore-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-SnapshotId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6bbc0-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6bbc0-106">ByParentObjectParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -Name <String> -PoolObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bbc0-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6bbc0-107">ByResourceIdParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bbc0-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6bbc0-108">ByObjectParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bbc0-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6bbc0-109">DESCRIPTION</span></span>
<span data-ttu-id="6bbc0-110">Ripristinare o ripristinare un volume nello snapshot specificato in SnapshotId parametro</span><span class="sxs-lookup"><span data-stu-id="6bbc0-110">Restore/Revert a volume to the snapshot specified in the SnapshotId paramter</span></span>

## <span data-ttu-id="6bbc0-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6bbc0-111">EXAMPLES</span></span>

### <span data-ttu-id="6bbc0-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6bbc0-112">Example 1</span></span>
```powershell
PS C:\> Restore-AzNetAppFilesVolume -ResourceGroupName "MyRG" -Location "westus2" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -SnapshotId 7d6e4069-6c78-6c61-7bf6-c60968e45fbf
```

<span data-ttu-id="6bbc0-113">Questo comando restituisce o Ripristina il volume volumetrico in uno degli snapshot con il snapshotId di 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span><span class="sxs-lookup"><span data-stu-id="6bbc0-113">This command Restores/Reverts the volume MyVolume to one of its snapshots with the snapshotId of 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span></span>

## <span data-ttu-id="6bbc0-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6bbc0-114">PARAMETERS</span></span>

### <span data-ttu-id="6bbc0-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6bbc0-115">-AccountName</span></span>
<span data-ttu-id="6bbc0-116">Nome dell'account di ANF</span><span class="sxs-lookup"><span data-stu-id="6bbc0-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="6bbc0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bbc0-117">-DefaultProfile</span></span>
<span data-ttu-id="6bbc0-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6bbc0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6bbc0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6bbc0-119">-InputObject</span></span>
<span data-ttu-id="6bbc0-120">Oggetto volume da rimuovere</span><span class="sxs-lookup"><span data-stu-id="6bbc0-120">The volume object to remove</span></span>

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

### <span data-ttu-id="6bbc0-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="6bbc0-121">-Name</span></span>
<span data-ttu-id="6bbc0-122">Nome del volume di ANF</span><span class="sxs-lookup"><span data-stu-id="6bbc0-122">The name of the ANF volume</span></span>

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

### <span data-ttu-id="6bbc0-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6bbc0-123">-PassThru</span></span>
<span data-ttu-id="6bbc0-124">Restituirà se il volume specificato è stato ripristinato/ripristinato correttamente</span><span class="sxs-lookup"><span data-stu-id="6bbc0-124">Return whether the specified volume was successfully restored/reverted</span></span>

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

### <span data-ttu-id="6bbc0-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="6bbc0-125">-PoolName</span></span>
<span data-ttu-id="6bbc0-126">Nome del pool di ANF</span><span class="sxs-lookup"><span data-stu-id="6bbc0-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="6bbc0-127">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="6bbc0-127">-PoolObject</span></span>
<span data-ttu-id="6bbc0-128">Oggetto pool contenente il volume da rimuovere</span><span class="sxs-lookup"><span data-stu-id="6bbc0-128">The pool object containing the volume to remove</span></span>

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

### <span data-ttu-id="6bbc0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bbc0-129">-ResourceGroupName</span></span>
<span data-ttu-id="6bbc0-130">Gruppo risorse del volume ANF</span><span class="sxs-lookup"><span data-stu-id="6bbc0-130">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="6bbc0-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6bbc0-131">-ResourceId</span></span>
<span data-ttu-id="6bbc0-132">ID risorsa del volume ANF</span><span class="sxs-lookup"><span data-stu-id="6bbc0-132">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="6bbc0-133">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="6bbc0-133">-SnapshotId</span></span>
<span data-ttu-id="6bbc0-134">SnapshotId dello snapshot.</span><span class="sxs-lookup"><span data-stu-id="6bbc0-134">SnapshotId of the snapshot.</span></span>
<span data-ttu-id="6bbc0-135">UUID V4 usato per identificare lo snapshot</span><span class="sxs-lookup"><span data-stu-id="6bbc0-135">UUID v4 used to identify the Snapshot</span></span>

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

### <span data-ttu-id="6bbc0-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6bbc0-136">-Confirm</span></span>
<span data-ttu-id="6bbc0-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6bbc0-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bbc0-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bbc0-138">-WhatIf</span></span>
<span data-ttu-id="6bbc0-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6bbc0-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bbc0-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6bbc0-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bbc0-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bbc0-141">CommonParameters</span></span>
<span data-ttu-id="6bbc0-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bbc0-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bbc0-143">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6bbc0-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bbc0-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6bbc0-144">INPUTS</span></span>

### <span data-ttu-id="6bbc0-145">System. String</span><span class="sxs-lookup"><span data-stu-id="6bbc0-145">System.String</span></span>

### <span data-ttu-id="6bbc0-146">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="6bbc0-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="6bbc0-147">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="6bbc0-147">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="6bbc0-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6bbc0-148">OUTPUTS</span></span>

### <span data-ttu-id="6bbc0-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6bbc0-149">System.Boolean</span></span>

## <span data-ttu-id="6bbc0-150">Note</span><span class="sxs-lookup"><span data-stu-id="6bbc0-150">NOTES</span></span>

## <span data-ttu-id="6bbc0-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6bbc0-151">RELATED LINKS</span></span>
