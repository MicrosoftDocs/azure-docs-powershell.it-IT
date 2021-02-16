---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/approve-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Approve-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Approve-AzNetAppFilesReplication.md
ms.openlocfilehash: 9afa4f22de142dba7608d33ed04c972758911aa9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187319"
---
# <span data-ttu-id="d6c33-101">Approve-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="d6c33-101">Approve-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="d6c33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6c33-102">SYNOPSIS</span></span>
<span data-ttu-id="d6c33-103">Approvazione/autorizzazione della connessione di replica nel volume di origine</span><span class="sxs-lookup"><span data-stu-id="d6c33-103">Approve/Authorize replication connection on the source volume</span></span>

## <span data-ttu-id="d6c33-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d6c33-104">SYNTAX</span></span>

### <span data-ttu-id="d6c33-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d6c33-105">ByFieldsParameterSet (Default)</span></span>
```
Approve-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> -DataProtectionVolumeId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6c33-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6c33-106">ByResourceIdParameterSet</span></span>
```
Approve-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6c33-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6c33-107">ByObjectParameterSet</span></span>
```
Approve-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6c33-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d6c33-108">DESCRIPTION</span></span>
<span data-ttu-id="d6c33-109">Approvare la connessione di replica nel volume di origine</span><span class="sxs-lookup"><span data-stu-id="d6c33-109">Approve the replication connection on the source volume</span></span>

## <span data-ttu-id="d6c33-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d6c33-110">EXAMPLES</span></span>

### <span data-ttu-id="d6c33-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d6c33-111">Example 1</span></span>
```powershell
PS C:\> Approve-AzNetAppFilesReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -DataProtectionVolumeId "MyDestinationVolumeId"

Output:
remoteVolumeResourceId          : resourceId
```

<span data-ttu-id="d6c33-112">Questo comando approva la replica in MyAnfVolume.</span><span class="sxs-lookup"><span data-stu-id="d6c33-112">This command Approves the Replication on MyAnfVolume.</span></span>

## <span data-ttu-id="d6c33-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d6c33-113">PARAMETERS</span></span>

### <span data-ttu-id="d6c33-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d6c33-114">-AccountName</span></span>
<span data-ttu-id="d6c33-115">Nome dell'account ANF del volume di origine della replica</span><span class="sxs-lookup"><span data-stu-id="d6c33-115">The name of the ANF account of the replication source volume</span></span>

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

### <span data-ttu-id="d6c33-116">-DataProtectionVolumeId</span><span class="sxs-lookup"><span data-stu-id="d6c33-116">-DataProtectionVolumeId</span></span>
<span data-ttu-id="d6c33-117">ID file system del volume di protezione dati di destinazione</span><span class="sxs-lookup"><span data-stu-id="d6c33-117">The file system id of the destination data protection volume</span></span>

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

### <span data-ttu-id="d6c33-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6c33-118">-DefaultProfile</span></span>
<span data-ttu-id="d6c33-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d6c33-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6c33-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6c33-120">-InputObject</span></span>
<span data-ttu-id="d6c33-121">Oggetto volume di origine ANF per l'autorizzazione della destinazione della replica</span><span class="sxs-lookup"><span data-stu-id="d6c33-121">The ANF source volume object to authorized the replication destination</span></span>

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

### <span data-ttu-id="d6c33-122">-Name</span><span class="sxs-lookup"><span data-stu-id="d6c33-122">-Name</span></span>
<span data-ttu-id="d6c33-123">Nome del volume di origine della replica ANF</span><span class="sxs-lookup"><span data-stu-id="d6c33-123">The name of the ANF replication source volume</span></span>

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

### <span data-ttu-id="d6c33-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d6c33-124">-PassThru</span></span>
<span data-ttu-id="d6c33-125">Restituisce se è stata eseguita l'autorizzazione di replica del volume specificato</span><span class="sxs-lookup"><span data-stu-id="d6c33-125">Return whether replication authorization of the specified volume was performed</span></span>

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

### <span data-ttu-id="d6c33-126">-PoolName</span><span class="sxs-lookup"><span data-stu-id="d6c33-126">-PoolName</span></span>
<span data-ttu-id="d6c33-127">Nome del pool ANF del volume di origine della replica</span><span class="sxs-lookup"><span data-stu-id="d6c33-127">The name of the ANF pool of the replication source volume</span></span>

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

### <span data-ttu-id="d6c33-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6c33-128">-ResourceGroupName</span></span>
<span data-ttu-id="d6c33-129">Gruppo di risorse del volume di origine della replica ANF</span><span class="sxs-lookup"><span data-stu-id="d6c33-129">The resource group of the ANF replication source volume</span></span>

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

### <span data-ttu-id="d6c33-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6c33-130">-ResourceId</span></span>
<span data-ttu-id="d6c33-131">ID risorsa del volume di origine della replica ANF</span><span class="sxs-lookup"><span data-stu-id="d6c33-131">The resource id of the ANF replication source volume</span></span>

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

### <span data-ttu-id="d6c33-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d6c33-132">-Confirm</span></span>
<span data-ttu-id="d6c33-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6c33-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6c33-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6c33-134">-WhatIf</span></span>
<span data-ttu-id="d6c33-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d6c33-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6c33-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d6c33-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6c33-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6c33-137">CommonParameters</span></span>
<span data-ttu-id="d6c33-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6c33-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6c33-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d6c33-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6c33-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="d6c33-140">INPUTS</span></span>

### <span data-ttu-id="d6c33-141">System.String</span><span class="sxs-lookup"><span data-stu-id="d6c33-141">System.String</span></span>

### <span data-ttu-id="d6c33-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="d6c33-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="d6c33-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d6c33-143">OUTPUTS</span></span>

### <span data-ttu-id="d6c33-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d6c33-144">System.Boolean</span></span>

## <span data-ttu-id="d6c33-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="d6c33-145">NOTES</span></span>

## <span data-ttu-id="d6c33-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d6c33-146">RELATED LINKS</span></span>
