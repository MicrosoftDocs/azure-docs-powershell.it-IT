---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
ms.openlocfilehash: 2326551a2b6a03e1904e8d0d90663ee796ccaa46
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359897"
---
# <span data-ttu-id="296a5-101">New-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="296a5-101">New-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="296a5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="296a5-102">SYNOPSIS</span></span>
<span data-ttu-id="296a5-103">Crea un nuovo volume di file NetApp (ANF) di Azure.</span><span class="sxs-lookup"><span data-stu-id="296a5-103">Creates a new Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="296a5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="296a5-104">SYNTAX</span></span>

### <span data-ttu-id="296a5-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="296a5-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String> -PoolName <String>
 -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String> [-VolumeType <String>]
 -ServiceLevel <String> [-SnapshotId <String>] [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ReplicationObject <PSNetAppFilesReplicationObject>] [-Snapshot <PSNetAppFilesVolumeSnapshot>]
 [-Backup <PSNetAppFilesVolumeBackupProperties>] [-ProtocolType <String[]>] [-SnapshotDirectoryVisible]
 [-BackupId <String>] [-SecurityStyle <String>] [-ThroughputMibps <Double>] [-KerberosEnabled]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="296a5-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="296a5-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesVolume -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String>
 -ServiceLevel <String> [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ReplicationObject <PSNetAppFilesReplicationObject>] [-Snapshot <PSNetAppFilesVolumeSnapshot>]
 [-Backup <PSNetAppFilesVolumeBackupProperties>] [-ProtocolType <String[]>] [-SnapshotDirectoryVisible]
 [-SecurityStyle <String>] [-ThroughputMibps <Double>] [-KerberosEnabled] [-Tag <Hashtable>]
 -PoolObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="296a5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="296a5-107">DESCRIPTION</span></span>
<span data-ttu-id="296a5-108">Il cmdlet **New-AzNetAppFilesVolume** crea un volume di ANF.</span><span class="sxs-lookup"><span data-stu-id="296a5-108">The **New-AzNetAppFilesVolume** cmdlet creates an ANF volume.</span></span>

## <span data-ttu-id="296a5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="296a5-109">EXAMPLES</span></span>

### <span data-ttu-id="296a5-110">Esempio 1: creare un volume ANF</span><span class="sxs-lookup"><span data-stu-id="296a5-110">Example 1: Create an ANF volume</span></span>
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

<span data-ttu-id="296a5-111">Questo comando crea il nuovo volume ANF "MyAnfVolume" nel pool "MyAnfPool".</span><span class="sxs-lookup"><span data-stu-id="296a5-111">This command creates the new ANF volume "MyAnfVolume" within the pool "MyAnfPool".</span></span>

## <span data-ttu-id="296a5-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="296a5-112">PARAMETERS</span></span>

### <span data-ttu-id="296a5-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="296a5-113">-AccountName</span></span>
<span data-ttu-id="296a5-114">Nome dell'account di ANF</span><span class="sxs-lookup"><span data-stu-id="296a5-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="296a5-115">-Backup</span><span class="sxs-lookup"><span data-stu-id="296a5-115">-Backup</span></span>
<span data-ttu-id="296a5-116">Matrice Hashtable che rappresenta l'oggetto di backup</span><span class="sxs-lookup"><span data-stu-id="296a5-116">A hashtable array which represents the backup object</span></span>

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

### <span data-ttu-id="296a5-117">-BackupId</span><span class="sxs-lookup"><span data-stu-id="296a5-117">-BackupId</span></span>
<span data-ttu-id="296a5-118">ID backup.</span><span class="sxs-lookup"><span data-stu-id="296a5-118">Backup ID.</span></span> <span data-ttu-id="296a5-119">UUID V4 o identificatore delle risorse usato per identificare il backup</span><span class="sxs-lookup"><span data-stu-id="296a5-119">UUID v4 or resource identifier used to identify the Backup</span></span>

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

### <span data-ttu-id="296a5-120">-CreationToken</span><span class="sxs-lookup"><span data-stu-id="296a5-120">-CreationToken</span></span>
<span data-ttu-id="296a5-121">Percorso file univoco per il volume</span><span class="sxs-lookup"><span data-stu-id="296a5-121">A unique file path for the volume</span></span>

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

### <span data-ttu-id="296a5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="296a5-122">-DefaultProfile</span></span>
<span data-ttu-id="296a5-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="296a5-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="296a5-124">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="296a5-124">-ExportPolicy</span></span>
<span data-ttu-id="296a5-125">Matrice Hashtable che rappresenta i criteri di esportazione</span><span class="sxs-lookup"><span data-stu-id="296a5-125">A hashtable array which represents the export policy</span></span>

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

### <span data-ttu-id="296a5-126">-KerberosEnabled</span><span class="sxs-lookup"><span data-stu-id="296a5-126">-KerberosEnabled</span></span>
<span data-ttu-id="296a5-127">Descrivi se un volume è abilitato per Kerberos</span><span class="sxs-lookup"><span data-stu-id="296a5-127">Describe if a volume is Kerberos Enabled</span></span>

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

### <span data-ttu-id="296a5-128">-Posizione</span><span class="sxs-lookup"><span data-stu-id="296a5-128">-Location</span></span>
<span data-ttu-id="296a5-129">Posizione della risorsa</span><span class="sxs-lookup"><span data-stu-id="296a5-129">The location of the resource</span></span>

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

### <span data-ttu-id="296a5-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="296a5-130">-Name</span></span>
<span data-ttu-id="296a5-131">Nome del volume di ANF</span><span class="sxs-lookup"><span data-stu-id="296a5-131">The name of the ANF volume</span></span>

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

### <span data-ttu-id="296a5-132">-PoolName</span><span class="sxs-lookup"><span data-stu-id="296a5-132">-PoolName</span></span>
<span data-ttu-id="296a5-133">Nome del pool di ANF</span><span class="sxs-lookup"><span data-stu-id="296a5-133">The name of the ANF pool</span></span>

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

### <span data-ttu-id="296a5-134">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="296a5-134">-PoolObject</span></span>
<span data-ttu-id="296a5-135">Pool per il nuovo oggetto volume</span><span class="sxs-lookup"><span data-stu-id="296a5-135">The pool for the new volume object</span></span>

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

### <span data-ttu-id="296a5-136">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="296a5-136">-ProtocolType</span></span>
<span data-ttu-id="296a5-137">Matrice Hashtable che rappresenta i criteri di esportazione</span><span class="sxs-lookup"><span data-stu-id="296a5-137">A hashtable array which represents the export policy</span></span>

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

### <span data-ttu-id="296a5-138">-ReplicationObject</span><span class="sxs-lookup"><span data-stu-id="296a5-138">-ReplicationObject</span></span>
<span data-ttu-id="296a5-139">Matrice Hashtable che rappresenta l'oggetto Replication</span><span class="sxs-lookup"><span data-stu-id="296a5-139">A hashtable array which represents the replication object</span></span>

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

### <span data-ttu-id="296a5-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="296a5-140">-ResourceGroupName</span></span>
<span data-ttu-id="296a5-141">Gruppo risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="296a5-141">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="296a5-142">-SecurityStyle</span><span class="sxs-lookup"><span data-stu-id="296a5-142">-SecurityStyle</span></span>
<span data-ttu-id="296a5-143">Stile di sicurezza di volume.</span><span class="sxs-lookup"><span data-stu-id="296a5-143">The security style of volume.</span></span> <span data-ttu-id="296a5-144">I valori possibili includono:' NTFS ',' Unix '</span><span class="sxs-lookup"><span data-stu-id="296a5-144">Possible values include: 'ntfs', 'unix'</span></span>

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

### <span data-ttu-id="296a5-145">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="296a5-145">-ServiceLevel</span></span>
<span data-ttu-id="296a5-146">Livello di servizio del volume ANF</span><span class="sxs-lookup"><span data-stu-id="296a5-146">The service level of the ANF volume</span></span>

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

### <span data-ttu-id="296a5-147">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="296a5-147">-Snapshot</span></span>
<span data-ttu-id="296a5-148">Matrice Hashtable che rappresenta l'oggetto snapshot</span><span class="sxs-lookup"><span data-stu-id="296a5-148">A hashtable array which represents the snapshot object</span></span>

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

### <span data-ttu-id="296a5-149">-SnapshotDirectoryVisible</span><span class="sxs-lookup"><span data-stu-id="296a5-149">-SnapshotDirectoryVisible</span></span>
<span data-ttu-id="296a5-150">Se Enabled (true) il volume conterrà una directory di sola lettura. snapshot che consente l'accesso a ogni snapshot del volume (impostazione predefinita: true)</span><span class="sxs-lookup"><span data-stu-id="296a5-150">If enabled (true) the volume will contain a read-only .snapshot directory which provides access to each of the volume's snapshots (default to true)</span></span>

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

### <span data-ttu-id="296a5-151">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="296a5-151">-SnapshotId</span></span>
<span data-ttu-id="296a5-152">Creare un volume da uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="296a5-152">Create volume from a snapshot.</span></span> <span data-ttu-id="296a5-153">UUID V4 o identificatore delle risorse usato per identificare lo snapshot</span><span class="sxs-lookup"><span data-stu-id="296a5-153">UUID v4 or resource identifier used to identify the Snapshot</span></span>

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

### <span data-ttu-id="296a5-154">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="296a5-154">-SubnetId</span></span>
<span data-ttu-id="296a5-155">URI di risorsa di Azure per una subnet delegata</span><span class="sxs-lookup"><span data-stu-id="296a5-155">The Azure Resource URI for a delegated subnet</span></span>

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

### <span data-ttu-id="296a5-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="296a5-156">-Tag</span></span>
<span data-ttu-id="296a5-157">Hashtable che rappresenta i tag delle risorse</span><span class="sxs-lookup"><span data-stu-id="296a5-157">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="296a5-158">-ThroughputMibps</span><span class="sxs-lookup"><span data-stu-id="296a5-158">-ThroughputMibps</span></span>
<span data-ttu-id="296a5-159">Velocità effettiva massima in Mibps che può essere ottenuta con questo volume</span><span class="sxs-lookup"><span data-stu-id="296a5-159">Maximum throughput in Mibps that can be achieved by this volume</span></span>

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

### <span data-ttu-id="296a5-160">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="296a5-160">-UsageThreshold</span></span>
<span data-ttu-id="296a5-161">La quota di archiviazione massima consentita per un file System in byte</span><span class="sxs-lookup"><span data-stu-id="296a5-161">The maximum storage quota allowed for a file system in bytes</span></span>

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

### <span data-ttu-id="296a5-162">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="296a5-162">-VolumeType</span></span>
<span data-ttu-id="296a5-163">Tipo di volume ANF</span><span class="sxs-lookup"><span data-stu-id="296a5-163">The type of the ANF volume</span></span>

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

### <span data-ttu-id="296a5-164">-Confermare</span><span class="sxs-lookup"><span data-stu-id="296a5-164">-Confirm</span></span>
<span data-ttu-id="296a5-165">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="296a5-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="296a5-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="296a5-166">-WhatIf</span></span>
<span data-ttu-id="296a5-167">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="296a5-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="296a5-168">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="296a5-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="296a5-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="296a5-169">CommonParameters</span></span>
<span data-ttu-id="296a5-170">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="296a5-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="296a5-171">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="296a5-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="296a5-172">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="296a5-172">INPUTS</span></span>

### <span data-ttu-id="296a5-173">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="296a5-173">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="296a5-174">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="296a5-174">OUTPUTS</span></span>

### <span data-ttu-id="296a5-175">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="296a5-175">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="296a5-176">Note</span><span class="sxs-lookup"><span data-stu-id="296a5-176">NOTES</span></span>

## <span data-ttu-id="296a5-177">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="296a5-177">RELATED LINKS</span></span>
