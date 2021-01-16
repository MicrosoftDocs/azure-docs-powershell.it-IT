---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/suspend-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Suspend-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Suspend-AzNetAppFilesReplication.md
ms.openlocfilehash: ab4d79b4770f438b233e5bfcc740e79364955ea6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380502"
---
# <span data-ttu-id="8f733-101">Suspend-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="8f733-101">Suspend-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="8f733-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8f733-102">SYNOPSIS</span></span>
<span data-ttu-id="8f733-103">Sospendere/interrompere la connessione di replica nel volume di destinazione</span><span class="sxs-lookup"><span data-stu-id="8f733-103">Suspend/break the replication connection on the destination volume</span></span>

## <span data-ttu-id="8f733-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8f733-104">SYNTAX</span></span>

### <span data-ttu-id="8f733-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8f733-105">ByFieldsParameterSet (Default)</span></span>
```
Suspend-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-ForceBreak] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8f733-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f733-106">ByResourceIdParameterSet</span></span>
```
Suspend-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f733-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f733-107">ByObjectParameterSet</span></span>
```
Suspend-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f733-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8f733-108">DESCRIPTION</span></span>
<span data-ttu-id="8f733-109">Sospendere/interrompere la connessione di replica nel volume di destinazione</span><span class="sxs-lookup"><span data-stu-id="8f733-109">Suspend/break the replication connection on the destination volume</span></span>

## <span data-ttu-id="8f733-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8f733-110">EXAMPLES</span></span>

### <span data-ttu-id="8f733-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8f733-111">Example 1</span></span>
```powershell
PS C:\> Suspend-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="8f733-112">Questo comando sospende la connessione di replica ANF nel volume "MyDestinationAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="8f733-112">This command suspends the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="8f733-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8f733-113">PARAMETERS</span></span>

### <span data-ttu-id="8f733-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8f733-114">-AccountName</span></span>
<span data-ttu-id="8f733-115">Nome dell'account di ANF del volume di replica</span><span class="sxs-lookup"><span data-stu-id="8f733-115">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="8f733-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f733-116">-DefaultProfile</span></span>
<span data-ttu-id="8f733-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8f733-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f733-118">-ForceBreak</span><span class="sxs-lookup"><span data-stu-id="8f733-118">-ForceBreak</span></span>
<span data-ttu-id="8f733-119">Se la replica è in stato di trasferimento e si vuole forzare l'interruzione della replica, impostare su true</span><span class="sxs-lookup"><span data-stu-id="8f733-119">If replication is in status transferring and you want to force break the replication, set to true</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f733-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f733-120">-InputObject</span></span>
<span data-ttu-id="8f733-121">Oggetto volume di destinazione ANF con la replica da interrompere</span><span class="sxs-lookup"><span data-stu-id="8f733-121">The ANF destination volume object with the replication to break</span></span>

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

### <span data-ttu-id="8f733-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="8f733-122">-Name</span></span>
<span data-ttu-id="8f733-123">Nome del volume di destinazione della replica di ANF</span><span class="sxs-lookup"><span data-stu-id="8f733-123">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="8f733-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8f733-124">-PassThru</span></span>
<span data-ttu-id="8f733-125">Restituisce se l'interruzione della replica del volume specificata è stata eseguita</span><span class="sxs-lookup"><span data-stu-id="8f733-125">Return whether the break of the specified volume replication was performed</span></span>

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

### <span data-ttu-id="8f733-126">-PoolName</span><span class="sxs-lookup"><span data-stu-id="8f733-126">-PoolName</span></span>
<span data-ttu-id="8f733-127">Nome del pool di ANF del volume di replica</span><span class="sxs-lookup"><span data-stu-id="8f733-127">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="8f733-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f733-128">-ResourceGroupName</span></span>
<span data-ttu-id="8f733-129">Gruppo risorse del volume di destinazione della replica di ANF</span><span class="sxs-lookup"><span data-stu-id="8f733-129">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="8f733-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f733-130">-ResourceId</span></span>
<span data-ttu-id="8f733-131">ID risorsa del volume di destinazione della replica di ANF</span><span class="sxs-lookup"><span data-stu-id="8f733-131">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="8f733-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8f733-132">-Confirm</span></span>
<span data-ttu-id="8f733-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f733-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f733-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f733-134">-WhatIf</span></span>
<span data-ttu-id="8f733-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8f733-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f733-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8f733-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f733-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f733-137">CommonParameters</span></span>
<span data-ttu-id="8f733-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f733-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f733-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8f733-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f733-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8f733-140">INPUTS</span></span>

### <span data-ttu-id="8f733-141">System. String</span><span class="sxs-lookup"><span data-stu-id="8f733-141">System.String</span></span>

### <span data-ttu-id="8f733-142">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="8f733-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="8f733-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8f733-143">OUTPUTS</span></span>

### <span data-ttu-id="8f733-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8f733-144">System.Boolean</span></span>

## <span data-ttu-id="8f733-145">Note</span><span class="sxs-lookup"><span data-stu-id="8f733-145">NOTES</span></span>

## <span data-ttu-id="8f733-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8f733-146">RELATED LINKS</span></span>
