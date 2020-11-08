---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/restore-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Restore-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Restore-AzNetAppFilesVolume.md
ms.openlocfilehash: 486bd44d3f48213fde6fb9b6c1d15a5683c1fd82
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188558"
---
# <span data-ttu-id="b6615-101">Restore-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="b6615-101">Restore-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="b6615-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b6615-102">SYNOPSIS</span></span>
<span data-ttu-id="b6615-103">Ripristina/ripristina un volume in uno degli snapshot</span><span class="sxs-lookup"><span data-stu-id="b6615-103">Restore/Revert a volume to one of its snapshots</span></span>

## <span data-ttu-id="b6615-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b6615-104">SYNTAX</span></span>

### <span data-ttu-id="b6615-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b6615-105">ByFieldsParameterSet (Default)</span></span>
```
Revert-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-SnapshotId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b6615-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6615-106">ByParentObjectParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -Name <String> -PoolObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6615-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6615-107">ByResourceIdParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6615-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6615-108">ByObjectParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6615-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b6615-109">DESCRIPTION</span></span>
<span data-ttu-id="b6615-110">Ripristinare o ripristinare un volume nello snapshot specificato in SnapshotId parametro</span><span class="sxs-lookup"><span data-stu-id="b6615-110">Restore/Revert a volume to the snapshot specified in the SnapshotId paramter</span></span>

## <span data-ttu-id="b6615-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b6615-111">EXAMPLES</span></span>

### <span data-ttu-id="b6615-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b6615-112">Example 1</span></span>
```powershell
PS C:\> Restore-AzNetAppFilesVolume -ResourceGroupName "MyRG" -Location "westus2" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -SnapshotId 7d6e4069-6c78-6c61-7bf6-c60968e45fbf
```

<span data-ttu-id="b6615-113">Questo comando restituisce o Ripristina il volume volumetrico in uno degli snapshot con il snapshotId di 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span><span class="sxs-lookup"><span data-stu-id="b6615-113">This command Restores/Reverts the volume MyVolume to one of its snapshots with the snapshotId of 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span></span>

## <span data-ttu-id="b6615-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b6615-114">PARAMETERS</span></span>

### <span data-ttu-id="b6615-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b6615-115">-AccountName</span></span>
<span data-ttu-id="b6615-116">Nome dell'account di ANF</span><span class="sxs-lookup"><span data-stu-id="b6615-116">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6615-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6615-117">-DefaultProfile</span></span>
<span data-ttu-id="b6615-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b6615-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6615-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6615-119">-InputObject</span></span>
<span data-ttu-id="b6615-120">Oggetto volume da rimuovere</span><span class="sxs-lookup"><span data-stu-id="b6615-120">The volume object to remove</span></span>

```yaml
Type: PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6615-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="b6615-121">-Name</span></span>
<span data-ttu-id="b6615-122">Nome del volume di ANF</span><span class="sxs-lookup"><span data-stu-id="b6615-122">The name of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6615-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b6615-123">-PassThru</span></span>
<span data-ttu-id="b6615-124">Restituirà se il volume specificato è stato ripristinato/ripristinato correttamente</span><span class="sxs-lookup"><span data-stu-id="b6615-124">Return whether the specified volume was successfully restored/reverted</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6615-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="b6615-125">-PoolName</span></span>
<span data-ttu-id="b6615-126">Nome del pool di ANF</span><span class="sxs-lookup"><span data-stu-id="b6615-126">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6615-127">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="b6615-127">-PoolObject</span></span>
<span data-ttu-id="b6615-128">Oggetto pool contenente il volume da rimuovere</span><span class="sxs-lookup"><span data-stu-id="b6615-128">The pool object containing the volume to remove</span></span>

```yaml
Type: PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6615-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6615-129">-ResourceGroupName</span></span>
<span data-ttu-id="b6615-130">Gruppo risorse del volume ANF</span><span class="sxs-lookup"><span data-stu-id="b6615-130">The resource group of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6615-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6615-131">-ResourceId</span></span>
<span data-ttu-id="b6615-132">ID risorsa del volume ANF</span><span class="sxs-lookup"><span data-stu-id="b6615-132">The resource id of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6615-133">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="b6615-133">-SnapshotId</span></span>
<span data-ttu-id="b6615-134">SnapshotId dello snapshot.</span><span class="sxs-lookup"><span data-stu-id="b6615-134">SnapshotId of the snapshot.</span></span>
<span data-ttu-id="b6615-135">UUID V4 usato per identificare lo snapshot</span><span class="sxs-lookup"><span data-stu-id="b6615-135">UUID v4 used to identify the Snapshot</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6615-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b6615-136">-Confirm</span></span>
<span data-ttu-id="b6615-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6615-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6615-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6615-138">-WhatIf</span></span>
<span data-ttu-id="b6615-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b6615-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6615-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b6615-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6615-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6615-141">CommonParameters</span></span>
<span data-ttu-id="b6615-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6615-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6615-143">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b6615-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6615-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b6615-144">INPUTS</span></span>

### <span data-ttu-id="b6615-145">System. String</span><span class="sxs-lookup"><span data-stu-id="b6615-145">System.String</span></span>

### <span data-ttu-id="b6615-146">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="b6615-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="b6615-147">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="b6615-147">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="b6615-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b6615-148">OUTPUTS</span></span>

### <span data-ttu-id="b6615-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b6615-149">System.Boolean</span></span>

## <span data-ttu-id="b6615-150">Note</span><span class="sxs-lookup"><span data-stu-id="b6615-150">NOTES</span></span>

## <span data-ttu-id="b6615-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b6615-151">RELATED LINKS</span></span>
