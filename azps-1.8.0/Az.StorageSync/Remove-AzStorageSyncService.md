---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/remove-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
ms.openlocfilehash: 5116ead7111902b1009517ff42ff6594ac87d8c5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676433"
---
# <span data-ttu-id="5b598-101">Remove-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="5b598-101">Remove-AzStorageSyncService</span></span>

## <span data-ttu-id="5b598-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5b598-102">SYNOPSIS</span></span>
<span data-ttu-id="5b598-103">Questo comando eliminerà il servizio di sincronizzazione dello spazio di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="5b598-103">This command will delete the specified storage sync service.</span></span>

## <span data-ttu-id="5b598-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5b598-104">SYNTAX</span></span>

### <span data-ttu-id="5b598-105">InputObjectParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5b598-105">InputObjectParameterSet (Default)</span></span>
```
Remove-AzStorageSyncService [-InputObject] <PSStorageSyncService> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b598-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b598-106">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncService [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b598-107">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b598-107">StringParameterSet</span></span>
```
Remove-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b598-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5b598-108">DESCRIPTION</span></span>
<span data-ttu-id="5b598-109">Questo comando eliminerà il servizio di sincronizzazione dello spazio di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="5b598-109">This command will delete the specified storage sync service.</span></span> <span data-ttu-id="5b598-110">Un servizio di sincronizzazione dello spazio di archiviazione può essere rimosso solo quando vengono eliminati per primi tutti i gruppi di sincronizzazione e i server registrati inclusi.</span><span class="sxs-lookup"><span data-stu-id="5b598-110">A storage sync service can only be removed when all of the contained sync groups and registered servers are deleted first.</span></span>

## <span data-ttu-id="5b598-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5b598-111">EXAMPLES</span></span>

### <span data-ttu-id="5b598-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5b598-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncService -Force -ResourceGroupName "myResourceGroup" -Name "myStorageSyncServiceName"
```

<span data-ttu-id="5b598-113">Questo comando consente di rimuovere il servizio di sincronizzazione dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="5b598-113">This command will remove the storage sync service.</span></span>

## <span data-ttu-id="5b598-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5b598-114">PARAMETERS</span></span>

### <span data-ttu-id="5b598-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5b598-115">-AsJob</span></span>
<span data-ttu-id="5b598-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="5b598-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5b598-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b598-117">-DefaultProfile</span></span>
<span data-ttu-id="5b598-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5b598-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b598-119">-Force</span><span class="sxs-lookup"><span data-stu-id="5b598-119">-Force</span></span>
<span data-ttu-id="5b598-120">Forza di fornitura per ignorare la conferma di questo comando.</span><span class="sxs-lookup"><span data-stu-id="5b598-120">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="5b598-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b598-121">-InputObject</span></span>
<span data-ttu-id="5b598-122">Oggetto di input StorageSyncService, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="5b598-122">StorageSyncService Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="5b598-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="5b598-123">-Name</span></span>
<span data-ttu-id="5b598-124">Nome della StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="5b598-124">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="5b598-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5b598-125">-PassThru</span></span>
<span data-ttu-id="5b598-126">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="5b598-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="5b598-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b598-127">-ResourceGroupName</span></span>
<span data-ttu-id="5b598-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5b598-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="5b598-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b598-129">-ResourceId</span></span>
<span data-ttu-id="5b598-130">ID risorsa StorageSyncService</span><span class="sxs-lookup"><span data-stu-id="5b598-130">StorageSyncService Resource Id</span></span>

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

### <span data-ttu-id="5b598-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5b598-131">-Confirm</span></span>
<span data-ttu-id="5b598-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b598-132">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b598-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b598-133">-WhatIf</span></span>
<span data-ttu-id="5b598-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5b598-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5b598-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5b598-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b598-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b598-136">CommonParameters</span></span>
<span data-ttu-id="5b598-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b598-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b598-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b598-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b598-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5b598-139">INPUTS</span></span>

### <span data-ttu-id="5b598-140">Microsoft. Azure. Commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="5b598-140">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

### <span data-ttu-id="5b598-141">System. String</span><span class="sxs-lookup"><span data-stu-id="5b598-141">System.String</span></span>

### <span data-ttu-id="5b598-142">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5b598-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5b598-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5b598-143">OUTPUTS</span></span>

### <span data-ttu-id="5b598-144">System. Object</span><span class="sxs-lookup"><span data-stu-id="5b598-144">System.Object</span></span>
## <span data-ttu-id="5b598-145">Note</span><span class="sxs-lookup"><span data-stu-id="5b598-145">NOTES</span></span>

## <span data-ttu-id="5b598-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5b598-146">RELATED LINKS</span></span>
