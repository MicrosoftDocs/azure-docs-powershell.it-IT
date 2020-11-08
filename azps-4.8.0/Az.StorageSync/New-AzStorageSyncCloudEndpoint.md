---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: 95b30bda3d824fccc5bb40e442697b81b6396d56
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032037"
---
# <span data-ttu-id="ef2e6-101">New-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="ef2e6-101">New-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="ef2e6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ef2e6-102">SYNOPSIS</span></span>
<span data-ttu-id="ef2e6-103">Questo comando crea un endpoint cloud di sincronizzazione di Azure file in un gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="ef2e6-103">This command creates an Azure File Sync cloud endpoint in a sync group.</span></span>

## <span data-ttu-id="ef2e6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ef2e6-104">SYNTAX</span></span>

### <span data-ttu-id="ef2e6-105">StringParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ef2e6-105">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -StorageAccountResourceId <String> -AzureFileShareName <String>
 [-StorageAccountTenantId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ef2e6-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef2e6-106">ObjectParameterSet</span></span>
```
New-AzStorageSyncCloudEndpoint [-ParentObject] <PSSyncGroup> -Name <String> -StorageAccountResourceId <String>
 -AzureFileShareName <String> [-StorageAccountTenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef2e6-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef2e6-107">ParentStringParameterSet</span></span>
```
New-AzStorageSyncCloudEndpoint [-ParentResourceId] <String> -Name <String> -StorageAccountResourceId <String>
 -AzureFileShareName <String> [-StorageAccountTenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef2e6-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ef2e6-108">DESCRIPTION</span></span>
<span data-ttu-id="ef2e6-109">Questo comando crea un endpoint cloud di sincronizzazione di Azure file.</span><span class="sxs-lookup"><span data-stu-id="ef2e6-109">This command creates an Azure File Sync cloud endpoint.</span></span> <span data-ttu-id="ef2e6-110">Un endpoint cloud è un riferimento a una condivisione di file Azure esistente.</span><span class="sxs-lookup"><span data-stu-id="ef2e6-110">A cloud endpoint is a reference to an existing Azure file share.</span></span> <span data-ttu-id="ef2e6-111">Rappresenta la condivisione di file e la definisce partecipazione alla sincronizzazione di tutti i file parte del gruppo di sincronizzazione in cui è stato creato l'endpoint cloud.</span><span class="sxs-lookup"><span data-stu-id="ef2e6-111">It represents the file share and defines it participation in syncing all the files part of the sync group the cloud endpoint has been created in.</span></span>

## <span data-ttu-id="ef2e6-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ef2e6-112">EXAMPLES</span></span>

### <span data-ttu-id="ef2e6-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ef2e6-113">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myCloudEndpointName" -StorageAccountResourceId $storageAccountResourceId -AzureFileShareName "myAzureFileShareName" -StorageAccountTenantId "myStorageAccountTenantId"
```

<span data-ttu-id="ef2e6-114">Un endpoint cloud è un membro integrale di un gruppo di sincronizzazione, questo è un esempio di creazione di uno all'interno di un gruppo di sincronizzazione esistente denominato "mySyncGroupName".</span><span class="sxs-lookup"><span data-stu-id="ef2e6-114">A cloud endpoint is an integral member of a sync group, this is an example of creating one inside of an existing sync group called "mySyncGroupName".</span></span>

## <span data-ttu-id="ef2e6-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ef2e6-115">PARAMETERS</span></span>

### <span data-ttu-id="ef2e6-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ef2e6-116">-AsJob</span></span>
<span data-ttu-id="ef2e6-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ef2e6-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ef2e6-118">-AzureFileShareName</span><span class="sxs-lookup"><span data-stu-id="ef2e6-118">-AzureFileShareName</span></span>
<span data-ttu-id="ef2e6-119">Nome condivisione account di archiviazione (nome condivisione file Azure)</span><span class="sxs-lookup"><span data-stu-id="ef2e6-119">Storage Account Share Name (Azure file share name)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef2e6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef2e6-120">-DefaultProfile</span></span>
<span data-ttu-id="ef2e6-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ef2e6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef2e6-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="ef2e6-122">-Name</span></span>
<span data-ttu-id="ef2e6-123">Nome dell'endpoint cloud.</span><span class="sxs-lookup"><span data-stu-id="ef2e6-123">Name of the cloud endpoint.</span></span> <span data-ttu-id="ef2e6-124">Quando viene creato tramite il portale di Azure, il nome viene impostato sul nome della condivisione di file di Azure a cui fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="ef2e6-124">When created through the Azure portal, Name is set to the name of the Azure file share it references.</span></span>

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

### <span data-ttu-id="ef2e6-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ef2e6-125">-ParentObject</span></span>
<span data-ttu-id="ef2e6-126">Oggetto SyncGroup, in genere passato tramite il parametro.</span><span class="sxs-lookup"><span data-stu-id="ef2e6-126">SyncGroup Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="ef2e6-127">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ef2e6-127">-ParentResourceId</span></span>
<span data-ttu-id="ef2e6-128">ID risorsa padre di SyncGroup</span><span class="sxs-lookup"><span data-stu-id="ef2e6-128">SyncGroup Parent Resource Id</span></span>

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

### <span data-ttu-id="ef2e6-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef2e6-129">-ResourceGroupName</span></span>
<span data-ttu-id="ef2e6-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ef2e6-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="ef2e6-131">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="ef2e6-131">-StorageAccountResourceId</span></span>
<span data-ttu-id="ef2e6-132">ID risorsa account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="ef2e6-132">Storage Account Resource Id</span></span>

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

### <span data-ttu-id="ef2e6-133">-StorageAccountTenantId</span><span class="sxs-lookup"><span data-stu-id="ef2e6-133">-StorageAccountTenantId</span></span>
<span data-ttu-id="ef2e6-134">ID tenant dell'account di archiviazione (ID directory aziendale)</span><span class="sxs-lookup"><span data-stu-id="ef2e6-134">Storage Account Tenant Id (Company Directory Id)</span></span>

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

### <span data-ttu-id="ef2e6-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="ef2e6-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="ef2e6-136">Nome della StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="ef2e6-136">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="ef2e6-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="ef2e6-137">-SyncGroupName</span></span>
<span data-ttu-id="ef2e6-138">Nome della SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="ef2e6-138">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="ef2e6-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ef2e6-139">-Confirm</span></span>
<span data-ttu-id="ef2e6-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef2e6-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef2e6-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef2e6-141">-WhatIf</span></span>
<span data-ttu-id="ef2e6-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ef2e6-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ef2e6-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ef2e6-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef2e6-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef2e6-144">CommonParameters</span></span>
<span data-ttu-id="ef2e6-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef2e6-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef2e6-146">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef2e6-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef2e6-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ef2e6-147">INPUTS</span></span>

### <span data-ttu-id="ef2e6-148">Microsoft. Azure. Commands. StorageSync. Models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="ef2e6-148">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="ef2e6-149">System. String</span><span class="sxs-lookup"><span data-stu-id="ef2e6-149">System.String</span></span>

## <span data-ttu-id="ef2e6-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ef2e6-150">OUTPUTS</span></span>

### <span data-ttu-id="ef2e6-151">Microsoft. Azure. Commands. StorageSync. Models. PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="ef2e6-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

## <span data-ttu-id="ef2e6-152">Note</span><span class="sxs-lookup"><span data-stu-id="ef2e6-152">NOTES</span></span>

## <span data-ttu-id="ef2e6-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ef2e6-153">RELATED LINKS</span></span>
