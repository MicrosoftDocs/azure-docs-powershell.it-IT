---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesReplication.md
ms.openlocfilehash: 04ad7f188a2280dcdf84e8b5c1f45e20edf4d07b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380617"
---
# <span data-ttu-id="a8210-101">Remove-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="a8210-101">Remove-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="a8210-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a8210-102">SYNOPSIS</span></span>
<span data-ttu-id="a8210-103">Rimuovere/eliminare la connessione di replica nel volume di destinazione e inviare il rilascio alla replica di origine</span><span class="sxs-lookup"><span data-stu-id="a8210-103">Remove/Delete the replication connection on the destination volume, and send release to the source replication</span></span>

## <span data-ttu-id="a8210-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a8210-104">SYNTAX</span></span>

### <span data-ttu-id="a8210-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a8210-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a8210-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8210-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8210-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8210-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8210-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a8210-108">DESCRIPTION</span></span>
<span data-ttu-id="a8210-109">Rimuovere/eliminare la connessione di replica nel volume di destinazione e inviare il rilascio alla replica di origine</span><span class="sxs-lookup"><span data-stu-id="a8210-109">Remove/Delete the replication connection on the destination volume, and send release to the source replication</span></span>

## <span data-ttu-id="a8210-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a8210-110">EXAMPLES</span></span>

### <span data-ttu-id="a8210-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a8210-111">Example 1</span></span>
```powershell
PS C:\> Remove-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="a8210-112">Questo comando rimuove la connessione di replica ANF nel volume "MyDestinationAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="a8210-112">This command removes the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="a8210-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a8210-113">PARAMETERS</span></span>

### <span data-ttu-id="a8210-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a8210-114">-AccountName</span></span>
<span data-ttu-id="a8210-115">Nome dell'account di ANF del volume di replica</span><span class="sxs-lookup"><span data-stu-id="a8210-115">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="a8210-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8210-116">-DefaultProfile</span></span>
<span data-ttu-id="a8210-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a8210-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8210-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a8210-118">-InputObject</span></span>
<span data-ttu-id="a8210-119">Il volume di destinazione ANF con la replica da rimuovere</span><span class="sxs-lookup"><span data-stu-id="a8210-119">The ANF destination volume with the replication to remove</span></span>

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

### <span data-ttu-id="a8210-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="a8210-120">-Name</span></span>
<span data-ttu-id="a8210-121">Nome del volume di destinazione della replica di ANF</span><span class="sxs-lookup"><span data-stu-id="a8210-121">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="a8210-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a8210-122">-PassThru</span></span>
<span data-ttu-id="a8210-123">Restituisce se la replica ANF specificata è stata rimossa correttamente</span><span class="sxs-lookup"><span data-stu-id="a8210-123">Return whether the specified ANF replication was successfully removed</span></span>

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

### <span data-ttu-id="a8210-124">-PoolName</span><span class="sxs-lookup"><span data-stu-id="a8210-124">-PoolName</span></span>
<span data-ttu-id="a8210-125">Nome del pool di ANF del volume di replica</span><span class="sxs-lookup"><span data-stu-id="a8210-125">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="a8210-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8210-126">-ResourceGroupName</span></span>
<span data-ttu-id="a8210-127">Gruppo risorse del volume di destinazione della replica di ANF</span><span class="sxs-lookup"><span data-stu-id="a8210-127">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="a8210-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8210-128">-ResourceId</span></span>
<span data-ttu-id="a8210-129">ID risorsa del volume di destinazione della replica di ANF</span><span class="sxs-lookup"><span data-stu-id="a8210-129">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="a8210-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a8210-130">-Confirm</span></span>
<span data-ttu-id="a8210-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8210-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8210-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8210-132">-WhatIf</span></span>
<span data-ttu-id="a8210-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a8210-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8210-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a8210-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8210-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8210-135">CommonParameters</span></span>
<span data-ttu-id="a8210-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8210-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8210-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a8210-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8210-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a8210-138">INPUTS</span></span>

### <span data-ttu-id="a8210-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a8210-139">System.String</span></span>

### <span data-ttu-id="a8210-140">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="a8210-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="a8210-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a8210-141">OUTPUTS</span></span>

### <span data-ttu-id="a8210-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a8210-142">System.Boolean</span></span>

## <span data-ttu-id="a8210-143">Note</span><span class="sxs-lookup"><span data-stu-id="a8210-143">NOTES</span></span>

## <span data-ttu-id="a8210-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a8210-144">RELATED LINKS</span></span>
