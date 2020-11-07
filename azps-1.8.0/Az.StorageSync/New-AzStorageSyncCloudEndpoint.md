---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: 7a8c11bc4b24415e1baf826824596bc06e1fe99a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676452"
---
# <span data-ttu-id="23b8a-101">New-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="23b8a-101">New-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="23b8a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="23b8a-102">SYNOPSIS</span></span>
<span data-ttu-id="23b8a-103">Questo comando crea un endpoint cloud di sincronizzazione di Azure file in un gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="23b8a-103">This command creates an Azure File Sync cloud endpoint in a sync group.</span></span>

## <span data-ttu-id="23b8a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="23b8a-104">SYNTAX</span></span>

### <span data-ttu-id="23b8a-105">ObjectParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="23b8a-105">ObjectParameterSet (Default)</span></span>
```
New-AzStorageSyncCloudEndpoint [-ParentObject] <PSSyncGroup> -Name <String> -StorageAccountResourceId <String>
 -AzureFileShareName <String> [-StorageAccountTenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23b8a-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="23b8a-106">StringParameterSet</span></span>
```
New-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -StorageAccountResourceId <String> -AzureFileShareName <String>
 [-StorageAccountTenantId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="23b8a-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="23b8a-107">ParentStringParameterSet</span></span>
```
New-AzStorageSyncCloudEndpoint [-ParentResourceId] <String> -Name <String> -StorageAccountResourceId <String>
 -AzureFileShareName <String> [-StorageAccountTenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23b8a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="23b8a-108">DESCRIPTION</span></span>
<span data-ttu-id="23b8a-109">Questo comando crea un endpoint cloud di sincronizzazione di Azure file.</span><span class="sxs-lookup"><span data-stu-id="23b8a-109">This command creates an Azure File Sync cloud endpoint.</span></span> <span data-ttu-id="23b8a-110">Un endpoint cloud è un riferimento a una condivisione di file Azure esistente.</span><span class="sxs-lookup"><span data-stu-id="23b8a-110">A cloud endpoint is a reference to an existing Azure file share.</span></span> <span data-ttu-id="23b8a-111">Rappresenta la condivisione di file e la definisce partecipazione alla sincronizzazione di tutti i file parte del gruppo di sincronizzazione in cui è stato creato l'endpoint cloud.</span><span class="sxs-lookup"><span data-stu-id="23b8a-111">It represents the file share and defines it participation in syncing all the files part of the sync group the cloud endpoint has been created in.</span></span>

## <span data-ttu-id="23b8a-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="23b8a-112">EXAMPLES</span></span>

### <span data-ttu-id="23b8a-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="23b8a-113">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myCloudEndpointName" -StorageAccountResourceId $storageAccountResourceId -AzureFileShareName "myAzureFileShareName" -StorageAccountTenantId "myStorageAccountTenantId"
```

<span data-ttu-id="23b8a-114">Un endpoint cloud è un membro integrale di un gruppo di sincronizzazione, questo è un esempio di creazione di uno all'interno di un gruppo di sincronizzazione esistente denominato "mySyncGroupName".</span><span class="sxs-lookup"><span data-stu-id="23b8a-114">A cloud endpoint is an integral member of a sync group, this is an example of creating one inside of an existing sync group called "mySyncGroupName".</span></span>

## <span data-ttu-id="23b8a-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="23b8a-115">PARAMETERS</span></span>

### <span data-ttu-id="23b8a-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="23b8a-116">-AsJob</span></span>
<span data-ttu-id="23b8a-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="23b8a-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="23b8a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23b8a-118">-DefaultProfile</span></span>
<span data-ttu-id="23b8a-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="23b8a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23b8a-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="23b8a-120">-Name</span></span>
<span data-ttu-id="23b8a-121">Nome dell'endpoint cloud.</span><span class="sxs-lookup"><span data-stu-id="23b8a-121">Name of the cloud endpoint.</span></span> <span data-ttu-id="23b8a-122">Quando viene creato tramite il portale di Azure, il nome viene impostato sul nome della condivisione di file di Azure a cui fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="23b8a-122">When created through the Azure portal, Name is set to the name of the Azure file share it references.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CloudEndpointName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23b8a-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="23b8a-123">-ParentObject</span></span>
<span data-ttu-id="23b8a-124">Oggetto SyncGroup, in genere passato tramite il parametro.</span><span class="sxs-lookup"><span data-stu-id="23b8a-124">SyncGroup Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup
Parameter Sets: ObjectParameterSet
Aliases: SyncGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23b8a-125">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="23b8a-125">-ParentResourceId</span></span>
<span data-ttu-id="23b8a-126">ID risorsa padre di SyncGroup</span><span class="sxs-lookup"><span data-stu-id="23b8a-126">SyncGroup Parent Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: SyncGroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23b8a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23b8a-127">-ResourceGroupName</span></span>
<span data-ttu-id="23b8a-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="23b8a-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="23b8a-129">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="23b8a-129">-StorageAccountResourceId</span></span>
<span data-ttu-id="23b8a-130">ID risorsa account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="23b8a-130">Storage Account Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23b8a-131">-AzureFileShareName</span><span class="sxs-lookup"><span data-stu-id="23b8a-131">-AzureFileShareName</span></span>
<span data-ttu-id="23b8a-132">Nome condivisione account di archiviazione (nome condivisione file Azure)</span><span class="sxs-lookup"><span data-stu-id="23b8a-132">Storage Account Share Name (Azure file share name)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23b8a-133">-StorageAccountTenantId</span><span class="sxs-lookup"><span data-stu-id="23b8a-133">-StorageAccountTenantId</span></span>
<span data-ttu-id="23b8a-134">ID tenant dell'account di archiviazione (ID directory aziendale)</span><span class="sxs-lookup"><span data-stu-id="23b8a-134">Storage Account Tenant Id (Company Directory Id)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23b8a-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="23b8a-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="23b8a-136">Nome della StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="23b8a-136">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="23b8a-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="23b8a-137">-SyncGroupName</span></span>
<span data-ttu-id="23b8a-138">Nome della SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="23b8a-138">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23b8a-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="23b8a-139">-Confirm</span></span>
<span data-ttu-id="23b8a-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23b8a-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23b8a-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23b8a-141">-WhatIf</span></span>
<span data-ttu-id="23b8a-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="23b8a-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="23b8a-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="23b8a-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23b8a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23b8a-144">CommonParameters</span></span>
<span data-ttu-id="23b8a-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23b8a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23b8a-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23b8a-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23b8a-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="23b8a-147">INPUTS</span></span>

### <span data-ttu-id="23b8a-148">Microsoft. Azure. Commands. StorageSync. Models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="23b8a-148">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="23b8a-149">System. String</span><span class="sxs-lookup"><span data-stu-id="23b8a-149">System.String</span></span>

## <span data-ttu-id="23b8a-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="23b8a-150">OUTPUTS</span></span>

### <span data-ttu-id="23b8a-151">Microsoft. Azure. Commands. StorageSync. Models. PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="23b8a-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

## <span data-ttu-id="23b8a-152">Note</span><span class="sxs-lookup"><span data-stu-id="23b8a-152">NOTES</span></span>

## <span data-ttu-id="23b8a-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="23b8a-153">RELATED LINKS</span></span>
