---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
ms.openlocfilehash: dce91ee25cac4a716dc604e38f1ac38e5a3f3f1d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201851"
---
# <span data-ttu-id="d3a35-101">New-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="d3a35-101">New-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="d3a35-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d3a35-102">SYNOPSIS</span></span>
<span data-ttu-id="d3a35-103">Crea un nuovo volume di file NetApp (ANF) di Azure.</span><span class="sxs-lookup"><span data-stu-id="d3a35-103">Creates a new Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="d3a35-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d3a35-104">SYNTAX</span></span>

### <span data-ttu-id="d3a35-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d3a35-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String> -PoolName <String>
 -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String> [-VolumeType <String>]
 -ServiceLevel <String> [-SnapshotId <String>] [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ReplicationObject <PSNetAppFilesReplicationObject>] [-ProtocolType <String[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3a35-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3a35-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesVolume -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String>
 -ServiceLevel <String> [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ReplicationObject <PSNetAppFilesReplicationObject>] [-ProtocolType <String[]>] [-Tag <Hashtable>]
 -PoolObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d3a35-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3a35-107">DESCRIPTION</span></span>
<span data-ttu-id="d3a35-108">Il cmdlet **New-AzNetAppFilesVolume** crea un volume di ANF.</span><span class="sxs-lookup"><span data-stu-id="d3a35-108">The **New-AzNetAppFilesVolume** cmdlet creates an ANF volume.</span></span>

## <span data-ttu-id="d3a35-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d3a35-109">EXAMPLES</span></span>

### <span data-ttu-id="d3a35-110">Esempio 1: creare un volume ANF</span><span class="sxs-lookup"><span data-stu-id="d3a35-110">Example 1: Create an ANF volume</span></span>
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

<span data-ttu-id="d3a35-111">Questo comando crea il nuovo volume ANF "MyAnfVolume" nel pool "MyAnfPool".</span><span class="sxs-lookup"><span data-stu-id="d3a35-111">This command creates the new ANF volume "MyAnfVolume" within the pool "MyAnfPool".</span></span>

## <span data-ttu-id="d3a35-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d3a35-112">PARAMETERS</span></span>

### <span data-ttu-id="d3a35-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d3a35-113">-AccountName</span></span>
<span data-ttu-id="d3a35-114">Nome dell'account di ANF</span><span class="sxs-lookup"><span data-stu-id="d3a35-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="d3a35-115">-CreationToken</span><span class="sxs-lookup"><span data-stu-id="d3a35-115">-CreationToken</span></span>
<span data-ttu-id="d3a35-116">Percorso file univoco per il volume</span><span class="sxs-lookup"><span data-stu-id="d3a35-116">A unique file path for the volume</span></span>

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

### <span data-ttu-id="d3a35-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3a35-117">-DefaultProfile</span></span>
<span data-ttu-id="d3a35-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d3a35-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3a35-119">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="d3a35-119">-ExportPolicy</span></span>
<span data-ttu-id="d3a35-120">Matrice Hashtable che rappresenta i criteri di esportazione</span><span class="sxs-lookup"><span data-stu-id="d3a35-120">A hashtable array which represents the export policy</span></span>

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

### <span data-ttu-id="d3a35-121">-Posizione</span><span class="sxs-lookup"><span data-stu-id="d3a35-121">-Location</span></span>
<span data-ttu-id="d3a35-122">Posizione della risorsa</span><span class="sxs-lookup"><span data-stu-id="d3a35-122">The location of the resource</span></span>

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

### <span data-ttu-id="d3a35-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="d3a35-123">-Name</span></span>
<span data-ttu-id="d3a35-124">Nome del volume di ANF</span><span class="sxs-lookup"><span data-stu-id="d3a35-124">The name of the ANF volume</span></span>

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

### <span data-ttu-id="d3a35-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="d3a35-125">-PoolName</span></span>
<span data-ttu-id="d3a35-126">Nome del pool di ANF</span><span class="sxs-lookup"><span data-stu-id="d3a35-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="d3a35-127">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="d3a35-127">-PoolObject</span></span>
<span data-ttu-id="d3a35-128">Pool per il nuovo oggetto volume</span><span class="sxs-lookup"><span data-stu-id="d3a35-128">The pool for the new volume object</span></span>

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

### <span data-ttu-id="d3a35-129">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="d3a35-129">-ProtocolType</span></span>
<span data-ttu-id="d3a35-130">Matrice Hashtable che rappresenta i criteri di esportazione</span><span class="sxs-lookup"><span data-stu-id="d3a35-130">A hashtable array which represents the export policy</span></span>

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

### <span data-ttu-id="d3a35-131">-ReplicationObject</span><span class="sxs-lookup"><span data-stu-id="d3a35-131">-ReplicationObject</span></span>
<span data-ttu-id="d3a35-132">Matrice Hashtable che rappresenta l'oggetto Replication</span><span class="sxs-lookup"><span data-stu-id="d3a35-132">A hashtable array which represents the replication object</span></span>

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

### <span data-ttu-id="d3a35-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3a35-133">-ResourceGroupName</span></span>
<span data-ttu-id="d3a35-134">Gruppo risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="d3a35-134">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="d3a35-135">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="d3a35-135">-ServiceLevel</span></span>
<span data-ttu-id="d3a35-136">Livello di servizio del volume ANF</span><span class="sxs-lookup"><span data-stu-id="d3a35-136">The service level of the ANF volume</span></span>

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

### <span data-ttu-id="d3a35-137">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="d3a35-137">-SnapshotId</span></span>
<span data-ttu-id="d3a35-138">Creare un volume da uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="d3a35-138">Create volume from a snapshot.</span></span> <span data-ttu-id="d3a35-139">UUID V4 o identificatore delle risorse usato per identificare lo snapshot</span><span class="sxs-lookup"><span data-stu-id="d3a35-139">UUID v4 or resource identifier used to identify the Snapshot</span></span>

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

### <span data-ttu-id="d3a35-140">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="d3a35-140">-SubnetId</span></span>
<span data-ttu-id="d3a35-141">URI di risorsa di Azure per una subnet delegata</span><span class="sxs-lookup"><span data-stu-id="d3a35-141">The Azure Resource URI for a delegated subnet</span></span>

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

### <span data-ttu-id="d3a35-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="d3a35-142">-Tag</span></span>
<span data-ttu-id="d3a35-143">Hashtable che rappresenta i tag delle risorse</span><span class="sxs-lookup"><span data-stu-id="d3a35-143">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="d3a35-144">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="d3a35-144">-UsageThreshold</span></span>
<span data-ttu-id="d3a35-145">La quota di archiviazione massima consentita per un file System in byte</span><span class="sxs-lookup"><span data-stu-id="d3a35-145">The maximum storage quota allowed for a file system in bytes</span></span>

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

### <span data-ttu-id="d3a35-146">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="d3a35-146">-VolumeType</span></span>
<span data-ttu-id="d3a35-147">Tipo di volume ANF</span><span class="sxs-lookup"><span data-stu-id="d3a35-147">The type of the ANF volume</span></span>

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

### <span data-ttu-id="d3a35-148">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d3a35-148">-Confirm</span></span>
<span data-ttu-id="d3a35-149">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3a35-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3a35-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3a35-150">-WhatIf</span></span>
<span data-ttu-id="d3a35-151">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d3a35-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3a35-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d3a35-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3a35-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3a35-153">CommonParameters</span></span>
<span data-ttu-id="d3a35-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3a35-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3a35-155">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3a35-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3a35-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d3a35-156">INPUTS</span></span>

### <span data-ttu-id="d3a35-157">System. String</span><span class="sxs-lookup"><span data-stu-id="d3a35-157">System.String</span></span>

### <span data-ttu-id="d3a35-158">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="d3a35-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="d3a35-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d3a35-159">OUTPUTS</span></span>

### <span data-ttu-id="d3a35-160">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="d3a35-160">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="d3a35-161">Note</span><span class="sxs-lookup"><span data-stu-id="d3a35-161">NOTES</span></span>

## <span data-ttu-id="d3a35-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d3a35-162">RELATED LINKS</span></span>
