---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
ms.openlocfilehash: 2d3b212ea24c9dda665d2e2ec2516f25a59318b2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203279"
---
# <span data-ttu-id="8856e-101">Update-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="8856e-101">Update-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="8856e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8856e-102">SYNOPSIS</span></span>
<span data-ttu-id="8856e-103">Aggiorna un volume dei file ANF (Azure NetApp Files) in base ai modificatori facoltativi disponibili.</span><span class="sxs-lookup"><span data-stu-id="8856e-103">Updates an Azure NetApp Files (ANF) volume according to the optional modifiers provided.</span></span>

## <span data-ttu-id="8856e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8856e-104">SYNTAX</span></span>

### <span data-ttu-id="8856e-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8856e-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8856e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8856e-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] -PoolObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8856e-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8856e-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8856e-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8856e-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] -InputObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8856e-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8856e-109">DESCRIPTION</span></span>
<span data-ttu-id="8856e-110">Il cmdlet **Update-AzNetAppFilesVolume** aggiorna un volume ANF.</span><span class="sxs-lookup"><span data-stu-id="8856e-110">The **Update-AzNetAppFilesVolume** cmdlet updates an ANF volume.</span></span>

## <span data-ttu-id="8856e-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8856e-111">EXAMPLES</span></span>

### <span data-ttu-id="8856e-112">Esempio 1: Aggiornare un volume ANF</span><span class="sxs-lookup"><span data-stu-id="8856e-112">Example 1: Update an ANF volume</span></span>
```
PS C:\>Update-AzNetAppFilesVolume -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume" -UsageThreshold Size

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
CreationToken     : MyAnfVolume
ServiceLevel      : Premium
UsageThreshold    : 2199023255552
ProvisioningState : Succeeded
SubnetId          : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyRG-vnet/subnets/default
```

<span data-ttu-id="8856e-113">Questo comando aggiorna il volume ANF "MyAnfVolume" con la nuova dimensione UsageThreshold.</span><span class="sxs-lookup"><span data-stu-id="8856e-113">This command updates the ANF volume "MyAnfVolume" with the new UsageThreshold size.</span></span>

## <span data-ttu-id="8856e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8856e-114">PARAMETERS</span></span>

### <span data-ttu-id="8856e-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8856e-115">-AccountName</span></span>
<span data-ttu-id="8856e-116">Nome dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="8856e-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="8856e-117">-Backup</span><span class="sxs-lookup"><span data-stu-id="8856e-117">-Backup</span></span>
<span data-ttu-id="8856e-118">Matrice di tabella hash che rappresenta l'oggetto di backup</span><span class="sxs-lookup"><span data-stu-id="8856e-118">A hashtable array which represents the backup object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolumeBackupProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8856e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8856e-119">-DefaultProfile</span></span>
<span data-ttu-id="8856e-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8856e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8856e-121">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="8856e-121">-ExportPolicy</span></span>
<span data-ttu-id="8856e-122">Matrice di tabella hash che rappresenta il criterio di esportazione</span><span class="sxs-lookup"><span data-stu-id="8856e-122">A hashtable array which represents the export policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolumeExportPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8856e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8856e-123">-InputObject</span></span>
<span data-ttu-id="8856e-124">Oggetto volume da aggiornare</span><span class="sxs-lookup"><span data-stu-id="8856e-124">The volume object to update</span></span>

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

### <span data-ttu-id="8856e-125">-Location</span><span class="sxs-lookup"><span data-stu-id="8856e-125">-Location</span></span>
<span data-ttu-id="8856e-126">Posizione della risorsa</span><span class="sxs-lookup"><span data-stu-id="8856e-126">The location of the resource</span></span>

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

### <span data-ttu-id="8856e-127">-Name</span><span class="sxs-lookup"><span data-stu-id="8856e-127">-Name</span></span>
<span data-ttu-id="8856e-128">Nome del volume ANF</span><span class="sxs-lookup"><span data-stu-id="8856e-128">The name of the ANF volume</span></span>

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

### <span data-ttu-id="8856e-129">-PoolName</span><span class="sxs-lookup"><span data-stu-id="8856e-129">-PoolName</span></span>
<span data-ttu-id="8856e-130">Nome del pool ANF</span><span class="sxs-lookup"><span data-stu-id="8856e-130">The name of the ANF pool</span></span>

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

### <span data-ttu-id="8856e-131">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="8856e-131">-PoolObject</span></span>
<span data-ttu-id="8856e-132">Oggetto pool contenente il volume da aggiornare</span><span class="sxs-lookup"><span data-stu-id="8856e-132">The pool object containing the volume to update</span></span>

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

### <span data-ttu-id="8856e-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8856e-133">-ResourceGroupName</span></span>
<span data-ttu-id="8856e-134">Gruppo di risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="8856e-134">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="8856e-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8856e-135">-ResourceId</span></span>
<span data-ttu-id="8856e-136">ID risorsa del volume ANF</span><span class="sxs-lookup"><span data-stu-id="8856e-136">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="8856e-137">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="8856e-137">-ServiceLevel</span></span>
<span data-ttu-id="8856e-138">Livello di servizio del volume ANF</span><span class="sxs-lookup"><span data-stu-id="8856e-138">The service level of the ANF volume</span></span>

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

### <span data-ttu-id="8856e-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="8856e-139">-Tag</span></span>
<span data-ttu-id="8856e-140">Tabella hash che rappresenta i tag di risorsa</span><span class="sxs-lookup"><span data-stu-id="8856e-140">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="8856e-141">-ThroughputMibps</span><span class="sxs-lookup"><span data-stu-id="8856e-141">-ThroughputMibps</span></span>
<span data-ttu-id="8856e-142">Velocità effettiva massima in Mibps che può essere raggiunta da questo volume</span><span class="sxs-lookup"><span data-stu-id="8856e-142">Maximum throughput in Mibps that can be achieved by this volume</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8856e-143">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="8856e-143">-UsageThreshold</span></span>
<span data-ttu-id="8856e-144">Quota di archiviazione massima consentita per un file system in byte</span><span class="sxs-lookup"><span data-stu-id="8856e-144">The maximum storage quota allowed for a file system in bytes</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8856e-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8856e-145">-Confirm</span></span>
<span data-ttu-id="8856e-146">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8856e-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8856e-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8856e-147">-WhatIf</span></span>
<span data-ttu-id="8856e-148">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8856e-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8856e-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8856e-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8856e-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8856e-150">CommonParameters</span></span>
<span data-ttu-id="8856e-151">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8856e-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8856e-152">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8856e-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8856e-153">INPUT</span><span class="sxs-lookup"><span data-stu-id="8856e-153">INPUTS</span></span>

### <span data-ttu-id="8856e-154">System.String</span><span class="sxs-lookup"><span data-stu-id="8856e-154">System.String</span></span>

### <span data-ttu-id="8856e-155">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="8856e-155">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="8856e-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="8856e-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="8856e-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8856e-157">OUTPUTS</span></span>

### <span data-ttu-id="8856e-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="8856e-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="8856e-159">NOTE</span><span class="sxs-lookup"><span data-stu-id="8856e-159">NOTES</span></span>

## <span data-ttu-id="8856e-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8856e-160">RELATED LINKS</span></span>
