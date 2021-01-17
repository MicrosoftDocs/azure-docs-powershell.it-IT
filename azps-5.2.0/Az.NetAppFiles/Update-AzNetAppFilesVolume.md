---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
ms.openlocfilehash: 2d3b212ea24c9dda665d2e2ec2516f25a59318b2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335272"
---
# <span data-ttu-id="44db3-101">Update-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="44db3-101">Update-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="44db3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="44db3-102">SYNOPSIS</span></span>
<span data-ttu-id="44db3-103">Aggiorna un volume di Azure NetApp file (ANF) in base ai modificatori facoltativi forniti.</span><span class="sxs-lookup"><span data-stu-id="44db3-103">Updates an Azure NetApp Files (ANF) volume according to the optional modifiers provided.</span></span>

## <span data-ttu-id="44db3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="44db3-104">SYNTAX</span></span>

### <span data-ttu-id="44db3-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="44db3-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="44db3-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="44db3-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] -PoolObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44db3-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="44db3-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44db3-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="44db3-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] -InputObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44db3-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="44db3-109">DESCRIPTION</span></span>
<span data-ttu-id="44db3-110">Il cmdlet **Update-AzNetAppFilesVolume** aggiorna un volume di ANF.</span><span class="sxs-lookup"><span data-stu-id="44db3-110">The **Update-AzNetAppFilesVolume** cmdlet updates an ANF volume.</span></span>

## <span data-ttu-id="44db3-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="44db3-111">EXAMPLES</span></span>

### <span data-ttu-id="44db3-112">Esempio 1: aggiornare un volume di ANF</span><span class="sxs-lookup"><span data-stu-id="44db3-112">Example 1: Update an ANF volume</span></span>
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

<span data-ttu-id="44db3-113">Questo comando Aggiorna il volume ANF "MyAnfVolume" con le nuove dimensioni di UsageThreshold.</span><span class="sxs-lookup"><span data-stu-id="44db3-113">This command updates the ANF volume "MyAnfVolume" with the new UsageThreshold size.</span></span>

## <span data-ttu-id="44db3-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="44db3-114">PARAMETERS</span></span>

### <span data-ttu-id="44db3-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="44db3-115">-AccountName</span></span>
<span data-ttu-id="44db3-116">Nome dell'account di ANF</span><span class="sxs-lookup"><span data-stu-id="44db3-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="44db3-117">-Backup</span><span class="sxs-lookup"><span data-stu-id="44db3-117">-Backup</span></span>
<span data-ttu-id="44db3-118">Matrice Hashtable che rappresenta l'oggetto di backup</span><span class="sxs-lookup"><span data-stu-id="44db3-118">A hashtable array which represents the backup object</span></span>

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

### <span data-ttu-id="44db3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44db3-119">-DefaultProfile</span></span>
<span data-ttu-id="44db3-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="44db3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44db3-121">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="44db3-121">-ExportPolicy</span></span>
<span data-ttu-id="44db3-122">Matrice Hashtable che rappresenta i criteri di esportazione</span><span class="sxs-lookup"><span data-stu-id="44db3-122">A hashtable array which represents the export policy</span></span>

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

### <span data-ttu-id="44db3-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44db3-123">-InputObject</span></span>
<span data-ttu-id="44db3-124">Oggetto volume da aggiornare</span><span class="sxs-lookup"><span data-stu-id="44db3-124">The volume object to update</span></span>

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

### <span data-ttu-id="44db3-125">-Posizione</span><span class="sxs-lookup"><span data-stu-id="44db3-125">-Location</span></span>
<span data-ttu-id="44db3-126">Posizione della risorsa</span><span class="sxs-lookup"><span data-stu-id="44db3-126">The location of the resource</span></span>

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

### <span data-ttu-id="44db3-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="44db3-127">-Name</span></span>
<span data-ttu-id="44db3-128">Nome del volume di ANF</span><span class="sxs-lookup"><span data-stu-id="44db3-128">The name of the ANF volume</span></span>

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

### <span data-ttu-id="44db3-129">-PoolName</span><span class="sxs-lookup"><span data-stu-id="44db3-129">-PoolName</span></span>
<span data-ttu-id="44db3-130">Nome del pool di ANF</span><span class="sxs-lookup"><span data-stu-id="44db3-130">The name of the ANF pool</span></span>

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

### <span data-ttu-id="44db3-131">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="44db3-131">-PoolObject</span></span>
<span data-ttu-id="44db3-132">Oggetto pool che contiene il volume da aggiornare</span><span class="sxs-lookup"><span data-stu-id="44db3-132">The pool object containing the volume to update</span></span>

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

### <span data-ttu-id="44db3-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44db3-133">-ResourceGroupName</span></span>
<span data-ttu-id="44db3-134">Gruppo risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="44db3-134">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="44db3-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="44db3-135">-ResourceId</span></span>
<span data-ttu-id="44db3-136">ID risorsa del volume ANF</span><span class="sxs-lookup"><span data-stu-id="44db3-136">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="44db3-137">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="44db3-137">-ServiceLevel</span></span>
<span data-ttu-id="44db3-138">Livello di servizio del volume ANF</span><span class="sxs-lookup"><span data-stu-id="44db3-138">The service level of the ANF volume</span></span>

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

### <span data-ttu-id="44db3-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="44db3-139">-Tag</span></span>
<span data-ttu-id="44db3-140">Hashtable che rappresenta i tag delle risorse</span><span class="sxs-lookup"><span data-stu-id="44db3-140">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="44db3-141">-ThroughputMibps</span><span class="sxs-lookup"><span data-stu-id="44db3-141">-ThroughputMibps</span></span>
<span data-ttu-id="44db3-142">Velocità effettiva massima in Mibps che può essere ottenuta con questo volume</span><span class="sxs-lookup"><span data-stu-id="44db3-142">Maximum throughput in Mibps that can be achieved by this volume</span></span>

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

### <span data-ttu-id="44db3-143">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="44db3-143">-UsageThreshold</span></span>
<span data-ttu-id="44db3-144">La quota di archiviazione massima consentita per un file System in byte</span><span class="sxs-lookup"><span data-stu-id="44db3-144">The maximum storage quota allowed for a file system in bytes</span></span>

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

### <span data-ttu-id="44db3-145">-Confermare</span><span class="sxs-lookup"><span data-stu-id="44db3-145">-Confirm</span></span>
<span data-ttu-id="44db3-146">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44db3-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44db3-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44db3-147">-WhatIf</span></span>
<span data-ttu-id="44db3-148">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="44db3-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44db3-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="44db3-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44db3-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44db3-150">CommonParameters</span></span>
<span data-ttu-id="44db3-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44db3-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44db3-152">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="44db3-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44db3-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="44db3-153">INPUTS</span></span>

### <span data-ttu-id="44db3-154">System. String</span><span class="sxs-lookup"><span data-stu-id="44db3-154">System.String</span></span>

### <span data-ttu-id="44db3-155">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="44db3-155">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="44db3-156">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="44db3-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="44db3-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="44db3-157">OUTPUTS</span></span>

### <span data-ttu-id="44db3-158">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="44db3-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="44db3-159">Note</span><span class="sxs-lookup"><span data-stu-id="44db3-159">NOTES</span></span>

## <span data-ttu-id="44db3-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="44db3-160">RELATED LINKS</span></span>
