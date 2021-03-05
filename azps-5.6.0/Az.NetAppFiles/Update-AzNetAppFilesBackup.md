---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/update-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesBackup.md
ms.openlocfilehash: 95b7ad2ea93f1e1b22eafe3fbaae811dc33f24d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968126"
---
# <span data-ttu-id="afee8-101">Update-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="afee8-101">Update-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="afee8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afee8-102">SYNOPSIS</span></span>
<span data-ttu-id="afee8-103">Aggiorna un backup dei file ANF (Azure NetApp Files) ai modificatori facoltativi forniti.</span><span class="sxs-lookup"><span data-stu-id="afee8-103">Updates an Azure NetApp Files (ANF) backup to the optional modifiers provided.</span></span>

## <span data-ttu-id="afee8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="afee8-104">SYNTAX</span></span>

### <span data-ttu-id="afee8-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="afee8-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesBackup -ResourceGroupName <String> -Location <String> -AccountName <String> -Name <String>
 -PoolName <String> -VolumeName <String> [-Label <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afee8-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="afee8-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesBackup -Name <String> [-Label <String>] [-Tag <Hashtable>]
 -VolumeObject <PSNetAppFilesVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="afee8-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="afee8-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesBackup [-Label <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afee8-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="afee8-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesBackup [-Label <String>] [-Tag <Hashtable>] -InputObject <PSNetAppFilesBackup>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afee8-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="afee8-109">DESCRIPTION</span></span>
<span data-ttu-id="afee8-110">Il cmdlet **Update-AzNetAppFilesBackup modifica** un backup ANF.</span><span class="sxs-lookup"><span data-stu-id="afee8-110">The **Update-AzNetAppFilesBackup** cmdlet modifies an ANF backup.</span></span>

## <span data-ttu-id="afee8-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="afee8-111">EXAMPLES</span></span>

### <span data-ttu-id="afee8-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="afee8-112">Example 1</span></span>
```powershell
PS C:\>  Update-AzNetAppFilesBackup -ResourceGroupName "MyRG" -AccountName $accName1 -Name $backupPolicyObject -Label "updatedLabel"
```

<span data-ttu-id="afee8-113">Questo comando esegue un aggiornamento del backup specificato modificando il nome utente specificato.</span><span class="sxs-lookup"><span data-stu-id="afee8-113">This command performs an update on the given backup modifying the username to that provided.</span></span>

## <span data-ttu-id="afee8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="afee8-114">PARAMETERS</span></span>

### <span data-ttu-id="afee8-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="afee8-115">-AccountName</span></span>
<span data-ttu-id="afee8-116">Nome dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="afee8-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="afee8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afee8-117">-DefaultProfile</span></span>
<span data-ttu-id="afee8-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="afee8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afee8-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="afee8-119">-InputObject</span></span>
<span data-ttu-id="afee8-120">Oggetto snapshot da rimuovere</span><span class="sxs-lookup"><span data-stu-id="afee8-120">The snapshot object to remove</span></span>

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

### <span data-ttu-id="afee8-121">-Label</span><span class="sxs-lookup"><span data-stu-id="afee8-121">-Label</span></span>
<span data-ttu-id="afee8-122">Etichetta per il backup</span><span class="sxs-lookup"><span data-stu-id="afee8-122">Label for backup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afee8-123">-Location</span><span class="sxs-lookup"><span data-stu-id="afee8-123">-Location</span></span>
<span data-ttu-id="afee8-124">Posizione della risorsa</span><span class="sxs-lookup"><span data-stu-id="afee8-124">The location of the resource</span></span>

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

### <span data-ttu-id="afee8-125">-Name</span><span class="sxs-lookup"><span data-stu-id="afee8-125">-Name</span></span>
<span data-ttu-id="afee8-126">Nome dei criteri di backup ANF</span><span class="sxs-lookup"><span data-stu-id="afee8-126">The name of the ANF backup policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: BackupPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afee8-127">-PoolName</span><span class="sxs-lookup"><span data-stu-id="afee8-127">-PoolName</span></span>
<span data-ttu-id="afee8-128">Nome del pool ANF</span><span class="sxs-lookup"><span data-stu-id="afee8-128">The name of the ANF pool</span></span>

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

### <span data-ttu-id="afee8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afee8-129">-ResourceGroupName</span></span>
<span data-ttu-id="afee8-130">Gruppo di risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="afee8-130">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="afee8-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="afee8-131">-ResourceId</span></span>
<span data-ttu-id="afee8-132">ID risorsa del backup ANF</span><span class="sxs-lookup"><span data-stu-id="afee8-132">The resource id of the ANF Backup</span></span>

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

### <span data-ttu-id="afee8-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="afee8-133">-Tag</span></span>
<span data-ttu-id="afee8-134">Tabella hash che rappresenta i tag di risorsa</span><span class="sxs-lookup"><span data-stu-id="afee8-134">A hashtable which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afee8-135">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="afee8-135">-VolumeName</span></span>
<span data-ttu-id="afee8-136">Nome del volume ANF</span><span class="sxs-lookup"><span data-stu-id="afee8-136">The name of the ANF volume</span></span>

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

### <span data-ttu-id="afee8-137">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="afee8-137">-VolumeObject</span></span>
<span data-ttu-id="afee8-138">Oggetto volume contenente il backup da restituire</span><span class="sxs-lookup"><span data-stu-id="afee8-138">The volume object containing the backup to return</span></span>

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

### <span data-ttu-id="afee8-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="afee8-139">-Confirm</span></span>
<span data-ttu-id="afee8-140">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="afee8-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afee8-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afee8-141">-WhatIf</span></span>
<span data-ttu-id="afee8-142">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="afee8-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afee8-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="afee8-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afee8-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afee8-144">CommonParameters</span></span>
<span data-ttu-id="afee8-145">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afee8-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afee8-146">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="afee8-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afee8-147">INPUT</span><span class="sxs-lookup"><span data-stu-id="afee8-147">INPUTS</span></span>

### <span data-ttu-id="afee8-148">System.String</span><span class="sxs-lookup"><span data-stu-id="afee8-148">System.String</span></span>

### <span data-ttu-id="afee8-149">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="afee8-149">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

### <span data-ttu-id="afee8-150">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="afee8-150">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="afee8-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="afee8-151">OUTPUTS</span></span>

### <span data-ttu-id="afee8-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="afee8-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="afee8-153">NOTE</span><span class="sxs-lookup"><span data-stu-id="afee8-153">NOTES</span></span>

## <span data-ttu-id="afee8-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="afee8-154">RELATED LINKS</span></span>
