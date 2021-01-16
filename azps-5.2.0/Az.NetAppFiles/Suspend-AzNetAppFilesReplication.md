---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/suspend-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Suspend-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Suspend-AzNetAppFilesReplication.md
ms.openlocfilehash: ab4d79b4770f438b233e5bfcc740e79364955ea6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341395"
---
# <span data-ttu-id="e348b-101">Suspend-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="e348b-101">Suspend-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="e348b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e348b-102">SYNOPSIS</span></span>
<span data-ttu-id="e348b-103">Sospendere/interrompere la connessione di replica nel volume di destinazione</span><span class="sxs-lookup"><span data-stu-id="e348b-103">Suspend/break the replication connection on the destination volume</span></span>

## <span data-ttu-id="e348b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e348b-104">SYNTAX</span></span>

### <span data-ttu-id="e348b-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e348b-105">ByFieldsParameterSet (Default)</span></span>
```
Suspend-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-ForceBreak] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e348b-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e348b-106">ByResourceIdParameterSet</span></span>
```
Suspend-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e348b-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e348b-107">ByObjectParameterSet</span></span>
```
Suspend-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e348b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e348b-108">DESCRIPTION</span></span>
<span data-ttu-id="e348b-109">Sospendere/interrompere la connessione di replica nel volume di destinazione</span><span class="sxs-lookup"><span data-stu-id="e348b-109">Suspend/break the replication connection on the destination volume</span></span>

## <span data-ttu-id="e348b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e348b-110">EXAMPLES</span></span>

### <span data-ttu-id="e348b-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e348b-111">Example 1</span></span>
```powershell
PS C:\> Suspend-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="e348b-112">Questo comando sospende la connessione di replica ANF nel volume "MyDestinationAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="e348b-112">This command suspends the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="e348b-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e348b-113">PARAMETERS</span></span>

### <span data-ttu-id="e348b-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e348b-114">-AccountName</span></span>
<span data-ttu-id="e348b-115">Nome dell'account di ANF del volume di replica</span><span class="sxs-lookup"><span data-stu-id="e348b-115">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="e348b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e348b-116">-DefaultProfile</span></span>
<span data-ttu-id="e348b-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e348b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e348b-118">-ForceBreak</span><span class="sxs-lookup"><span data-stu-id="e348b-118">-ForceBreak</span></span>
<span data-ttu-id="e348b-119">Se la replica è in stato di trasferimento e si vuole forzare l'interruzione della replica, impostare su true</span><span class="sxs-lookup"><span data-stu-id="e348b-119">If replication is in status transferring and you want to force break the replication, set to true</span></span>

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

### <span data-ttu-id="e348b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e348b-120">-InputObject</span></span>
<span data-ttu-id="e348b-121">Oggetto volume di destinazione ANF con la replica da interrompere</span><span class="sxs-lookup"><span data-stu-id="e348b-121">The ANF destination volume object with the replication to break</span></span>

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

### <span data-ttu-id="e348b-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="e348b-122">-Name</span></span>
<span data-ttu-id="e348b-123">Nome del volume di destinazione della replica di ANF</span><span class="sxs-lookup"><span data-stu-id="e348b-123">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="e348b-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e348b-124">-PassThru</span></span>
<span data-ttu-id="e348b-125">Restituisce se l'interruzione della replica del volume specificata è stata eseguita</span><span class="sxs-lookup"><span data-stu-id="e348b-125">Return whether the break of the specified volume replication was performed</span></span>

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

### <span data-ttu-id="e348b-126">-PoolName</span><span class="sxs-lookup"><span data-stu-id="e348b-126">-PoolName</span></span>
<span data-ttu-id="e348b-127">Nome del pool di ANF del volume di replica</span><span class="sxs-lookup"><span data-stu-id="e348b-127">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="e348b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e348b-128">-ResourceGroupName</span></span>
<span data-ttu-id="e348b-129">Gruppo risorse del volume di destinazione della replica di ANF</span><span class="sxs-lookup"><span data-stu-id="e348b-129">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="e348b-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e348b-130">-ResourceId</span></span>
<span data-ttu-id="e348b-131">ID risorsa del volume di destinazione della replica di ANF</span><span class="sxs-lookup"><span data-stu-id="e348b-131">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="e348b-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e348b-132">-Confirm</span></span>
<span data-ttu-id="e348b-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e348b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e348b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e348b-134">-WhatIf</span></span>
<span data-ttu-id="e348b-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e348b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e348b-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e348b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e348b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e348b-137">CommonParameters</span></span>
<span data-ttu-id="e348b-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e348b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e348b-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e348b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e348b-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e348b-140">INPUTS</span></span>

### <span data-ttu-id="e348b-141">System. String</span><span class="sxs-lookup"><span data-stu-id="e348b-141">System.String</span></span>

### <span data-ttu-id="e348b-142">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="e348b-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="e348b-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e348b-143">OUTPUTS</span></span>

### <span data-ttu-id="e348b-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e348b-144">System.Boolean</span></span>

## <span data-ttu-id="e348b-145">Note</span><span class="sxs-lookup"><span data-stu-id="e348b-145">NOTES</span></span>

## <span data-ttu-id="e348b-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e348b-146">RELATED LINKS</span></span>
