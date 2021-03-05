---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/remove-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
ms.openlocfilehash: 648ef711d030f7600863d286df24cfdf1d2f7927
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974014"
---
# <span data-ttu-id="bcc93-101">Remove-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="bcc93-101">Remove-AzStorageSyncService</span></span>

## <span data-ttu-id="bcc93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bcc93-102">SYNOPSIS</span></span>
<span data-ttu-id="bcc93-103">Questo comando eliminerà il servizio di sincronizzazione di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="bcc93-103">This command will delete the specified storage sync service.</span></span>

## <span data-ttu-id="bcc93-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bcc93-104">SYNTAX</span></span>

### <span data-ttu-id="bcc93-105">StringParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="bcc93-105">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bcc93-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bcc93-106">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncService [-InputObject] <PSStorageSyncService> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bcc93-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bcc93-107">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncService [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcc93-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bcc93-108">DESCRIPTION</span></span>
<span data-ttu-id="bcc93-109">Questo comando eliminerà il servizio di sincronizzazione di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="bcc93-109">This command will delete the specified storage sync service.</span></span> <span data-ttu-id="bcc93-110">Un servizio di sincronizzazione di archiviazione può essere rimosso solo quando tutti i gruppi di sincronizzazione contenuti e i server registrati vengono eliminati per primi.</span><span class="sxs-lookup"><span data-stu-id="bcc93-110">A storage sync service can only be removed when all of the contained sync groups and registered servers are deleted first.</span></span>

## <span data-ttu-id="bcc93-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bcc93-111">EXAMPLES</span></span>

### <span data-ttu-id="bcc93-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bcc93-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncService -Force -ResourceGroupName "myResourceGroup" -Name "myStorageSyncServiceName"
```

<span data-ttu-id="bcc93-113">Questo comando rimuove il servizio di sincronizzazione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="bcc93-113">This command will remove the storage sync service.</span></span>

## <span data-ttu-id="bcc93-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bcc93-114">PARAMETERS</span></span>

### <span data-ttu-id="bcc93-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bcc93-115">-AsJob</span></span>
<span data-ttu-id="bcc93-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="bcc93-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bcc93-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcc93-117">-DefaultProfile</span></span>
<span data-ttu-id="bcc93-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bcc93-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bcc93-119">-Force</span><span class="sxs-lookup"><span data-stu-id="bcc93-119">-Force</span></span>
<span data-ttu-id="bcc93-120">Supply -Force to skip confirmation of this command.</span><span class="sxs-lookup"><span data-stu-id="bcc93-120">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="bcc93-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bcc93-121">-InputObject</span></span>
<span data-ttu-id="bcc93-122">Oggetto di input StorageSyncService, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="bcc93-122">StorageSyncService Input Object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bcc93-123">-Name</span><span class="sxs-lookup"><span data-stu-id="bcc93-123">-Name</span></span>
<span data-ttu-id="bcc93-124">Nome di StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="bcc93-124">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: StorageSyncServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcc93-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bcc93-125">-PassThru</span></span>
<span data-ttu-id="bcc93-126">Nella normale esecuzione, questo cmdlet non restituisce alcun valore in caso di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="bcc93-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="bcc93-127">Se si fornisce il parametro PassThru, il cmdlet scriverà un valore nella pipeline dopo l'esecuzione corretta.</span><span class="sxs-lookup"><span data-stu-id="bcc93-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="bcc93-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcc93-128">-ResourceGroupName</span></span>
<span data-ttu-id="bcc93-129">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bcc93-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="bcc93-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bcc93-130">-ResourceId</span></span>
<span data-ttu-id="bcc93-131">ID risorsa StorageSyncService</span><span class="sxs-lookup"><span data-stu-id="bcc93-131">StorageSyncService Resource Id</span></span>

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

### <span data-ttu-id="bcc93-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bcc93-132">-Confirm</span></span>
<span data-ttu-id="bcc93-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bcc93-133">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcc93-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcc93-134">-WhatIf</span></span>
<span data-ttu-id="bcc93-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bcc93-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bcc93-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bcc93-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcc93-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcc93-137">CommonParameters</span></span>
<span data-ttu-id="bcc93-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcc93-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcc93-139">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcc93-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcc93-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="bcc93-140">INPUTS</span></span>

### <span data-ttu-id="bcc93-141">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="bcc93-141">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

### <span data-ttu-id="bcc93-142">System.String</span><span class="sxs-lookup"><span data-stu-id="bcc93-142">System.String</span></span>

### <span data-ttu-id="bcc93-143">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bcc93-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="bcc93-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bcc93-144">OUTPUTS</span></span>

### <span data-ttu-id="bcc93-145">System.Object</span><span class="sxs-lookup"><span data-stu-id="bcc93-145">System.Object</span></span>
## <span data-ttu-id="bcc93-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="bcc93-146">NOTES</span></span>

## <span data-ttu-id="bcc93-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bcc93-147">RELATED LINKS</span></span>
