---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/suspend-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Suspend-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Suspend-AzNetAppFilesReplication.md
ms.openlocfilehash: eb695da1dc1fea238a57ea1c98bec42899e8f28f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310879"
---
# <span data-ttu-id="e5b1a-101">Suspend-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="e5b1a-101">Suspend-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="e5b1a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e5b1a-102">SYNOPSIS</span></span>
<span data-ttu-id="e5b1a-103">Sospendere/interrompere la connessione di replica nel volume di destinazione</span><span class="sxs-lookup"><span data-stu-id="e5b1a-103">Suspend/break the replication connection on the destination volume</span></span>

## <span data-ttu-id="e5b1a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e5b1a-104">SYNTAX</span></span>

### <span data-ttu-id="e5b1a-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e5b1a-105">ByFieldsParameterSet (Default)</span></span>
```
Suspend-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e5b1a-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5b1a-106">ByResourceIdParameterSet</span></span>
```
Suspend-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5b1a-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5b1a-107">ByObjectParameterSet</span></span>
```
Suspend-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5b1a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e5b1a-108">DESCRIPTION</span></span>
<span data-ttu-id="e5b1a-109">Sospendere/interrompere la connessione di replica nel volume di destinazione</span><span class="sxs-lookup"><span data-stu-id="e5b1a-109">Suspend/break the replication connection on the destination volume</span></span>

## <span data-ttu-id="e5b1a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e5b1a-110">EXAMPLES</span></span>

### <span data-ttu-id="e5b1a-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e5b1a-111">Example 1</span></span>
```powershell
PS C:\> Suspend-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="e5b1a-112">Questo comando sospende la connessione di replica ANF nel volume "MyDestinationAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="e5b1a-112">This command suspends the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="e5b1a-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e5b1a-113">PARAMETERS</span></span>

### <span data-ttu-id="e5b1a-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e5b1a-114">-AccountName</span></span>
<span data-ttu-id="e5b1a-115">Nome dell'account di ANF del volume di replica</span><span class="sxs-lookup"><span data-stu-id="e5b1a-115">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="e5b1a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5b1a-116">-DefaultProfile</span></span>
<span data-ttu-id="e5b1a-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e5b1a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5b1a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5b1a-118">-InputObject</span></span>
<span data-ttu-id="e5b1a-119">Oggetto volume di destinazione ANF con la replica da interrompere</span><span class="sxs-lookup"><span data-stu-id="e5b1a-119">The ANF destination volume object with the replication to break</span></span>

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

### <span data-ttu-id="e5b1a-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="e5b1a-120">-Name</span></span>
<span data-ttu-id="e5b1a-121">Nome del volume di destinazione della replica di ANF</span><span class="sxs-lookup"><span data-stu-id="e5b1a-121">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="e5b1a-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e5b1a-122">-PassThru</span></span>
<span data-ttu-id="e5b1a-123">Restituisce se l'interruzione della replica del volume specificata è stata eseguita</span><span class="sxs-lookup"><span data-stu-id="e5b1a-123">Return whether the break of the specified volume replication was performed</span></span>

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

### <span data-ttu-id="e5b1a-124">-PoolName</span><span class="sxs-lookup"><span data-stu-id="e5b1a-124">-PoolName</span></span>
<span data-ttu-id="e5b1a-125">Nome del pool di ANF del volume di replica</span><span class="sxs-lookup"><span data-stu-id="e5b1a-125">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="e5b1a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5b1a-126">-ResourceGroupName</span></span>
<span data-ttu-id="e5b1a-127">Gruppo risorse del volume di destinazione della replica di ANF</span><span class="sxs-lookup"><span data-stu-id="e5b1a-127">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="e5b1a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5b1a-128">-ResourceId</span></span>
<span data-ttu-id="e5b1a-129">ID risorsa del volume di destinazione della replica di ANF</span><span class="sxs-lookup"><span data-stu-id="e5b1a-129">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="e5b1a-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e5b1a-130">-Confirm</span></span>
<span data-ttu-id="e5b1a-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5b1a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5b1a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5b1a-132">-WhatIf</span></span>
<span data-ttu-id="e5b1a-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e5b1a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5b1a-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e5b1a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5b1a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5b1a-135">CommonParameters</span></span>
<span data-ttu-id="e5b1a-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5b1a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5b1a-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e5b1a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5b1a-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e5b1a-138">INPUTS</span></span>

### <span data-ttu-id="e5b1a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e5b1a-139">System.String</span></span>

### <span data-ttu-id="e5b1a-140">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="e5b1a-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="e5b1a-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e5b1a-141">OUTPUTS</span></span>

### <span data-ttu-id="e5b1a-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e5b1a-142">System.Boolean</span></span>

## <span data-ttu-id="e5b1a-143">Note</span><span class="sxs-lookup"><span data-stu-id="e5b1a-143">NOTES</span></span>

## <span data-ttu-id="e5b1a-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e5b1a-144">RELATED LINKS</span></span>
