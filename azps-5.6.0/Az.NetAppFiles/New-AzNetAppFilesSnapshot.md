---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/new-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 47d1aeb2868e8f104791527636a67a31b1e42c1a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968445"
---
# <span data-ttu-id="ef44b-101">New-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="ef44b-101">New-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="ef44b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef44b-102">SYNOPSIS</span></span>
<span data-ttu-id="ef44b-103">Crea un nuovo snapshot dei file ANF (Azure NetApp).</span><span class="sxs-lookup"><span data-stu-id="ef44b-103">Creates a new Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="ef44b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ef44b-104">SYNTAX</span></span>

### <span data-ttu-id="ef44b-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ef44b-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesSnapshot -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -VolumeName <String> -Name <String> [-FileSystemId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef44b-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef44b-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesSnapshot -Name <String> [-Tag <Hashtable>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef44b-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ef44b-107">DESCRIPTION</span></span>
<span data-ttu-id="ef44b-108">Il cmdlet **New-AzNetAppFilesSnapshot** crea uno snapshot ANF.</span><span class="sxs-lookup"><span data-stu-id="ef44b-108">The **New-AzNetAppFilesSnapshot** cmdlet creates an ANF snapshot.</span></span>

## <span data-ttu-id="ef44b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ef44b-109">EXAMPLES</span></span>

### <span data-ttu-id="ef44b-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ef44b-110">Example 1</span></span>
```
PS C:\>New-AzNetAppFilesSnapshot -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -SnapshotName "MyAnfSnapshot" -FileSystemId "3e2773a7-2a72-d003-0637-1a8b1fa3eaaf"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume/snapshots/MyAnfSnapshot
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume/MyAnfSnapshot
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes/snapshots
Tags              :
SnapshotId        : ca7c4ebd-91cb-0e30-91f5-9154050033df
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
Created           :
ProvisioningState : Succeeded
```

<span data-ttu-id="ef44b-111">Questo comando crea il nuovo snapshot ANF "MyAnfSnapshot" all'interno del volume "MyAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="ef44b-111">This command creates the new ANF snapshot "MyAnfSnapshot" within the volume "MyAnfVolume".</span></span>

## <span data-ttu-id="ef44b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef44b-112">PARAMETERS</span></span>

### <span data-ttu-id="ef44b-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ef44b-113">-AccountName</span></span>
<span data-ttu-id="ef44b-114">Nome dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="ef44b-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="ef44b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef44b-115">-DefaultProfile</span></span>
<span data-ttu-id="ef44b-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ef44b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef44b-117">-FileSystemId</span><span class="sxs-lookup"><span data-stu-id="ef44b-117">-FileSystemId</span></span>
<span data-ttu-id="ef44b-118">ID del file system</span><span class="sxs-lookup"><span data-stu-id="ef44b-118">The file system id</span></span>

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

### <span data-ttu-id="ef44b-119">-Location</span><span class="sxs-lookup"><span data-stu-id="ef44b-119">-Location</span></span>
<span data-ttu-id="ef44b-120">Posizione della risorsa</span><span class="sxs-lookup"><span data-stu-id="ef44b-120">The location of the resource</span></span>

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

### <span data-ttu-id="ef44b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ef44b-121">-Name</span></span>
<span data-ttu-id="ef44b-122">Nome dello snapshot ANF</span><span class="sxs-lookup"><span data-stu-id="ef44b-122">The name of the ANF snapshot</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SnapshotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef44b-123">-PoolName</span><span class="sxs-lookup"><span data-stu-id="ef44b-123">-PoolName</span></span>
<span data-ttu-id="ef44b-124">Nome del pool ANF</span><span class="sxs-lookup"><span data-stu-id="ef44b-124">The name of the ANF pool</span></span>

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

### <span data-ttu-id="ef44b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef44b-125">-ResourceGroupName</span></span>
<span data-ttu-id="ef44b-126">Gruppo di risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="ef44b-126">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="ef44b-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="ef44b-127">-Tag</span></span>
<span data-ttu-id="ef44b-128">Tabella hash che rappresenta i tag di risorsa</span><span class="sxs-lookup"><span data-stu-id="ef44b-128">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="ef44b-129">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="ef44b-129">-VolumeName</span></span>
<span data-ttu-id="ef44b-130">Nome del volume ANF</span><span class="sxs-lookup"><span data-stu-id="ef44b-130">The name of the ANF volume</span></span>

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

### <span data-ttu-id="ef44b-131">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="ef44b-131">-VolumeObject</span></span>
<span data-ttu-id="ef44b-132">Il volume del nuovo oggetto snapshot</span><span class="sxs-lookup"><span data-stu-id="ef44b-132">The volume for the new snapshot object</span></span>

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

### <span data-ttu-id="ef44b-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ef44b-133">-Confirm</span></span>
<span data-ttu-id="ef44b-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef44b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef44b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef44b-135">-WhatIf</span></span>
<span data-ttu-id="ef44b-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ef44b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef44b-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ef44b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef44b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef44b-138">CommonParameters</span></span>
<span data-ttu-id="ef44b-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef44b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef44b-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ef44b-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef44b-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="ef44b-141">INPUTS</span></span>

### <span data-ttu-id="ef44b-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="ef44b-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="ef44b-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ef44b-143">OUTPUTS</span></span>

### <span data-ttu-id="ef44b-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="ef44b-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="ef44b-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="ef44b-145">NOTES</span></span>

## <span data-ttu-id="ef44b-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ef44b-146">RELATED LINKS</span></span>
