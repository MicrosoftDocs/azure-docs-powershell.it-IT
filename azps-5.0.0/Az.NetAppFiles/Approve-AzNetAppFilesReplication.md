---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/approve-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Approve-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Approve-AzNetAppFilesReplication.md
ms.openlocfilehash: 9afa4f22de142dba7608d33ed04c972758911aa9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201854"
---
# <span data-ttu-id="e4dcf-101">Approve-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="e4dcf-101">Approve-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="e4dcf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e4dcf-102">SYNOPSIS</span></span>
<span data-ttu-id="e4dcf-103">Approva/autorizza la connessione di replica nel volume di origine</span><span class="sxs-lookup"><span data-stu-id="e4dcf-103">Approve/Authorize replication connection on the source volume</span></span>

## <span data-ttu-id="e4dcf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e4dcf-104">SYNTAX</span></span>

### <span data-ttu-id="e4dcf-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e4dcf-105">ByFieldsParameterSet (Default)</span></span>
```
Approve-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> -DataProtectionVolumeId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4dcf-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4dcf-106">ByResourceIdParameterSet</span></span>
```
Approve-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4dcf-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4dcf-107">ByObjectParameterSet</span></span>
```
Approve-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4dcf-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e4dcf-108">DESCRIPTION</span></span>
<span data-ttu-id="e4dcf-109">Approva la connessione di replica nel volume di origine</span><span class="sxs-lookup"><span data-stu-id="e4dcf-109">Approve the replication connection on the source volume</span></span>

## <span data-ttu-id="e4dcf-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e4dcf-110">EXAMPLES</span></span>

### <span data-ttu-id="e4dcf-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e4dcf-111">Example 1</span></span>
```powershell
PS C:\> Approve-AzNetAppFilesReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -DataProtectionVolumeId "MyDestinationVolumeId"

Output:
remoteVolumeResourceId          : resourceId
```

<span data-ttu-id="e4dcf-112">Questo comando approva la replica in MyAnfVolume.</span><span class="sxs-lookup"><span data-stu-id="e4dcf-112">This command Approves the Replication on MyAnfVolume.</span></span>

## <span data-ttu-id="e4dcf-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e4dcf-113">PARAMETERS</span></span>

### <span data-ttu-id="e4dcf-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e4dcf-114">-AccountName</span></span>
<span data-ttu-id="e4dcf-115">Nome dell'account di ANF del volume di origine della replica</span><span class="sxs-lookup"><span data-stu-id="e4dcf-115">The name of the ANF account of the replication source volume</span></span>

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

### <span data-ttu-id="e4dcf-116">-DataProtectionVolumeId</span><span class="sxs-lookup"><span data-stu-id="e4dcf-116">-DataProtectionVolumeId</span></span>
<span data-ttu-id="e4dcf-117">ID del file System del volume di protezione dei dati di destinazione</span><span class="sxs-lookup"><span data-stu-id="e4dcf-117">The file system id of the destination data protection volume</span></span>

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

### <span data-ttu-id="e4dcf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4dcf-118">-DefaultProfile</span></span>
<span data-ttu-id="e4dcf-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e4dcf-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4dcf-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4dcf-120">-InputObject</span></span>
<span data-ttu-id="e4dcf-121">L'oggetto volume di origine ANF per autorizzare la destinazione della replica</span><span class="sxs-lookup"><span data-stu-id="e4dcf-121">The ANF source volume object to authorized the replication destination</span></span>

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

### <span data-ttu-id="e4dcf-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="e4dcf-122">-Name</span></span>
<span data-ttu-id="e4dcf-123">Nome del volume di origine della replica di ANF</span><span class="sxs-lookup"><span data-stu-id="e4dcf-123">The name of the ANF replication source volume</span></span>

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

### <span data-ttu-id="e4dcf-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e4dcf-124">-PassThru</span></span>
<span data-ttu-id="e4dcf-125">Restituisce se è stata eseguita l'autorizzazione di replica del volume specificato</span><span class="sxs-lookup"><span data-stu-id="e4dcf-125">Return whether replication authorization of the specified volume was performed</span></span>

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

### <span data-ttu-id="e4dcf-126">-PoolName</span><span class="sxs-lookup"><span data-stu-id="e4dcf-126">-PoolName</span></span>
<span data-ttu-id="e4dcf-127">Nome del pool di ANF del volume di origine della replica</span><span class="sxs-lookup"><span data-stu-id="e4dcf-127">The name of the ANF pool of the replication source volume</span></span>

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

### <span data-ttu-id="e4dcf-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4dcf-128">-ResourceGroupName</span></span>
<span data-ttu-id="e4dcf-129">Gruppo risorse del volume di origine della replica di ANF</span><span class="sxs-lookup"><span data-stu-id="e4dcf-129">The resource group of the ANF replication source volume</span></span>

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

### <span data-ttu-id="e4dcf-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4dcf-130">-ResourceId</span></span>
<span data-ttu-id="e4dcf-131">ID risorsa del volume di origine della replica di ANF</span><span class="sxs-lookup"><span data-stu-id="e4dcf-131">The resource id of the ANF replication source volume</span></span>

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

### <span data-ttu-id="e4dcf-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e4dcf-132">-Confirm</span></span>
<span data-ttu-id="e4dcf-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4dcf-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4dcf-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4dcf-134">-WhatIf</span></span>
<span data-ttu-id="e4dcf-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e4dcf-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4dcf-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e4dcf-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4dcf-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4dcf-137">CommonParameters</span></span>
<span data-ttu-id="e4dcf-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4dcf-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4dcf-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e4dcf-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4dcf-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e4dcf-140">INPUTS</span></span>

### <span data-ttu-id="e4dcf-141">System. String</span><span class="sxs-lookup"><span data-stu-id="e4dcf-141">System.String</span></span>

### <span data-ttu-id="e4dcf-142">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="e4dcf-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="e4dcf-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e4dcf-143">OUTPUTS</span></span>

### <span data-ttu-id="e4dcf-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e4dcf-144">System.Boolean</span></span>

## <span data-ttu-id="e4dcf-145">Note</span><span class="sxs-lookup"><span data-stu-id="e4dcf-145">NOTES</span></span>

## <span data-ttu-id="e4dcf-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e4dcf-146">RELATED LINKS</span></span>
