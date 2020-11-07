---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/remove-azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
ms.openlocfilehash: b2c6d074f51f1ef2aa26e9d0c75fe6338a094419
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93858325"
---
# <span data-ttu-id="b9c98-101">Remove-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="b9c98-101">Remove-AzStorageSyncGroup</span></span>

## <span data-ttu-id="b9c98-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b9c98-102">SYNOPSIS</span></span>
<span data-ttu-id="b9c98-103">Questo comando eliminerà il gruppo di sincronizzazione specificato.</span><span class="sxs-lookup"><span data-stu-id="b9c98-103">This command will delete the specified sync group.</span></span>

## <span data-ttu-id="b9c98-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b9c98-104">SYNTAX</span></span>

### <span data-ttu-id="b9c98-105">StringParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b9c98-105">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-Name] <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b9c98-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9c98-106">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-InputObject] <PSSyncGroup> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9c98-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9c98-107">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9c98-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b9c98-108">DESCRIPTION</span></span>
<span data-ttu-id="b9c98-109">Questo comando eliminerà il gruppo di sincronizzazione specificato.</span><span class="sxs-lookup"><span data-stu-id="b9c98-109">This command will delete the specified sync group.</span></span> <span data-ttu-id="b9c98-110">Un gruppo di sincronizzazione può essere rimosso solo quando tutti gli endpoint contenuti vengono eliminati per primi.</span><span class="sxs-lookup"><span data-stu-id="b9c98-110">A sync group can only be removed when all of the contained endpoints are deleted first.</span></span>

## <span data-ttu-id="b9c98-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b9c98-111">EXAMPLES</span></span>

### <span data-ttu-id="b9c98-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b9c98-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncGroup -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="b9c98-113">Questo comando rimuoverà il gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="b9c98-113">This command will remove the sync group.</span></span>

## <span data-ttu-id="b9c98-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b9c98-114">PARAMETERS</span></span>

### <span data-ttu-id="b9c98-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b9c98-115">-AsJob</span></span>
<span data-ttu-id="b9c98-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="b9c98-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b9c98-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9c98-117">-DefaultProfile</span></span>
<span data-ttu-id="b9c98-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b9c98-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9c98-119">-Force</span><span class="sxs-lookup"><span data-stu-id="b9c98-119">-Force</span></span>
<span data-ttu-id="b9c98-120">Forza di fornitura per ignorare la conferma di questo comando.</span><span class="sxs-lookup"><span data-stu-id="b9c98-120">Supply -Force to skip confirmation of this command.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9c98-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b9c98-121">-InputObject</span></span>
<span data-ttu-id="b9c98-122">Oggetto di input SyncGroup</span><span class="sxs-lookup"><span data-stu-id="b9c98-122">SyncGroup Input Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9c98-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="b9c98-123">-Name</span></span>
<span data-ttu-id="b9c98-124">Nome della SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="b9c98-124">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: SyncGroupName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c98-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b9c98-125">-PassThru</span></span>
<span data-ttu-id="b9c98-126">In esecuzione normale, questo cmdlet non restituisce alcun valore per l'esito positivo.</span><span class="sxs-lookup"><span data-stu-id="b9c98-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="b9c98-127">Se fornisci il parametro PassThru, il cmdlet scriverà un valore nella pipeline dopo l'esecuzione corretta.</span><span class="sxs-lookup"><span data-stu-id="b9c98-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="b9c98-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9c98-128">-ResourceGroupName</span></span>
<span data-ttu-id="b9c98-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b9c98-129">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c98-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9c98-130">-ResourceId</span></span>
<span data-ttu-id="b9c98-131">ID risorsa SyncGroup</span><span class="sxs-lookup"><span data-stu-id="b9c98-131">SyncGroup Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9c98-132">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="b9c98-132">-StorageSyncServiceName</span></span>
<span data-ttu-id="b9c98-133">Nome della StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="b9c98-133">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c98-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b9c98-134">-Confirm</span></span>
<span data-ttu-id="b9c98-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9c98-135">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9c98-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9c98-136">-WhatIf</span></span>
<span data-ttu-id="b9c98-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b9c98-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b9c98-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b9c98-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9c98-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9c98-139">CommonParameters</span></span>
<span data-ttu-id="b9c98-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9c98-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9c98-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9c98-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9c98-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b9c98-142">INPUTS</span></span>

### <span data-ttu-id="b9c98-143">Microsoft. Azure. Commands. StorageSync. Models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="b9c98-143">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="b9c98-144">System. String</span><span class="sxs-lookup"><span data-stu-id="b9c98-144">System.String</span></span>

### <span data-ttu-id="b9c98-145">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b9c98-145">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b9c98-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b9c98-146">OUTPUTS</span></span>

### <span data-ttu-id="b9c98-147">System. Object</span><span class="sxs-lookup"><span data-stu-id="b9c98-147">System.Object</span></span>
## <span data-ttu-id="b9c98-148">Note</span><span class="sxs-lookup"><span data-stu-id="b9c98-148">NOTES</span></span>

## <span data-ttu-id="b9c98-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b9c98-149">RELATED LINKS</span></span>
