---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesReplication.md
ms.openlocfilehash: 04ad7f188a2280dcdf84e8b5c1f45e20edf4d07b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179974"
---
# <span data-ttu-id="f3341-101">Remove-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="f3341-101">Remove-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="f3341-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3341-102">SYNOPSIS</span></span>
<span data-ttu-id="f3341-103">Rimuovere/eliminare la connessione di replica nel volume di destinazione e inviare il rilascio alla replica di origine</span><span class="sxs-lookup"><span data-stu-id="f3341-103">Remove/Delete the replication connection on the destination volume, and send release to the source replication</span></span>

## <span data-ttu-id="f3341-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f3341-104">SYNTAX</span></span>

### <span data-ttu-id="f3341-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f3341-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f3341-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3341-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3341-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3341-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3341-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f3341-108">DESCRIPTION</span></span>
<span data-ttu-id="f3341-109">Rimuovere/eliminare la connessione di replica nel volume di destinazione e inviare il rilascio alla replica di origine</span><span class="sxs-lookup"><span data-stu-id="f3341-109">Remove/Delete the replication connection on the destination volume, and send release to the source replication</span></span>

## <span data-ttu-id="f3341-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f3341-110">EXAMPLES</span></span>

### <span data-ttu-id="f3341-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f3341-111">Example 1</span></span>
```powershell
PS C:\> Remove-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="f3341-112">Questo comando rimuove la connessione a Replica ANF sul volume "MyDestinationAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="f3341-112">This command removes the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="f3341-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3341-113">PARAMETERS</span></span>

### <span data-ttu-id="f3341-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f3341-114">-AccountName</span></span>
<span data-ttu-id="f3341-115">Nome dell'account ANF del volume di replica</span><span class="sxs-lookup"><span data-stu-id="f3341-115">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="f3341-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3341-116">-DefaultProfile</span></span>
<span data-ttu-id="f3341-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f3341-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3341-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f3341-118">-InputObject</span></span>
<span data-ttu-id="f3341-119">Volume di destinazione ANF con la replica da rimuovere</span><span class="sxs-lookup"><span data-stu-id="f3341-119">The ANF destination volume with the replication to remove</span></span>

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

### <span data-ttu-id="f3341-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f3341-120">-Name</span></span>
<span data-ttu-id="f3341-121">Nome del volume di destinazione della replica ANF</span><span class="sxs-lookup"><span data-stu-id="f3341-121">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="f3341-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f3341-122">-PassThru</span></span>
<span data-ttu-id="f3341-123">Restituisce se la replica ANF specificata è stata rimossa correttamente</span><span class="sxs-lookup"><span data-stu-id="f3341-123">Return whether the specified ANF replication was successfully removed</span></span>

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

### <span data-ttu-id="f3341-124">-PoolName</span><span class="sxs-lookup"><span data-stu-id="f3341-124">-PoolName</span></span>
<span data-ttu-id="f3341-125">Nome del pool ANF del volume di replica</span><span class="sxs-lookup"><span data-stu-id="f3341-125">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="f3341-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3341-126">-ResourceGroupName</span></span>
<span data-ttu-id="f3341-127">Gruppo di risorse del volume di destinazione della replica ANF</span><span class="sxs-lookup"><span data-stu-id="f3341-127">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="f3341-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3341-128">-ResourceId</span></span>
<span data-ttu-id="f3341-129">ID risorsa del volume di destinazione della replica ANF</span><span class="sxs-lookup"><span data-stu-id="f3341-129">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="f3341-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f3341-130">-Confirm</span></span>
<span data-ttu-id="f3341-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3341-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3341-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3341-132">-WhatIf</span></span>
<span data-ttu-id="f3341-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f3341-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3341-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f3341-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3341-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3341-135">CommonParameters</span></span>
<span data-ttu-id="f3341-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3341-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3341-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f3341-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3341-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="f3341-138">INPUTS</span></span>

### <span data-ttu-id="f3341-139">System.String</span><span class="sxs-lookup"><span data-stu-id="f3341-139">System.String</span></span>

### <span data-ttu-id="f3341-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="f3341-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="f3341-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f3341-141">OUTPUTS</span></span>

### <span data-ttu-id="f3341-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f3341-142">System.Boolean</span></span>

## <span data-ttu-id="f3341-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="f3341-143">NOTES</span></span>

## <span data-ttu-id="f3341-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f3341-144">RELATED LINKS</span></span>
