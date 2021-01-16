---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/remove-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
ms.openlocfilehash: f64c085f742eeabea235660d4af7ba6bd5970fdf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366547"
---
# <span data-ttu-id="1a627-101">Remove-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="1a627-101">Remove-AzStorageSyncService</span></span>

## <span data-ttu-id="1a627-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1a627-102">SYNOPSIS</span></span>
<span data-ttu-id="1a627-103">Questo comando eliminerà il servizio di sincronizzazione dello spazio di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="1a627-103">This command will delete the specified storage sync service.</span></span>

## <span data-ttu-id="1a627-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1a627-104">SYNTAX</span></span>

### <span data-ttu-id="1a627-105">StringParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1a627-105">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a627-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a627-106">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncService [-InputObject] <PSStorageSyncService> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a627-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a627-107">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncService [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a627-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a627-108">DESCRIPTION</span></span>
<span data-ttu-id="1a627-109">Questo comando eliminerà il servizio di sincronizzazione dello spazio di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="1a627-109">This command will delete the specified storage sync service.</span></span> <span data-ttu-id="1a627-110">Un servizio di sincronizzazione dello spazio di archiviazione può essere rimosso solo quando vengono eliminati per primi tutti i gruppi di sincronizzazione e i server registrati inclusi.</span><span class="sxs-lookup"><span data-stu-id="1a627-110">A storage sync service can only be removed when all of the contained sync groups and registered servers are deleted first.</span></span>

## <span data-ttu-id="1a627-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1a627-111">EXAMPLES</span></span>

### <span data-ttu-id="1a627-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1a627-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncService -Force -ResourceGroupName "myResourceGroup" -Name "myStorageSyncServiceName"
```

<span data-ttu-id="1a627-113">Questo comando consente di rimuovere il servizio di sincronizzazione dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="1a627-113">This command will remove the storage sync service.</span></span>

## <span data-ttu-id="1a627-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1a627-114">PARAMETERS</span></span>

### <span data-ttu-id="1a627-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1a627-115">-AsJob</span></span>
<span data-ttu-id="1a627-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="1a627-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1a627-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a627-117">-DefaultProfile</span></span>
<span data-ttu-id="1a627-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1a627-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a627-119">-Force</span><span class="sxs-lookup"><span data-stu-id="1a627-119">-Force</span></span>
<span data-ttu-id="1a627-120">Forza di fornitura per ignorare la conferma di questo comando.</span><span class="sxs-lookup"><span data-stu-id="1a627-120">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="1a627-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1a627-121">-InputObject</span></span>
<span data-ttu-id="1a627-122">Oggetto di input StorageSyncService, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="1a627-122">StorageSyncService Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="1a627-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="1a627-123">-Name</span></span>
<span data-ttu-id="1a627-124">Nome della StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="1a627-124">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="1a627-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1a627-125">-PassThru</span></span>
<span data-ttu-id="1a627-126">In esecuzione normale, questo cmdlet non restituisce alcun valore per l'esito positivo.</span><span class="sxs-lookup"><span data-stu-id="1a627-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="1a627-127">Se fornisci il parametro PassThru, il cmdlet scriverà un valore nella pipeline dopo l'esecuzione corretta.</span><span class="sxs-lookup"><span data-stu-id="1a627-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="1a627-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a627-128">-ResourceGroupName</span></span>
<span data-ttu-id="1a627-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1a627-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="1a627-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1a627-130">-ResourceId</span></span>
<span data-ttu-id="1a627-131">ID risorsa StorageSyncService</span><span class="sxs-lookup"><span data-stu-id="1a627-131">StorageSyncService Resource Id</span></span>

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

### <span data-ttu-id="1a627-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1a627-132">-Confirm</span></span>
<span data-ttu-id="1a627-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a627-133">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a627-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a627-134">-WhatIf</span></span>
<span data-ttu-id="1a627-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1a627-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1a627-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1a627-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a627-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a627-137">CommonParameters</span></span>
<span data-ttu-id="1a627-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a627-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a627-139">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a627-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a627-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1a627-140">INPUTS</span></span>

### <span data-ttu-id="1a627-141">Microsoft. Azure. Commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="1a627-141">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

### <span data-ttu-id="1a627-142">System. String</span><span class="sxs-lookup"><span data-stu-id="1a627-142">System.String</span></span>

### <span data-ttu-id="1a627-143">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1a627-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1a627-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1a627-144">OUTPUTS</span></span>

### <span data-ttu-id="1a627-145">System. Object</span><span class="sxs-lookup"><span data-stu-id="1a627-145">System.Object</span></span>
## <span data-ttu-id="1a627-146">Note</span><span class="sxs-lookup"><span data-stu-id="1a627-146">NOTES</span></span>

## <span data-ttu-id="1a627-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1a627-147">RELATED LINKS</span></span>
