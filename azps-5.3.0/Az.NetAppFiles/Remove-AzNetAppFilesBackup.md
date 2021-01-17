---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackup.md
ms.openlocfilehash: 34b4e43dcd09df600c73a6dd0a459a41b491da3d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385654"
---
# <span data-ttu-id="5d545-101">Remove-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="5d545-101">Remove-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="5d545-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5d545-102">SYNOPSIS</span></span>
<span data-ttu-id="5d545-103">Elimina un backup di Azure NetApp file (ANF).</span><span class="sxs-lookup"><span data-stu-id="5d545-103">Deletes an Azure NetApp Files (ANF) backup.</span></span>

## <span data-ttu-id="5d545-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5d545-104">SYNTAX</span></span>

### <span data-ttu-id="5d545-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5d545-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesBackup -ResourceGroupName <String> [-AccountName <String>] -PoolName <String>
 [-VolumeName <String>] -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d545-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d545-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackup -Name <String> -VolumeObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d545-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d545-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesBackup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d545-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d545-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackup -InputObject <PSNetAppFilesBackup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d545-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5d545-109">DESCRIPTION</span></span>
<span data-ttu-id="5d545-110">Il cmdlet **Remove-AzNetAppFilesBackup** Elimina un account ANF.</span><span class="sxs-lookup"><span data-stu-id="5d545-110">The **Remove-AzNetAppFilesBackup** cmdlet deletes an ANF account.</span></span>

## <span data-ttu-id="5d545-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5d545-111">EXAMPLES</span></span>

### <span data-ttu-id="5d545-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5d545-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesBackup -ResourceGroupName "MyRG" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -Name "MyBackup"
```

<span data-ttu-id="5d545-113">Questo comando Elimina il nuovo backup di ANF con il nome "backup" per il volume "Tomo".</span><span class="sxs-lookup"><span data-stu-id="5d545-113">This command deletes the new ANF backup with a the name "MyBackup" for volume "MyVolume".</span></span>

## <span data-ttu-id="5d545-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5d545-114">PARAMETERS</span></span>

### <span data-ttu-id="5d545-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5d545-115">-AccountName</span></span>
<span data-ttu-id="5d545-116">Nome dell'account di ANF</span><span class="sxs-lookup"><span data-stu-id="5d545-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="5d545-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d545-117">-DefaultProfile</span></span>
<span data-ttu-id="5d545-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5d545-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d545-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5d545-119">-InputObject</span></span>
<span data-ttu-id="5d545-120">Oggetto snapshot da rimuovere</span><span class="sxs-lookup"><span data-stu-id="5d545-120">The snapshot object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d545-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="5d545-121">-Name</span></span>
<span data-ttu-id="5d545-122">Nome del backup di ANF</span><span class="sxs-lookup"><span data-stu-id="5d545-122">The name of the ANF backup</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: BackupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d545-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5d545-123">-PassThru</span></span>
<span data-ttu-id="5d545-124">Restituire se il backup specificato è stato rimosso correttamente</span><span class="sxs-lookup"><span data-stu-id="5d545-124">Return whether the specified backup was successfully removed</span></span>

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

### <span data-ttu-id="5d545-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="5d545-125">-PoolName</span></span>
<span data-ttu-id="5d545-126">Nome del pool di ANF</span><span class="sxs-lookup"><span data-stu-id="5d545-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="5d545-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d545-127">-ResourceGroupName</span></span>
<span data-ttu-id="5d545-128">Gruppo risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="5d545-128">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="5d545-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5d545-129">-ResourceId</span></span>
<span data-ttu-id="5d545-130">ID risorsa del backup di ANF</span><span class="sxs-lookup"><span data-stu-id="5d545-130">The resource id of the ANF Backup</span></span>

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

### <span data-ttu-id="5d545-131">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="5d545-131">-VolumeName</span></span>
<span data-ttu-id="5d545-132">Nome del volume di ANF</span><span class="sxs-lookup"><span data-stu-id="5d545-132">The name of the ANF volume</span></span>

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

### <span data-ttu-id="5d545-133">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="5d545-133">-VolumeObject</span></span>
<span data-ttu-id="5d545-134">Oggetto volume contenente il backup da restituire</span><span class="sxs-lookup"><span data-stu-id="5d545-134">The volume object containing the backup to return</span></span>

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

### <span data-ttu-id="5d545-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5d545-135">-Confirm</span></span>
<span data-ttu-id="5d545-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d545-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d545-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d545-137">-WhatIf</span></span>
<span data-ttu-id="5d545-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5d545-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d545-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5d545-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d545-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d545-140">CommonParameters</span></span>
<span data-ttu-id="5d545-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d545-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d545-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5d545-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d545-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5d545-143">INPUTS</span></span>

### <span data-ttu-id="5d545-144">System. String</span><span class="sxs-lookup"><span data-stu-id="5d545-144">System.String</span></span>

### <span data-ttu-id="5d545-145">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="5d545-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

### <span data-ttu-id="5d545-146">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="5d545-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="5d545-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5d545-147">OUTPUTS</span></span>

### <span data-ttu-id="5d545-148">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="5d545-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="5d545-149">Note</span><span class="sxs-lookup"><span data-stu-id="5d545-149">NOTES</span></span>

## <span data-ttu-id="5d545-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5d545-150">RELATED LINKS</span></span>
