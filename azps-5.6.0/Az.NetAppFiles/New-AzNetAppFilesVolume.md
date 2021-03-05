---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/new-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
ms.openlocfilehash: c92e1b2536fab3584ebdf7f63b75bf264ff3eae4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968397"
---
# <span data-ttu-id="a7b9d-101">New-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="a7b9d-101">New-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="a7b9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7b9d-102">SYNOPSIS</span></span>
<span data-ttu-id="a7b9d-103">Crea un nuovo volume FILE (ANF) Di Azure NetApp.</span><span class="sxs-lookup"><span data-stu-id="a7b9d-103">Creates a new Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="a7b9d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a7b9d-104">SYNTAX</span></span>

### <span data-ttu-id="a7b9d-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a7b9d-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String> -PoolName <String>
 -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String> [-VolumeType <String>]
 -ServiceLevel <String> [-SnapshotId <String>] [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ReplicationObject <PSNetAppFilesReplicationObject>] [-Snapshot <PSNetAppFilesVolumeSnapshot>]
 [-Backup <PSNetAppFilesVolumeBackupProperties>] [-ProtocolType <String[]>] [-SnapshotDirectoryVisible]
 [-BackupId <String>] [-SecurityStyle <String>] [-ThroughputMibps <Double>] [-KerberosEnabled]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7b9d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7b9d-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesVolume -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String>
 -ServiceLevel <String> [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ReplicationObject <PSNetAppFilesReplicationObject>] [-Snapshot <PSNetAppFilesVolumeSnapshot>]
 [-Backup <PSNetAppFilesVolumeBackupProperties>] [-ProtocolType <String[]>] [-SnapshotDirectoryVisible]
 [-SecurityStyle <String>] [-ThroughputMibps <Double>] [-KerberosEnabled] [-Tag <Hashtable>]
 -PoolObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a7b9d-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a7b9d-107">DESCRIPTION</span></span>
<span data-ttu-id="a7b9d-108">Il cmdlet **New-AzNetAppFilesVolume** crea un volume ANF.</span><span class="sxs-lookup"><span data-stu-id="a7b9d-108">The **New-AzNetAppFilesVolume** cmdlet creates an ANF volume.</span></span>

## <span data-ttu-id="a7b9d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a7b9d-109">EXAMPLES</span></span>

### <span data-ttu-id="a7b9d-110">Esempio 1: Creare un volume ANF</span><span class="sxs-lookup"><span data-stu-id="a7b9d-110">Example 1: Create an ANF volume</span></span>
```
PS C:\>New-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume" -l "westus2" -CreationToken "MyAnfVolume" -UsageThreshold 1099511627776 -ServiceLevel "Premium" -SubnetId "/subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyVnetName/subnets/MySubNetName"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
CreationToken     : MyAnfVolume
ServiceLevel      : Premium
UsageThreshold    : 1099511627776
ProvisioningState : Succeeded
SubnetId          : /subscriptions/f557b96d-2308-4a18-aae1-b8f7e7e70cc7/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyVnetName/subnets/default
```

<span data-ttu-id="a7b9d-111">Questo comando crea il nuovo volume ANF "MyAnfVolume" all'interno del pool "MyAnfPool".</span><span class="sxs-lookup"><span data-stu-id="a7b9d-111">This command creates the new ANF volume "MyAnfVolume" within the pool "MyAnfPool".</span></span>

## <span data-ttu-id="a7b9d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a7b9d-112">PARAMETERS</span></span>

### <span data-ttu-id="a7b9d-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a7b9d-113">-AccountName</span></span>
<span data-ttu-id="a7b9d-114">Nome dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="a7b9d-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="a7b9d-115">-Backup</span><span class="sxs-lookup"><span data-stu-id="a7b9d-115">-Backup</span></span>
<span data-ttu-id="a7b9d-116">Matrice di tabella hash che rappresenta l'oggetto di backup</span><span class="sxs-lookup"><span data-stu-id="a7b9d-116">A hashtable array which represents the backup object</span></span>

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

### <span data-ttu-id="a7b9d-117">-BackupId</span><span class="sxs-lookup"><span data-stu-id="a7b9d-117">-BackupId</span></span>
<span data-ttu-id="a7b9d-118">ID backup.</span><span class="sxs-lookup"><span data-stu-id="a7b9d-118">Backup ID.</span></span> <span data-ttu-id="a7b9d-119">UUID v4 o identificatore di risorsa usato per identificare il backup</span><span class="sxs-lookup"><span data-stu-id="a7b9d-119">UUID v4 or resource identifier used to identify the Backup</span></span>

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

### <span data-ttu-id="a7b9d-120">-CreationToken</span><span class="sxs-lookup"><span data-stu-id="a7b9d-120">-CreationToken</span></span>
<span data-ttu-id="a7b9d-121">Un percorso file univoco per il volume</span><span class="sxs-lookup"><span data-stu-id="a7b9d-121">A unique file path for the volume</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7b9d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7b9d-122">-DefaultProfile</span></span>
<span data-ttu-id="a7b9d-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a7b9d-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7b9d-124">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="a7b9d-124">-ExportPolicy</span></span>
<span data-ttu-id="a7b9d-125">Matrice di tabella hash che rappresenta il criterio di esportazione</span><span class="sxs-lookup"><span data-stu-id="a7b9d-125">A hashtable array which represents the export policy</span></span>

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

### <span data-ttu-id="a7b9d-126">-KerberosEnabled</span><span class="sxs-lookup"><span data-stu-id="a7b9d-126">-KerberosEnabled</span></span>
<span data-ttu-id="a7b9d-127">Descrivere se un volume è abilitato per Kerberos</span><span class="sxs-lookup"><span data-stu-id="a7b9d-127">Describe if a volume is Kerberos Enabled</span></span>

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

### <span data-ttu-id="a7b9d-128">-Location</span><span class="sxs-lookup"><span data-stu-id="a7b9d-128">-Location</span></span>
<span data-ttu-id="a7b9d-129">Posizione della risorsa</span><span class="sxs-lookup"><span data-stu-id="a7b9d-129">The location of the resource</span></span>

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

### <span data-ttu-id="a7b9d-130">-Name</span><span class="sxs-lookup"><span data-stu-id="a7b9d-130">-Name</span></span>
<span data-ttu-id="a7b9d-131">Nome del volume ANF</span><span class="sxs-lookup"><span data-stu-id="a7b9d-131">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7b9d-132">-PoolName</span><span class="sxs-lookup"><span data-stu-id="a7b9d-132">-PoolName</span></span>
<span data-ttu-id="a7b9d-133">Nome del pool ANF</span><span class="sxs-lookup"><span data-stu-id="a7b9d-133">The name of the ANF pool</span></span>

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

### <span data-ttu-id="a7b9d-134">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="a7b9d-134">-PoolObject</span></span>
<span data-ttu-id="a7b9d-135">Pool per il nuovo oggetto volume</span><span class="sxs-lookup"><span data-stu-id="a7b9d-135">The pool for the new volume object</span></span>

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

### <span data-ttu-id="a7b9d-136">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="a7b9d-136">-ProtocolType</span></span>
<span data-ttu-id="a7b9d-137">Matrice di tabella hash che rappresenta il criterio di esportazione</span><span class="sxs-lookup"><span data-stu-id="a7b9d-137">A hashtable array which represents the export policy</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7b9d-138">-ReplicationObject</span><span class="sxs-lookup"><span data-stu-id="a7b9d-138">-ReplicationObject</span></span>
<span data-ttu-id="a7b9d-139">Matrice di tabella hash che rappresenta l'oggetto replica</span><span class="sxs-lookup"><span data-stu-id="a7b9d-139">A hashtable array which represents the replication object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesReplicationObject
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7b9d-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7b9d-140">-ResourceGroupName</span></span>
<span data-ttu-id="a7b9d-141">Gruppo di risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="a7b9d-141">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="a7b9d-142">-SecurityStyle</span><span class="sxs-lookup"><span data-stu-id="a7b9d-142">-SecurityStyle</span></span>
<span data-ttu-id="a7b9d-143">Stile di sicurezza del volume.</span><span class="sxs-lookup"><span data-stu-id="a7b9d-143">The security style of volume.</span></span> <span data-ttu-id="a7b9d-144">I valori possibili includono: 'ntfs', 'unix'</span><span class="sxs-lookup"><span data-stu-id="a7b9d-144">Possible values include: 'ntfs', 'unix'</span></span>

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

### <span data-ttu-id="a7b9d-145">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="a7b9d-145">-ServiceLevel</span></span>
<span data-ttu-id="a7b9d-146">Livello di servizio del volume ANF</span><span class="sxs-lookup"><span data-stu-id="a7b9d-146">The service level of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7b9d-147">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="a7b9d-147">-Snapshot</span></span>
<span data-ttu-id="a7b9d-148">Matrice di tabella hash che rappresenta l'oggetto snapshot</span><span class="sxs-lookup"><span data-stu-id="a7b9d-148">A hashtable array which represents the snapshot object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolumeSnapshot
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7b9d-149">-SnapshotDirectoryVisible</span><span class="sxs-lookup"><span data-stu-id="a7b9d-149">-SnapshotDirectoryVisible</span></span>
<span data-ttu-id="a7b9d-150">Se abilitato (true), il volume conterrà una directory .snapshot di sola lettura che fornisce l'accesso a ognuno degli snapshot del volume (impostazione predefinita su true)</span><span class="sxs-lookup"><span data-stu-id="a7b9d-150">If enabled (true) the volume will contain a read-only .snapshot directory which provides access to each of the volume's snapshots (default to true)</span></span>

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

### <span data-ttu-id="a7b9d-151">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="a7b9d-151">-SnapshotId</span></span>
<span data-ttu-id="a7b9d-152">Creare il volume da uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="a7b9d-152">Create volume from a snapshot.</span></span> <span data-ttu-id="a7b9d-153">UUID v4 o identificatore di risorsa usato per identificare lo snapshot</span><span class="sxs-lookup"><span data-stu-id="a7b9d-153">UUID v4 or resource identifier used to identify the Snapshot</span></span>

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

### <span data-ttu-id="a7b9d-154">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="a7b9d-154">-SubnetId</span></span>
<span data-ttu-id="a7b9d-155">URI della risorsa Azure per una subnet delegata</span><span class="sxs-lookup"><span data-stu-id="a7b9d-155">The Azure Resource URI for a delegated subnet</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7b9d-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="a7b9d-156">-Tag</span></span>
<span data-ttu-id="a7b9d-157">Tabella hash che rappresenta i tag di risorsa</span><span class="sxs-lookup"><span data-stu-id="a7b9d-157">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="a7b9d-158">-ThroughputMibps</span><span class="sxs-lookup"><span data-stu-id="a7b9d-158">-ThroughputMibps</span></span>
<span data-ttu-id="a7b9d-159">Velocità effettiva massima in Mibps che può essere raggiunta da questo volume</span><span class="sxs-lookup"><span data-stu-id="a7b9d-159">Maximum throughput in Mibps that can be achieved by this volume</span></span>

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

### <span data-ttu-id="a7b9d-160">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="a7b9d-160">-UsageThreshold</span></span>
<span data-ttu-id="a7b9d-161">Quota di archiviazione massima consentita per un file system in byte</span><span class="sxs-lookup"><span data-stu-id="a7b9d-161">The maximum storage quota allowed for a file system in bytes</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7b9d-162">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="a7b9d-162">-VolumeType</span></span>
<span data-ttu-id="a7b9d-163">Il tipo di volume ANF</span><span class="sxs-lookup"><span data-stu-id="a7b9d-163">The type of the ANF volume</span></span>

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

### <span data-ttu-id="a7b9d-164">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a7b9d-164">-Confirm</span></span>
<span data-ttu-id="a7b9d-165">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7b9d-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7b9d-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7b9d-166">-WhatIf</span></span>
<span data-ttu-id="a7b9d-167">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a7b9d-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7b9d-168">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a7b9d-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7b9d-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7b9d-169">CommonParameters</span></span>
<span data-ttu-id="a7b9d-170">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7b9d-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7b9d-171">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a7b9d-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7b9d-172">INPUT</span><span class="sxs-lookup"><span data-stu-id="a7b9d-172">INPUTS</span></span>

### <span data-ttu-id="a7b9d-173">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="a7b9d-173">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="a7b9d-174">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a7b9d-174">OUTPUTS</span></span>

### <span data-ttu-id="a7b9d-175">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="a7b9d-175">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="a7b9d-176">NOTE</span><span class="sxs-lookup"><span data-stu-id="a7b9d-176">NOTES</span></span>

## <span data-ttu-id="a7b9d-177">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a7b9d-177">RELATED LINKS</span></span>
