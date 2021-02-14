---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/remove-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
ms.openlocfilehash: f64c085f742eeabea235660d4af7ba6bd5970fdf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188814"
---
# <span data-ttu-id="81f6e-101">Remove-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="81f6e-101">Remove-AzStorageSyncService</span></span>

## <span data-ttu-id="81f6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81f6e-102">SYNOPSIS</span></span>
<span data-ttu-id="81f6e-103">Questo comando eliminerà il servizio di sincronizzazione di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="81f6e-103">This command will delete the specified storage sync service.</span></span>

## <span data-ttu-id="81f6e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="81f6e-104">SYNTAX</span></span>

### <span data-ttu-id="81f6e-105">StringParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="81f6e-105">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81f6e-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="81f6e-106">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncService [-InputObject] <PSStorageSyncService> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81f6e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="81f6e-107">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncService [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81f6e-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="81f6e-108">DESCRIPTION</span></span>
<span data-ttu-id="81f6e-109">Questo comando eliminerà il servizio di sincronizzazione di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="81f6e-109">This command will delete the specified storage sync service.</span></span> <span data-ttu-id="81f6e-110">Un servizio di sincronizzazione di archiviazione può essere rimosso solo quando tutti i gruppi di sincronizzazione contenuti e i server registrati vengono eliminati per primi.</span><span class="sxs-lookup"><span data-stu-id="81f6e-110">A storage sync service can only be removed when all of the contained sync groups and registered servers are deleted first.</span></span>

## <span data-ttu-id="81f6e-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="81f6e-111">EXAMPLES</span></span>

### <span data-ttu-id="81f6e-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="81f6e-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncService -Force -ResourceGroupName "myResourceGroup" -Name "myStorageSyncServiceName"
```

<span data-ttu-id="81f6e-113">Questo comando rimuove il servizio di sincronizzazione dell'archiviazione.</span><span class="sxs-lookup"><span data-stu-id="81f6e-113">This command will remove the storage sync service.</span></span>

## <span data-ttu-id="81f6e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="81f6e-114">PARAMETERS</span></span>

### <span data-ttu-id="81f6e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="81f6e-115">-AsJob</span></span>
<span data-ttu-id="81f6e-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="81f6e-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="81f6e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81f6e-117">-DefaultProfile</span></span>
<span data-ttu-id="81f6e-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="81f6e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81f6e-119">-Force</span><span class="sxs-lookup"><span data-stu-id="81f6e-119">-Force</span></span>
<span data-ttu-id="81f6e-120">Supply -Force to skip confirmation of this command.</span><span class="sxs-lookup"><span data-stu-id="81f6e-120">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="81f6e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="81f6e-121">-InputObject</span></span>
<span data-ttu-id="81f6e-122">Oggetto di input StorageSyncService, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="81f6e-122">StorageSyncService Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="81f6e-123">-Name</span><span class="sxs-lookup"><span data-stu-id="81f6e-123">-Name</span></span>
<span data-ttu-id="81f6e-124">Nome di StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="81f6e-124">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="81f6e-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="81f6e-125">-PassThru</span></span>
<span data-ttu-id="81f6e-126">Nella normale esecuzione, questo cmdlet non restituisce alcun valore in caso di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="81f6e-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="81f6e-127">Se si fornisce il parametro PassThru, il cmdlet scriverà un valore nella pipeline dopo l'esecuzione corretta.</span><span class="sxs-lookup"><span data-stu-id="81f6e-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="81f6e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81f6e-128">-ResourceGroupName</span></span>
<span data-ttu-id="81f6e-129">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="81f6e-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="81f6e-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="81f6e-130">-ResourceId</span></span>
<span data-ttu-id="81f6e-131">ID risorsa StorageSyncService</span><span class="sxs-lookup"><span data-stu-id="81f6e-131">StorageSyncService Resource Id</span></span>

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

### <span data-ttu-id="81f6e-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="81f6e-132">-Confirm</span></span>
<span data-ttu-id="81f6e-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81f6e-133">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81f6e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81f6e-134">-WhatIf</span></span>
<span data-ttu-id="81f6e-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="81f6e-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="81f6e-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="81f6e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81f6e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81f6e-137">CommonParameters</span></span>
<span data-ttu-id="81f6e-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81f6e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81f6e-139">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81f6e-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81f6e-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="81f6e-140">INPUTS</span></span>

### <span data-ttu-id="81f6e-141">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="81f6e-141">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

### <span data-ttu-id="81f6e-142">System.String</span><span class="sxs-lookup"><span data-stu-id="81f6e-142">System.String</span></span>

### <span data-ttu-id="81f6e-143">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="81f6e-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="81f6e-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="81f6e-144">OUTPUTS</span></span>

### <span data-ttu-id="81f6e-145">System.Object</span><span class="sxs-lookup"><span data-stu-id="81f6e-145">System.Object</span></span>
## <span data-ttu-id="81f6e-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="81f6e-146">NOTES</span></span>

## <span data-ttu-id="81f6e-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="81f6e-147">RELATED LINKS</span></span>
