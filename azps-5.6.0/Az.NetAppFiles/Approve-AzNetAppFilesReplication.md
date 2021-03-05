---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/approve-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Approve-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Approve-AzNetAppFilesReplication.md
ms.openlocfilehash: ac562f95ad6d5cbc97e31cd3832b90d2aa2362e3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968701"
---
# <span data-ttu-id="10538-101">Approve-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="10538-101">Approve-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="10538-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10538-102">SYNOPSIS</span></span>
<span data-ttu-id="10538-103">Approvare/autorizzare la connessione di replica nel volume di origine</span><span class="sxs-lookup"><span data-stu-id="10538-103">Approve/Authorize replication connection on the source volume</span></span>

## <span data-ttu-id="10538-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="10538-104">SYNTAX</span></span>

### <span data-ttu-id="10538-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="10538-105">ByFieldsParameterSet (Default)</span></span>
```
Approve-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> -DataProtectionVolumeId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10538-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="10538-106">ByResourceIdParameterSet</span></span>
```
Approve-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10538-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="10538-107">ByObjectParameterSet</span></span>
```
Approve-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10538-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="10538-108">DESCRIPTION</span></span>
<span data-ttu-id="10538-109">Approvare la connessione di replica nel volume di origine</span><span class="sxs-lookup"><span data-stu-id="10538-109">Approve the replication connection on the source volume</span></span>

## <span data-ttu-id="10538-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="10538-110">EXAMPLES</span></span>

### <span data-ttu-id="10538-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="10538-111">Example 1</span></span>
```powershell
PS C:\> Approve-AzNetAppFilesReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -DataProtectionVolumeId "MyDestinationVolumeId"

Output:
remoteVolumeResourceId          : resourceId
```

<span data-ttu-id="10538-112">Questo comando approva la replica in MyAnfVolume.</span><span class="sxs-lookup"><span data-stu-id="10538-112">This command Approves the Replication on MyAnfVolume.</span></span>

## <span data-ttu-id="10538-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10538-113">PARAMETERS</span></span>

### <span data-ttu-id="10538-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="10538-114">-AccountName</span></span>
<span data-ttu-id="10538-115">Nome dell'account ANF del volume di origine della replica</span><span class="sxs-lookup"><span data-stu-id="10538-115">The name of the ANF account of the replication source volume</span></span>

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

### <span data-ttu-id="10538-116">-DataProtectionVolumeId</span><span class="sxs-lookup"><span data-stu-id="10538-116">-DataProtectionVolumeId</span></span>
<span data-ttu-id="10538-117">ID file system del volume di protezione dati di destinazione</span><span class="sxs-lookup"><span data-stu-id="10538-117">The file system id of the destination data protection volume</span></span>

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

### <span data-ttu-id="10538-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10538-118">-DefaultProfile</span></span>
<span data-ttu-id="10538-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="10538-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10538-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10538-120">-InputObject</span></span>
<span data-ttu-id="10538-121">Oggetto volume di origine ANF per l'autorizzazione della destinazione della replica</span><span class="sxs-lookup"><span data-stu-id="10538-121">The ANF source volume object to authorized the replication destination</span></span>

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

### <span data-ttu-id="10538-122">-Name</span><span class="sxs-lookup"><span data-stu-id="10538-122">-Name</span></span>
<span data-ttu-id="10538-123">Nome del volume di origine della replica ANF</span><span class="sxs-lookup"><span data-stu-id="10538-123">The name of the ANF replication source volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10538-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="10538-124">-PassThru</span></span>
<span data-ttu-id="10538-125">Restituisce se è stata eseguita l'autorizzazione di replica del volume specificato</span><span class="sxs-lookup"><span data-stu-id="10538-125">Return whether replication authorization of the specified volume was performed</span></span>

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

### <span data-ttu-id="10538-126">-PoolName</span><span class="sxs-lookup"><span data-stu-id="10538-126">-PoolName</span></span>
<span data-ttu-id="10538-127">Nome del pool ANF del volume di origine della replica</span><span class="sxs-lookup"><span data-stu-id="10538-127">The name of the ANF pool of the replication source volume</span></span>

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

### <span data-ttu-id="10538-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10538-128">-ResourceGroupName</span></span>
<span data-ttu-id="10538-129">Gruppo di risorse del volume di origine della replica ANF</span><span class="sxs-lookup"><span data-stu-id="10538-129">The resource group of the ANF replication source volume</span></span>

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

### <span data-ttu-id="10538-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="10538-130">-ResourceId</span></span>
<span data-ttu-id="10538-131">ID risorsa del volume di origine della replica ANF</span><span class="sxs-lookup"><span data-stu-id="10538-131">The resource id of the ANF replication source volume</span></span>

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

### <span data-ttu-id="10538-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="10538-132">-Confirm</span></span>
<span data-ttu-id="10538-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10538-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10538-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10538-134">-WhatIf</span></span>
<span data-ttu-id="10538-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="10538-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10538-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="10538-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10538-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10538-137">CommonParameters</span></span>
<span data-ttu-id="10538-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10538-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10538-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="10538-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10538-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="10538-140">INPUTS</span></span>

### <span data-ttu-id="10538-141">System.String</span><span class="sxs-lookup"><span data-stu-id="10538-141">System.String</span></span>

### <span data-ttu-id="10538-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="10538-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="10538-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="10538-143">OUTPUTS</span></span>

### <span data-ttu-id="10538-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="10538-144">System.Boolean</span></span>

## <span data-ttu-id="10538-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="10538-145">NOTES</span></span>

## <span data-ttu-id="10538-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="10538-146">RELATED LINKS</span></span>
